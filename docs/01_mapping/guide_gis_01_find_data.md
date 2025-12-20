# GUIDE_GIS_01 — Find and Evaluate Spatial Data for a Site (US)

**Version:** v01.0  
**Audience:** Mixed ability  
**Last updated:** 2025-12-20  
**Primary workflow:** Mapping  
**Applies to:** United States contexts  

---

## 1. What this does

This guide shows you **where to find reliable spatial data** for a site in the United States and how to quickly judge whether that data is usable.

The goal is not completeness.  
The goal is **good-enough data for design work**.

---

## 2. When to use this

Use this guide:
- At the start of a project
- When a studio does not provide base data
- When you don’t know what data already exists

---

## 3. Core idea (read this)

**Good design data is boring, documented, and boring again.**

If a dataset:
- Has a source
- Has a date
- Has a projection

It is usually usable.

---

## 4. Start with authoritative sources

Always start here before searching randomly.

### Federal
- USGS (topography, elevation, hydrography)
- Census Bureau (boundaries, roads)
- USDA (soils)

### State
Search:
```
[State Name] GIS data
```

Most states maintain open GIS portals.

### County / City
Search:
```
[County or City Name] GIS open data
```

Local data is often the most detailed.

---

## 5. What datasets you usually need

At minimum:
- Roads
- Parcels
- Water bodies
- Elevation (contours or DEM)
- Municipal boundaries

You rarely need everything.

---

## 6. How to evaluate a dataset quickly

Check:
- **Date**: Is it recent enough?
- **Source**: Who published it?
- **Projection**: Is it projected (not geographic)?
- **Extent**: Does it cover your site?

If any of these are missing, be cautious.

---

## 7. Common failures & fixes

**Problem:** Data won’t align  
**Fix:** Projection mismatch. Reproject.

**Problem:** Data is overwhelming  
**Fix:** You downloaded too much. Clip later.

**Problem:** Data looks inaccurate  
**Fix:** Check date and scale.

---

## 8. What to do next

- Make a context map:  
  → [Create a GIS Context Map](guide_gis_02_context_map.md)

- Set up files first (if you haven’t):  
  → [Set Up Project Folders & File Naming](../00_getting_started/guide_00_01_folders.md)

Finding data is a skill. It gets faster with practice.
