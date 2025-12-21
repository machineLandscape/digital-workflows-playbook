# CAD Technique — Viewports & Scale That Actually Work

**Version:** v1.1  
**Use when:** PDFs plot at the wrong scale, annotations behave strangely, or viewports keep changing.  
**Applies to:** AutoCAD-based workflows  
**Last updated:** 2025-12-21

---

## 1. What this technique does

This guide teaches the standard, repeatable model-space / paper-space workflow:
- model space = real-world geometry at 1:1
- paper space = viewports + sheet composition
- viewport scale = the only place you scale the drawing

---

## 2. Core idea (read this)

**Never scale geometry in model space.**  
Scale belongs to viewports.

If your drawing scale is wrong, do not fix it in Illustrator. Fix it here.

---

## 3. Clean setup assumptions

This assumes:
- geometry drawn at real size in model space
- a layout (paper space) exists
- you are plotting from the layout

If you are plotting from model space, stop and switch to a layout workflow.

---

## 4. Step-by-step workflow

### Step 4.1 — Create/enter a layout
- Click a Layout tab (Paper Space)
- Ensure you see the paper boundary

### Step 4.2 — Create a viewport
Command:
```
MVIEW
```
- Draw a rectangle where the drawing should appear

### Step 4.3 — Activate the viewport
- Double-click inside the viewport (you are now in model space *through* the viewport)

### Step 4.4 — Set the viewport scale
Use either:
- status bar viewport scale dropdown, or
- properties panel for the viewport

Typical scales (examples):
- 1"=20', 1"=40', 1"=60'
- 1:200, 1:500

**Checkpoint:** After setting scale, pan to the correct location (do not zoom).

### Step 4.5 — Lock the viewport (non-negotiable)
Select the viewport border → Properties → **Display Locked = Yes**

If you don't lock it, it will change accidentally.

---

## 5. Annotation behavior (why this matters)

Two common approaches:

### A. Annotative text/dims (advanced)
- allows multiple scales
- requires discipline

### B. Non-annotative (simpler)
- set text size appropriate to plot scale

If your class is mixed-skill, keep it simple: consistent text size per scale.

---

## 6. Troubleshooting scale (fast tests)

### Test 1: Measure in PDF
Plot a PDF and measure a known distance. If wrong:
- check viewport scale
- check page setup plot scale is 1:1
- ensure you plotted the layout

### Test 2: Viewport unlocked
If things keep shifting:
- confirm Display Locked = Yes

### Test 3: Geometry not at real size
If scale never matches:
- someone scaled objects in model space
- fix by rescaling to real-world units

---

## 7. Common failures & fixes

**Problem:** Each viewport is a different scale accidentally  
**Fix:** Lock viewports and set scale intentionally.

**Problem:** Annotations are tiny/huge  
**Fix:** Choose consistent text height strategy; avoid mixing annotative/non-annotative.

**Problem:** Plot scale changes output  
**Fix:** Page Setup must remain 1:1; only viewport scale should change.

---

## 8. Checkpoint

You should be able to:
- state the viewport scale
- measure correct distances in PDF
- plot repeatedly without changes

Next:
- [Page Setup Manager (Step-by-Step)](cad_page_setup_manager.md)

- ## Linked video tutorials (optional)

For visual reinforcement of the steps above, see the  
[Curated Video Tutorial Index](../video_index.md).
