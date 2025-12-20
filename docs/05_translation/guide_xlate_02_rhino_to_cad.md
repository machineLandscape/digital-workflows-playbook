# GUIDE_XLATE_02 — Rhino → CAD: Clean Geometry for Drafting

**Version:** v01.0  
**Audience:** Mixed ability  
**Last updated:** 2025-12-20  
**Primary workflow:** Modeling → Drafting  
**Does not cover:** CAD annotation, layout, or plotting

---

## 1. What this does

This guide explains **how to move geometry from Rhino into CAD** so it can be used reliably for drafting.

The goal is **clean, scaled, usable linework**, not a perfect visual match.

---

## 2. When to use this

Use this guide:
- After building a terrain or site model in Rhino
- Before drafting plans, sections, or details in CAD
- When Rhino exports look messy or unusable in CAD

If you skip cleanup in Rhino, CAD problems multiply.

---

## 3. Core idea (read this)

**Rhino is flexible. CAD is strict.**

Anything ambiguous in Rhino becomes a problem in CAD.

Your job is to **remove ambiguity before export**.

---

## 4. Prepare the Rhino file (most important step)

Before exporting:

- Delete unused geometry
- Hide layers you don’t need
- Ensure geometry is:
  - 2D when it should be 2D
  - Planar when exporting plans
  - Not duplicated

Check units:
- Rhino model units must be intentional
- Do not “guess and fix later”

---

## 5. Decide what you are exporting

Only export what CAD needs:

- Contours
- Edges
- Section cuts
- Plan outlines

Do **not** export:
- Surfaces unless required
- Construction geometry
- Reference images

Less geometry = cleaner CAD files.

---

## 6. Export workflow

Preferred formats:
- DWG
- DXF

Steps:
1. Select only needed geometry
2. Use `Export Selected`
3. Set units explicitly
4. Export by layer when possible

Do not rely on defaults.

---

## 7. Open and verify in CAD immediately

In CAD:
- Check units
- Measure a known distance
- Zoom to extents
- Confirm layer structure

If scale is wrong, **stop and fix it now**.

---

## 8. Clean in CAD (expected step)

Once imported:
- Move objects to correct layers
- Delete stray geometry
- Join or redraw lines if needed
- Apply lineweights and hierarchy

This is not failure — it is the workflow.

---

## 9. Common failures & fixes

**Problem:** Lines are broken  
**Fix:** Join or redraw selectively

**Problem:** Scale is incorrect  
**Fix:** Units mismatch — fix source file

**Problem:** File is heavy  
**Fix:** Export less geometry

---

## 10. Checkpoint

You should now have:
- Clean, scaled linework
- Logical layers
- A stable base for drafting

If not, return to Rhino and fix it there.

---

## 11. What to do next

- Draft drawings:  
  → CAD drafting guides (coming soon)

- If geometry keeps breaking:  
  → [Troubleshoot When Something Goes Wrong](../00_getting_started/guide_00_03_troubleshoot.md)

Rhino → CAD is a **filtering process**, not a transfer.
