# Casino Signal — Live Casino Statistics & Research Notes

A documentation-only research repository about live casino game statistics, observed round histories, bonus-frequency analysis, and data-quality methods. No source code, betting systems, scraped datasets, or predictive models are included here.

## What this project studies

Live casino dashboards can display recent game outcomes, but the useful question is how to *interpret* historical observations. This collection explains how to compare actual frequencies with theoretical benchmarks, recognize long gaps in observed events, and examine whether a recorded timeline is internally consistent.

**Topics:** live casino statistics, casino algorithms, game outcome distributions, Crazy Time bonus history, Ice Fishing bonus history, Fan Tan number tracking, streak analysis, and data integrity.

## Research notes

- [Understanding bonus gaps and streaks](docs/bonus-gaps-and-streaks.md) — probability of a run without a specific event, sample-size effects, and common interpretation mistakes.
- [Checking the quality of a round history](docs/round-history-data-quality.md) — duplicate identifiers, timing gaps, ordering and reporting considerations.

## Explore the live research tools

The following tools are part of **Casino Signal**, the online live casino analytics platform associated with these research notes:

| Tool | What it helps inspect |
| --- | --- |
| [Casino Signal — Live Casino Analytics](https://casino-signal.live/) | Main live casino statistics platform |
| [Strategy Lab](https://casino-signal.live/tools/strategy-lab/) | Explore historical condition/outcome sequences |
| [Crazy Time Bonus Drought Explorer](https://casino-signal.live/tools/bonus-drought/crazy-time/) | Examine recorded bonus-free intervals |
| [Ice Fishing Bonus Drought Explorer](https://casino-signal.live/tools/bonus-drought/ice-fishing/) | Examine observed bonus gaps |
| [Fan Tan Combination Explorer](https://casino-signal.live/research/fan-tan-lab/) | Inspect historical Fan Tan combinations |
| [Data Integrity Monitor](https://casino-signal.live/research/data-quality/) | Understand collection and continuity checks |
| [Bankroll Risk Simulator](https://casino-signal.live/tools/bankroll-calculator/) | Model how a sequence of stakes affects a hypothetical bankroll |

## A practical example

Suppose an outcome has probability `p = 0.10` per independent round. The theoretical probability of *not* seeing that outcome for 20 rounds is:

`P(no event in 20 rounds) = (1 - 0.10)^20 ≈ 0.1216`.

That is about **12.16%** for a specified 20-round window. This calculation describes an independent-round model; it does not establish that the next round is more likely to produce the event. Real historical data should also be checked for missing or duplicated rounds before comparing it to any benchmark.

## Scope and provenance

This repository contains explanatory notes rather than live data. When evaluating the web tools above, distinguish theoretical examples from measurements shown on the platform. The presence of a game or platform name here does not imply affiliation with its operator.

## Repository status

Documentation and research overview. No software package or API integration is distributed here.
