# CAD Technique — Page Setup Manager (Step-by-Step)

**Use when:** drawings plot inconsistently, printers change, or PDFs don’t match expectations.  
**Applies to:** AutoCAD-based workflows (including Civil 3D)

---

## What this technique covers

This guide walks through **Page Setup Manager** in detail so you can:
- Lock plotting behavior
- Standardize output across sheets
- Avoid reconfiguring settings every time you plot

Page Setup Manager is how you make plotting **repeatable**.

---

## Core idea (read this)

**Page setups are templates for plotting.**

Once configured correctly, you should rarely touch plot settings again.

---

## Step 1 — Open Page Setup Manager

1. Switch to **Paper Space**
2. Right-click on a layout tab
3. Choose **Page Setup Manager**
4. Click **Modify** (or **New**)

Never plot “from scratch.” Always use a page setup.

---

## Step 2 — Printer / plotter selection

Choose:
- `DWG To PDF.pc3` (recommended for most cases)

Do not change printers between layouts unless necessary.

---

## Step 3 — Paper size

Select the **final output size**:
- Arch D, Arch E, etc.
- Match studio or review requirements

Never rely on scaling PDFs later.

---

## Step 4 — Plot area

Set:
- **Plot area:** Layout
- **Plot offset:** Centered

Avoid plotting “Window” unless troubleshooting.

---

## Step 5 — Plot scale

Set:
- **Scale:** 1:1

Scaling happens in **viewports**, not in Page Setup Manager.

---

## Step 6 — Plot style table

Select:
- The correct `.ctb` or `.stb` file

This controls lineweights and color behavior.
If this is wrong, nothing else matters.

---

## Step 7 — Drawing orientation

Set:
- Portrait or Landscape intentionally

Do not rotate PDFs later.

---

## Step 8 — Save and apply

- Save the page setup
- Apply it to other layouts
- Reuse it across files when possible

This is how standards are enforced.

---

## Common failures & fixes

**Problem:** Different layouts plot differently  
**Fix:** They are using different page setups

**Problem:** PDF looks faint  
**Fix:** Plot style table mismatch

---

## Checkpoint

You should be able to:
- Plot multiple layouts consistently
- Reuse page setups across drawings
- Stop reconfiguring plot dialogs

If not, rebuild the page setup from scratch.
