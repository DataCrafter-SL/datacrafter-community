---
title: Earthquakes, collected daily
summary: A public feed collected into dated snapshots each morning, so the trend builds itself.
author: DataCrafter
version: 0.90.1
date: 2026-11-04
media:
  - file: 01-workflow.png
    alt: "The Collect earthquakes Workflow after its run: fetch the day from the USGS, load it, register the day, count by region and magnitude, then report. Every step says SUCCESS."
  - file: 02-schedule.png
    alt: "The Scheduler. The Collect earthquakes daily Schedule is armed and runs the Workflow at 11 am each day, Queensland time. Its fire on 4 November succeeded."
  - file: 03-instances-by-day.png
    alt: The Earthquakes data source's instances, one per day from 3 October to 3 November 2026, each READY.
  - file: 04-report.png
    alt: "The report for 3 November: earthquakes per day by magnitude band for the last 30 days, 5 October to 3 November, with the 30-day totals at the foot: 1,973 in all, the largest magnitude 7.7."
---
Each morning DataCrafter fetches the previous day's earthquakes of magnitude 2.5 and over
from the United States Geological Survey's public event service. It loads them as that
day's snapshot, then counts them by region and magnitude band and builds a 30-day report.
Nobody touches it: the Scheduler starts the run at 11 am Queensland time, an hour after the
UTC day ends.

Each day is kept as its own dated snapshot, so the history grows by one day each morning
and the report reads all the days collected so far. This one started with a 90-day backfill.

The data is the USGS's own, unchanged. The fetch is one approved host command per day.
