---
image: /assets/images/ProductPalette.png
title: Programmer on Good Company
---

{{< youtube XluplAWL8hY >}}

I was one of about 9 people working at chasing carrots while working on Good Company. Because of the nature of such a small team I did programming on all corners of the game. Backend programming in both Go and C++ (the backend was rewritten in C++ at one point) and programming in the frontend which included everything from expanding the networking code, ui programming, graphics programming, tweaking and expanding gameplay and of course lots of bugfixing.
Sadly I do not have any access to the code and many of the assets anymore.

Some of the most notable features I added include...

## Dynamic Product Icons

In Good Company items are materials, modules or products. Materials and modules can be represented by simple icons, but products had multiple parts making up their visuals, leading to thousands of possibilities. I wrote a system that allows authoring of hierarchical models with part names and then rendering them into icons, but only as they're first seen in an inventory by the player. Addtionally the system cached a certain amount of icons to not rerender icons too often, but also dont keep icons that are only seen once in a blue moon into memory.

This system also ended up being handy for labels on boxes in the game world as well as dynamic models in the "blueprint editor" where you design new products for your company to produce.

![](/assets/images/ProductShelf.png)

![](/assets/images/ProductAssembly.png)

## Outline System

The outline system I wrote for Good Company works with any mesh, is easy to add to any renderer in the game and to enable/disable, renders outlines in a faded out way when behind other objects and scales extremely well with multiple outlines, including outlines with multiple colors on screen.

![](/assets/images/gc_outline.png)

## A Discord Bot

While I worked on Good Company, we started building a community upcoming to the early access launch. To keep the community more active and engaged I, at first with another programmer but then maintaining it myself, made a discord bot that allowed players to enact a simplified version of the game, funding companies, creating products and selling them on a changing market.

![](/assets/images/discord_bot.png)

Part of this project was also a web interface where you can see the developments of the game over time.

![](/assets/images/discord_stats.png)

## An Animation Tool

One other thing I worked on and that I'd like to mention is an animation tool that I wrote. It utilized the existing game assets and architecture to show scripted sequences. In addition to replicating all movements that existed in the game at the time and some UI effects coordinated between multiple actors, it supports jumping to time points and generating some "busy looking" movements procedurally. This tool was used to make a trailer for Good Company, first shown at gamescom 2018 (it sadly isnt online anymore).