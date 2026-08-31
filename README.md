# .github

The FlashyLabs organisation repository. It holds two unrelated things and it is
worth knowing which is which before editing either.

## `profile/README.md` is the organisation's front page

That file is what GitHub renders at
[github.com/FlashyLabs](https://github.com/FlashyLabs) — the first thing a
stranger sees. It is not documentation for this repository, and a change to it
is a change to a public page. This file, the one you are reading, is the
repository's own README and appears nowhere but here.

## The rest is the estate's record of itself

Like every repository in this estate, this one publishes what it intends and
what it shipped:

| File | What it is |
|---|---|
| `backlog.fragment.json` | `backlog/1` — the future tense. Decays; never sealed. |
| `shiplog.fragment.json` | `shipped/1` — the past tense. Sealed; never decays. |
| `checkpoint.json` | `checkpoint/1` — an RFC 6962 tree head over the sealed claims. |
| `directory.fragment.json` | `directory/1` — this repository's nodes and edges in the estate graph. |

It emits those because the organisation profile is a thing that changes and had
no record of any of it. `docs/tenses.md` in flashyos says why the two tenses are
shaped differently and what breaks if you make them symmetric.

## Rules

**`vendor-*.mjs` are copies, not sources.** They are byte-identical to their
originals in flashyos, and `node tools/estate-hygiene.mjs` there reports any
that have drifted. Editing one here does not change the format — it makes this
repository disagree with the estate, silently, about whichever field somebody
just changed.

**The fragments are generated.** Run the emitter; never hand-edit the JSON. An
edit is a change the next run discards without saying so.

The estate-wide house rules are in `CLAUDE.md`.
