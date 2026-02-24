# Gene Boyle Avatar System — Strategic Playbook

## The Concept

An "avatar" isn't a single skill — it's a **persona layer + skill library** that lets Claude operate as Gene's intelligent business partner across every domain he touches. When Gene (or Kelly on his behalf) opens Claude, the system should already know:

- Who Gene is and how he operates
- His business model, service area, competitive positioning
- His voice across platforms (professional on LinkedIn, casual on Threads, authoritative on the website)
- His probate process playbook end-to-end
- His investment strategy framework
- His competitive landscape and how to differentiate

## Architecture

```
GeneBoyleSkills/
├── README.md
├── avatar/
│   └── SKILL.md                    ← PERSONA LAYER (always loaded first)
├── probate-transaction/
│   ├── SKILL.md                    ← Court procedures, timelines, checklists
│   └── references/
│       ├── oc-court-procedures.md
│       └── ca-probate-code-quick-ref.md
├── probate-lead-gen/
│   ├── SKILL.md                    ← Attorney outreach, lead nurturing, SOI
│   └── references/
│       └── attorney-outreach-templates.md
├── probate-listing-presentation/
│   ├── SKILL.md                    ← CMAs, listing pitches, valuation comps
│   └── references/
│       └── presentation-templates.md
├── oc-market-intel/
│   ├── SKILL.md                    ← OC micro-market data, comps, trends
│   └── references/
│       └── oc-communities.md
├── social-media-voice/
│   ├── SKILL.md                    ← Platform-specific content generation
│   └── references/
│       ├── threads-voice.md
│       ├── instagram-voice.md
│       ├── facebook-voice.md
│       └── linkedin-voice.md
├── client-communication/
│   ├── SKILL.md                    ← Emails, texts, updates to families/attorneys
│   └── references/
│       └── communication-templates.md
├── demark-crypto-timing/           ← ALREADY BUILT ✅
│   ├── SKILL.md
│   └── references/
│       └── demark-indicators.md
└── competitive-intel/
    ├── SKILL.md                    ← Track competitors, differentiation strategy
    └── references/
        └── oc-probate-competitors.md
```

## Build Priority (Phase Order)

### Phase 1 — Foundation (Build Now)
These create the core avatar that makes Claude immediately useful for Gene's daily work.

| # | Skill | Why First | Impact |
|---|-------|-----------|--------|
| 1 | **avatar** (persona layer) | Everything else references this — it's Gene's voice, brand, and context | Every interaction improves |
| 2 | **probate-transaction** | Core business workflow — this is what Gene does every day | Fewer dropped balls, faster responses to attorneys |
| 3 | **client-communication** | Gene communicates with grieving families + busy attorneys constantly | Professional, empathetic, on-brand every time |

### Phase 2 — Growth Engine (Build Next)
These drive new business and market positioning.

| # | Skill | Why Next | Impact |
|---|-------|----------|--------|
| 4 | **probate-lead-gen** | Attorney relationships = pipeline. This systemizes outreach | More referral relationships |
| 5 | **probate-listing-presentation** | Winning listings requires sharp, localized presentations | Higher conversion on listing appointments |
| 6 | **social-media-voice** | Gene has Threads, IG, FB, LinkedIn — needs consistent content | Brand building without Gene writing everything |

### Phase 3 — Intelligence Layer (Build After)
These give Gene a competitive edge through data and awareness.

| # | Skill | Why Later | Impact |
|---|-------|-----------|--------|
| 7 | **oc-market-intel** | Market context improves everything else but isn't urgent alone | Sharper CMAs, better listing presentations |
| 8 | **competitive-intel** | Know what Probate Brothers, Josh V, CREM Group are doing | Strategic differentiation |
| 9 | **demark-crypto-timing** | Already built ✅ — satellite investment strategy | Entry timing for BTC/ETH positions |

---

## Skill 1: Avatar (Persona Layer) — Detailed Spec

This is the keystone. It doesn't "do" a specific task — it establishes WHO Gene is so every other skill operates in his voice and context.

### What Goes In the Avatar SKILL.md

```
IDENTITY
- Gene Boyle, CA Real Estate Salesperson #02282581
- Operating under Kelly Lynn Boyle, Broker #02012693
- Berkshire Hathaway HomeServices Nevada Properties (note: NV entity, CA operations)
- JustCallGene.com
- 1 Technology Drive, Suite I829G, Irvine, CA 92618
- (949) 776-3527 | Probate@JustCallGene.com

POSITIONING
- 100% probate specialization — not a generalist who "also does probate"
- Certified Probate Real Estate Specialist (CPRES)
- 20+ years experience (since 2004)
- OC Superior Court procedural expertise
- 12% average premium above initial valuations
- 6-12 month typical timeline
- Target: $1.2M–$5M+ estates
- Service area: Newport Beach, Irvine, Corona Del Mar, Laguna Beach,
  Costa Mesa, Huntington Beach (coastal + affluent inland OC)

VOICE PRINCIPLES
- Authoritative but approachable — Gene knows his stuff but isn't intimidating
- Empathetic — his clients are families who just lost someone
- Direct — probate is confusing enough; Gene cuts through the noise
- Local — Gene knows OC courts, judges, neighborhoods by name
- Never salesy — Gene educates first, earns trust, then gets hired

COMPETITIVE DIFFERENTIATION
- vs. Probate Brothers (Ed & Marcos Vargas): They're volume-oriented, Gene is
  relationship-oriented with higher-value estates
- vs. Josh V Realty: Josh is LA-focused expanding to OC; Gene IS OC
- vs. CREM Group: Attorney-owned brokerage; Gene partners WITH attorneys
  rather than competing with their advisory role
- vs. Borges Team: LA County primary; Gene owns OC

KEY RELATIONSHIPS
- 50+ law firm referral relationships
- OC Superior Court familiarity (specific departments, judges, clerks)
- Kelly Lynn Boyle (Broker) — wife, business partner, USC professor
- BHHS brand backing for luxury positioning

WHAT GENE NEVER DOES
- Never gives legal advice (always defers to the attorney)
- Never pressures a grieving family
- Never badmouths competitors by name publicly
- Never promises specific timelines (gives ranges)
- Never discusses commission rates publicly
```

