# Voting

## TL;DR

A vote is a plus or a minus on a post or a comment. It moves the post within an order, counts
towards the reputation of whoever wrote it, and counts towards the post's admission to the
catalog; it never removes anything. Not every vote counts the same — what the voter has earned
here adds to what their vote weighs.

## Definition

A vote is a plus or a minus, cast by a signed-in account on a post or a comment.

A vote does three things. It moves the post within an order, it counts towards the reputation of
whoever wrote it, and it counts towards the post's admission to the catalog. It does nothing
else: a vote never removes a post, never hides one, and never moves its address. A post leaves a listing only under the rules of moderation, with a public
record.

Not every vote counts the same. A vote carries a weight, and that weight rests on what the voter
has earned here: their rank, their reputation in the domain of the post, and the medals they hold.

Weight is bounded at both ends. No vote falls below the floor and none rises above its ceiling.
Weight applies to the plus and to the minus alike.

## Particulars

- A signed-in account votes. A guest does not.
- Nobody votes on their own post or their own comment.
- A vote may be changed or retracted at any time; voting never closes.
- Weight is read at the moment a vote is cast and does not change afterwards.
- Every value below is published and is identical for everyone.

## Implementation

Weight is a base of 1 and three additions. A person's vote is bounded to the range 1 to 10, an
organization's to 1 to 20:

```
weight = 1 + rank + reputation + medals
```

| Addition | What it adds |
| --- | --- |
| Rank | 1 for each step up the ladder: Newcomer 0, Contributor 1, Established 2, Distinguished 3, Eminent 4. |
| Reputation | 0.01 for every 100 points of reputation, counted within the domain of the post being voted on. Below zero adds 0, and never subtracts. |
| Medals | Each medal that carries weight computes its own addition — a fixed amount, or a multiplier on a stated measure — published with its conditions. Medals held together add together. A medal resting on a verified qualification adds only within the domain that qualification was verified in. |

Weight is carried to two decimal places.
