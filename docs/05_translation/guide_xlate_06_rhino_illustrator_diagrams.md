# GUIDE_XLATE_06 — Rhino ↔ Illustrator: Diagram Workflows

**Version:** v01.0  
**Audience:** Mixed ability  
**Last updated:** 2025-12-20  
**Primary workflow:** Modeling ↔ Representation  
**Does not cover:** Photoreal rendering or layout

---

## 1. What this does

This guide explains how to move **diagrammatic geometry** back and forth between **Rhino and Illustrator** for conceptual diagrams, section diagrams, and analytic drawings.

The goal is **clarity and control**, not precision drafting.

---

## 2. When to use this

Use this guide:
- When diagrams start in Rhino but need graphic refinement
- When Illustrator diagrams need geometric adjustment
- When CAD feels too rigid for diagram work

---

## 3. Core idea (read this)

**Rhino controls geometry. Illustrator controls meaning.**

Use each tool for what it does best.

---

## 4. Rhino → Illustrator (most common direction)

### Prepare in Rhino
Before export:
- Isolate only diagram geometry
- Simplify curves and surfaces
- Set correct view (Top, Front, Section)

Avoid exporting construction geometry.

### Export methods
Preferred:
- Export as PDF from Rhino view
Alternative:
- Export AI if needed

Set scale intentionally, but expect Illustrator to be scale-agnostic.

---

## 5. Illustrator cleanup and styling

In Illustrator:
- Ungroup carefully
- Delete unnecessary paths
- Reassign strokes and fills
- Establish hierarchy using lineweight and color

Lock reference layers early.

---

## 6. Illustrator → Rhino (less common, but useful)

Use this when:
- Diagram proportions need adjustment
- Spatial logic needs testing

### Export from Illustrator
- Save as AI (legacy compatibility if needed)
- Avoid effects and strokes that don’t translate

### Import into Rhino
- Set units first
- Expect curves, not fills
- Clean and join geometry

Illustrator is not a modeling environment.

---

## 7. Common failures & fixes

**Problem:** Diagrams feel muddy  
**Fix:** Reduce elements, increase hierarchy

**Problem:** Geometry imports oddly  
**Fix:** Simplify before export

**Problem:** Scale confusion  
**Fix:** Decide which tool controls scale

---

## 8. Checkpoint

You should have:
- Clear diagram logic
- Editable geometry
- A repeatable workflow

---

## 9. What to do next

- Assemble boards:  
  → InDesign guides

- Add raster effects if needed:  
  → Photoshop guides

Rhino ↔ Illustrator workflows support **thinking**, not documentation.
