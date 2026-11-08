# Checking the Quality of a Live Casino Round History

Statistical analysis depends on what was recorded. A dataset of thousands of rounds can still be unsuitable for fine-grained interpretation if identifiers are repeated or observations were lost.

## A minimal review checklist

1. **Identifiers:** Are any round IDs duplicated? If so, distinguish true duplicates from legitimate updates to an existing round.
2. **Ordering:** Does the displayed sequence follow the intended event-time order, rather than the time a request completed?
3. **Timestamp coverage:** Are there large or unexplained gaps between recorded rounds?
4. **Outcome labels:** Are names consistently normalized across historical periods?
5. **Count reconciliation:** Do the totals by outcome add up to the count of included rounds?
6. **Collection horizon:** Does each chart clearly say which games and time windows it covers?

## Example: a duplicate observation

Imagine the sequence of recorded identifiers:

`R-101, R-102, R-102, R-103`

If the second appearance of `R-102` is the same underlying round, counting every record as a distinct round will inflate both the sample size and the frequency of its outcome. The correct handling depends on the data contract, but the duplicate should not silently become a new independent round.

## Why timestamp gaps deserve context

An unusually long interval between two recorded rounds can result from a genuine pause in the game, delayed network delivery, temporary source unavailability, or a missed collection cycle. It is an anomaly to investigate, not automatic evidence of an unusual game outcome.

## Separating measurement from interpretation

Keep raw observations, cleaned observations, and calculated metrics conceptually separate. A miss-streak, hit-streak, or HOT/COLD indicator is derived from the recorded observations and the chosen reference probabilities. The same apparent pattern can change when duplicate records are removed or a missing interval is accounted for.

## Further reading and tools

- [Casino Signal Data Integrity Monitor](https://casino-signal.live/research/data-quality/)
- [Casino Signal — Live Casino Analytics](https://casino-signal.live/)
- [Understanding bonus gaps and streaks](bonus-gaps-and-streaks.md)

This repository is a documentation resource; it does not publish underlying database records or claim to be an independent audit of any casino operator.
