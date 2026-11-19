---
layout: post
title: "Don’t get caught, keep your Onions in a Vault"
date: 2026-11-19
paper_authors: "H. Ikram, R. Habib, M. Ali, Z. A. Uzmi"
paper_venue: "NINeS 2026"
paper_url: "https://2026.nines-conference.org/papers/p017-Ikram.pdf"
week: 9
tags: [tor, anonymity, privacy, security]
---

## Key Idea

Onion Services provide a method to anonymously host websites through the
Tor network. With how the services currently work, there exists a possible
exploit where an attacker that controls a guard node used by the service
can perform deanonymization. This paper presents VaulTor, a new architecture
that allows services to be hosted on "vaults," that prevent discovery of the
original content provider.

## Critique

This is an interesting approach, but seems to have many flaws that may make it
not worth the effort. The paper discounts side-channel attacks from within the
Trusted Execution Environment. There are also problems with liability and incentives,
i.e. if the vault operators are held liable for content they host, it would disincentivise
them from hosting in the first place. The architecture may never take off with
this problem.

## Connections

This paper is unlike any other we've read so far. Most papers focus on improving
network efficiency, but this one focuses on an entirely different metric. In this
sense, it's similar to _Exploring the Benefits of Carbon-Aware Routing_, which also
forgos efficiency in favor of another goal.
