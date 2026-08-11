# Post metadata

## TL;DR

A post is the unit of publication: one text, of one type, in one domain, in one language. It is made
of parts — some fixed at publication for good, the rest editable only until the post is locked.
Votes, admission, reputation and comments attach to the post.

## Definition

A post is the unit of publication: one text, of one type, in one domain, in one language.

A post is made of parts. Some are settled at publication and never change; the rest change only
while the post is unlocked; addenda alone are appended after the lock. Where the post sits — its
domain, topics and keywords — its authors settle at publication; after that only a holder of
`taxonomy` moves it.

A post is published unlocked. Its authors lock it at any moment, and it locks on its own after a
published term. A lock is never lifted.

A post has one permanent address.

Votes, admission, reputation and comments attach to the post.

## Particulars

- The title names the subject of the post.
- A post belongs to all its authors equally and stands under each of their names.
- Any account claims authorship of a post. A holder of `moderate` decides the claim; approved,
  the claimant joins the post's authors.
- The summary is written by its authors and stands for the post wherever the post is listed.
- A post stands in three tiers: the summary, the body, and an extended version. The extended
  version alone is optional.
- The body holds text and images. Images are held by the platform; video and every other medium is
  embedded, and the platform holds none of it.
- A narration — the article read aloud, by an author or made professionally — is attached to the
  post and held by the platform.
- A post is original or borrowed. A borrowed post names the source of the original.
- A passage a machine generated is marked as machine-generated where it stands.
- An addendum is appended and never removed.
- An edited post is marked as edited.
- A comment is never edited. Whoever wrote it removes it; a holder of `moderate` hides it.

## Implementation

| Part | Required | Changes by |
| --- | --- | --- |
| Title | yes | its authors, until the post is locked |
| Summary | yes | its authors, until the post is locked |
| Body | yes | its authors, until the post is locked |
| Extended version | no | its authors, until the post is locked |
| Sources | by type | its authors, until the post is locked |
| Licence | yes | its authors, until the post is locked |
| Authors | one or more | its authors, until the post is locked; an approved claim, at any time |
| Type | yes | never |
| Origin | yes | its authors, until the post is locked |
| Language | yes | never |
| Domain | yes | a holder of `taxonomy` |
| Topics | no | a holder of `taxonomy` |
| Keywords | no | a holder of `taxonomy` |
| Addenda | no | appended, never removed |
| Narration | no | its authors, until the post is locked |

A post locks on its own 7 days after publication. The body runs from 1,500 to 200,000
characters. Images and the narration are held under published size limits.
