# GeneBoyleSkills

Custom Claude AI skills for Gene Boyle — Orange County Probate Real Estate Specialist.

## Avatar System

This isn't a collection of random tools. It's an **avatar system** — a persona layer + skill library that lets Claude operate as Gene's intelligent business partner. The `avatar/` skill loads first and establishes Gene's identity, voice, and operating principles. Every other skill builds on that foundation.

## Skills

| Skill | Domain | Description |
|-------|--------|-------------|
| **avatar** | 🧠 Persona | Gene's identity, voice, brand, competitive positioning — load first |
| **probate-transaction** | 🏠 Core Business | End-to-end probate sale workflow: intake → court → close |
| **client-communication** | 💬 Communication | Emails, texts, updates for families, attorneys, and partners |
| **probate-lead-gen** | 📈 Growth | Attorney outreach, referral nurturing, pipeline building |
| **probate-listing-presentation** | 📊 Sales | CMAs, listing pitches, property valuations for probate estates |
| **social-media-voice** | 📱 Marketing | Platform-specific content: Threads, Instagram, Facebook, LinkedIn |
| **oc-market-intel** | 🗺️ Intelligence | Always-current OC market data, comps, neighborhood analysis |
| **competitive-intel** | 🔍 Strategy | Track competitors, differentiation strategy |
| **demark-crypto-timing** | 📉 Investment | DeMark indicator analysis for BTC/ETH entry timing |

## Usage

Claude fetches skills from this repo via:

```
raw.githubusercontent.com/geneboyle/GeneBoyleSkills/main/{skill-name}/SKILL.md
```

## Structure

```
GeneBoyleSkills/
├── README.md
├── AVATAR-PLAYBOOK.md              # Strategic playbook (architecture & build plan)
├── avatar/
│   └── SKILL.md                    # PERSONA LAYER — always load first
├── probate-transaction/
│   └── SKILL.md                    # Court procedures, timelines, checklists
├── client-communication/
│   └── SKILL.md                    # Emails, texts, updates
├── probate-lead-gen/
│   └── SKILL.md                    # Attorney outreach, referral nurturing
├── probate-listing-presentation/
│   └── SKILL.md                    # CMAs, listing pitches, valuations
├── social-media-voice/
│   └── SKILL.md                    # Multi-platform content generation
├── oc-market-intel/
│   └── SKILL.md                    # OC market data & analysis
├── competitive-intel/
│   └── SKILL.md                    # Competitor tracking & differentiation
└── demark-crypto-timing/
    ├── SKILL.md                    # DeMark indicators for crypto timing
    └── references/
        └── demark-indicators.md    # TD Sequential/Combo technical reference
```

## The Kelly Advantage

Kelly builds and maintains this system. Gene benefits from it. Claude executes it.
Gene doesn't need to understand skills, GitHub, or prompting — he just talks to Claude
and gets a business partner that knows his pipeline, writes in his voice, and stays current.
