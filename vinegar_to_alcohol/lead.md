## Electrochemical Reduction of Acetic Acid to Ethanol

### The Half-Reactions

**Cathode (target):**
```
CH₃COOH + 4H⁺ + 4e⁻ → CH₃CH₂OH + H₂O   (E° ≈ +0.13 V vs SHE)
```
**Anode (water oxidation):**
```
2H₂O → O₂ + 4H⁺ + 4e⁻   (E° = +1.23 V vs SHE)
```
**Cell voltage needed:** ~1.1 V thermodynamic minimum, realistically **2.5–4 V** due to overpotential and HER competition.

---

### Recommended Cell Architecture

**Divided H-cell** is strongly recommended — prevents anodic re-oxidation of product.

```
  [CATHODE COMPARTMENT]  |  [ANODE COMPARTMENT]
                         |
  Vinegar + Na₂SO₄      |  Dilute H₂SO₄ or same
  (acidic, pH 2–3)       |  electrolyte
                         |
  Pb or Sn plate         |  Graphite rod
                         |
         [Nafion 117 membrane or dense porous frit]
```

---

### Component Recommendations (Cost + Resilience Priority)

| Component | Recommendation | Rationale |
|---|---|---|
| **Cathode** | **Lead (Pb) sheet** | Cheapest material with partial selectivity for organic reduction over H₂ evolution; tolerates acidic impurity-laden solutions |
| **Anode** | **Graphite rod/plate** | Inert, cheap, handles oxidative environment; degrades slowly but acceptable |
| **Separator** | **Nafion 117** (preferred) or dense glass frit | Nafion survives acetic acid well; glass frit is cheaper but allows more cross-diffusion |
| **Electrolyte** | **0.5–1 M Na₂SO₄** added to vinegar | Boosts conductivity without introducing problematic ions; sulfate is inert |
| **Power supply** | Benchtop CC/CV supply, ~0–6V / 0–5A | Need cathodic potential of −1.8 to −2.5 V vs Ag/AgCl |
| **Reference** | Ag/AgCl (optional but useful) | Lets you log and control cathode potential precisely |

> **Why Lead over Copper or Indium?**  
> Copper gives better CO₂ reduction but is poor for carboxylic acid reduction and forms oxides readily. Indium is more selective but expensive. Lead's high hydrogen overpotential (−1.2 V vs SHE) suppresses parasitic H₂ evolution, favoring organic reduction in acidic media. It's also nearly immune to the organic impurities in real vinegar.

---

### Operating Parameters

| Parameter | Value |
|---|---|
| Cathodic potential | −1.8 to −2.5 V vs Ag/AgCl |
| Cell voltage | 3–5 V applied |
| Current density | 5–20 mA/cm² (start low) |
| pH | 2–4 (vinegar as-is is fine) |
| Temperature | Room temp; cooling if running >1h |
| Stirring | Magnetic stirrer on cathode side |

---

### Practical Notes

**Main competing reaction** is H₂ evolution — you will always get some. Detection of product ethanol requires GC or at minimum careful distillation + smell/density check.

**Faradaic efficiency** for this reaction with Pb cathodes is typically 5–25% in literature — not impressive, but the question is whether *any* ethanol accumulates over long runs, which it can.

**Scaling**: Run in **batch mode** with recirculation (pump cathode solution through a larger reservoir) rather than making a large cell — easier to control, easier to analyze samples.

**Impurity resilience**: Lead + graphite + sulfate electrolyte is one of the most forgiving combinations you can build. Commercial vinegar with colorants, preservatives, or metal traces won't kill the electrodes.

---

### Minimum Bill of Materials

- 1× glass H-cell (DIY from two mason jars + rubber stopper + glass tube works)
- Nafion 117 membrane (small piece, ~€5–15 on eBay)
- Lead sheet, 2–5 mm thick (roofing lead, plumbing supply)
- Graphite rod (electrode-grade or even pencil-grade carbon block)
- Na₂SO₄ (anhydrous, food/lab grade)
- DC bench supply with voltage/current display
- Optional: Ag/AgCl reference electrode

This is a genuinely non-trivial reduction to run efficiently, but as an experimental reactor to demonstrate the *principle* and collect measurable ethanol, it's quite achievable with this setup.
