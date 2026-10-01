---
layout: post
title: "Understanding Partial Reachability in the Internet Core"
date: 2026-10-01
paper_authors: "G. Baltra, T. Saluja, Y. Pradkin, J. Heidemann"
paper_venue: "NINeS 2026"
paper_url: "https://nines-conference.org/papers/p004-Baltra.pdf"
week: 2
tags: [routing]
---

## Key Idea

The paper discusses partial reachability, a problem with the internet distinct from outages.
Partial reachability can take on two forms: "peninsulas," where a network can only reach another
network through an intermediary; and "islands," where a network can communicate internally,
but is isolated from the wider internet. The paper defines algorithms for detecting both phenomena
and tests them against public datasets. This new framework has wide reaching geopolitical and
reliability engineering implications.

## Critique

A perfect algorithm for detecting partial reachability would be O(n^2), making it infeasible.
The given algorithms give us a good heuristic answer, but still leave a lot to be desired. For
example, Chiloe cannot tell an outage from an island if that island does not contain any vantage
points. Taitao cannot identify a peninsulas in all cases either. I'm uncertain how one can
work around these issues without just increasing the amount of VPs. Work will have to be done
to address these problems.

## Connections

It is interesting how this paper effectively proves that the primary goal of the Internet's design,
as described in _The Design Philosophy of the DARPA Internet Protocols_, has persisted; depsite the
many shifts that have happended over the years, such as the move to centralized services in place of
peer-to-peer connections. Using the author's definition of the Internet core, there is no single
entity in the world that can seize it.

Additionally, it seems that partial reachability is a terminal condition of the internet. Like in
_There Is More to Internet Invariants Than Meets the Eye_, human organizational constraints lead to
patterns such as IP address cascade. Partial reachability is partially explained by disputes between
organizations, so as long as we have disputes (forever) we will have partial reachability. Perhaps
partial reachability should be treated as an invariant rather than a problem to be squashed?

