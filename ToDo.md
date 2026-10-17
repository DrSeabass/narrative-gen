# ToDo

## 1. Survey: AI and Solo TTRPGs

Goal: map what exists (academic, commercial, community) across the three roles in the
mission statement — **assistant** to a solo GM, **automated player** (playtesting), and
**automated GM** — and find where planning and NLP each have something to contribute.

### 1.1 Set up the review

- [x] Decide the review's research questions
  - Academic focus is computer science. "Fun" is out of scope for now because it is hard to measure; revisit later.
  - RQ1: How have story and narrative been modelled computationally, and which models suit planning?
  - RQ2: What AI support exists today for solo play, GMing, and playtesting (research and products)?
  - RQ3: How have "believable narrative", "good story", "good characterization", and "good adventure" been evaluated?
  - RQ4: Where are the gaps that planning, NLP, or both together could fill?
- [x] Decide on the review style: scoping/narrative (seed papers + snowballing).
- [ ] Set up tooling
  - [x] `.bib` in repo (`solo_ttrpg.bib`): citekey `firstauthorYEARfirstword`; per-field collections via the `keywords` field, using the same tags as notes' `fields:`. Contains a mock `doe2025example` entry as a template example.
  - [x] One notes file per source in `survey/notes/` using a common template (`survey/notes/_template.md`; file name = citekey)
  - [ ] Markdown table for coding sources in `survey/coding.md` (see 1.6)
- [x] Define inclusion/exclusion criteria (2000+ and historically relevant papers, English only. Story & Narrative gen alone in scope, TTRPG + RPG + Interactive Fiction Preferred)
- [x] List search venues and databases (see 1.5)
- [ ] Pick seed papers per field (see 1.2) and snowball backwards/forwards
- [x] Decide on the output: internal notes + a survey paper. Assume obsidian vaults (use linked markdown in this repository)

### 1.2 Academic fields to cover

Seed sources marked *(verify)* came from memory; check citations before relying on them.

- [ ] **Narrative planning** — plan-based story generation, character intentionality, conflict
  - Riedl & Young, "Narrative Planning: Balancing Plot and Character", JAIR 2010 *(verify)*
  - Ware & Young, CPOCL / Glaive / Sabre line of work *(verify)*
  - Porteous, Cavazza & Charles, planning for interactive storytelling *(verify)*
  - Young et al., review of plan-based narrative generation *(verify)*
- [ ] **Computational narrative / story generation (pre-LLM)** — TALE-SPIN, MINSTREL, MEXICA, Universe
  - Gervás, story generation survey *(verify)*; Kybartas & Bidarra, survey of story generation techniques, IEEE TCIAIG *(verify)*
- [ ] **Interactive narrative and drama/experience management** — Façade, the Oz project, experience managers
  - Riedl & Bulitko, "Interactive Narrative: An Intelligent Systems Approach", AI Magazine *(verify)*
- [ ] **Emergent narrative and story sifting** — simulation-driven stories, finding stories after the fact
  - Kreminski & Wardrip-Fruin and collaborators (story sifting, mixed-initiative play with solo journaling games) *(verify)*
  - Ryan, Mateas & Wardrip-Fruin, *Talk of the Town* *(verify)*
- [ ] **LLMs for TTRPGs and interactive fiction**
  - Rameshkumar & Bailey, CRD3 (Critical Role dataset) *(verify)*
  - Callison-Burch et al., D&D as a dialogue challenge *(verify)*; Zhu et al., FIREBALL dataset and CALYPSO *(verify)*
  - Martin, Sood & Riedl, "Dungeons and DQNs" *(verify)*
  - Text-adventure agents (Jericho, TextWorld) as a model for automated players
- [ ] **Automated playtesting and simulation-based game design** — procedural personas, agents as playtesters, balance analysis
- [ ] **Player modelling and player experience** — Yannakakis & Togelius, *Artificial Intelligence and Games* *(verify)*
- [ ] **Mixed-initiative and co-creative systems** — creativity support tools, AI as a co-author
- [ ] **Cognitive and affective models of narrative** — suspense, surprise, and comprehension models (e.g. Cheong & Young; Cardona-Rivera) *(verify)*
- [ ] **Procedural content generation** — quest, dungeon, and adventure generation
- [ ] **Game studies on TTRPGs** — Fine, *Shared Fantasy* (1983); *Analog Game Studies*; *International Journal of Role-Playing*; Knutepunkt books
- [ ] **Narratology** — Propp, Ryan, Bal; what a "story" is, to ground the modelling
- [ ] ~~**Theories of fun and game design**~~ — deferred (see 1.1). Koster, *A Theory of Fun*, already read; MDA framework (Hunicke, LeBlanc & Zubek) if revisited.

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

- [x] Databases, venues, commercial sources, queries, and output rules are in [`survey/search_notes.md`](survey/search_notes.md). Hand that file to an agent as input for searches.

### 1.6 Coding scheme (apply to every source)

Record codes as a markdown table in `survey/coding.md`: one row per source, one column per dimension, citekey in the first column linking to its note.

- [ ] Draft the dimensions and test them on ~10 sources before coding everything:
  - **Role**: assistant / player / GM / designer tool / analysis
  - **Technique**: tables, symbolic, planning, search, learning, LLM, hybrid
  - **Narrative model**: what counts as story state, and how it is represented
  - **Human involvement**: autonomous / mixed-initiative / human-led
  - **Evaluation**: none, computational metrics, user study, expert review; what "good" meant
  - **Planning hook / NLP hook**: where each field could contribute

### 1.7 Open questions to discuss

- [x] How wide should the review go? Answered by the inclusion criteria in 1.1.
- [ ] Should LLM work be its own strand, or a technique spread across the others?
- [ ] Who does the review: solo, or a student project (fits the "attract students" goal)?
- [ ] How do we measure "fun" well enough to compare systems? (Deferred; outside the current CS focus.)
