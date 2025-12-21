# CAD Technique — Layer Properties Manager (Linework Control)

**Version:** v1.1  
**Use when:** lineweights don't behave, drawings lack hierarchy, or plotting is inconsistent.  
**Applies to:** AutoCAD-based workflows (AutoCAD, Civil 3D)  
**Last updated:** 2025-12-21

---

## 1. What this technique does

This guide teaches how to use **Layer Properties Manager** to control:
- what is visible
- what is editable
- what prints heavy vs light (via color → CTB mapping)
- drafting discipline (ByLayer settings)

**Most plotting problems start here.**

---

## 2. Core idea (read this)

In a standard CTB workflow:

**Layer Properties Manager assigns colors → Plot Style Table converts colors into lineweights → Page Setup outputs a PDF.**

If layers are wrong, plot styles can't save you.

---

## 3. Open Layer Properties Manager

Use any of these:
- Command: `LAYER`
- Home tab → Layers panel → Layer Properties
- Type `LA` (alias in many setups)

You should see a list of layers with columns for **On/Off, Freeze, Lock, Color, Linetype, Lineweight, Plot**.

---

## 4. Establish layer roles

A layer name should communicate purpose. Typical landscape roles:

- `A-CUT` (cut / poche / section cut)
- `A-EDGE` (primary edges)
- `A-LINE` (secondary linework)
- `A-CONTEXT` (roads, parcels, background)
- `A-ANNO` (text, dims, leaders)
- `A-HATCH` (hatches, poche fills)
- `A-REF` (xref / underlay)

**Rule:** Do not draft everything on one layer.

---

## 5. Set ByLayer defaults (non-negotiable)

For each layer, set:
- **Color:** specific (not "ByLayer"—layers *are* the source of truth)
- **Linetype:** Continuous unless you need dashed/center
- **Lineweight:** **ByLayer**
- Objects: set to **ByLayer** (not overrides)

### Quick cleanup for objects
- Select objects → Properties
- Set Color = ByLayer, Linetype = ByLayer, Lineweight = ByLayer

**Abort condition:** If students override object colors, CTB logic breaks.

---

## 6. Assign color intentionally for hierarchy

In a CTB workflow, color is not aesthetic; it is a **lineweight code**.

Example hierarchy mapping (you will match this to CTB later):
- Cut: Color 8 or 30 (heavy)
- Primary: Color 9 (medium-heavy)
- Secondary: Color 4 (medium)
- Background/context: Color 2 (light)
- Reference: Color 253/254 (very light)

**Checkpoint:** You should be able to predict hierarchy on paper based on layer color choices.

---

## 7. Freeze/Lock/Isolate strategically

Use:
- **Freeze** layers to improve performance and reduce noise
- **Lock** layers to prevent accidental edits
- **Isolate** (right-click) when working on one system at a time

**Tip:** Lock xrefs and base data (survey, GIS xref) early.

---

## 8. Plot column (yes/no)

Ensure critical layers have **Plot = Yes**.
For guide layers, construction layers, or reference:
- Plot = No

**Common failure:** A student turns Plot off on a key layer and thinks the CTB is broken.

---

## 9. Common failures & fixes

**Problem:** Everything prints the same weight  
**Cause:** Too many layers share one color OR objects are overridden (not ByLayer).

**Problem:** Some lines won't change weight  
**Cause:** Object-level overrides or blocks with internal colors.

**Fix:** Explode only if necessary; otherwise use `BEDIT` and enforce ByLayer.

**Problem:** Some things disappear in PDF  
**Cause:** Layer Plot = No, or layer is frozen in the layout, or viewport layer freeze.

---

## 10. Checkpoint

Before moving to plot styles:
- Layers are named and purposeful
- Objects are ByLayer
- Colors encode hierarchy
- Plot column is correct

Next:
- [Plot Style Tables (CTB/STB) in Detail](cad_plot_style_tables.md)
- 
## Linked video tutorials (optional)

For visual reinforcement of the steps above, see the  
[Curated Video Tutorial Index](../video_index.md).
