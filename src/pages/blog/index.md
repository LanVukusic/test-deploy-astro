---
layout: ../../layouts/MarkdownLayout.astro
title: Dev log post
draft: true
---

# Dev log

## Stuff that need to work

Since we'd eventually like to control the software (on either PC or a console) remotely, we need a few things:

- [ ] Read inputs
- [ ] Get a way to connect to MQ fast and reliably over network
  - [ ] MIDI
  - [ ] Hardware buttons

## Language, design

I chose to go with [GO]("https://go.dev/"), since my previous wing project, the [NetWingV2]("https://github.com/LanVukusic/NetWing2"), works quite well and i believe that with the right tweaks that thing could fly.
I need a fast language (go, rust, C, ...), since data processing should happen with no to minimal delay. Since I suck writing C and i haven't really tried Rust (yet), Golang is really my only option here.

One thing that I really missed from my old project is cross compatibility. Since I daily drive Ubuntu and most people in lighting world use a Mac or windows, software should run everywhere.

**Terminal is king**. I made a choice that its best to create a config file for mapping everywhere and software just reads it at start. A web interface for monitoring or simpler management can be added in the future.  
No fat and hungry web-views or anything... just a simple executable that pops a terminal window open.

## Development

- [Reverse engineering MagicQ](reverse-engineering/1-reverse-engineering.md)