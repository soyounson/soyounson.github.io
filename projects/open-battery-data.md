---
layout: project
title: Open Battery Data
slug: open-battery-data
permalink: /projects/open-battery-data/
---

## The question

Before building anything on battery health or fire risk, the first question is simply: *what open data exists, what does it actually record, and can I download it?* The answers are scattered across lab sites, data portals, papers and fire-agency pages, and they rarely use the same terms.

Open Battery Data collects them in one place, checked against each source, and shows where each dataset comes from.

## What's in it

15 open datasets in four groups:

- **EV field data (5)**: battery signals recorded in real vehicles, from 5 buses to 464 vehicles, including 21 Korean E-GMP taxis (NCM) sampled every second
- **Lab cell data (7)**: cells cycled to end of life (NASA, CALCE, MIT / Stanford / TRI, Sandia) and abuse tests that force thermal runaway (NREL Battery Failure Databank, Sandia ARC)
- **EV fire incidents (2)**: the Korean National Fire Agency's EV fire records and the EV FireSafe global database
- **ESS fire incidents (1)**: EPRI's stationary storage failure database

For each one: access (open, login, or request), country, signals (V, I, T, SOC, SOH, R and more), how it was collected and how often, chemistry, scale, license and source. Anything the source doesn't state is marked **n/s** rather than guessed.

## What the catalogue shows

- **No open dataset links an EV's own telemetry to a fire on that vehicle.** Telemetry and fire records exist only separately, which is the main gap for data-driven fire risk work.
- Field data is collected in very different ways: BMS telemetry, CAN data loggers that stop while charging, or charging-station records that only see charging. That shapes what each dataset can and can't tell you.
- Chemistry is often unstated, even for large EV datasets.

## Design

- **Globe first**: a dotted globe with one icon per data type (car, flask, flame, bolt). Tap a marker for a detail card; datasets from the same site are grouped.
- **Tables below**: the same four groups as the README, so the site and the repository never disagree.
- Black background and glass panels in the same Apple-style look as this site, with Tesla red and blue accents.

## Stack

One `datasets.csv` is the single source of truth. A Python build script generates the README and the site's data; a download script fetches the five datasets that have direct links. The globe uses globe.gl (three.js), hosted on GitHub Pages.

## Next

- Fill in `n/s` values as datasets are opened
- Add new datasets as they're published
- Use it to pick the data for the next battery project
