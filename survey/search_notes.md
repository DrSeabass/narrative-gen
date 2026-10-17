# Search Notes

Brief for anyone (human or agent) searching for sources for the survey.

**Read [`README.md`](README.md) (the survey protocol) first.** It defines the goal,
research questions, focus, and inclusion criteria that this brief assumes.
Then read this whole file before searching.

## Where to look

### Academic databases

- Google Scholar
- Semantic Scholar (good for following citations forwards and backwards)
- ACM Digital Library
- IEEE Xplore
- ACL Anthology
- AAAI digital library

### Venues

| Venue | Why |
|---|---|
| ICAPS | Planning, including narrative planning |
| RPG workshop (Role of Planning in Games) | Planning applied to games |
| AIIDE | AI in games, interactive narrative |
| ICIDS | Interactive digital storytelling |
| FDG | Foundations of digital games |
| CoG | Computational intelligence in games |
| IEEE Transactions on Games (formerly TCIAIG) | Journal for games AI |
| ACL / EMNLP / NAACL | NLP, incl. Wordplay and storytelling workshops |
| INT workshop | Intelligent narrative technologies |
| DiGRA | Game studies (use sparingly; focus is CS) |

### Commercial and community

- DriveThruRPG (solo category)
- itch.io (solo tag)
- App stores (search "AI game master", "solo RPG", "AI dungeon master")
- Kickstarter / BackerKit
- r/Solo_Roleplaying, solo-play blogs, GM craft blogs (see `ToDo.md` §1.3)

## What to look for

Use these as starting queries. Combine with "tabletop", "role-playing", "TTRPG", "solo", or "interactive fiction" where results are too broad.

| Field tag | Topic | Example queries |
|---|---|---|
| `narrative-planning` | Plan-based story generation | "narrative planning", "plan-based story generation", "intentional planning" characters, "conflict" narrative planner |
| `story-generation` | Story generation before LLMs | "story generation" survey, "computational narrative", TALE-SPIN, MINSTREL, MEXICA |
| `interactive-narrative` | Drama and experience management | "drama manager", "experience management", "interactive narrative" |
| `emergent-narrative` | Simulation-driven stories, story sifting | "emergent narrative", "story sifting", "social simulation" narrative |
| `llm-ttrpg` | LLMs for TTRPGs and interactive fiction | "Dungeons and Dragons" language model, "game master" LLM, "text adventure" agent |
| `automated-playtesting` | Agents as playtesters | "automated playtesting", "procedural personas", "simulation-based game design" |
| `player-modelling` | Player modelling and experience | "player modeling", "player experience" |
| `mixed-initiative` | Co-creative systems | "mixed-initiative" creativity, "co-creative" storytelling |
| `narrative-cognition` | Suspense, surprise, comprehension | "suspense" narrative generation, "narrative comprehension" model |
| `pcg` | Procedural content generation | "quest generation", "procedural content generation" adventure |
| `game-studies` | Game studies on TTRPGs (use sparingly; focus is CS) | "tabletop role-playing" ethnography, "role-playing games" social |

The field tags are the values used in note frontmatter (`fields:`) and in `.bib` `keywords`.

### Seed papers

Verified seeds are the entries in `solo_ttrpg_recovered.bib`; `ToDo.md` §1.2 lists them by field and flags fields that still **need seeds**. Snowball one step backwards (a seed's references) and one step forwards (papers citing it) and apply the inclusion criteria. New finds go in `solo_ttrpg_believed.bib` until their metadata is confirmed.

## What to produce for each source

1. **Bib entry**: in `solo_ttrpg_recovered.bib` if you confirmed the metadata from an authoritative source; otherwise in `solo_ttrpg_believed.bib` with a `note` saying where the lead came from
   - Citekey: `firstauthorYEARfirstword`, lowercase (skip "a", "an", "the").
   - `keywords` = field tags from the table above.
   - Include a DOI or URL.
2. **Note** at `survey/notes/<citekey>.md`, copied from `survey/notes/_template.md`.
   - Fill the frontmatter. Set `status: to-read` unless the full text was actually read.
   - Write the Summary from the abstract at minimum. Leave other sections blank rather than guessing.
3. **PDF** (if freely and legally available) in `survey/inputs/<citekey>_<title-slug>.pdf` (title slug: lowercase, hyphenated, about 8 words; e.g. `riedl2010narrative_narrative-planning-balancing-plot-and-character.pdf`). This folder is git-ignored; never commit PDFs.
4. **Log the search** in the query log below.

## Rules

- Never invent or "fill in" a citation. If you cannot confirm a detail from the source itself or a publisher/indexing page, leave it out and flag it.
- Prefer the published version over a preprint. Note the preprint URL if that is all there is.
- Check both `.bib` files and `survey/notes/` for duplicates before adding. If a believed entry gets confirmed, move it to the recovered file.
- For commercial products, record whether the product still exists and the date you checked.
- If a source doesn't fit any field tag, add it anyway and flag it. It may mean the taxonomy needs a new field.

## Query log

| Date | Database / site | Query | Results scanned | Added |
|---|---|---|---|---|
|  |  |  |  |  |
