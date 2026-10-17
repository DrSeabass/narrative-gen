# ToDo

## 1. Survey: AI and Solo TTRPGs

Goal: map what exists (academic, commercial, community) across the three roles in the
mission statement — **assistant** to a solo GM, **automated player** (playtesting), and
**automated GM** — and find where planning and NLP each have something to contribute.

### 1.1 Set up the review

Decisions (research questions, scope, inclusion criteria, outputs, conventions) are in
[`survey/README.md`](survey/README.md).

- [ ] Set up tooling
  - [ ] Markdown table for coding sources in `survey/coding.md` (see 1.6)
- [ ] Find seed papers for the fields in 1.2 marked **needs seeds**
- [ ] Snowball one step backwards/forwards from the seeds (see [`survey/search_notes.md`](survey/search_notes.md))
- [ ] Obtain sources with no PDF (notes get `status: to-obtain`)
  - [ ] `porteous2010applying`: download in a browser from https://research.tees.ac.uk/files/5954785/118625.pdf (blocks curl)
  - [ ] `cheong2008narrative`, `cheong2015suspenser`: paywalled; library access
- [ ] Confirm or drop the leads in `solo_ttrpg_believed.bib`
- [ ] Record the 2026-10-17 seed verification in the query log in `survey/search_notes.md`
- [ ] Pre-survey: draft notes and build `survey/reading_list.md` following [`survey/triage_notes.md`](survey/triage_notes.md). Can run now on the verified seeds; rerun after snowballing.

### 1.2 Academic fields to cover

Seeds are verified entries in [`solo_ttrpg_recovered.bib`](solo_ttrpg_recovered.bib) with the
field's tag in `keywords`. Sources appear under their main field; see the bib for all tags.

- [ ] **Narrative planning** (`narrative-planning`) — plan-based story generation, character intentionality, conflict
  - Seeds: [[riedl2010narrative]], [[ware2011cpocl]], [[ware2014glaive]], [[ware2021sabre]], [[porteous2010applying]], [[young2013plans]]
- [ ] **Story generation, pre-LLM** (`story-generation`) — TALE-SPIN, MINSTREL, MEXICA, Universe
  - Seeds: [[gervas2009computational]], [[kybartas2017survey]]. The historical systems themselves are not yet in the bib.
- [ ] **Interactive narrative and drama/experience management** (`interactive-narrative`) — Façade, the Oz project, experience managers
  - Seeds: [[riedl2013interactive]]; also [[porteous2010applying]]
- [ ] **Emergent narrative and story sifting** (`emergent-narrative`) — simulation-driven stories, finding stories after the fact
  - Seeds: [[kreminski2019felt]], [[kreminski2020why]], [[kreminski2021winnow]], [[ryan2015toward]], [[ryan2015open]], [[ryan2016characters]]
- [ ] **LLMs for TTRPGs and interactive fiction** (`llm-ttrpg`)
  - Seeds: [[rameshkumar2020storytelling]], [[callisonburch2022dungeons]], [[zhu2023fireball]], [[zhu2023calypso]], [[martin2018dungeons]], [[hausknecht2020interactive]], [[cote2018textworld]]
- [ ] **Automated playtesting and simulation-based game design** (`automated-playtesting`) — procedural personas, agents as playtesters, balance analysis
  - **Needs seeds.** Text-game agents ([[martin2018dungeons]], [[hausknecht2020interactive]], [[cote2018textworld]]) are tagged here but aren't playtesting work.
- [ ] **Player modelling and player experience** (`player-modelling`)
  - Seeds: [[yannakakis2018artificial]]
- [ ] **Mixed-initiative and co-creative systems** (`mixed-initiative`) — creativity support tools, AI as a co-author
  - Seeds: [[kreminski2019generative]], [[kreminski2022loose]]; also [[kreminski2020why]], [[zhu2023calypso]]
- [ ] **Cognitive and affective models of narrative** (`narrative-cognition`) — suspense, surprise, and comprehension
  - Seeds: [[cheong2006computational]], [[cheong2008narrative]], [[cheong2015suspenser]], [[cardonarivera2012indexter]]
- [ ] **Procedural content generation** (`pcg`) — quest, dungeon, and adventure generation
  - **Needs seeds.** [[yannakakis2018artificial]] covers PCG and may help find them.
- [ ] **Narratology** — Propp, Ryan, Bal; what a "story" is, to ground the modelling
  - **Needs seeds**, and no field tag yet.
- [ ] ~~**Theories of fun and game design**~~ — deferred (see [`survey/README.md`](survey/README.md)). Koster, *A Theory of Fun*, already read; MDA framework (Hunicke, LeBlanc & Zubek) if revisited.

### 1.3 Non-academic writing

- [ ] **GM craft** — Laws, *Robin's Laws of Good Game Mastering* and *Hamlet's Hit Points* (beat analysis, which fits planning well); Justin Alexander / The Alexandrian (node-based scenario design, the Three Clue Rule); Sly Flourish (*Return of the Lazy Dungeon Master*); The Angry GM
- [ ] **RPG theory** — the Forge (GNS, Ron Edwards), Story Games forum archives, the Nordic larp tradition
- [ ] **Solo play community** — r/Solo_Roleplaying, solo-play blogs and YouTube actual plays, community guides to oracle use
- [ ] **Narrative design writing** — Emily Short's blog, GDC narrative summit talks
- [ ] **Community attitudes to generative AI** — publisher policies (e.g. DriveThruRPG AI labelling, the Wizards of the Coast art controversies), creator backlash. This affects how the work will be received and should shape how it is positioned.

### 1.4 Commercial landscape

Build a catalogue, one entry per product: what it does, which role it plays, technique (tables, rules, or LLM), and price/licence.

- [ ] **Solo rules and GM emulators** — Mythic GME, *Ironsworn* / *Starforged*, Juice Oracle, Four Against Darkness, *Scarlet Heroes*, the Solo Investigator's Handbook, *Alone Against the Flames*
- [ ] **Journaling RPGs** — *Thousand Year Old Vampire* and similar (prompt-driven narrative structure)
- [ ] **Gamebooks** — Fighting Fantasy / Lone Wolf (pre-authored branching narrative as a baseline)
- [ ] **AI storytelling and GM products** — AI Dungeon, NovelAI, Hidden Door, Friends & Fables, and other "AI GM" apps; check which still exist
- [ ] **Digital tools for solo and GM play** — Foundry VTT and its solo modules, Obsidian plugins (e.g. Iron Vault), World Anvil, Kanka, donjon generators
- [ ] **Video games with storytellers** — RimWorld's AI storytellers, Dwarf Fortress, *Wildermyth* (closest commercial analogues to an automated GM)

### 1.5 Where to search

See [`survey/search_notes.md`](survey/search_notes.md).

### 1.6 Coding scheme (apply to every source)

Record codes as a markdown table in `survey/coding.md`: one row per source, one column per dimension, citekey in the first column linking to its note.

- [ ] Draft the dimensions and test them on ~10 sources before coding everything:
  - **Role**: assistant / player / GM / designer tool / analysis
  - **Technique**: tables, symbolic, planning, search, learning, LLM, hybrid
  - **Narrative model**: what counts as story state, and how it is represented
  - **Human involvement**: autonomous / mixed-initiative / human-led
  - **Evaluation**: none, computational metrics, user study, expert review; what "good" meant
  - **Planning hook / NLP hook**: where each field could contribute

