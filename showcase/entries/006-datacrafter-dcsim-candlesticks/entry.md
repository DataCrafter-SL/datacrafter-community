---
title: DCSIM, a simulated share in candlesticks
summary: A fictional share whose every price DataCrafter makes and rolls up, drawn by Excel as daily candles with a 10-day moving average. Simulated prices. Not real market data.
author: DataCrafter
version: 0.94.2
date: 2026-11-13
media:
  - file: 01-daily-candles.png
    alt: "The report for 13 November 2026, opened in Excel: a stock chart of DCSIM's last 60 trading days, 24 August to 13 November, as green up and red down candles with wicks, and the 10-day simple moving average as a dark line. The price falls from about 99 to 93 in September, climbs to about 111 in late October, eases to about 101 and closes at 110.34. Simulated prices. Not real market data."
  - file: 02-intraday-bars.png
    alt: "The same report's second chart in Excel: the 24 fifteen-minute bars of 13 November 2026, 10:00 to 15:45 Sydney time. The day opens at 109.13, reaches 111.32 around midday and closes at 110.34. Simulated prices. Not real market data."
  - file: 03-workflow.png
    alt: "The Trade a DCSIM day Workflow in the web client after its run for 13 November 2026, every step SUCCESS: draw the day's bars, copy every day so far, pair each bar with the bars before it, add up the returns, make the prices, roll up the daily candles, pair each day with the nine before it, the moving average, then the report."
  - file: 04-report-runs.png
    alt: "The report in the web client with its list of stored runs open: one run for each trading day, newest first from 13 November 2026, weekends skipped. Behind it, the web viewer draws the daily chart's moving average and notes that the candles are shown in Excel."
---
DCSIM is a made-up share. Its prices are simulated: they are not real market data, and DCSIM is
not a listed code. DataCrafter makes every price itself. Each weekday a Data Generator draws 24
fifteen-minute bars from 10:00 to 16:00 Sydney time, as a seeded random walk from 100.00. Each
bar opens where the last one closed, so each day opens at the previous day's close. Weekends
are skipped. Public holidays are not modelled.

DataCrafter then turns the draws into prices, rolls each day up into one candle (the first
bar's open, the last bar's close, the day's high and low), and averages the last ten closes.
The report stores one run per trading day. Excel draws its two stock charts from those stored
figures. The web client shows the same figures and the moving-average line; stock charts are
drawn in full in Excel.

The whole build went through DataCrafter's connection for AI assistants (MCP), with no
hand-written scripts against the server, and it was replayed the same way onto this demo. Every
bar, every daily candle and every moving average was recomputed outside DataCrafter from the
raw draws, and every one agreed. A new trading day is added each weekday at 4.30 pm Sydney time.
