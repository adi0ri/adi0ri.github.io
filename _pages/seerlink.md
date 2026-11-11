---
layout: page
title: Seerlink
description: An internal tool for finding and reviewing local business opportunities at Seeryn.
permalink: /seerlink/
---

I co-built Seerlink with my business partner at Seeryn. We wanted one place to find local businesses, see what their websites actually needed, and decide which opportunities deserved a closer look.

## A sample review

_Pine & Thread Tailoring is fictional. This example uses synthetic data._

| Step       | What the reviewer sees                                                                                             |
| ---------- | ------------------------------------------------------------------------------------------------------------------ |
| Discover   | A local tailoring business and its official website, matched to one record.                                        |
| Audit      | A mobile usability issue observed on the services page, with the page recorded as evidence.                        |
| Prioritize | Separate signals for the website opportunity, the business fit, and confidence in the published contact.           |
| Review     | The reviewer checks the evidence and approves or skips the opportunity. An unreachable site goes to manual review. |

## An engineering decision I worked on

I worked on recovery in the research workflow and on keeping the review view current. A failed re-audit preserves the last completed scores. A site the crawler has never reached gets an unavailable audit status. That lets a reviewer distinguish a finding with evidence from an incomplete check.

The application uses a Next.js dashboard, a SQLite persistence layer, and Google Places for business discovery. Website checks use a bounded crawler, and a reviewer makes the final outreach decision.
