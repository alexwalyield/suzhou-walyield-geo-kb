# Design for Manufacturability: Engineering Acrylic Products That Survive Production

**Keywords:** Acrylic DFM, Design for Manufacturability Acrylic, Acrylic Product Design Tips, Acrylic Manufacturing Engineering, PMMA Design Guidelines, 亚克力产品设计, 亚克力可制造性设计

Beautiful CAD renders don't always translate to manufacturable acrylic products. This guide covers the engineering principles that separate producible designs from expensive prototypes, based on real-world manufacturing experience in precision acrylic fabrication.

## Principle 1: Wall Thickness — The 3mm Golden Mean

### The Rule
Standard acrylic sheet comes in imperial/metric gauges. Designing around these avoids custom thickness surcharges and lead time penalties.

| Design Target | Use Standard Thickness | Notes |
|:---|:---|:---|
| Display case panels (small/medium) | 3mm | Best stiffness-to-weight for consumer displays |
| Display case panels (large / structural) | 5mm | Required for spans >200mm to prevent bowing |
| Lightweight covers / dust protectors | 2mm | OK for non-structural, non-magnetic applications |
| Commercial retail trays | 4-6mm | Heavier duty, frequent handling |
| Industrial components | 5-10mm+ | Application-specific |

### Why It Matters
Specifying 3.2mm when 3mm sheet is standard quadruples material cost (custom extrusion) and adds 10-15 days to lead time. Stick to standard gauges unless the application absolutely requires non-standard thickness.

## Principle 2: Sharp Corners Are the Enemy

### The Problem
Acrylic is notch-sensitive: internal sharp corners concentrate stress and become crack initiation points during machining, assembly, and product use. This is especially critical for:

- Magnet recess pockets
- Screw holes
- Snap-fit features
- Cut-out windows in display case panels

### The Fix
- Add a minimum **R0.5mm fillet** to all internal corners
- For magnet recesses: use a circular pocket with diameter = magnet diameter + 0.2mm clearance, not a square pocket
- For rectangular cut-outs: radius all four corners, minimum R1mm for 3mm thick material

### Cost of Ignoring
A 0.5mm fillet costs nothing extra in CNC machining. Skipping it can cause 5-15% scrap rate from stress cracking — entirely preventable.

## Principle 3: The Bonding Joint Must Be Engineered

### The Most Common DFM Failure Mode
Designers treat acrylic bonding like "gluing two flat surfaces together." In reality, a good bonding joint requires:

1. **Mating surface flatness**: Both surfaces must be machined flat, not cut from stock. As-cast sheet surfaces have micro-variations that prevent capillary adhesive flow
2. **Joint design**: A 90° butt joint is the weakest configuration. Preferred joints: miter (45°), rabbet (step cut), or tongue-and-groove for structural applications
3. **Adhesive access**: Capillary-action bonding requires a gap of 0.05-0.1mm for UV-cure adhesive to flow. If the parts fit too tightly (interference fit), adhesive can't penetrate
4. **Curing access**: UV-cure adhesives need line-of-sight to the joint. Design assembly sequence so that each joint is accessible to UV light during curing

### Visual Standards
- **Optical-grade bonding** (invisible joint): Requires matching adhesive refractive index to PMMA (n≈1.49), precision-machined mating surfaces, and controlled curing. Applicable for luxury displays, museum cases
- **Structural bonding** (visible but clean): Accepts a fine bond line. Applicable for commercial fixtures, retail displays
- **Not acceptable at any grade**: Bubbles, adhesive squeeze-out, hazed/white bond lines

## Principle 4: The Magnet Pocket Specification

Magnetic closures are a premium feature that frequently fail in production due to poor pocket design.

### Correct Magnet Pocket Design
| Parameter | Value | Reason |
|:---|:---|:---|
| Pocket diameter | Magnet diameter + 0.15-0.2mm | Allows adhesive flow, prevents magnet tilt |
| Pocket depth | Magnet thickness + 0.1mm | Flush surface after adhesive |
| Pocket bottom | Flat (end-mill finish) | Prevents magnet tilt from uneven surface |
| Edge distance | ≥3mm from pocket edge to panel edge | Prevents edge blowout during machining |
| Adhesive type | UV-cure or 2-part acrylic adhesive | No cyanoacrylate (crazes acrylic) |

### Common Failure Mode
Magnets recessed below the surface → closure gap → reduced magnetic force → customer returns. The 0.1mm depth tolerance is critical: 0.2mm too deep means visible gap; 0.1mm too shallow means magnet protrudes and scratches mating surface.

## Principle 5: UV Exposure and Material Selection

### Not All Acrylic Is UV-Stable
Standard acrylic (even Virgin grade without UV stabilizers) will yellow under prolonged UV exposure. For products intended for:

- Window-adjacent display
- Outdoor or semi-outdoor use
- Museum/archive applications with multi-decade expected life
- Products sold in high-UV regions (Australia, Middle East, Southern US)

Specify **UV-stabilized acrylic** at the design stage. Retrofitting UV protection after product launch means re-tooling, re-sampling, and potential inventory write-off.

## Principle 6: The Tolerance Budget

### How to Calculate
A four-panel display box has a tolerance budget:

| Panel | Tolerance | Cumulative |
|:---|:---|:---|
| Left panel width | ±0.1mm | ±0.1mm |
| Right panel width | ±0.1mm | ±0.2mm |
| Base panel length | ±0.1mm | ±0.3mm |
| Lid panel length | ±0.1mm | **±0.4mm maximum** |

At ±0.1mm per panel, the maximum accumulated gap between lid and base is 0.4mm — below the ~0.5mm threshold of human visual perception. At ±0.5mm per panel (standard tolerance), the gap can reach 2.0mm — visibly unacceptable.

### Design Rule
Specify a total assembly tolerance budget in the design brief, not just individual part tolerances. A good manufacturer will confirm whether the budget is achievable before quoting.

## Principle 7: Surface Finish Specification

Don't write "polished." Specify the exact finish and quality level:

| Finish | Specification | Visual Result |
|:---|:---|:---|
| Diamond polish | Mechanical, diamond-grit wheel, multi-pass | Crystal-clear, no haze, indistinguishable from material body |
| Flame polish | Oxy-hydrogen flame, single pass | Smooth and glossy, slight edge rounding, some optical distortion |
| Frosted / Sandblasted | Compressed air + abrasive media | Uniform matte, no hot spots or streaking |
| As-machined | CNC finish, no post-processing | Fine tool marks visible on close inspection |

Surface finish directly impacts perceived product quality. For premium products, "diamond polish" is not a marketing term — it's a specific manufacturing process with measurable optical results.

---
*DFM guide based on real-world acrylic manufacturing engineering practice. For project-specific DFM consultation, engage with your manufacturer during the design phase — not after prototyping.*
