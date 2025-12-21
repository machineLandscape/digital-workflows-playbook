# CAD Technique — Viewports & Scale That Actually Work

**Use when:** drawings plot at the wrong scale or annotation behaves unpredictably.

---

## Core principle

- **Model space = full scale (1:1)**
- **Paper space = representation only**

Never scale objects in model space.

---

## Correct workflow

1. Draw everything at real-world size in model space
2. Switch to paper space
3. Create a viewport
4. Set viewport scale explicitly (e.g. 1" = 40')
5. Lock the viewport

If scale is wrong, fix it here.

---

## Common failures

- Multiple scales in one viewport
- Unlocked viewports
- Scaling geometry instead of viewports

---

## Quick check

Measure a known distance in the plotted PDF.
If it’s wrong, return here.
