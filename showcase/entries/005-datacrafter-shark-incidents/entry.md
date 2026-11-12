---
title: Shark incidents, kept release by release
summary: The Australian Shark-Incident Database, one snapshot a month since its first release, with what each new release changed.
author: DataCrafter
version: 0.94.2
date: 2026-11-13
media:
  - file: 03-per-decade.png
    alt: "The report for 13 November 2026 in the web client: a column chart of unprovoked incidents per decade since 1900, by outcome. Injured incidents rise from about 10 a decade early in the century to 101 in the 2010s; fatal incidents stay between 5 and 26 a decade."
  - file: 01-workflow.png
    alt: "The Collect shark incidents Workflow after its run on 13 November 2026, every step SUCCESS: fetch the newest release, load the incidents and the release, register them, four summaries, the incident changes model, then the report."
  - file: 02-collection-days.png
    alt: "The report's list of stored runs: ten collection days from 29 October 2021 to 13 November 2026, one for each release of the database and one for today."
  - file: 04-last-30-years.png
    alt: "The same report scrolled to its second chart: unprovoked incidents a year from 1997 to 2026 as blue columns, with the fatal ones beside them in orange. The busiest year is 2020, with 28 incidents, 7 of them fatal."
---
The Australian Shark-Incident Database records every known encounter between a shark and a
person in Australian waters since 1791, with its outcome, the species and what the person was
doing. Its curators publish a new release on Zenodo a few times a year. DataCrafter keeps one
dated snapshot of the database each month, so any month's figures can be read back as they
stood then.

History came for free here: every past release stays on Zenodo, so the first build loaded
nine of them, each dated by the day it was released. One report shows incidents per decade,
the last 30 years, the states, the species and the activities. It also says what changed
since the previous snapshot: release 10 added 8 incidents to release 9. A month with no new
release says so, and that nothing changed.

Each snapshot's figures were recounted straight from the published workbook, outside
DataCrafter, and every one agreed. The report loads only what it shows. It holds no victim
details and none of the database's free text.

Source: Australian Shark-Incident Database, release 10, by P Meagher (Taronga Conservation
Society Australia) with C Bradshaw, C Huveneers, M Riley (Flinders University), V Peddemors
(NSW DPI) and D Slip, Zenodo, doi:10.5281/zenodo.22262542, licensed under CC BY 4.0. Data
descriptor: Riley et al. (2022), Scientific Data 9: 378, doi:10.1038/s41597-022-01453-9. The
database's creators do not endorse this page. The fetch is one approved host command a month,
and it sends only GET requests with no credential.
