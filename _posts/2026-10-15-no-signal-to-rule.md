---
layout: post
title: "No Signal to Rule Them All: A Systematic Analysis of In-Network Congestion Signals"
date: 2026-10-15
paper_authors: "S. McClure, N. Dukkipati, S. Ratnasamy, S. Shenker"
paper_venue: "NINeS 2026"
paper_url: "https://nines-conference.org/papers/p012-McClure.pdf"
week: 4
tags: [cca, congestion]
---

## Key Idea

This papers aims to analyze different In-Network Telemetry (INT) signals used by
congestion control algorithms. INT signals often need to be specially implemented
in networking hardware. The paper found that, INT signals do not perform that much
better than E2E signals, except in a few special cases. Additionally, different INT
signals do better at optimizing different objectives (i.e. latency over throughput).

## Critique

The paper seems to be a rare instance of a _disproof_ of a hypothesis, namely that
INT signals don't perform much better than E2E signals. There is still a lot of work
to be done, such as trying new network configurations and INT signal variation. This
leaves the paper feeling a bit incomplete.

## Connections

Like in _Raha: A General Tool to Analyze WAN Degradation_, this paper is attempting
to algorithmically solve an optimization problem. Unfortunately, the paper did not
find results that were as fruitful when it comes to improving networks. Hopefully,
future work will change that.

