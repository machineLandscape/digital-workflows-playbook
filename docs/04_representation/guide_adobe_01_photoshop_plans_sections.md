# GUIDE_ADOBE_01 — Photoshop for Plans & Sections (Rendering Basics)

**Version:** v1.1  
**Audience:** Mixed ability  
**Last updated:** 2025-12-20  
**Primary workflow:** Representation  
**Input:** Clean vector drawings from CAD or Illustrator  
**Output:** Rendered plans and sections with depth, hierarchy, and atmosphere  

---

## 1. What this guide actually teaches

This guide teaches **how to render plans and sections in Photoshop**, not just when to use it.

You will learn how to:
- Set up a correct Photoshop file
- Add shadows, poche, and textures
- Control depth and hierarchy
- Render without breaking scale or clarity

This is **diagrammatic rendering**, not photorealism.

---

## 2. When to use Photoshop (and when not to)

Use Photoshop:
- After drafting and scaling are complete
- After Illustrator hierarchy is resolved
- When drawings need depth, contrast, or emphasis

Do **not** use Photoshop to:
- Fix linework
- Fix scale
- Design geometry

Those problems belong upstream.

---

## 3. Core idea (read this)

**Photoshop renders relationships, not objects.**

Every effect should clarify:
- What is foreground
- What is background
- What matters

If an effect doesn’t do that, remove it.

---

## 4. File setup (critical)

### Start correctly
1. Create a new PSD at final output size
2. Resolution:
   - Print: 300 dpi
   - Screen: 150 dpi
3. Color mode:
   - RGB while working
   - Convert later if needed

### Bring in base drawings
- Place CAD or Illustrator exports as **Smart Objects**
- Lock the base drawing layer
- Never paint directly on it

Name this layer:
```
BASE_linework_DO_NOT_EDIT
```

---

## 5. Rendering plans (step-by-step)

### A. Ground poche (first pass)
- Create a new layer below linework
- Use a solid fill or subtle texture
- Keep values light

Purpose: establish figure/ground.

---

### B. Shadows (most important step)
- Duplicate linework if needed
- Fill with black or dark gray
- Offset consistently (one light direction)
- Blur slightly (Gaussian Blur)

Lower opacity to 10–30%.

Shadows create **depth**, not drama.

---

### C. Vegetation and surface textures
- Use soft brushes or textures
- Mask everything
- Vary opacity, not color wildly

Avoid photographic realism.

---

### D. Highlights and emphasis
- Light overlays to guide attention
- Slight glow or brightness near key areas
- Very restrained use

This is compositional, not decorative.

---

## 6. Rendering sections (step-by-step)

### A. Cut plane poche
- Create a bold, dark fill at the cut
- This must be the strongest graphic element

If the cut is not obvious, the section fails.

---

### B. Depth behind the cut
- Use lighter tones as elements recede
- Reduce contrast with distance

Sections should read front-to-back instantly.

---

### C. Context and ground
- Add subtle textures or gradients
- Keep background quiet

Never compete with the cut.

---

## 7. Layer discipline (non-negotiable)

Use clear layer groups:
```
01_base_linework
02_poche
03_shadows
04_textures
05_highlights
```

Name everything. Group everything.

This keeps files editable and reusable.

---

## 8. Common rendering mistakes

**Problem:** Drawing looks muddy  
**Fix:** Too many effects — remove half

**Problem:** Scale feels wrong  
**Fix:** You edited geometry — go back

**Problem:** Everything is the same weight  
**Fix:** Increase hierarchy, not contrast

---

## 9. Checkpoint

Your rendered drawing should:
- Read clearly at pin-up distance
- Support the design idea
- Still work in black and white

If it doesn’t, simplify.

---

## 10. What to do next

- Combine with vector graphics:
  → Illustrator guides

- Assemble boards:
  → InDesign guides

Photoshop is a **clarifier**, not a fixer.
