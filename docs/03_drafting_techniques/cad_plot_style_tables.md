# CAD Technique — Plot Style Tables (CTB / STB) in Detail

**Use when:** lineweights are wrong, colors plot incorrectly, or PDFs look faint.  
**Applies to:** AutoCAD-based workflows

---

## What this technique covers

This guide explains **plot style tables** in detail:
- What CTB and STB are
- How they control lineweight and color
- How to choose and edit them safely

This is the heart of CAD plotting.

---

## How Plot Styles connect to layers (critical)

Plot style tables do **not** act directly on objects.

They act on:
- **Layer color assignments**
- **Object color overrides**

In a CTB workflow:
1. Layer Properties Manager assigns a color to a layer
2. The CTB file converts that color into a lineweight
3. The PDF reflects the CTB, not the on-screen color

If layers are not assigned intentionally, plot styles cannot work.

---

## CTB vs STB (understand this first)

### CTB — Color-Based Plot Styles
- Lineweight tied to color
- Most common in architecture and landscape
- Simple and predictable

### STB — Named Plot Styles
- Lineweight tied to style names
- More flexible
- Less common in school settings

**Rule of thumb:**  
If you didn’t choose STB intentionally, you are using CTB.

---

## How CTB works

In CTB:
- Each color = specific lineweight
- Colors may plot black or gray
- Screen color ≠ printed weight

Example:
- Color 8 → 0.50 mm
- Color 9 → 0.35 mm

This is why color discipline matters.

---

## Step-by-step: Editing a CTB

1. Open **Plot Style Manager**
2. Open the `.ctb` file you are using
3. Select a color
4. Set:
   - Lineweight
   - Screening (100% recommended)
   - Plot color (usually black)

Save changes deliberately.

---

## Best-practice lineweight ranges

Typical landscape ranges:
- Cut lines: 0.50–0.70 mm
- Primary edges: 0.30–0.40 mm
- Secondary context: 0.18–0.25 mm
- Background: 0.13 mm

More variation ≠ better.

---

## Common failures

**Problem:** Everything plots the same weight  
**Cause:** All objects on same color

**Problem:** Lines look faint  
**Cause:** Screening < 100%

**Problem:** Colors plot in color  
**Cause:** Plot color not set to black

---

## How to work safely

- Never edit a shared CTB without copying it
- Name CTBs clearly
- Keep one “standard” CTB per studio

Plot styles are standards, not experiments.

---

## Checkpoint

You should:
- Know which CTB you’re using
- Understand what each color does
- Trust your plotted output

If not, stop and fix the CTB.
