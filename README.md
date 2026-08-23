# Schema Studio — Learn Dimensional Modelling by Building It

**Live app:** https://shauryadevhub.github.io/data-modeling-with-coach/

Schema Studio is a hands-on, browser-based tool for learning Kimball-style dimensional data modelling — not by reading about star schemas, but by building them. You drag real tables onto a canvas, decide what's a fact and what's a dimension, and get a scored, explained review of your design.

## Why this exists

Most data modelling tutorials are static: diagrams and prose explaining what a star schema *is*. That doesn't build the instinct for declaring grain, spotting a snowflaked dimension, or knowing when an accumulating snapshot fits better than a periodic one. Schema Studio is built on the belief that dimensional modelling is a skill you build with your hands — so every concept here is something you construct, break, and fix, with a coach checking your work.

## What's inside

**Read the concepts first** — a proper primer, not a glossary:
- Kimball's **four-step design process**: select the business process → declare the grain → identify the dimensions → identify the facts.
- **Nine building blocks**: fact and dimension tables, grain, star vs snowflake, surrogate keys, slowly changing dimensions, additivity of measures, degenerate and junk dimensions, factless facts and bridge tables.
- **The Kimball architecture**: source systems → ETL back room → presentation area → BI applications, plus the bus matrix and how Kimball's bottom-up approach differs from Inmon's.

**Practice scenarios** — five real business cases, starter to intermediate: retail sales, ride-sharing trips, hospital appointments, streaming sessions, and an e-commerce orders snowflake. Each hands you a pool of tables and a business story — some tables belong in the model, some are decoys you're meant to leave out.

**Check my schema** — the core loop. Submit your design and get a percentage score, a line-by-line verdict on every placement (including tables you correctly excluded), and a written coach's review explaining *why* the model works or where the grain slipped. Hints and a solution reveal are there when you're stuck.

**Two build modes** — *Guided slots* for beginners (drop tables into a fact-in-the-middle layout) and *Free canvas* for advanced learners who place tables anywhere and declare roles themselves.

**Advanced studio** — four drills for learners past the basics:
- *Challenges* — periodic snapshot facts, accumulating snapshot facts, and a multi-hierarchy snowflake.
- *ER drills* — reading and building entity-relationship diagrams.
- *NoSQL drills* — modelling for MongoDB and Cassandra, where the rules change.
- *Ask the coach* — open Q&A on Kimball vs. Inmon and dimensional modelling concepts.

**Custom table builder** — define your own fact and dimension tables with columns, types, and keys to practice beyond the scripted scenarios. Progress saves locally in your browser.

## Screenshots

![Home screen](screenshots/01-hero.png)

![Kimball's four-step design process](screenshots/02-concepts.png)

![Building the retail sales star schema](screenshots/03-builder.png)

![Check my schema — score, verdicts, and coach's review](screenshots/04-check-schema.png)

## Tech

A single self-contained `index.html` — no build step, no server, no dependencies, no account. Scoring is rule-based and runs locally, so the tool works fully offline.

## Running it locally

Clone the repo and open `index.html` in any browser. That's it.

## Status

**v1** — first public iteration. Scenarios, drills, and UI will keep evolving; feedback and issues welcome.
