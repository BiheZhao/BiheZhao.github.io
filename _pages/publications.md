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
  /* Publication list: keep the badge + thumbnail column usable at every width.
     The theme's default (2 of 12 grid columns) gets too small below ~1000px. */
  .publications .row > .abbr { padding-right: 0; }
  @media (max-width: 575.98px) {
    .publications .row > .abbr { flex: 0 0 30%; max-width: 30%; }
    .publications .row > .col-sm-8,
    .publications .row > .col-sm-10 { flex: 0 0 70%; max-width: 70%; }
    .publications .row > .col-sm-8 .title,
    .publications .row > .col-sm-10 .title { font-size: 0.95rem; }
  }
  @media (min-width: 576px) and (max-width: 767.98px) {
    .publications .row > .abbr { flex: 0 0 26%; max-width: 26%; }
    .publications .row > .col-sm-8,
    .publications .row > .col-sm-10 { flex: 0 0 74%; max-width: 74%; }
  }
  @media (min-width: 768px) and (max-width: 991.98px) {
    .publications .row > .abbr { flex: 0 0 22%; max-width: 22%; }
    .publications .row > .col-sm-8,
    .publications .row > .col-sm-10 { flex: 0 0 78%; max-width: 78%; }
  }
  @media (min-width: 992px) {
    .publications .row > .abbr { flex: 0 0 18%; max-width: 18%; }
    .publications .row > .col-sm-8,
    .publications .row > .col-sm-10 { flex: 0 0 82%; max-width: 82%; }
  }
</style>

<!-- Bibsearch Feature -->

{% include bib_search.liquid %}

<div class="publications">

{% bibliography %}

</div>
