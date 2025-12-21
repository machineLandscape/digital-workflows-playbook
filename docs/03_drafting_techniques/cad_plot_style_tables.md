# CAD Technique — Plot Style Tables (CTB / STB) in Detail

**Version:** v1.1  
**Use when:** lineweights are wrong, drawings plot faint, or PDFs plot in unexpected colors.  
**Applies to:** AutoCAD-based workflows  
**Last updated:** 2025-12-21

---

## 1. What this technique does

This guide teaches how to:
- understand CTB vs STB
- choose the correct plot style table
- edit CTB safely
- debug lineweight issues

Plot styles are the **translation layer** between CAD colors and printed lineweights.

---

## 2. Core idea (read this)

In a CTB workflow:

**Layer color (Layer Properties Manager) → CTB mapping → printed lineweight**

CTB doesn't act on objects magically. It interprets **colors** (layer or object).

---

## 3. CTB vs STB (decide what you're using)

### CTB (Color-dependent)
- Most common for landscape/architecture
- Lineweight is tied to color number
- You draft using a controlled color system

### STB (Named styles)
- Lineweight tied to style names (e.g., "Heavy", "Light")
- Requires a different discipline and file configuration

**Rule:** If you did not intentionally set up STB, you are almost certainly using CTB.

---

## 4. Find out what your drawing uses

In AutoCAD:
- Command: `PLOT`
- Look for the field: **Plot style table (pen assignments)**

If you see a `.ctb` file → CTB workflow
If you see a `.stb` file → STB workflow

Also check:
- Command: `STYLESMANAGER` (opens Plot Styles folder)

---

## 5. How CTB actually works

A CTB file contains 255 color rows (1–255). Each row can define:
- lineweight (mm/in)
- screening (percent)
- dithering
- plot color (often set to black)

**Best practice:** Keep screening at **100%** for clarity unless intentionally gray.

---

## 6. Safe CTB editing workflow (do not skip)

1. Locate the CTB you are using (from PLOT dialog)
2. **Copy it** and rename the copy for your class/studio
   - e.g., `Studio_Standard.ctb`
3. Edit the copy only

Never edit the system default CTB unless you control all machines.

---

## 7. Edit a CTB (step-by-step)

1. Run: `STYLESMANAGER`
2. Double-click your `.ctb`
3. In the editor:
   - Select a color row (e.g., Color 9)
   - Set **Lineweight**
   - Set **Screening = 100**
   - Set **Plot color = Black** (common standard)
4. Save

**Checkpoint:** After saving, re-open PLOT dialog and ensure the same CTB is selected.

---

## 8. Recommended landscape lineweight bands (starting point)

These are typical, not universal:

- Heavy / cut: **0.50–0.70 mm**
- Primary: **0.30–0.40 mm**
- Secondary: **0.18–0.25 mm**
- Background: **0.13 mm**
- Very light: **0.09–0.10 mm**

**Rule:** 4–5 weights are enough. More weights usually reduce clarity.

---

## 9. Debugging lineweights (fast diagnosis)

### Symptom A: Everything prints the same weight
- Objects all on one color
- OR object overrides ignore ByLayer
- OR CTB is not applied

Fix:
- Enforce ByLayer
- Ensure CTB is selected in Page Setup / Plot dialog

### Symptom B: Output is faint
- Screening < 100
- Lineweights too low
- Plot with lineweights off

Fix:
- Set screening 100
- Increase key lineweights
- Ensure "Plot with lineweights" is ON

### Symptom C: PDF prints in color
- Plot color not forced to black
- Using "None" plot style

Fix:
- Set plot color to black for relevant rows
- Select proper CTB in Page Setup

---

## 10. Connection back to layers (critical)

CTB assumes your **layer colors** encode hierarchy.

If your layers are random colors, your CTB can't produce predictable drawings.

## Related techniques

- [Layer Properties Manager (Linework Control)](cad_layer_properties_manager.md)
- [Lineweights & Graphic Hierarchy](cad_lineweights_and_hierarchy.md)
- [Page Setup Manager (Step-by-Step)](cad_page_setup_manager.md)

