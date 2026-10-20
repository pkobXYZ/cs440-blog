---
layout: post
title: "Waiting for QUIC: Passive Measurements to Understand QUIC Deployments"
date: 2026-10-20
paper_authors: "J. Mücke, M. Nawrocki, R. Hiesgen et al."
paper_venue: "CoNEXT 2025"
paper_url: "https://dl.acm.org/doi/10.1145/3768988"
week: 4
tags: [quic]
---

## Key Idea

This paper aims to systemically analyze the rollout of the QUIC protocol
after standardization in 2021. The protocol features built in encryption
that makes it difficult to analyze, so the authors employ a passive
measurement technique verified with active measurement. They find that
QUICv1 has experienced rapid adoption. While they're at it, they also
found information that hypergiants (Google, Meta, etc.) hide from the
public, such as load balancer configuration.

## Critique

Overall, the paper feels unfocused. What central question is it trying
to answer? Is it merely about QUIC adoption? Is it about passive
measurement techniques? Is it about using QUIC to reveal hidden
information? 

## Connections

The paper seems to suffer from the same problem that _Understanding
Partial Reachability in the Internet Core_ has to contend with, namely
that the quality of its measurements depend on where the vantage points
are located. This could make some of its finding a skewed picture.

