# GUIDE_XLATE — CAD → Illustrator (Step-by-Step Import for Clean Diagrams)

**Version:** v1.0  
**Audience:** Mixed ability  
**Last updated:** 2025-12-21  
**Primary workflow:** Drafting → Representation  
**Use when:** You need clean vector linework from CAD in Illustrator (plans, sections, axons)

---

## 1. What this technique does

This guide teaches a **repeatable, low-drama** method to move CAD drawings into Illustrator so you can:
- control lineweights and hierarchy
- apply color and symbols cleanly
- avoid missing lines, exploded junk, and scale confusion

The goal is **clean vectors**, not “whatever comes through.”

---

## 2. Core idea (read this)

**CAD controls scale and geometry. Illustrator controls meaning and graphic hierarchy.**

Do not fix geometry in Illustrator.  
Do not “repair” plotting in Illustrator.  
If the base export is wrong, go back to CAD.

---

## 3. Recommended approach (best practice)

**Export a clean PDF from CAD → Place it into Illustrator.**

This is more reliable than importing DWG directly into Illustrator for most student workflows.

---

## 4. Before you export from CAD (non-negotiable)

### A. Confirm you are plotting from a Layout
- Use Paper Space (Layout tab)
- Use viewports with explicit scales
- Lock viewports

### B. Confirm lineweights are working in CAD
- Layer colors intentional (CTB workflow)
- Correct CTB selected in page setup
- Plot with plot styles ON
- Plot with lineweights ON

### C. Clean the drawing
- Freeze/hide construction layers
- Turn off xref layers you don’t need
- Remove annotation you don’t want (optional)
- Ensure you’re only plotting what you intend

**Checkpoint:** Plot Preview looks correct before exporting.

---

## 5. Export a “CAD-to-Illustrator” PDF (step-by-step)

1. In CAD, run:
   ```
   PLOT
   ```
2. Printer/plotter:
   - `DWG To PDF.pc3`
3. Plot area:
   - `Layout`
4. Plot scale:
   - `1:1` (always)
5. Plot style table:
   - your class/studio CTB (e.g., `Studio_Standard.ctb`)
6. Confirm options:
   - ✅ Plot with plot styles
   - ✅ Plot with lineweights
7. Click **Preview**
8. If preview is correct, click **OK** and save the PDF

**Name the file clearly:**  
`PROJECT_sheetname_CADexport.pdf`

---

## 6. Import into Illustrator (recommended method)

### Step 6.1 — Create an Illustrator file at correct artboard size
- File → New
- Choose the same sheet size as the CAD layout (Arch D/E, etc.)

### Step 6.2 — Place the PDF (do NOT open it)
- File → **Place**
- Select your CAD-exported PDF
- Ensure **Link** is ON (recommended while iterating)
- Click once to place at 100%

**Why Place instead of Open?**  
Place keeps your AI file stable and allows you to swap PDFs later.

---

## 7. Scale verification (critical)

7. Scale verification and correction (step-by-step)

Even though the PDF came from CAD, you must verify scale once in Illustrator.
If it is wrong, the fix always happens in CAD, not Illustrator.

Step 7.1 — Verify scale in Illustrator

Open your Illustrator file

Select the Measure Tool (hidden under the Eyedropper)

Measure a known distance (e.g. a 100′ baseline or a grid spacing)

Compare this to the expected real-world value

If the measurement matches → continue working.
If it does not match → stop and return to CAD.

Do not scale the Illustrator artwork to “make it fit.”

Step 7.2 — Return to CAD and locate the scale control

Scale errors almost always come from one of three places in CAD.
Check them in this order.

A. Confirm you are in Paper Space (Layout)

Click a Layout tab (not Model)

You should see:

a white sheet boundary

one or more rectangular viewports

If you plotted from Model Space, scale will almost always be wrong.

B. Activate the viewport (this is where the scale menu appears)

Double-click inside the viewport
(you are now viewing Model Space through the viewport)

Look at the Status Bar at the bottom of the CAD window

You should see a Viewport Scale dropdown that reads something like:

1" = 40'

1" = 20'

1:200

1:500

This is the scale control you want.

C. Set the viewport scale (do not zoom)

