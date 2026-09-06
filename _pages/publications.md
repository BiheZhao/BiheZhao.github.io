---
layout: page
permalink: /publications/
title: Publications
description: Publications in reversed chronological order. * denotes equal contribution.
nav: true
nav_order: 2
---

<!-- _pages/publications.md -->
<style>
  /* Paper thumbnails: uniform 2:1 frame; non-2:1 figures are letterboxed on white, centered */
  .publications .abbr img.preview {
    aspect-ratio: 2 / 1;
    width: 100%;
    height: auto;
    object-fit: contain;
    object-position: center;
    background: #ffffff;
    padding: 3px;
  }
  /* Venue badges: condensed label font; keep venue capitalization (NeurIPS) */
  .publications .abbr abbr {
    font-family: "Barlow Semi Condensed", "Roboto", sans-serif;
    font-weight: 700;
    font-size: 0.9rem;
    letter-spacing: 0.05em;
    text-transform: none;
    padding-top: 0.15rem;
    padding-bottom: 0.15rem;
  }
  /* Publication list: keep the badge + thumbnail column usable at every width.
     The theme's default (2 of 12 grid columns) gets too small below ~1000px. */
  .publications .row > .abbr { padding-right: 0; }
  @media (max-width: 575.98px) {
    .publications .row > .abbr { flex: 0 0 36%; max-width: 36%; }
    .publications .row > .col-sm-8,
    .publications .row > .col-sm-10 { flex: 0 0 64%; max-width: 64%; }
    .publications .row > .col-sm-8 .title,
    .publications .row > .col-sm-10 .title { font-size: 0.95rem; }
  }
  @media (min-width: 576px) and (max-width: 767.98px) {
    .publications .row > .abbr { flex: 0 0 30%; max-width: 30%; }
    .publications .row > .col-sm-8,
    .publications .row > .col-sm-10 { flex: 0 0 70%; max-width: 70%; }
  }
  @media (min-width: 768px) and (max-width: 991.98px) {
    .publications .row > .abbr { flex: 0 0 27%; max-width: 27%; }
    .publications .row > .col-sm-8,
    .publications .row > .col-sm-10 { flex: 0 0 73%; max-width: 73%; }
  }
  @media (min-width: 992px) {
    .publications .row > .abbr { flex: 0 0 24%; max-width: 24%; }
    .publications .row > .col-sm-8,
    .publications .row > .col-sm-10 { flex: 0 0 76%; max-width: 76%; }
  }
</style>

<!-- Bibsearch Feature -->

{% include bib_search.liquid %}

<div class="publications">

{% bibliography %}

</div>
