# Lab 2 · Reflection

**Name:**
**Due:** Sunday, November 8 at 11:59 PM

Answer in a few sentences each. Specific beats long.

**1. Your join.**I joined the electricity and industry tables using `state_fips` and `year`. Both tables had 51 rows before the join, and the result also had 51 rows. The electricity table originally used state names, so I added FIPS codes using a lookup table to make the keys consistent. After checking the join, I found no unmatched rows or duplicate keys, so I didn't need to remove any observations.

**2. The reading.** I think the relational model works best for both datasets. Each table has a simple structure, with one row per state in 2023 and a few columns describing electricity prices or industry establishments. Since both datasets share state and year identifiers, SQL makes it easy to connect them and compare the results.

A document model like JSON would add unnecessary complexity because there is no nested information. A graph model would also be less useful because I am comparing state-level values rather than studying relationships between connected entities. For this analysis, relational tables are the simplest and most practical choice.
---

**Checklist before you submit**

- [ ] `notebooks/lab2_joins.ipynb`: Part A run in class, Part B completed with your own tables
- [ ] Every Part B text cell filled in (grain, unmatched rows, what the result tells you)
- [ ] This file answered
- [ ] Notebook saved (Cmd+S), then committed and pushed
- [ ] Repo URL submitted on CourseWorks
