# GUIDE_00_01 — Set Up Project Folders & File Naming

**Version:** v01.1  
**Audience:** Mixed ability  
**Last updated:** 2025-12-20  
**Applies to:** All software and all studios  
**Does not cover:** Any software-specific commands

---

## 1. What this does

This guide shows you how to set up a **clean, predictable project folder structure** and a **consistent file-naming system** so your work remains stable across GIS, modeling, drafting, and representation software.

This is not about aesthetics.  
This is about **not losing your work**.

---

## 2. When to use this

Use this guide:

- At the **start of every project**
- Before opening **any** software
- When files feel confusing or broken
- Before asking for technical help

If your folders are disorganized, **stop and do this first**.

---

## 3. What you need

- Your computer’s file system
- A project name
- Your last name

This guide applies **before** opening GIS, CAD, Rhino, Illustrator, Photoshop, or InDesign.

---

## 4. Ground rules (read once)

- Do **not** work from the Desktop
- Software does **not** manage files — you do
- Every file must have a clear purpose
- If you cannot explain a file name, it is wrong
- Never use “final” in a file name

This system is intentionally simple.

---

## 5. Step-by-step setup

### Step 1 — Create the project root folder

Create a folder named:

```
Studio_ProjectName_LastName
```

Example:

```
LA401_UrbanRiver_Garcia
```

This is your **project root**. Everything lives here.

---

### Step 2 — Create the required subfolders

Inside the project root, create **exactly these folders**:

```
/00_admin
/01_source
/02_exports
/03_refs
```

Do not rename them.

---

### Step 3 — Know what goes where

#### `/00_admin`
Use for:
- Assignment prompts
- Notes
- Screenshots for troubleshooting

This folder is for **humans**, not software.

---

#### `/01_source`
Use for **editable working files**:
- `.dwg` (CAD)
- `.3dm` (Rhino)
- `.qgz` (QGIS)
- `.ai`, `.psd`, `.indd`

Rule:  
If you open it and edit it, it lives here.

---

#### `/02_exports`
Use for:
- PDFs
- JPGs / PNGs
- Files you submit or pin up

Rule:  
Nothing in this folder should be edited.

---

#### `/03_refs`
Use for:
- GIS data
- Base drawings
- Images you did not create
- Downloaded reference files

Rule:  
If you didn’t make it, it goes here.

---

### Step 4 — Name files consistently

Use this format:

```
Project_DrawingType_LastName_YYYYMMDD.ext
```

Examples:

```
UrbanRiver_ContextMap_Garcia_20250312.pdf
UrbanRiver_TerrainModel_Garcia_20250318.3dm
UrbanRiver_SitePlan_Garcia_20250402.dwg
```

---

### Step 5 — Never overwrite without changing the date

If you revise a file:
- Update the date
- Save a new version

This creates version history **without extra software**.

---

## 6. Checkpoint

Someone else should be able to open your project folder and immediately understand:

- What the project is
- Where working files live
- What has been exported
- What is reference material

If not, fix it now.

---

## 7. Common failures & fixes

**Problem:** Files everywhere  
**Fix:** Move them into the four folders. Do not overthink it.

**Problem:** Multiple files named “final”  
**Fix:** Replace “final” with dates.

**Problem:** Missing links or broken imports  
**Fix:** Keep all files inside the project root.

**Problem:** You don’t know what a file is  
**Fix:** Rename it immediately.

---

## 8. What to do next

- Next:  
  → [Find and Evaluate Spatial Data for a Site (US)](../01_mapping/guide_gis_01_find_data.md)

- If files keep breaking:  
  → [Troubleshoot When Something Goes Wrong](guide_00_03_troubleshoot.md)

Folder structure is **workflow infrastructure**.  
Get it right once and everything else gets easier.
