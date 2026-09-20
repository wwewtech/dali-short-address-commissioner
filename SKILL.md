---
name: dali-short-address-commissioner
description: Commission DALI/DALI-2 lighting buses with an agent: short-address assignment (0-63), clash resolution, 16 groups, 16 scenes, DT8 devices, and emergency ballast tests per IEC 62386. Use when bringing up or extending a DALI installation (KNX/DALI gateways, Tridonic/Philips/Osram gear). Never energize unverified wiring.
---

# DALI Short-Address Commissioner

A DALI bus with duplicate or missing addresses misbehaves in ways that look like bad ballasts. Commission methodically: discover → address → group → scene → verify.

## Scope

- DALI-1 and DALI-2 control gear (ballasts, drivers, DT8 colour gear) and control devices.
- Limits that rule everything: max 64 short addresses (0–63) per bus, max 16 groups, max 16 scenes.
- Out of scope: mains wiring, DALI bus power supply sizing beyond sanity checks, KNX-side programming (only the DALI side).

## When NOT to use

- DMX/RDM stage lighting, 0-10V, or proprietary RF lighting — different protocols.
- Diagnosing dead ballasts before bus wiring is verified — check power and polarity first.

## Method

1. **Pre-flight.** Confirm bus power present, no shorts, max 64 devices per bus. If the bus has more than 64 gear units, stop: it must be split across interfaces first.
2. **Discover.** Run addressing discovery: `Initialize` (cmd 258, sent twice within 100ms), then `Randomize` (259, twice). The 15-minute commissioning timer starts — all addressing commands (259–270) must complete inside it.
3. **Assign short addresses.** Each gear generates a 24-bit random address; assign short addresses 0–63 one by one. Factory-fresh gear shows long address `0xFFFFFF`. Verify each assignment (lamp lights up / Identify).
4. **Resolve clashes.** Two gear units on one short address show as conflict: move one to a free address, never leave duplicates. Re-run discovery to confirm zero clashes.
5. **Groups.** Assign gear to groups (each gear can join up to 16 groups). Groups are the daily-use control unit — plan them by room/function, not by bus order.
6. **Scenes.** Program up to 16 scenes (level per gear/group). Keep one scene as known-good fallback (e.g., all 100%).
7. **Emergency gear.** Configure function/duration tests schedule (daily/weekly/monthly/yearly); emergency ballasts follow the same addressing but separate test regime.
8. **Verify.** Walk every address (0–63 used), every group, every scene; record failures with address + symptom. Upload/persist the controller config so ballast replacement (`readdress` flow) restores settings.

## Replacement flow (failed ballast)

1. Install new gear (address 255/unassigned). 2. Discover → assign the OLD short address explicitly (do not randomize the whole bus). 3. Re-apply group/scene membership from the saved config. 4. Verify.

## Safety rules

- Commissioning commands affect live luminaires: warn before broadcast commands that flash/switch whole buses.
- Never commission on a bus with known wiring faults; address assignment on a shorted bus corrupts the address table.
- Sources: IEC 62386 (DALI-2), Microchip AN1465/1487 (control gear behavior), Philips ABCs of DALI.
