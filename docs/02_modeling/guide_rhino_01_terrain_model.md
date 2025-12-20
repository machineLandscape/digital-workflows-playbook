# GUIDE_RHINO_01 — Build a Terrain Model

**Version:** v01.0  
**Audience:** Mixed ability  
**Last updated:** 2025-12-20  
**Primary workflow:** Modeling  
**Input:** Contours or DEM  
**Output:** Clean terrain surface  

---

## 1. What this does

This guide shows you how to build a **reliable terrain model** in Rhino from GIS-derived data.

The goal is **usable geometry**, not visual realism.

---

## 2. When to use this

Use this guide:
- After creating a GIS context map
- Before site modeling or sectioning
- When topography drives design

---

## 3. Core idea (read this)

**Clean inputs create stable surfaces.**

Most terrain problems come from messy contours.

---

## 4. Prepare input data

Before modeling:
- Remove duplicate contours
- Check elevation values
- Ensure consistent units

Do this before Rhino.

---

## 5. Build the surface

Common approaches:
- From contours (Patch / Loft / Drape)
- From DEM (Mesh → Surface)

Choose the simplest method that works.

---

## 6. Check the model

Verify:
- No spikes or holes
- Smooth transitions
- Correct scale

Fix issues now.

---

## 7. Simplify

Do not over-model:
- Remove excess detail
- Keep file light
- Model only what matters

---

## 8. Checkpoint

You should have:
- A stable terrain surface
- Correct scale
- Geometry ready for design

---

## 9. What to do next

- Cut sections:  
  → Rhino section guides (coming soon)

- Export to CAD:  
  → [Rhino → CAD: Clean Geometry for Drafting](../05_translation/guide_xlate_02_rhino_to_cad.md)

Terrain models are infrastructure, not renderings.
