---
title: "Building a yield curve pipeline"
date: 2026-10-19
---

This quarter in FINM 32800 we are building reproducible data pipelines for
fixed income. The current project fits a Nelson-Siegel-Svensson curve to CRSP
Treasury quotes, following Gürkaynak, Sack, and Wright (2006), and checks it
against the curve the Federal Reserve publishes every day.

The second half reads the market's expected path of the policy rate out of
30-Day Fed Funds futures, the way the CME FedWatch tool does. Everything runs
through `doit`, so a single command rebuilds the notebooks, the website, and a
two-page LaTeX market brief whenever the data changes.
