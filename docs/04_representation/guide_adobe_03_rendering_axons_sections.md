# GUIDE_ADOBE_03 — Rendering Axons & Sections in Photoshop

**Version:** v1.0  
**Audience:** Mixed ability  
**Last updated:** 2025-12-20  
**Primary workflow:** Representation  
**Input:** Rhino axonometric or section exports  
**Output:** Atmospheric axons and sections with depth and clarity  
**Does not cover:** Photorealistic rendering or materials

---

## 1. What this guide teaches

This guide teaches **how to render axonometric drawings and sections in Photoshop** to communicate spatial depth, hierarchy, and intent.

This is **diagrammatic atmosphere**, not realism.

---

## 2. When to use this

Use this guide:
- After axons or sections are exported from Rhino
- When spatial depth is unclear
- When drawings need emphasis and legibility

Do not use this if geometry is still changing.

---

## 3. Core idea (read this)

**Axons and sections must read in layers.**

Photoshop is used to:
- Separate foreground from background
- Clarify cuts and overlaps
- Control mood without distraction

---

## 4. File setup (critical)

### Create the Photoshop file
- Canvas size = final output size
- Resolution:
  - Print: 300 dpi
  - Screen: 150 dpi
- Color mode: RGB while working

### Import base geometry
- Place Rhino export as a Smart Object
- Lock the base layer
- Name clearly:
  ```
  BASE_RHINO_EXPORT
  ```

Never paint on the base layer.

---

## 5. Rendering axonometric drawings

### A. Establish depth
- Duplicate base geometry
- Darken foreground elements
- Lighten background elements

Depth comes from value, not color.

---

### B. Cast shadows
- Create a shadow layer
- Offset consistently in one direction
- Blur slightly
- Set opacity between 10–25%

Shadows explain space.

---

### C. Surface tone
- Add subtle fills for ground and planes
- Use large, soft brushes
- Keep saturation low

Avoid texture overload.

---

### D. Highlights and focus
- Light overlays near key spaces
- Slight contrast increase where attention is needed

This guides the eye.

---

## 6. Rendering sections

### A. Cut plane dominance
- Fill cut geometry with dark poche
- This must be the strongest element

If the cut isn’t obvious, the section fails.

---

### B. Receding depth
- Reduce contrast with distance
- Use lighter values behind the cut

Sections should read front-to-back instantly.

---

### C. Ground and context
- Keep ground textures minimal
- Avoid background noise

Context supports, never competes.

---

## 7. Color discipline

- Use a limited palette (3–5 tones)
- Avoid strong hues unless intentional
- Let value do the work

Most good axons are nearly monochrome.

---

## 8. Layer organization (non-negotiable)

Use groups such as:
```
01_base
02_cut_poche
03_shadows
04_surface_tone
05_highlights
```

Name everything. Group everything.

---

## 9. Common failures & fixes

**Problem:** Axon feels flat  
**Fix:** Increase value contrast, not effects

**Problem:** Section is confusing  
**Fix:** Strengthen cut plane

**Problem:** Drawing looks busy  
**Fix:** Remove textures and colors

---

## 10. Checkpoint

Your drawing should:
- Read clearly at pin-up distance
- Explain spatial relationships
- Support the design idea

If not, simplify.

---

## 11. What to do next

- Combine with vector graphics:
  → Illustrator guides

- Assemble boards:
  → InDesign guides

Photoshop rendering is about **spatial clarity**, not polish.
