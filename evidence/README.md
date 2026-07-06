# Evidence archive — protecting this report against bit-rot

Every dated claim in [`../TIMELINE.md`](../TIMELINE.md) and the report at
[history.disclose.io](https://history.disclose.io) is anchored to an external artifact — a git
commit, a Wayback snapshot, a standard, a court opinion, a piece of legislation, or a press
release. Links rot. This directory keeps the receipts so the claims stay verifiable even after the
originals move or disappear.

## The four layers

Redundancy is the point — no single failure (a dead link, an archive.org outage, a repo deletion)
should take an assertion's proof with it.

1. **Local byte captures** — [`captures/`](captures/). The actual bytes of every fetchable source
   (HTML, PDF, GitHub commit/repo JSON, raw policy text) are committed into this repo. They travel
   with every clone, so the evidence survives even if every original URL dies. GitHub commit objects
   are content-addressed — the commit hash *is* the proof it hasn't been altered.
2. **Integrity hashes** — [`SHA256SUMS`](SHA256SUMS). A SHA-256 for every captured file. Verify with
   `sha256sum -c SHA256SUMS` (or `shasum -a 256 -c`). Any later tampering with a capture is detectable.
3. **Redundant web archives** — [`wayback-results.json`](wayback-results.json). Every live URL is
   (re)submitted to the Internet Archive's Wayback Machine, and its latest immutable snapshot URL is
   recorded. Wayback snapshots are themselves immutable and independently hosted.
4. **Rendered-in-browser confirmation** — the three sources that block automated fetching (SSRN,
   iso.org, X) were opened in a real logged-in browser to confirm they render with the expected
   content, and each is backed by a Wayback snapshot recorded in the manifest. No local HTML
   byte-capture is possible for these (they 403 to automation), which is disclosed per-row rather
   than hidden. Drop human screenshots into [`screenshots/`](screenshots/) for a visual layer on top.

## The index

[`manifest.json`](manifest.json) is the machine-readable map: for every source URL — its type, the
local capture path, the SHA-256, the byte count, the HTTP status at capture time, the capture
timestamp, and (from layer 3) its Wayback snapshot. [`MANIFEST.md`](MANIFEST.md) is the
human-readable version, grouped by the assertion each source supports.

## Re-running the capture

The captures are reproducible. Re-run the pipeline (see the project's working repo) to refresh the
byte captures, re-hash, and re-submit to Wayback. The `capturedAt` field records when each artifact
was last pulled.

## What is *not* here

Sources that block automated fetching (403 to bots) have no local HTML capture — they are covered
by a Wayback copy and a screenshot instead, and that is noted per-entry in the manifest. This is
disclosed, not hidden: an honest archive says where its coverage is thinner.
