---
layout: post
title: "Revisiting RDMA Reliability for Lossy Fabrics"
date: 2026-10-27
paper_authors: "W. Li, X. Liu, Y. Zhang et al."
paper_venue: "SIGCOMM 2025"
paper_url: "https://dl.acm.org/doi/10.1145/3718958.3750480"
week: 5
tags: [rdma, congestion]
---

## Key Idea

RDMA is an important protocol that enables datacenters to transmit large
amounts of data in a latency sensitive manner through bypassing the regular
networking stack. RDMA traffic still has to deal with congestion, and historically
used PFC to counteract this. However, PFC introduces its own overhead. This paper
introduces DCP, which reacts to congestion by guaranteeing the delivery of control
information. This allows a quicker response to network congestion.

## Critique

The implementation of DCP takes significant overhead and relies on hardware support.
Furthermore, it isn't a complete solution to network congestion. More work will
have to be done on these two problems.

## Connections

Like in [Simulate Before Sending: Rethinking Transport in Datacenter Networks]({% post_url 2026-10-22-sim-before-sending %}),
this paper uses a simulated network to tests its transport architecture. It also
goes one step further and tests on a small physical network. The paper still falls
short of testing on a full blown datacenter. It will be interesting to see how the
architecture pans out.

