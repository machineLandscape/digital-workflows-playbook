# CAD Technique — Page Setup Manager (Step-by-Step)

**Version:** v1.1  
**Use when:** layouts plot inconsistently, settings keep changing, or you need repeatable PDFs.  
**Applies to:** AutoCAD-based workflows  
**Last updated:** 2025-12-21

---

## 1. What this technique does

This guide teaches how to configure **Page Setup Manager** so plotting becomes:
- repeatable
- consistent across layouts
- fast (no re-setting the Plot dialog every time)

Page setups are **plot templates**.

---

## 2. Core idea (read this)

**If plotting is not repeatable, it is not finished.**

You should plot by applying a page setup, not by rebuilding settings every time.

---

## 3. Open Page Setup Manager

1. Go to a **Layout** (Paper Space)
2. Right-click a layout tab → **Page Setup Manager**
3. Choose:
   - **Modify** to edit an existing setup
   - **New** to create one

---

## 4. Configure the page setup (field-by-field)

### A. Printer/Plotter
Recommended default:
- `DWG To PDF.pc3`

**Rule:** Changing plotters between layouts is a common cause of inconsistency.

### B. Paper size
Select the required sheet size (Arch D/E, etc.).

**Checkpoint:** Paper size must match studio deliverable. Do not plan to scale later.

### C. Plot area
Set:
- **Plot area:** Layout
- **Plot offset:** Center the plot

Avoid "Window" unless troubleshooting.

### D. Plot scale
Set:
- **Scale:** 1:1

**Important:** Scaling happens in viewports, not here.

### E. Plot style table
Select the CTB/STB you intend to use (e.g., `Studio_Standard.ctb`).

If this is wrong, lineweights will be wrong.

### F. Plot options
Ensure:
- **Plot with plot styles** = ON
- **Plot with lineweights** = ON

### G. Drawing orientation
Set Portrait/Landscape intentionally.

---

## 5. Apply page setup to multiple layouts

From Page Setup Manager:
- Select the page setup → **Set Current**
- Repeat across layouts, or use "Import" if needed

**Best practice:** One page setup per sheet size per project.

---

## 6. Preview and validate

Before final plotting:
- Use **Preview**
- Confirm:
  - titleblock fits the sheet
  - nothing is clipped
  - lineweights look plausible

Then export PDF.

---

## 7. Common failures & fixes

**Problem:** Different layouts plot differently  
**Cause:** Different page setups applied.

**Fix:** Apply one standard page setup to all layouts.

**Problem:** CTB changes unexpectedly  
**Cause:** Plot dialog overrides page setup.

**Fix:** Re-open Page Setup Manager and reapply.

---

## 8. Checkpoint

A correct page setup allows you to:
- plot any layout with the same behavior
- switch between drawings without reconfiguring
- trust output

Next:
- [Fix Broken PDF Exports](cad_export_failures.md)

- ## Linked video tutorials (optional)

For visual reinforcement of the steps above, see the  
[Curated Video Tutorial Index](../video_index.md).
