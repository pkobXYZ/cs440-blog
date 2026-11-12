---
layout: post
title: "Tight Loops, Smooth Streams: Responsive Congestion Control for Real-Time Video"
date: 2026-11-12
paper_authors: "P. Karimi, S. Fouladi, V. Sivaraman, M. Alizadeh"
paper_venue: "NINeS 2026"
paper_url: "https://nines-conference.org/papers/p009-Karimi.pdf"
week: 8
tags: [congestion, video]
---

## Key Idea

Typical congestion control algorithms don't play well with real-time video. This is caused
by slow reaction to network changes by video rate controllers working poorly with the tight
feedback loop of CCAs. The paper introduced Vidaptive, a framework that decouples encoding
and transmission by injecting dummy packets to "feed" the CCA. This improves network utilization,
reduces latency spikes, and works with existing CCAs.

## Critique

The results are interesting, but is there a way to accomplish this without wasting bandwidth
with injected dummy packets? The overhead can be quite substantial, 30-65%. The authors suggest
putting error correcting data in the dummy packets, which could reduce waste. Future work should
expand on this.

## Connections

Like in [LeoCC]({{ site.baseurl }}{% post_url 2026-11-10-leocc %}), the paper deals with problems
arising from traditional congestion control algorithms. They take different approaches however,
LeoCC is an entirely new CCA, whereas this paper seeks to adapt the application to pre-existing CCAs.
This presents an interesting dichotomy, is it better to change the CCA or the application?
