---
title: Mortgage rates, collected daily
summary: Every Australian bank's published home loan rates, collected each morning into a dated snapshot and read by one report.
author: DataCrafter
version: 0.91.0
date: 2026-11-06
media:
  - file: 01-workflow.png
    alt: "The Collect mortgage rates Workflow after its run on 6 November: collect the day's rates, load the rates and the RBA cash rate, then four aggregations and a changes model feed the report. Every step after the collection says SUCCESS. The collection says WARNING because 4 of 116 banks did not answer."
  - file: 02-schedule.png
    alt: "The Scheduler: the Schedule Collect mortgage rates daily is armed, runs at 7 am every day as nick, and fired on 6 November at 7:00 with the outcome WARNING. The next run is 7 November at 7:00."
  - file: 03-league-table.png
    alt: "The report for 6 November, part 1: the lowest published owner-occupier variable rate of each of 91 banks, lowest first, from RACQ Bank's Green Home Loan at 2.79 per cent. Beside it, the 30-day trend: only its last day, 6 November, is filled so far, with the average of every bank's lowest rate, the four major banks and the RBA cash rate of 4.85."
  - file: 04-ten-lowest.png
    alt: "The report for 6 November, part 2: the ten lowest rates and the product each comes from. A green loan and a veterans' loan lead, then ordinary variable loans from 5.93 per cent."
---
Each morning DataCrafter collects the home loan rates that every Australian bank publishes
under the Consumer Data Right, plus the Reserve Bank's cash rate target. One run asks 116
banks for about 1,500 product pages, loads more than 8,000 rates as that day's snapshot,
and builds a report: each bank's lowest variable rate, the ten lowest products, what
changed since the day before, and a 30-day trend beside the cash rate.

Nobody touches it: the Scheduler starts the run at 7 am Queensland time. Each day is kept
as its own dated snapshot, so the trend and the day-on-day changes grow by one day each
morning. These pictures show the first day.

The rates are each bank's own, as published. Product data under the Consumer Data Right
carries no conditions on its use (CDR Rules 2020, rule 2.6); no bank endorses this page.
Cash rate: Source: Reserve Bank of Australia 2026, CC BY 4.0. The fetch is one approved
host command per day, and it sends only GET requests with no credential.