Click the Viewport Scale dropdown

Choose the correct scale for the drawing

Common examples:

Site plans: 1" = 40', 1" = 60'

Sections: 1" = 20'

Metric: 1:200, 1:500

⚠️ Important rules:

Do not zoom after setting scale

Use Pan only to position the drawing

Zooming changes the scale

D. Lock the viewport (non-negotiable)

Click the viewport boundary

Open the Properties panel

Set:

Display Locked = Yes

If you do not lock the viewport, scale will change accidentally.

Step 7.3 — Confirm Page Setup scale (final check)

Right-click the Layout tab → Page Setup Manager

Select the active page setup → Modify

Confirm:

Plot scale = 1:1

Plot area = Layout

If Page Setup scale is not 1:1, Illustrator scale will be wrong even if the viewport is correct.

Step 7.4 — Re-export the PDF

Run:

PLOT


Preview the plot

Export the PDF again using the same filename

Return to Illustrator. If the PDF was placed as a linked file, it will update automatically.

Step 7.5 — Re-verify in Illustrator

Repeat the Measure Tool check.
If the scale is still wrong, stop and re-check:

Viewport scale

Viewport lock

Page Setup scale

That you plotted from a Layout (not Model)

Only proceed once scale is correct.

Why this matters (for students)

If scale is wrong at this stage:

lineweights won’t read correctly

text sizes will feel off

diagrams will never feel “right”

Fixing scale upstream is always faster than compensating downstream.

---

## 8. Convert to editable vectors (only if needed)

If you need to edit individual lines:

1. Select the placed PDF
2. Object → **Flatten Transparency…**
   - Raster/Vector balance: favor Vector
   - Check “Convert All Text to Outlines” **only** if text is causing issues
3. Then:
   - Object → **Expand** (if available/necessary)

**Warning:** This can create lots of paths.  
Only do this when you truly need editable vectors.

---

## 9. Clean up the Illustrator file (high impact)

After expanding/flattening:

### A. Put linework into logical layers
Create top-level layers like:
- `00_BASE_REFERENCE` (locked)
- `01_LINEWORK_PRIMARY`
- `02_LINEWORK_SECONDARY`
- `03_CONTEXT_LIGHT`
- `04_FILL_COLOR`
- `05_LABELS`

### B. Reduce clutter
- Delete duplicate strokes
- Remove tiny fragments
- Use Select → Same → Stroke Color / Weight to batch-edit

### C. Establish hierarchy
- Primary edges heavier
- Background/context lighter
- Keep total number of stroke weights small (4–6)

**Checkpoint:** If everything looks equally important, hierarchy is not solved.

---

## 10. Common failures & fixes

### Problem: Lines missing in Illustrator
**Cause:** They were missing in the PDF.  
**Fix:** Return to CAD and check:
- Layer Plot = Yes
- viewport freeze states
- xref visibility
- plot preview

### Problem: Everything becomes thousands of fragments
**Cause:** Overly complex export and aggressive expand/flatten.  
**Fix:**
- Keep PDF linked and don’t expand unless necessary
- Simplify CAD before export (turn off unnecessary detail)

### Problem: Text is a mess
**Cause:** CAD text styles don’t translate cleanly.  
**Fix:**
- Delete CAD text; redo labels in Illustrator
- Or convert text to outlines during flattening (last resort)

### Problem: Wrong lineweights/hierarchy
**Cause:** CTB not applied or layer colors not intentional.  
**Fix:** Fix in CAD (layers + CTB), then re-export PDF.

---

## 11. Best practice for iteration (swap-PDF workflow)

If you used **Place with Link**:
- Update CAD
- Re-export PDF with the **same filename**
- In Illustrator: Window → Links → **Relink** (or it updates automatically)

Keep your Illustrator styling in separate layers above the base linework.

---

## 12. Final checkpoint

You should have:
- Correctly scaled linework
- Stable layer organization
- Clear hierarchy
- A workflow that supports iteration

If not, fix the CAD export first, then re-import.

---

## 13. What to do next

- Add atmospheric effects:
  → Photoshop guides

- Assemble boards:
  → InDesign guides

- If importing from Rhino instead:
  → Rhino ↔ Illustrator diagram guide
