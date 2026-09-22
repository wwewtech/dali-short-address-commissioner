# DALI Short Address Commissioner — Global Launch & Distribution Kit

This kit contains high-engagement announcement templates to publish and distribute `dali-short-address-commissioner` across major smart building, IoT, and developer communities.

---

## 1. Twitter / X Viral Launch Thread

### Post 1 (Hook + Banner):
> Anyone who has commissioned a commercial building with DALI-2 (IEC 62386) knows the pain:
>
> 64 ballasts on a loop, random address collisions during INITIALISE, and proprietary $1,000 commissioning boxes.
>
> We just open-sourced **DALI Short Address Commissioner**: an autonomous agent skill for fast, collision-free DALI commissioning 🧵👇
>
> `npx skills add wwewtech/dali-short-address-commissioner`
> [Attach: assets/dali-banner.svg]

### Post 2 (The 24-bit Search Problem):
> When 60 fixtures wake up simultaneously with 24-bit random addresses, binary search can take 15 minutes if implemented naively.
>
> This skill enforces:
> - Search address binary tree partitioning with branch pruning
> - Non-destructive conflict scanning (never wipes previously verified short addresses A0-A63)
> - Physical blink locate verification loops
> - IEC 62386-102 framing compliant timing (backward frame 9.17ms to 10.5ms)

### Post 3 (Hardware Agnostic):
> Works over USB-to-DALI interfaces (DALI USB, Haseman, Lunatone, Raspberry Pi DALI hat, or TCP/IP gateways).
>
> Compatible with Claude Code, Cursor, Windsurf, and Antigravity.

### Post 4 (Install & Links):
> 📦 skills.sh: https://skills.sh/wwewtech/dali-short-address-commissioner
> ⭐ GitHub: https://github.com/wwewtech/dali-short-address-commissioner
> 🌐 Interactive Demo: https://wwewtech.github.io/dali-short-address-commissioner/

---

## 2. Reddit (`r/homeautomation`, `r/smarthome`, `r/embedded`, `r/ClaudeAI`)

### Title:
> **Automating DALI-2 (IEC 62386) short address commissioning and collision resolution with an open-source agent skill**

### Body:
> Hey everyone,
>
> DALI-2 lighting commissioning usually requires clunky vendor-specific software (Tridonic masterCONFIGURATOR, Lunatone DALI Cockpit) that doesn't script or automate well.
>
> We built **DALI Short Address Commissioner** (https://github.com/wwewtech/dali-short-address-commissioner), a standard agent skill (`SKILL.md`) that guides agents in:
> - Executing the IEC 62386-102 collision resolution algorithm
> - Assigning short addresses A0 through A63 without collisions
> - Isolating unaddressed ballast units using binary search on the 24-bit random address space
> - Generating human-readable verification logs and blink confirmation scripts
>
> **Install:**
> ```bash
> npx skills add wwewtech/dali-short-address-commissioner
> ```
>
> Web App: https://wwewtech.github.io/dali-short-address-commissioner/
> Repo: https://github.com/wwewtech/dali-short-address-commissioner

---

## 3. Pull Request Submission Template

```markdown
## Summary
Adds the `dali-short-address-commissioner` skill to `skills/dali-short-address-commissioner/SKILL.md`.

### Overview
`dali-short-address-commissioner` equips autonomous coding agents with IEC 62386-102 lighting commissioning logic, 24-bit random address collision resolution, short address assignment (A0-A63), and physical fixture identification workflows.

### Features
- Rigorous IEC 62386-102 binary search collision resolution
- Safe, non-destructive re-addressing of conflicted lighting gear
- Physical blink/locate confirmation protocols
- Bus current telemetry and frame timing compliance checks

### Validation
Passes all CI checks with 0 errors and 0 warnings. Verified against multi-ballast collision evals.
```
