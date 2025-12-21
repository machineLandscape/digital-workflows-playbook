# Rhino Technique — Fix Spiky or Broken Terrain Surfaces
**Version:** v1.1  
**Tool:** Rhino  
**Scope:** Repair and diagnosis  

---

## 1. When to use this technique

Use this guide when:
- A terrain surface has spikes, pits, or tears
- Sections fail or look jagged
- The surface looks fine in Top view but breaks in 3D

Do not attempt grading or drafting until this is resolved.

---

## 2. Core idea (read this)

**Broken surfaces are almost always caused by bad input curves.**

The surface is a symptom — not the problem.

---

## 3. Step 1 — Inspect the surface in 3D

- Switch to `Perspective`
- Use `Shaded` or `Rendered` view
- Orbit slowly

Look for:
- Vertical spikes
- Pinched ridges
- Sudden drops

Mark problem areas mentally before fixing anything.

---

## 4. Step 2 — Identify the offending contours

Hide the surface.
Show contours.

Common issues:
- Overlapping contours
- Contours that touch or cross
- Duplicate curves
- Extreme elevation jumps

Use `SelDup` to find duplicates.

---

## 5. Step 3 — Fix the curves (upstream)

Do **not** fix the surface yet.

Actions:
- Delete bad curves
- Simplify overly complex contours
- Rebuild problematic curves only where needed

Keep edits local.

---

## 6. Step 4 — Recreate the surface

- Delete the broken surface
- Re-run **Patch** or **Drape**
- Adjust parameters conservatively

Never try to “heal” a fundamentally bad surface.

---

## 7. Step 5 — Reduce surface complexity

If the surface is heavy:
- Use `Rebuild`
- Reduce control points
- Preserve overall form

Overly dense surfaces fail later.

---

## 8. Immediate validation

- Cut a test section
- Rotate in perspective
- Check for continuity

If sections fail, the surface is still broken.

---

## 9. Common mistakes

❌ Editing surfaces endlessly  
❌ Ignoring contour problems  
❌ Fixing symptoms downstream  

Always return to curves.

---

## 10. Checkpoint

You should have:
- A smooth surface
- No spikes
- Clean section cuts

If not, repeat upstream fixes.

## Related techniques

- [Create a Terrain Surface from Contours](rhino_surface_from_contours.md)
- [Patch vs Drape (Decision Guide)](rhino_patch_vs_drape.md)

