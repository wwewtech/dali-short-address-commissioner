# Changelog

All notable changes to the `dali-short-address-commissioner` skill will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [1.0.0] - 2026-09-22

### Initial Release — Deterministic IEC 62386 Bus Commissioning

#### Added
- **Master Skill (`SKILL.md`):** Complete protocol specification for DALI and DALI-2 commissioning.
- **Double-Command 100ms Rule:** Enforced repeat window for all critical configuration frames.
- **24-Bit Binary Search Collision Resolution:** Mathematical space navigation across 16,777,216 addresses.
- **Capacity Enforcement:** Strict 64-address (0–63), 16-group (0–15), and 16-scene (0–15) boundaries.
- **DT8 Tunable White Architecture:** Mirek calculation and DTR0/DTR1 payload formatting for Part 209.
- **Emergency Lighting Safety:** Staggered duration test scheduling per Part 202.
- **Interactive Bus Simulator (`docs/index.html`):** 64-node interactive visualizer and current budget calculator.
- **CI Validation:** Automated YAML frontmatter and SHA256 file symmetry verification.
