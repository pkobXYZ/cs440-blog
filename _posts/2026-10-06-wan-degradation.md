---
layout: post
title: "Raha: A General Tool to Analyze WAN Degradation"
date: 2026-10-06
paper_authors: "B. Arzani, S. Taheri, P. Namyar, R. Beckett, S. K. Kakarla, E. Jalilipour"
paper_venue: "SIGCOMM 2025"
paper_url: "https://dl.acm.org/doi/10.1145/3718958.3754348"
week: 2
tags: [design, performance, planning, wan]
---

## Key Idea

The paper introduces the RAHA algorithm for analyzing performance degradation of wide area
networks (WANs). Unlike previous algorithms, RAHA will not make make assumptions like limiting
the maximum number of failures and it measures the _difference_ in performance between a the
network in a healthy and failed state. Overall, the algorithm provides a more robust tool for
network operators to find possible issues and fix them before they become a problem.

## Critique

The paper is overall well written. The mathematical notation for RAHA can be hard to follow,
there are many variables defined. The paper can use more pseudo-code.

## Connections

This paper is a great case study in how to work through design invariants, like those discussed
in _There Is More to Internet Invariants Than Meets the Eye_. Rather than throwing the invariants
away like previous algorithms, RAHA seeks to take them _all_ into account.

Also, this paper is similar in structure to _Understanding Partial Reachability in the Internet Core_.
Both present new algorithms which seek to improve on previous work. Both take a heuristic approach, since
finding a perfect solution would be computationally infeasible.

