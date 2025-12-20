# GUIDE_XLATE_05 — CAD → Rhino: Bring Drafted Linework into a Model

**Version:** v01.0  
**Audience:** Mixed ability  
**Last updated:** 2025-12-20  
**Primary workflow:** Drafting → Modeling  
**Does not cover:** Rendering, materials, or visualization

---

## 1. What this does

This guide explains how to move **CAD linework** into Rhino so it can be used reliably for modeling.

The goal is **clean, correctly scaled curves** that behave predictably in Rhino.

---

## 2. When to use this

Use this guide:
- When site or design geometry was drafted in CAD
- Before building 3D models from 2D drawings
- When Rhino imports from CAD look wrong or broken

---

## 3. Core idea (read this)

**CAD is strict. Rhino is flexible.**

That flexibility becomes a problem if CAD data is not prepared correctly.

Clean data first.

---

## 4. Prepare the CAD file (critical)

Before exporting from CAD:

- Purge unused layers
- Delete annotation (text, dimensions, hatches)
- Ensure all geometry is:
  - On correct layers
  - At true scale
  - Near the origin

Flatten geometry if importing plans:
- Everything should be at Z = 0

Save a copy specifically for Rhino.

---

## 5. Export from CAD

Preferred formats:
- DWG
- DXF

Export settings:
- Use model space
- Maintain units
- Export by layer

Do not export paper space.

---

## 6. Import into Rhino

In Rhino:
- Set units **before** importing
- Use `Import`, not `Open`
- Check scale immediately

Zoom to extents to find geometry.

---

## 7. Verify and clean in Rhino

Immediately after import:
- Check distances
- Remove duplicate curves
- Join curves where appropriate
- Simplify overly complex geometry

Do not model until this step is complete.

---

## 8. Organize layers

- Preserve CAD layer structure when possible
- Rename layers if needed
- Group logically

Good layers prevent modeling errors.

---

## 9. Common failures & fixes

**Problem:** Geometry imports at wrong scale  
**Fix:** Units mismatch — fix before modeling

**Problem:** Lines won’t join  
**Fix:** Clean and simplify curves

**Problem:** File feels heavy  
**Fix:** Remove unnecessary detail

---

## 10. Checkpoint

You should now have:
- Clean curves
- Correct scale
- Geometry ready for modeling

If not, fix the CAD file and re-import.

---

## 11. What to do next

- Build models:  
  → Rhino modeling guides

- If geometry breaks downstream:  
  → [Troubleshoot When Something Goes Wrong](../00_getting_started/guide_00_03_troubleshoot.md)

CAD → Rhino is about **discipline before flexibility**.
