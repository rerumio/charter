# Temperature

## TL;DR

Temperature is how present the holder of an account has been lately, computed from what they did
within a moving window. Recent action warms it, absence cools it, and nothing accumulates. It
affects nothing at all — it is shown on the account and goes no further.

## Definition

Temperature is a reading of an account: warm if its holder has been about lately, cold if they have
not. It is computed, never conferred. Nobody raises it and nobody lowers it.

It is read from what the holder did within a moving window. Recent action warms an account, absence
cools it, and nothing accumulates.

Temperature does one thing: it is shown on the account it belongs to. It grants no access, carries
no vote weight, and confers no rank. It is a reading of the account, not a standing of its holder.

## Particulars

- Action outside the window does not count.
- The formula and its scale are published and identical for everyone.

## Implementation

```
temperature = min(100, sum of points over the actions within the window)
```

The scale runs 0 to 100: 0 cold, 100 hot.

| Value | Stands at |
| --- | --- |
| Window | 30 days |
| A day present | 1 point |
| A post published | 15 points |
| A translation proposed | 5 points |
| A comment written | 3 points |
| A vote cast | 1 point |
| A post read | 1 point |
