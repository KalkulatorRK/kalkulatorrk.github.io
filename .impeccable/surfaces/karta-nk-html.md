---
version: 1
slug: "karta-nk-html"
primary_target: "karta-nk.html"
related_targets: []
---

# Surface brief — karta-nk.html

## Mode
Operate

## Job
Собрать типовой черновик технологической карты РК, скачать DOCX или напечатать A4, затем доработать файл у себя.

## Audience
Дефектоскопист / технолог ЛНК на объекте или в лаборатории.

## Structure
Sectioned accordion + sticky summary (seed 9acaf4b2, candidate 5). Live document preview. Static FAQ/справка below the tool. Client-side DOCX via JSZip. No AI consultant, no external LLM/API assistance.

## Constraints
Inherit PRODUCT.md / DESIGN.md. No purple AI palette, no side-tab cards, no nested cards. WCAG AA contrast. Russian UI. Help is FAQ, not chat.

## Unresolved
Customer-specific blank templates may remain a manual Word step by design.
