---
"@emdash-cms/admin": patch
---

Fix the content list showing "Pending changes" for draft or scheduled entries that have never been published.

A never-published entry only has a `draftRevisionId`, so the previous check (`draftRevisionId !== liveRevisionId`) was always true once the draft had been saved more than once. The list now matches the editor and only shows "Pending changes" when the entry is live and the draft revision differs from the live revision.
