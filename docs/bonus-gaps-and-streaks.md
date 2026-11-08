# Understanding Bonus Gaps and Streaks in Live Casino Data

A long interval without a particular result can feel remarkable. To determine whether it is statistically unusual, first define the event, the observation window, and a reference probability.

## 1. Define an event precisely

For an analysis of Crazy Time bonus history or Ice Fishing bonus history, a tracked event might be one named bonus result. Avoid combining different event types without stating the rule. Record whether the count covers all rounds or only a subset.

## 2. A simple independent-round model

If an event has constant probability `p` in each independent round, the probability it will not appear in a sequence of `n` rounds is:

`P(no event in n rounds) = (1 - p)^n`

For illustration only, with `p = 0.10`:

| Rounds without the event | Probability for a specified window |
| ---: | ---: |
| 5 | 59.05% |
| 10 | 34.87% |
| 20 | 12.16% |
| 30 | 4.24% |

These figures are calculated from an example probability, not measured or claimed odds for a named game.

## 3. Why the observation period matters

A 20-round drought in a single predefined window is different from searching through thousands of overlapping windows and selecting the longest drought after the fact. The latter approach is much more likely to identify an extreme-looking streak. Report the number of rounds reviewed and whether the event was selected before or after examining the results.

## 4. Compare windows consistently

When comparing 10-minute, 1-hour, and 24-hour periods, show both raw counts and the number of completed rounds. A longer time interval does not always contain a proportional number of rounds; breaks in collection and game pace can affect coverage.

## 5. Data quality comes before interpretation

Duplicate round IDs, missing timestamps, reordered observations, or inconsistent labels can produce misleading miss-streak values. The companion note, [Checking the quality of a round history](round-history-data-quality.md), outlines practical checks.

## Related tools

- [Casino Signal Strategy Lab](https://casino-signal.live/tools/strategy-lab/)
- [Crazy Time Bonus Drought Explorer](https://casino-signal.live/tools/bonus-drought/crazy-time/)
- [Ice Fishing Bonus Drought Explorer](https://casino-signal.live/tools/bonus-drought/ice-fishing/)

These pages let readers explore historical observations rather than relying only on an illustrative formula.
