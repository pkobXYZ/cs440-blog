---
layout: post
title: "OpenFLAME: A Federated Spatial Naming Infrastructure"
date: 2026-11-05
paper_authors: "S. Bharadwaj, Z. Ma, I. Liang, M. Farb, A. Rowe, S. Seshan"
paper_venue: "NINeS 2026"
paper_url: "https://nines-conference.org/papers/p020-Bharadwaj.pdf"
week: 7
tags: [dns]
---

## Key Idea

The paper introduces OpenFLAME, a system for different organizations to host
maps in a distributed way. OpenFLAME is implemented on top of DNS. OpenFLAME
does not maintain a global map database and instead delegates that functionality
to organizations. The end result is a system that allows for more granular mapping
than what was previously possible.

## Critique

The paper provides a clever way of solving the problem of distributed mapping,
but one has to ask whether or not DNS is the correct answer to this problem?
Reusing its infrastructure and caching makes sense, but overlapping map regions
require following multiple delegation chains. I would like to see whether the
deployment benefits outweigh that extra complexity at a larger scale.

## Connections

Like in [Unlocking ECMP Programmability for Precise Traffic Control]({{ site.baseurl }}{% post_url 2026-10-08-unlocking-ecmp-prog %}),
this paper builds new functionality on top of existing infrastructure. Both
approaches lower the cost of deployment, but depend on working around limitations
in systems designed for something else. Perhaps that is a necessary tradeoff for
getting a new architecture adopted?

