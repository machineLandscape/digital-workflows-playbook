# Rhino Technique — Patch vs Drape (Decision + Parameters)
**Version:** v1.1  
**Tool:** Rhino  
**Scope:** Decision support and parameter guidance  

---

## 1. The real choice

You are choosing between:
- **Forgiveness (Patch)**
- **Precision (Drape)**

This is about data quality, not preference.

---

## 2. Use Patch when

- Contours are incomplete
- Site is large
- You expect revisions
- Input data is imperfect

### Key parameters
- **Stiffness:** low to medium
- **Sample spacing:** start coarse

Patch smooths aggressively — use restraint.

---

## 3. Use Drape when

- Contours are clean and complete
- Elevation logic is clear
- You want predictable structure

### Key parameters
- **Resolution:** lowest acceptable
- Avoid over-refinement

Drape assumes discipline.

---

## 4. Common failures explained

**Spikes after Drape:**  
Contours too close or crossing

**Over-smoothed Patch:**  
Stiffness too high

**Heavy surfaces:**  
Resolution too fine

---

## 5. Rule of thumb

If you asked “Which should I use?”  
Use **Patch first**.

Switch only if necessary.

---

## 6. Validation step

After either method:
- Rotate in perspective
- Cut a test section

If it fails, stop and reassess input curves.
