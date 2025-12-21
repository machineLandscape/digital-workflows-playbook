# CAD Technique — Lineweights & Graphic Hierarchy (CAD → PDF)

**Version:** v1.1  
**Use when:** drawings look flat, everything prints the same, or lineweight control feels mysterious.  
**Applies to:** AutoCAD-based workflows (CTB or STB)  
**Last updated:** 2025-12-21

---

## 1. What this technique does

This guide teaches an end-to-end lineweight system:
- assign hierarchy via layers (Layer Properties Manager)
- encode hierarchy via color (CTB workflow)
- output predictable weights via CTB
- validate in PDF

---

## 2. Core idea (read this)

**Lineweight is hierarchy.**

Before color, before texture, before Photoshop:
- what is cut?
- what is primary?
- what is background?

If hierarchy fails, the drawing fails.

---

## 3. Minimal lineweight palette (recommended)

Use 4–5 weights only:

- Very light: 0.09–0.10 mm (background)
- Light: 0.13 mm (context)
- Medium: 0.18–0.25 mm (secondary)
- Heavy: 0.30–0.40 mm (primary)
- Cut: 0.50–0.70 mm (section cut / poche)

More weights usually decrease clarity.

---

## 4. CTB-based workflow (most common)

### Step 4.1 — Layers encode hierarchy via color
Set layer colors intentionally (not aesthetically).

### Step 4.2 — CTB maps colors to lineweights
The CTB is the dictionary translating your color system into printed weights.

### Step 4.3 — Page setup applies the CTB
Without page setup, output becomes inconsistent.

---

## 5. Fast setup (do this in order)

1. Define layer roles (cut, primary, secondary, background)
2. Assign layer colors to match your CTB plan
3. Ensure objects are ByLayer (no overrides)
4. Select the correct CTB in Page Setup
5. Plot preview and validate

---

## 6. Validation (do not trust the screen)

Lineweights on screen can mislead.

Always validate by:
- plotting a PDF
- zooming in and out
- printing a test sheet if possible

**Checkpoint:** You can visually identify cut/primary/background in the PDF without color.

---

## 7. Common failures & fixes

**Problem:** Everything prints same weight  
**Cause:** same color everywhere OR wrong CTB OR overrides

**Fix:** enforce ByLayer + check CTB selection

**Problem:** Output is faint  
**Cause:** screening < 100, or weights too low

**Fix:** set screening 100, increase key weights

**Problem:** Viewport shows different weights than PDF  
**Cause:** LWDISPLAY and screen display settings

**Fix:** ignore screen; trust PDF preview

---

## 8. Related step-by-step techniques

- [Layer Properties Manager (Linework Control)](cad_layer_properties_manager.md)
- [Plot Style Tables (CTB/STB) in Detail](cad_plot_style_tables.md)
- [Page Setup Manager (Step-by-Step)](cad_page_setup_manager.md)

- ## Linked video tutorials (optional)

For visual reinforcement of the steps above, see the  
[Curated Video Tutorial Index](../video_index.md).
