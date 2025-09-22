# AI StoryForge — Prototype

**Author:** Ossimi Ziv  
**GitHub:** wifies  
**Deployed Version:** https://ai-story-forge.netlify.app/  
**Team PRD:** [PRD DOC LINK](https://docs.google.com/document/d/1Tu_tpIomwoIAXnEmw5HWW7LTYrBZ8-jsJhDoQ2uhOeQ/edit?usp=sharing)  

---

## Overview

**AI StoryForge** is a lightweight, **no-backend** prototype that helps creators outline and draft story episodes (Mysteries, YouTube series, multi-POV narratives) while maintaining continuity. It runs entirely in the browser and stores data in `localStorage`. This repo demonstrates a possible user journey: premise → outline → puzzles → scene drafts → release packet.

**YES Included:** a quick, streamlined prototype for concept demonstration.  
**NOT Included (yet):** a full AI system—logic that can train on inputted documents

---

## USAGE:

* **Netlify (recommended):** https://ai-story-forge.netlify.app/    
* **Static file:** open `index.html` directly in a browser  

---

## Getting Started

### Run Locally

1. Clone the repo
2. Open `index.html` in your browser
   *(or serve the folder)*:

   ```bash
   npx serve .
   # then open the printed localhost URL
   ```


Or simply use the link, the whole project runs locally through web browser. Open it and begin generating!

---

## Core Features

### 0) Project Setup & Canon

* Enter **Series Title**, **Characters** (comma-separated), **World Rules** (one per line)  
* Auto **Canon Snapshot** (characters, rules) + basic KPIs (character/rule/scene counts)  
* Data stored locally via `localStorage` (no server)  

### 1) Premise & Tone  

* Write a one-sentence **logline**  
* Generate **logline variants** by style: *safe / wild / experimental* (heuristic)  

### 2) Outline & Beat Design

* One-click **8-Beat outline** generator (Hook → Aftermath)
* Add/edit/delete custom beats
* **Puzzle suggestions** (3 ideas) based on your canon
* **Fair-Play Meter** (low/medium/high) based on clue-like keywords in scenes

### 3) Scene Drafting & Continuity Watcher

* Add scenes with **Title**, **POV**, and **Draft** text
* **Continuity checks**:

  * Flags **unknown names** not in your character list
  * Naive **rule breaches** (e.g., rules starting with “No …” / “Never …”)

### 4) Simple Release Packet

* **Hook Workshop** (write your opening 10s, get a **Promise Check** on hype/spoiler risk)
* Live **Markdown preview** of Project → Outline → Puzzles → Scenes
* **Export**: `Export JSON` (full state) and `Export Markdown` (release packet)

---

## Usage Flow (Suggested)

1. **Project**: Add characters/rules and optional prior notes.
2. **Premise**: Draft your logline; generate a couple of variants.
3. **Outline**: Auto-generate 8 beats; tweak or add custom beats.
4. **Puzzles**: Click “Suggest Puzzle Mechanics” and check the Fair-Play Meter.
5. **Scenes**: Draft scenes, set POVs, and run **Continuity Checks**.
6. **Report**: Write a hook, review **Promise Check**, export Markdown/JSON.

---

## Data & Privacy

* All data is stored **locally** in your browser’s `localStorage` under the key `storyforge_v1`.
* **No network calls.** Nothing is uploaded.
* **Reset** clears local data (toolbar → **Reset**).

---

## Known Limitations

* “AI” behaviors are **heuristics only** (no model calls).
* Continuity/rule checking is **best-effort** (string-based).
* No multi-user collaboration, auth, or cloud persistence.
* Single-project state (you can export/import JSON manually).

---

## Roadmap Ideas

* Import JSON (UI) and **read-only share links**
* Real AI options: tone control, beat alternatives, line editing
* Stronger continuity engine (entity/timeline graphs)
* Puzzle fairness checker with explicit breadcrumb tracing
* Collaboration (comments, presence) + cloud save
* Theming and accessibility pass (WCAG color/contrast)

---

## License

This project is for educational purposes as part of CS1060 coursework.

---
