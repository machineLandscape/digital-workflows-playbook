# GUIDE_XLATE_01 — GIS → CAD: What Transfers and What Doesn’t

**Version:** v01.0  
**Audience:** Mixed ability  
**Last updated:** 2025-12-20  
**Primary workflow:** Mapping → Drafting  
**Does not cover:** Advanced GIS analysis or CAD drafting techniques

---

## 1. What this does

This guide explains **how spatial data moves from GIS into CAD**, what survives that translation, and what commonly breaks.

Its goal is to help you:
- Avoid scale and alignment errors
- Import only what you need
- Understand why GIS drawings often look “wrong” in CAD

---

## 2. When to use this

Use this guide:
- After creating a GIS context map
- Before drafting a context plan in CAD
- Anytime GIS data does not align or scale correctly in CAD

If you skip this step, problems will compound later.

---

## 3. Core idea (read this)

**GIS is geographic. CAD is geometric.**

When you move data:
- Coordinates survive
- Attributes mostly do not
- Symbology never does

Expect to **re-draw and re-style** in CAD.

---

## 4. What transfers reliably

These usually transfer correctly:

- Linework geometry (roads, parcels, contours)
- Points (intersections, landmarks)
- Relative positions
- Overall extents

---

## 5. What does NOT transfer

Do not expect these to survive:

- Lineweights
- Colors
- Labels
- Hatches
- Text formatting
- Map layout elements

Those are **representation decisions**, not data.

---

## 6. Step-by-step transfer workflow

### Step 1 — Prepare data in GIS
- Turn off unnecessary layers
- Clip data to your site + context
- Simplify geometry if possible

Less data = fewer CAD problems.

---

### Step 2 — Export from GIS
Preferred formats:
- DXF (most common)
- DWG (if available)

Rules:
- Export only visible layers
- Use projected coordinates (not geographic)

---

### Step 3 — Open in CAD (do not attach blindly)
- Open a new CAD file
- Insert or open the exported file
- Do **not** explode everything immediately

---

### Step 4 — Check scale and alignment
Immediately verify:
- Does a known distance measure correctly?
- Does north align as expected?
- Does the site match known references?

If scale is wrong, stop and fix it now.

---

### Step 5 — Clean the drawing
In CAD:
- Move geometry to correct layers
- Delete excess data
- Re-assign lineweights and colors
- Redraw key elements if needed

This is normal and expected.

---

## 7. Common failures & fixes

**Problem:** Everything is tiny or huge  
**Fix:** Units mismatch. Check GIS projection and CAD units.

**Problem:** Data is offset far away  
**Fix:** Coordinate system issue. Zoom to extents.

**Problem:** Lines look messy  
**Fix:** Simplify in GIS or redraw selectively in CAD.

---

## 8. Checkpoint

You should now have:
- Correctly scaled geometry
- Clean layers
- A stable CAD base for drafting

If not, fix it before proceeding.

---

## 9. What to do next

- Draft a context plan:  
  → [Draft a GIS-Based Context Plan](../03_drafting/guide_cad_02_gis_context.md)

- If exports keep failing:  
  → [Troubleshoot When Something Goes Wrong](../00_getting_started/guide_00_03_troubleshoot.md)

GIS → CAD translation is a **filtering process**, not a copy-paste.
