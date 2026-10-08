---
layout: post
title: "Unlocking ECMP Programmability for Precise Traffic Control"
date: 2026-10-08
paper_authors: "Y. Liu, Y. Xiao, X. Zhang et al."
paper_venue: "NSDI 2025"
paper_url: "https://www.usenix.org/conference/nsdi25/presentation/liu-yadong"
week: 3
tags: [ecmp, ptc]
---

## Key Idea

The paper introduces Programmable ECMP (P-ECMP), which aims to bridge the gap between
the randomness of ECMP and the deterministic demands of Precise Traffic Control (PTC).
It accomplishes this through a clever trick via a little known feature, ECMP groups.
By using an additional group selector parameter, it can deterministically control
the next hop. This provides many benefits in network failover, load balancing, etc.

## Critique

The paper is good and provides a lot of incite into the inner-workings of ECMP. However,
it all seems to hinge on a "hack." Wouldn't the problem be better solved at the hardware
level? I suppose changing out all those switches would be prohibitively expensive. Still,
it seems like a bad idea to leave uncontrollable randomness in your network.

## Connections

Like _Understanding Partial Reachability in the Internet Core_ and _Raha: A General Tool
to Analyze WAN Degradation_, this paper covers inefficiencies in the way networks are
typically set up, which then lead to failure. However, unlike those previous papers,
this paper discusses how to respond to network failure rather than just analyzing or
anticipating it. As a result, this paper is much less algorithm heavy.

