# CAD Technique — Fix Broken PDF Exports

**Version:** v1.1  
**Use when:** PDFs are missing objects, are the wrong scale, have wrong lineweights, or look faint.  
**Applies to:** AutoCAD-based workflows  
**Last updated:** 2025-12-21

---

## 1. What this technique does

This is a **diagnostic checklist** that helps you isolate whether the problem is:
- viewport / scale
- layer visibility
- plot style (CTB/STB)
- page setup
- PDF driver

---

## 2. Core idea (read this)

**Fix exports in CAD.**  
Do not “repair” scale or lineweights in Illustrator/Photoshop.

If the PDF is wrong, the drawing is not finished.

---

## 3. Step 1 — Confirm you are plotting from a Layout

- Go to a layout tab (paper space)
- Plot from the layout

If you plot from model space, scale is often wrong and output is inconsistent.

---

## 4. Step 2 — Scale is wrong

### Symptoms
- Measured distances in PDF are incorrect
- Titleblock fits but drawing scale is off

### Causes
- Viewport scale incorrect
- Viewport not locked
- Page setup plot scale not 1:1

### Fix
- Set viewport scale explicitly
- Lock viewport
- Ensure Page Setup scale = 1:1

Related:
- [Viewports & Scale That Actually Work](cad_viewports_and_scale.md)
- [Page Setup Manager](cad_page_setup_manager.md)

---

## 5. Step 3 — Missing objects

### Symptoms
- Some layers disappear in PDF
- Some items vanish only in one viewport

### Causes
- Layer Off/Frozen
- Layer Plot = No
- VP Freeze (viewport layer freeze)
- Objects on DEFPOINTS or non-plot layers

### Fix
- Check layer states in Layer Properties Manager
- Ensure Plot = Yes for key layers
- Check VP Freeze

Related:
- [Layer Properties Manager](cad_layer_properties_manager.md)

---

## 6. Step 4 — Lineweights wrong or faint

### Symptoms
- Everything prints same thickness
- Output is very light
- Output prints in color unexpectedly

### Causes
- Wrong CTB selected
- Plot with plot styles OFF
- Screening values lowered
- Plot with lineweights OFF

### Fix
- Select correct CTB in Page Setup
- Ensure Plot with plot styles ON
- Screening 100
- Plot with lineweights ON

Related:
- [Viewports & Scale That Actually Work](cad_viewports_and_scale.md)
- [Page Setup Manager](cad_page_setup_manager.md)
- [Plot Style Tables](cad_plot_style_tables.md)
- [Lineweights & Graphic Hierarchy](cad_lineweights_and_hierarchy.md)

---

## 7. Step 5 — PDF driver issues

### Symptoms
- Rasterized output
- Jagged lines
- Unexpected clipping

### Fix
- Use `DWG To PDF.pc3` (recommended)
- Preview before final plot
- Avoid third-party PDF printers unless required

---

## 8. Checkpoint

A correct export produces:
- correct measured scale
- consistent lineweights
- no missing geometry
- repeatability across layouts

If any item fails, diagnose upstream before proceeding.
