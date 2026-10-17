# Survey Protocol

How the literature survey on AI for solo TTRPGs is run. This file is the source of truth
for the review's scope and conventions; open tasks live in [`../ToDo.md`](../ToDo.md) §1.

## Goal

Map what exists on AI for solo tabletop role-playing games (TTRPGs), academic, commercial,
and community, across three roles:

- **Assistant**: tools that help a solo player act as their own game master (GM)
- **Automated player**: agents that play games, e.g. to playtest new systems
- **Automated GM**: systems that run or generate adventures

Then find where planning and NLP each have something to contribute.

## Focus

The academic focus is computer science, especially automated planning and NLP.
"Fun" is out of scope for now because it is hard to measure; revisit later.
Narratology and classic story-craft writing (Vonnegut, the monomyth, *Save the Cat*, etc.)
are also deferred; targets are listed in `ToDo.md` §1.2.

## Research questions

- **RQ1**: How have story and narrative been modelled computationally, and which models suit planning?
- **RQ2**: What AI support exists today for solo play, GMing, and playtesting (research and products)?
- **RQ3**: How have "believable narrative", "good story", "good characterization", and "good adventure" been evaluated?
- **RQ4**: Where are the gaps that planning, NLP, or both together could fill?

## Review style

A scoping (narrative) review, not a systematic one: start from seed papers per field and
snowball backwards (references) and forwards (citing papers). Search procedure is in
[`search_notes.md`](search_notes.md).

## Inclusion criteria

- English only.
- Published 2000 or later, **or** historically important regardless of date (heavily cited, or foundational to a surveyed field). Mark these `historical: true` in the note.
- General story and narrative generation is in scope. Work on TTRPGs, RPGs, and interactive fiction is preferred.
- Out of scope for now: theories of fun and work that is mainly about measuring fun; narratology and story-craft treatises.

## Outputs

- Internal notes: one linked markdown note per source.
- A survey paper.

## Tooling and conventions

The repository is used as an Obsidian vault: notes are plain markdown linked with `[[citekey]]`.

| What | Where | Convention |
|---|---|---|
| Bibliography: recovered | [`../solo_ttrpg_recovered.bib`](../solo_ttrpg_recovered.bib) | Metadata confirmed from an authoritative web source (PDF not required). Cite only from here. Citekey `firstauthorYEARfirstword`; `keywords` = field tags. |
| Bibliography: believed | [`../solo_ttrpg_believed.bib`](../solo_ttrpg_believed.bib) | Sources we think exist but haven't confirmed. Move to recovered once confirmed. |
| Source notes | `notes/<citekey>.md` | Copy [`notes/_template.md`](notes/_template.md). File name = citekey. |
| Coding table | [`coding.md`](coding.md) | One row per source, one column per coding dimension (ToDo §1.6). |
| Downloaded papers | `inputs/<citekey>_<title-slug>.pdf` | Title slug: lowercase, hyphenated, about 8 words. Git-ignored. Never commit PDFs. |
| Search brief | [`search_notes.md`](search_notes.md) | Where to look, queries, field tags, rules, query log. |
| Triage brief | [`triage_notes.md`](triage_notes.md) | Pre-populating notes and prioritising; produces [`reading_list.md`](reading_list.md). |
