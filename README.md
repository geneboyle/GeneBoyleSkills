# GeneBoyleSkills

Custom Claude AI skills for Gene Boyle.

## Skills

| Skill | Description | Path |
|-------|-------------|------|
| **demark-crypto-timing** | DeMark indicator analysis (TD Sequential, TD Combo, cycle timing) for BTC/ETH entry/exit timing. Fundstrat/Tom Lee macro framing + DeMark micro-timing signals. | `demark-crypto-timing/` |

## Usage

Claude fetches skills from this repo via:

```
raw.githubusercontent.com/geneboyle/GeneBoyleSkills/main/{skill-name}/SKILL.md
```

## Structure

```
GeneBoyleSkills/
├── README.md
├── demark-crypto-timing/
│   ├── SKILL.md                          # Main skill instructions
│   └── references/
│       └── demark-indicators.md          # Deep reference on DeMark mechanics
└── [future skills]/
```