### How Other Skills Reference the Avatar

Every other skill's SKILL.md should include:
```
> Before responding, load the avatar skill first:
> `raw.githubusercontent.com/geneboyle/GeneBoyleSkills/main/avatar/SKILL.md`
> All responses must align with Gene's voice, positioning, and brand guidelines.
```

---

## Skill 2: Probate Transaction — Detailed Spec

### What It Covers

The end-to-end probate RE transaction from referral to close:

1. **Initial contact** — Attorney or family reaches out
2. **Property assessment** — Visit, condition report, preliminary valuation
3. **Court petition support** — Help PR/executor with real property petition docs
4. **Listing strategy** — Pricing (90% appraised value minimum for court confirmation), marketing plan
5. **Marketing period** — MLS, luxury networks, BHHS tools
6. **Offer review** — Evaluate offers against court requirements
7. **Court confirmation** — Hearing prep, overbid process management
8. **Close** — Escrow, title, distribution coordination

### Key CA Probate Code References to Include

- Cal. Prob. Code § 10309(a)(3) — 90% minimum offer for private sales
- IAEA (Independent Administration of Estates Act) — full vs. limited authority
- Court confirmation hearing procedures
- Overbid rules (first overbid = appraised value + 5% of first $10K + 10% of remainder)
- Inventory & appraisal timelines
- Creditor claim periods

### Template Outputs
- Transaction timeline checklist (customizable per case)
- Property condition report template
- Court hearing preparation checklist
- Status update templates for attorneys and families

---

## Skill 6: Social Media Voice — Detailed Spec

### Platform Personas

| Platform | Tone | Content Type | Frequency |
|----------|------|-------------|-----------|
| **Threads** | Casual, witty, approachable | Hot takes, probate myths, personal stories | Daily |
| **Instagram** | Visual, educational, professional | Before/after properties, infographics, reels scripts | 3-4x/week |
| **Facebook** | Community-oriented, informative | Long-form posts, client stories, market updates | 3x/week |
| **LinkedIn** | Professional, thought-leadership | Attorney-facing content, market analysis, industry insights | 2x/week |

### Voice Examples

**Threads voice:**
> "Probate court in OC today. Three-hour wait for a five-minute hearing. This is why you need someone who knows which department to file in."

**Instagram caption:**
> "This Corona Del Mar estate sat vacant for 8 months before the family called us. 47 days later: sold at 14% above the initial appraisal. Probate doesn't have to mean discount. 📍Corona Del Mar | 📞 Link in bio"

**LinkedIn:**
> "Attorneys: your probate clients deserve a RE specialist, not a generalist learning on the job. Here's what to look for when referring out real property matters..."

**Facebook:**
> "Question I get weekly: 'Can we sell Mom's house before probate is finished?' Short answer: yes, with court approval. Here's how the process actually works in Orange County..."

---

## Implementation Plan

### Week 1: Foundation
- [ ] Build `avatar/SKILL.md` — the persona layer
- [ ] Build `probate-transaction/SKILL.md` + court procedure references
- [ ] Build `client-communication/SKILL.md` + templates
- [ ] Push all to `geneboyle/GeneBoyleSkills`

### Week 2: Growth
- [ ] Build `probate-lead-gen/SKILL.md` — attorney outreach system
- [ ] Build `probate-listing-presentation/SKILL.md` — CMA + pitch tools
- [ ] Build `social-media-voice/SKILL.md` — multi-platform content engine

### Week 3: Intelligence
- [ ] Build `oc-market-intel/SKILL.md` — always-current market data
- [ ] Build `competitive-intel/SKILL.md` — track competitors
- [ ] Refine all skills based on Gene's actual usage feedback

### Ongoing
- Skills are living documents — edit on GitHub, Claude always fetches latest
- Add new skills as Gene's business evolves
- Kelly can edit skills to shape Gene's AI assistant without Gene needing to touch code

---

## The Kelly Advantage

Here's the strategic play: **Kelly builds and maintains Gene's avatar system.** Gene doesn't need to understand skills, GitHub, or prompting. He just talks to Claude and gets a business partner who:

- Knows his pipeline and procedures
- Writes in his voice across all platforms
- Drafts client communications he'd actually send
- Preps his listing presentations with current data
- Tracks his competitors so he stays ahead
- Manages his crypto timing signals

Kelly shapes the system. Gene benefits from the system. Claude executes the system.

That's the avatar.
