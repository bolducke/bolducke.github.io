---
layout: post
title: Design Takeaway | ECS-Like (Archetypes) - Overengineer/Overthink Breakout Clone
date: 2023-05-28 11:59:00-0000
description: A small breakdown of my architecture experimentation on my breakout clone
categories: Odin SDL Languages
disqus_comments: false
related_posts: false
---

[source code](https://github.com/bolducke/OOBC)

For my breakout game, I wanted to explore different architectural designs and stay away from OOP. I intentionally overcomplicated my project to identify more easily the potential "pain point" from such design that are harder to detect from "synthetic" test case.

## Close Set / Open Set Mindset

My mindset was to change my perspective from an "open-set" to a "close-set" problem. It's very hard to successfully create a *future-proof* project/library. A good *real-life* example is Vulkan with their API where they recently *backed down* from their original API (proposed in 2016) because most people, in the game dev. community, were unsatisfied.

In that regard, by having an "close-set" mentality, I went for the simplest approach that I came up. In small time frame, I was able to build something way more efficiently than before. 

## ECS Coupling

ECS-like architecture is a great way to make your code more modular while not compromising too much on performance. However, Pure ECS can be a little janky when systems are coupled/related (which happen all the time). This is an issue on its own. (There is multiple blog post on the matter on the internet). In practice, it involves dealing with events, callbacks, and dynamic components. Even for entities, it can be a little overwhelming (See (https://skypjack.github.io/2019-06-25-ecs-baf-part-4/)).

#### Systems
Instead, I went, again, for a "simpler" approach where each system gathers information through their process, and then, in the main loop, you intertwine those pieces of information "manually". As a developper, I find it easier to make the systems interact together than to rely on "black-box" framework.

#### Entity
I went for a pointer/index-based approach that references each entity internally through a tree-like data structure as mentioned in the blog post of Skypjack.

### ECS Archetype

There is no unique way to represent an ECS system. In practice, however, there is two mainstream way. You can separate each likable entity with a common archetype or trait each component individually. In the former case, you have a pool of components for every archetype. In the latter case, your components are all share in a common pool.

Personally, I separate each pool statiscally to make it easier to process them because it is common to apply logic based on specific type that share common components, but behave differently. However, It make it harder to add "custom" information to one entity. It's hard to say if I should change my way of thinking or use a common pool so that it is easier to add components dynamically.

## Breakdown: Subtype Polymorphism & Archetype Design

Before this experiment, I always went for OOP without truly thinking about why I was using OOP in the first place. I try something differently. I was always finding myself in this over-abstraction hole and was heavily slowdown. Anyway, this is a very profound and interesting subject and I am just beginning to form an opinion of my own. I present two simple showcase highlighting the main difference between those two approaches.

#### Subtype Polymorphism

Subtype Polymorphism is a tool closely related to OOP where you derived each component member.
Then, to use an entity, you need to cast it for each one.

{% raw %}
```C
package main

import "core:fmt"

Position :: struct{
    x,y: int,
}

Velocity :: struct {
    dx,dy: int,
}

//Preset
Entity :: struct {
    derived: union{^Ball,^Brick}
}

Ball :: struct {
    using entity: Entity,
    pos: Position,
    vel: Velocity,
}

Brick :: struct {
    using entity: Entity,
    pos: Position,
}

Scene :: struct {
    entities: [dynamic]Entity,
}

init_scene :: proc() -> (s: Scene) {
}

new_entity :: proc(T: typeid) -> Entity {
    t := new(T)
    t.derived = &t
    return t.entity
}

main :: proc() {
    scene := init_scene()

    append(&scene.entities,new_entity(Ball))
    append(&scene.entities,new_entity(Brick))

    for ent in scene.entities {
        switch e in &ent.derived {
            case Ball:
                fmt.println(e.position)
            case Brick:
                fmt.println(e.position)
        }
    }

    for ent in scene.entities {
        #partial switch e in &ent.derived {                
            case Ball:
                fmt.println(e.velocity)
        }
    }

    for ent in scene.entities {
        #partial switch e in &ent.derived {                
            case Ball:
                fmt.println("Ball", e.position,e.velocity)
        }
    }

}

```
{% endraw %}

#### ECS-Like

In ECS-like archetype, I keep every entity into different block of memory for each archetype. I can reduce duplication of code between entity that share similar behavior.

{% raw %}
```C
package main

import "core:fmt"

Position :: struct{
    x,y: int,
}

Velocity :: struct {
    dx,dy: int,
}

//Preset
Ball :: struct {
    pos: Position,
    vel: Velocity,
}

Brick :: struct {
    pos: Position,
}

Archetype :: struct{
    //similar to add a bit_set because union in Odin keep tag
    pos: Maybe([dynamic]Position),
    vel: Maybe([dynamic]Velocity),
}

Scene :: struct {
    archetypes: [2]Archetype,
}

init_scene :: proc() -> (s: Scene) {
    s.archetypes[0].pos = make([dynamic]Position)
    s.archetypes[0].vel = make([dynamic]Velocity)

    s.archetypes[1].pos = make([dynamic]Position)
    s.archetypes[1].vel = nil

    return
}

add_entity_ball :: proc(scene: ^Scene, ball: Ball) {
    append(&scene.archetypes[0].pos.?,ball.pos)
    append(&scene.archetypes[0].vel.?,ball.vel)

}
add_entity_brick :: proc(scene: ^Scene, brick: Brick) {
    append(&scene.archetypes[1].pos.?,brick.pos)
}
add_entity :: proc{add_entity_ball,add_entity_brick}

main :: proc() {
    scene := init_scene()

    add_entity(&scene,Brick{{10,10}})
    add_entity(&scene,Ball{{2,2},{1,1}})

    for a in scene.archetypes {
        if ps, ok := a.pos.?; ok {
            for p in ps {
                fmt.println("Position", p)
            }
        }
    }

    for a in scene.archetypes {
        if vs, ok := a.vel.?; ok {
            for v in vs {
                fmt.println("Velocity", v)
            }
        }
    }

    {
        a := scene.archetypes[0]

        ps := a.pos.?
        vs := a.vel.?

        nb := len(ps)

        for i in 0..<nb {
            fmt.println("Ball", ps[i],vs[i])
        }
    }

    //Alternative
    for a in scene.archetypes {
        ps, okp := a.pos.?
        vs, okv := a.vel.?

        if okp && okv {
            nb := len(ps)

            for i in 0..<nb {
                fmt.println("p+v", ps[i],vs[i])
            }
        }
    }
}
```
{% endraw %}