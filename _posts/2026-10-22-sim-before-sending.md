---
layout: post
title: "Simulate Before Sending: Rethinking Transport in Datacenter Networks"
date: 2026-10-22
paper_authors: "D. Straussman, I. Keslassy, A. Shpiner, L. Liss"
paper_venue: "NINeS 2026"
paper_url: "https://nines-conference.org/papers/p019-Straussman.pdf"
week: 5
tags: [datacenter, simulation]
---

## Key Idea

The rapid adoption of AI is changing how datacenters have to operate. Modern
AI training workflow have created a burst pattern in traffic that existing
solutions are ill-suited for. The paper proposes dcSim, a new transport
protocol that prevents congestion and packet loss. It accomplishes this
by creating a "shadow network" over the existing network that simulates
traffic before sending the actual data. In a simulated network, the protocol
achieves its goal of reducing congestion.

## Critique

The paper only tests dcSim within a simulated network and not a real one,
so the results may not reflect a real datacenter. The whole idea seems to
depend on precise timing. Would real switches and hosts keep that timing
consistent enough? The authors even show that data can be dropped after
its probe succeeds. I would like to see hardware tests before treating
the lack of losses as something we can rely on.

## Connections

Like [Unlocking ECMP Programmability for Precise Traffic Control]({{ site.baseurl }}{% post_url 2026-10-08-unlocking-ecmp-prog %}),
this paper works around ECMP randomness without replacing switches.
However, dcSim tests random paths rather than making next-hop selection
deterministic. Perhaps randomness is less of a problem if we can test
a path first?

