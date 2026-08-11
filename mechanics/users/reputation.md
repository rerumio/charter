# Reputation

## TL;DR

Reputation is the count of votes an account's posts and comments have collected, held separately in
each domain they write in. Within a domain it raises the weight of their votes and, above a published
figure, puts their posts into the catalog. Every voter counts for one, however heavy their own vote
is.

## Definition

Reputation is the sum of the votes cast on an account's posts and comments: a plus raises it, a minus
lowers it. It is what readers have made of the account's work.

It is counted by head, not by weight. A vote adds one whoever cast it — weight moves a post within
an order, it does not make one account's approval worth more than another's.

Reputation is held within a domain. An account holds one in each domain they have written in, and none
outside them.

Reputation does two things, each within its own domain. It raises the weight of the account's votes,
and above a published figure it admits their posts to the catalog as they lock. It grants
no access and confers no rank.

## Particulars

- A comment counts in the domain of the post it stands under.
- The profile shows the sum across the domains. Only the figure within a domain carries anything
  there.
- Reputation does not decay. How recently an account has been present is measured by temperature.

## Implementation

```
reputation(account, domain) = pluses − minuses
```

Counted over the account's posts and comments in that domain, one per voter, whatever the weight of
the vote.

What each point adds to vote weight stands in voting. The figure above which an account's posts are
admitted stands in admission.
