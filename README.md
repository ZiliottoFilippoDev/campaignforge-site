# Character Forge

Character Forge is a Flutter app that helps users design D&D characters and NPCs by guiding them through a structured creation process and generating a polished, AI-ready prompt.

It is **not a chatbot** — it is a **guided prompt forge** that transforms fragmented ideas into a complete, well-structured character description ready to paste into ChatGPT or similar AI tools.

---

## ✨ What It Does

- Guides users through character creation step by step
- Supports both **Player Characters (PC)** and **NPC profiles**
- Organizes inputs into structured sections (concept, role, personality, backstory, voice, extras)
- Generates a **complete prompt locally on-device**
- Presents the result in a **premium parchment-style UI**
- Enables copy, share, and direct handoff to AI tools
- Supports drafts, presets, and local saving
- Includes monetization via ads, rewarded unlocks, and one-time premium purchase

---

## 🎯 Why It Exists

Creating high-quality AI-generated characters requires structured input:
- Race, class, and role
- Personality traits and motivations
- Backstory hooks and relationships
- Voice and roleplaying style

Most users either:
- Provide too little detail → generic output  
- Provide unstructured text → inconsistent results  

Character Forge solves this by turning the process into a **guided, opinionated workflow** that ensures completeness and clarity.

---

## 🧭 Core Experience

1. **Choose Entry Options**
   - Character Mode: PC or NPC
   - Output Format: Full Sheet, Backstory, Summary, or Stat Block
   - Optional Presets for quick start

2. **Build the Character**
   - Navigate freely using a hub-and-spoke interface
   - Fill in structured sections:
     - Concept
     - Role
     - Personality
     - Backstory
     - Voice & Style
     - Extras (PC only)

3. **Live Preview**
   - See the generated prompt update in real time

4. **Forge Output**
   - Generate the final prompt
   - Rendered in a parchment-style screen

5. **Export**
   - Copy to clipboard
   - Share
   - Open directly in AI tools
   - Save drafts locally

---

## 🧱 Key Concepts

- **Hub-and-Spoke UI**: Sections can be accessed in any order
- **Guided Mode**: Optional linear step-by-step flow
- **Live Prompt Builder**: Prompt is generated continuously during input
- **Local-First**: No backend required for core functionality
- **Section-Based Architecture**: Each part of the character maps to a structured prompt block
- **Mode-Driven UI**: PC vs NPC determines available sections and depth
- **Output Formats**:
  - Full Sheet
  - Backstory Only
  - Quick Summary
  - Stat Block (PC only)

---

## 🧠 Architecture Overview

- **models/**: Immutable data structures for character sections and options
- **services/**: Asset loading and prompt generation logic
- **ui/**:
  - entry/ → initial selection screen
  - forge/ → character builder
  - parchment/ → final output presentation
  - shared/ → reusable UI components
- **theme/**: Visual identity and styling
- **monetization/**: Ads, rewards, and purchase handling
- **onboarding/**: Launch walkthrough overlay
- **audio/**: UI feedback sounds

---

## ⚙️ Prompt Generation

- Prompt is generated programmatically using a builder pattern
- Inputs are combined into a structured markdown output
- Templates serve as reference specifications, not runtime dependencies
- Output is optimized for direct use in AI tools

---

## 💾 Data & Storage

- Character options, presets, and traits are stored locally in assets (YAML)
- Drafts are saved locally using SQLite (via Drift)
- No backend dependency for core workflow
- Preferences stored using shared preferences

---

## 🎭 Presets

Predefined archetypes that pre-fill most of the character fields:
- Classic Hero
- Mysterious Stranger
- Comic Relief
- Tragic Villain

Some presets can be premium-gated.

---

## 💡 Relationship to Campaign Forge

Character Forge complements Campaign Forge:

- Campaign Forge builds the **world and story**
- Character Forge builds the **characters within it**

It supports importing campaign context via deep links to help align character creation with an existing setting.

---

## 🚀 Key Features

- Guided character creation workflow
- Structured prompt generation
- Live preview of output
- Hub-and-spoke navigation
- Guided mode alternative
- NPC and PC modes
- Multiple output formats
- Presets and drafts
- Local-first storage
- Export via copy, share, or handoff
- Monetization (ads, rewards, premium)
- Onboarding walkthrough
- Theme-aware fantasy UI

---

## 📦 Status

This project is actively structured as a modular Flutter application with clear separation of concerns and scalable architecture for future expansion.

---

## 🧾 Summary

Character Forge turns character creation into a guided, structured, and repeatable process that produces high-quality AI-ready prompts — helping users go from vague ideas to fully realized characters in minutes.
