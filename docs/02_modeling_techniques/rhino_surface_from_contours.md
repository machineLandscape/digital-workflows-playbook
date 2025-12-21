# Rhino Technique — Create a Terrain Surface from Contours

**Version:** v1.2  
**Tool:** Rhino  
**Layer:** Technique (Modeling)  
**Purpose:** Create a reliable base terrain surface suitable for sectioning and CAD export

---

## 1. When to use this technique

Use this guide when:
- You have **2D contour lines with correct elevations**
- You need a **continuous terrain surface**
- You plan to cut sections or export geometry downstream

Do **not** use this technique when:
- Contours are unverified or messy
- You need final grading geometry
- You only need 2D analysis

This creates a **base terrain surface**, not a finished landform.

---

## 2. Input requirements (non-negotiable)

Before running *any* surface command, verify **all** of the following.

### Geometry checks
- Contours are **polylines** (not loose segments)
- Each contour has **one Z elevation**
- No contours overlap or touch
- No duplicate curves (`SelDup`)
- Contours are reasonably spaced (no extreme clustering)

### Rhino environment checks
- Units are correct (`Units`)
- Geometry is near the origin
- File is saved before starting

> If any of these conditions fail, **stop and fix upstream**.  
> Rhino will not warn you — it will fail later.

---

## 3. Mandatory pre-inspection

1. Switch to **Shaded** view  
2. Rotate slightly in **Perspective**
3. Select several contours and confirm they step smoothly in Z

### Abort if:
- Contours jump vertically
- Curves cross in plan
- Multiple contours share the same elevation accidentally

Fix contours **before** surface creation.

---

## 4. Choose your surface method

| Condition | Method |
|--------|--------|
| GIS-derived or incomplete contours | **Patch** |
| Clean, survey-grade contours | **Drape** |
| Unsure | **Patch first** |

If Patch works, do **not** switch to Drape.

---

## 5. Method A — Patch (recommended default)

### Step 5.1 — Select input curves
- Select **only** contour curves
- Exclude boundaries, roads, spot grades, annotations

### Step 5.2 — Run the command
```
Patch
```

### Step 5.3 — Patch parameters (critical)

- **Sample point spacing**
  - Start **coarse**
  - Smaller values = heavier surface
- **Stiffness**
  - Start low (≈ 1–3)
  - High stiffness causes flattening and spikes

Leave advanced options unchanged.

### Step 5.4 — Preview inspection
Before clicking **OK**:
- Switch to **Perspective**
- Rotate the preview
- Look for spikes, pits, or folds

If problems appear:
- Click **Cancel**
- Reduce stiffness
- Retry

---

## 6. Method B — Drape (use carefully)

### Step 6.1 — Select contours
Same selection rules as Patch.

### Step 6.2 — Run the command
```
Drape
```

### Step 6.3 — Resolution control
- Too low → blocky surface
- Too high → unstable surface

Use the **lowest resolution that preserves form**.

### Step 6.4 — Immediate inspection
Immediately rotate in **Perspective**.
If spikes appear:
- Stop
- Fix contours
- Do **not** continue

---

## 7. Mandatory post-creation inspection

After any method:
- Orbit in **Perspective**
- Inspect for:
  - Vertical spikes
  - Pinched ridges
  - Sudden elevation jumps

If present → go to **Fix Spiky or Broken Terrain Surfaces**.

---

## 8. Rhino-specific failure patterns

| Symptom | Likely cause |
|------|------------|
| Fine in Top, broken in 3D | Bad Z-values |
| Sharp spikes | Crossing contours |
| Sections fail later | Surface too dense |

Do not work around these.

---

## 9. Create a clean checkpoint

Once acceptable:
1. Duplicate the surface
2. Lock one copy
3. Save a new file version

Never risk the clean base.

---

## 10. Downstream test (required)

Before proceeding:
```
Section
```

If section curves break or jump:
- The surface is **not ready**
- Fix now, not in CAD

---

## 11. What this surface is (and is not)

**Is:**
- Base terrain
- Section-ready
- Exportable

**Is not:**
- Final grading
- Construction geometry
- Something to endlessly tweak

---

## 12. Final checkpoint

You should now have:
- One continuous surface
- No visible spikes
- Clean test sections

If not, redo the surface. That is faster.

## Related techniques

- [Fix Spiky or Broken Terrain Surfaces](rhino_fix_spiky_surfaces.md)
- [Patch vs Drape (Decision Guide)](rhino_patch_vs_drape.md)
- [Prepare Terrain Surfaces for Sectioning](rhino_prepare_for_sectioning.md)

