# Lab 1

**Name:**
**Due:** Sunday, October 25 at 11:59 PM
**Submit:** your repo URL in the Lab 1 assignment on CourseWorks

| Part | Where | File |
|---|---|---|
| **In class:** first DuckDB query on the penguins data | Session 1 | `notebooks/lab1_first_query.ipynb` |
| **At home:** two related tables of your own in DuckDB | Before Sunday | `notebooks/lab1_home_your_data.ipynb` |
| **At home:** lifecycle map of your data | Before Sunday | This file (below) |

---

## Lifecycle map of your data

In class we named five stages every data system has. Trace them for the two tables you loaded at home. Some rows ask what you did this week; the last two ask you to look ahead to the system you'll build by December. Educated guesses are fine; say where you're unsure.

**My tables:** `industry` (Census CBP 2023) + `electricity` (EIA 2023)

| Stage | Your answer |
|---|---|
| **1. Ingestion** | Downloaded Census CBP and EIA data and converted both to CSV. Changes in source formats could break imports. |
| **2. Validation** | Both datasets have 51 records, correct data types, no missing values, and 51 matching geographic keys. |
| **3. Transformation** | Filtered NAICS 518210, selected 2023 electricity prices, and converted state FIPS codes to names for the JOIN. |
| **4. Scheduling** | Both datasets are updated annually. I would refresh the analysis when new matching-year data becomes available. |
| **5. Interface** | Urban planners and investors could compare electricity prices and industry establishments across states using a dashboard. |

**Which stage feels most fragile, and why?**

Transformation is most fragile because the datasets use different state identifiers, and establishment counts do not directly measure physical data center capacity.
## Checklist before you submit

- [ ] In-class notebook: every cell ran, including your own query and three observations
- [ ] At-home notebook: both CSVs in `data/`, both tables loaded and checked, the key relationship described, five queries each with a one-line note, three observations, two dataset cards
- [ ] This lifecycle map filled in, plus the "most fragile" answer
- [ ] Every notebook saved (Cmd+S), then committed and pushed
- [ ] Repo URL pasted into CourseWorks
