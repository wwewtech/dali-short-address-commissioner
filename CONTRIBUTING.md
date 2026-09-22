# Contributing to DALI Short-Address Commissioner

We welcome contributions from building automation engineers, lighting designers, and IoT protocol developers.

---

## Ways to Contribute

1. **Protocol Presets:** Add configuration templates for specific gateway families (KNX/DALI, Tridonic connecDIM, Helvar, Philips Dynalite, Siemens Gamma).
2. **Device Type Profiles:** Expand DT8 (Part 209) color coordinate conversions or DT1 (Part 202) emergency lighting test sequences.
3. **Evals (`evals/evals.json`):** Add challenging edge cases (e.g. multi-gateway bus contention, noise tolerance, high-capacitance bus dropouts).

---

## Submission Guidelines

- Ensure byte-for-byte SHA256 symmetry between `./SKILL.md` and `./skills/dali-short-address-commissioner/SKILL.md`.
- Maintain single-file self-containment in `SKILL.md`.
- Validate before opening a PR:
  ```bash
  python -c "import hashlib; assert hashlib.sha256(open('SKILL.md','rb').read()).hexdigest() == hashlib.sha256(open('skills/dali-short-address-commissioner/SKILL.md','rb').read()).hexdigest(), 'Hash mismatch!'"
  ```
