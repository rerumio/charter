# Trends algorithm

## TL;DR

The Trends algorithm sets the order of Trends: posts stand by how fast they gain vote weight,
counted within a moving window. It orders and does nothing else — it neither puts a post into
Trends nor takes one out.

## Definition

The algorithm orders the posts standing in Trends by the pace of their votes.

A post's score is the weight of the votes cast on it within a moving window. A plus adds its
weight and a minus subtracts it. A vote outside the window counts for nothing, and nothing
accumulates. The higher the score, the higher the post stands.

The algorithm orders and does nothing else. It does not decide what stands in Trends, does not
admit a post to the catalog, and does not move an address. The order is computed once and is the
same for everyone.

The length of the window and the cadence of recomputation are published values.

## Particulars

- What a vote weighs stands in voting.
- A vote counts as it stands: a changed vote counts anew, a retracted vote counts for nothing.
- A post with no votes within the window scores zero. Posts of equal score stand newest first.
- Who stands in Trends, and for how long, stands in admission to the catalog.

## Implementation

```
score(post) = pluses − minuses, counted in weight, over the votes cast within the window
```

| Value | Stands at |
| --- | --- |
| Window | 24 hours |
| Recomputation | every 15 minutes |
