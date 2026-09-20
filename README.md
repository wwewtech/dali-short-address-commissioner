# dali-short-address-commissioner

Commission DALI/DALI-2 lighting buses with an agent: short-address assignment (0-63), clash resolution, 16 groups, 16 scenes, DT8 devices, and emergency ballast tests per IEC 62386.

## Why use this skill?
A DALI bus with duplicate or missing addresses misbehaves in ways that look like bad ballasts. This skill helps you commission methodically: discover → address → group → scene → verify.

## Quick Installation

### 1. Via `skills.sh` / Vercel Skills CLI
```bash
npx skills add wwewtech/dali-short-address-commissioner
```

### 2. Via Claude Code
```bash
claude skills add https://github.com/wwewtech/dali-short-address-commissioner
```

### 3. For Google Antigravity
Clone or copy `SKILL.md` directly into your Antigravity skills directory:
```bash
# Windows
mkdir -p "$HOME\.gemini\config\skills\dali-short-address-commissioner"
curl -sL https://raw.githubusercontent.com/wwewtech/dali-short-address-commissioner/main/SKILL.md -o "$HOME\.gemini\config\skills\dali-short-address-commissioner\SKILL.md"

# macOS / Linux
mkdir -p ~/.gemini/config/skills/dali-short-address-commissioner
curl -sL https://raw.githubusercontent.com/wwewtech/dali-short-address-commissioner/main/SKILL.md -o ~/.gemini/config/skills/dali-short-address-commissioner/SKILL.md
```

### 4. For Cursor & Windsurf
Add `SKILL.md` to your workspace prompt context:
```bash
mkdir -p .cursor/skills/dali-short-address-commissioner
curl -sL https://raw.githubusercontent.com/wwewtech/dali-short-address-commissioner/main/SKILL.md -o .cursor/skills/dali-short-address-commissioner/SKILL.md
```


## Links
- [Live Showcase](https://wwew.tech/dali-short-address-commissioner)
- [skills.sh](https://skills.sh)
- [SKILL.md](SKILL.md)

## Core Concepts
- Max 64 short addresses (0–63) per bus, max 16 groups, max 16 scenes.
- 15-minute commissioning timer for addressing commands.
- Discover → assign short addresses → resolve clashes.
- Assign groups and scenes.
- Schedule emergency gear testing.
- Replacement flow: Install new gear → explicitly assign OLD short address → re-apply config.

## License
MIT © wwewtech
