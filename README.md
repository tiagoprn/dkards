# dkards

**Always on deck of cards carousel for everything you want to glance at.**

dkards is a self-hosted carousel for your life. Left alone, it shuffles through a deck of ambient cards on a timer, styled after the old LG webOS television cards interface: your latest Readwise highlight, a random tricorder fact, this week's top OpenRouter coding models, your Raspberry Pi usage streak, a post-it note you left yourself. Click any card and the shuffle pauses so you can read that one in detail, then it resumes on its own once you look away. It behaves like an appliance rather than an application: something you glance at on a side monitor, not something you operate.

## What it is not

dkards idea started as a replacement for a side monitor I have which displays a rasperry-pi powered MagicMirror². But dkards is not that. MagicMirror² is a Node.js/Electron platform meant to run behind a physical two-way mirror, and dkards has no hardware requirement at all; it is a server-rendered Django app you can point at any spare screen.

dkards is also not a homelab launcher like Homepage, Glance, or Dashy. Those tools give you a grid of links to the other services you self-host. dkards has no links out. Every card is a self-contained snapshot of your own data, not a shortcut to somewhere else.

## Interface

The interface is a direct homage to the old webOS television card-deck UX: a horizontal row of cards along the bottom of the screen, one of which is always in focus, rendered full-bleed above the row.

**Idle behavior.** By default, the deck auto-shuffles, advancing to a new card on a configurable interval. No input is required; this is the "screensaver" half of the experience.

**Focus behavior.** Clicking any card in the bottom row pulls it into focus immediately, pausing the automatic shuffle. Focus mode ends either by an explicit dismiss action or after a configurable idle timeout, at which point auto-shuffle resumes.

The whole thing is server-rendered HTML with light animation and minimal client-side JavaScript, deliberately avoiding a heavy SPA framework for what is, functionally, a glorified carousel.

## Initial Cards Catalog

- daily calendar (using remind)
- latest achievements (md file, top 5)
- news from RSS feeds sources
- weather forecast

I already have some other cards planned, but this will be initial set.

## Requirements

New card types should support both lifecycle states (ambient shuffle, focused) rather than assuming the card is only ever viewed one way.

## Status

Early stage. Features above reflect the current design intent, not a finished feature set.

## Contributions

Although I may accept contributions in the future, at least initially while I am building and iterating on its' core I will be ignoring them.
This project exists to attend to a personal need of mine, so that is my focus for the time being.
