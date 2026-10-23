# Rock's CoC Unified

**A unified collection of content and tools for Call of Cthulhu 7th Edition on Foundry Virtual Tabletop.**

Rock CoC Unified brings together multiple independently developed modules into one organized project, providing Keepers with equipment, reference books, occupations, additional skills, and investigator creation resources.

The project is designed for **Foundry VTT v14** and the **Call of Cthulhu 7th Edition (CoC7) system v8.16 or later**.

> **Current Release: v0.1.0**
>
> This release acts as a dependency-based launcher for the Rock CoC collection. It does not yet bundle all four modules into a single ZIP.

---

## Features

### Equipment Library

A collection of equipment and tools for Call of Cthulhu investigations, including general-purpose items, weapons, armor, and light sources.

The Equipment module also includes experimental interactive features such as light resource tracking, medical item usage, and temporary effects.

**Note:** Some equipment automation, particularly medical treatment and roll detection, remains experimental. Keepers should verify results and inventory changes before applying them during play.

### Books Library

Reference books and reading materials intended to enrich investigations, character backgrounds, and period-appropriate gameplay.

### Occupations & Additional Skills

Classic and Modern occupation collections, along with additional skills for character creation and campaign customization.

### Investigator Setups

Resources to help Keepers organize investigator creation and provide starting character equipment or setup options.

---

## Included Modules

| Module | Version | Module ID |
|---|---|---|
| CoC7 Universal Books Library | 0.2.0 | `coc7-universal-books` |
| CoC7 Universal Equipment | 1.7.7 | `coc7-universal-equipment` |
| CoC7 Universal Investigator Setups | 0.1.0 | `coc7-investigator-setups` |
| CoC7 Universal Occupations + Additional Skills | 0.7.0 | `coc7-universal-occupations` |

Each module is maintained independently and connected to this repository through Git submodules.

---

## Requirements

- Foundry Virtual Tabletop v14
- Call of Cthulhu 7th Edition system v8.16 or later
- The four standalone Rock CoC modules listed above

## Installation

### Method 1 — Foundry VTT Manifest URL

1. Open Foundry VTT Setup.
2. Navigate to **Add-on Modules**.
3. Select **Install Module**.
4. Paste the following URL into the Manifest URL field:

   ```
   https://github.com/Rockuse/rock-coc-unified/releases/latest/download/module.json
   ```

5. Click **Install**.
6. Ensure the four required standalone modules are also installed.
7. Launch your Call of Cthulhu 7th Edition world.
8. Open **Game Settings → Manage Modules**.
9. Enable **Rock CoC Unified** and its required modules.
10. Save the module settings and reload the world.

**Important:** The current Unified release does not contain the standalone modules' files. Foundry may prompt you to install missing dependencies. Automatic dependency installation requires those modules to have accessible distribution manifests.

### Method 2 — Manual Installation

1. Visit the [Rock CoC Unified Releases](https://github.com/Rockuse/rock-coc-unified/releases).
2. Download `rock-coc-unified.zip`.
3. Extract it into your Foundry User Data directory under:

   ```
   FoundryVTT/
   └── Data/
       └── modules/
           └── rock-coc-unified/
               └── module.json
   ```

4. Install the four standalone modules into the same `Data/modules/` directory, each in its own folder.
5. Restart Foundry VTT.
6. Enable the required modules in your CoC7 world.

## Repository Structure

```text
rock-coc-unified/
├── .github/
│   └── workflows/
│       └── release.yml
├── modules/
│   ├── books/
│   ├── equipment/
│   ├── investigator/
│   └── occupations/
├── .gitmodules
├── module.json
└── README.md
```

The `modules/` directories are Git submodules. Each points to an independent repository with its own source code, commits, and release history.

---

## Compendium Organization

The collection is intended to support a structured compendium library such as:

```text
Rock CoC
├── Character Creation
├── Item
│   ├── Armor
│   ├── Books
│   ├── Weapon
│   └── Item Universal
├── Occupations
│   ├── Classic Occupations
│   └── Modern Occupations
└── Skills
    └── Additional Skills
```

Individual modules create or reuse world-level compendiums. The exact folder arrangement may depend on your world's existing configuration.

## Updating

To update Rock CoC Unified through Foundry, use Foundry's module update functionality once a newer release is available.

Standalone modules are versioned independently and may require separate updates.

Developers updating Git submodules should commit the updated submodule references to the Unified repository.

---

## Known Limitations

- **Dependency-based distribution:** v0.1.0 is not a self-contained installer for all four modules.
- **Experimental equipment automation:** Medical roll detection and related effects may require manual Keeper verification.
- **World-level compendiums:** The standalone modules create or reuse compendiums within the active Foundry world.
- **Duplicate content:** Installing or importing the same content multiple times may result in duplicates, depending on the individual module's installation logic.
- **Module compatibility:** The project targets Foundry v14 and CoC7 v8.16 or later; other versions have not been verified.

## License and Credits

Developed by **Rockuse** for use with Call of Cthulhu 7th Edition on Foundry Virtual Tabletop.

The licensing terms for this collection and its individual modules should be documented in their respective repositories.

This is an independent fan-made project and is not officially affiliated with or endorsed by Chaosium or Foundry Gaming LLC.

---

**Repository:** https://github.com/Rockuse/rock-coc-unified

**Releases:** https://github.com/Rockuse/rock-coc-unified/releases

**Issues:** https://github.com/Rockuse/rock-coc-unified/issues