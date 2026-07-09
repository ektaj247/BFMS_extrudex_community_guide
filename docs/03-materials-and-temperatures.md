# 3. Materials and Temperature Settings

The values in this document are the **current best-known settings for this specific machine**, refined through logged use. They are working values, not fixed specifications: individual builds, thermistor placement, and material batches all vary. Superior values, once demonstrated, replace the values here via pull request, with supporting evidence recorded in the [Experiment Log](07-experiment-log.md).

## 3.1 Supported materials

The machine processes common FDM thermoplastics, **one polymer type at a time**:

| Material | Supported | Notes |
|----------|-----------|-------|
| PLA | Yes | Lowest processing temperature and mildest emissions. Recommended material for training runs. |
| PETG | Yes | Higher melt tack; requires disciplined cooling and moisture control. |
| ABS | Yes | **Ventilation mandatory** — emissions contain styrene. |
| Mixed or unidentified plastics | No | Incompatible melt temperatures; contaminates the barrel. |
| TPU / flexible filaments | Untested | Not yet attempted on this machine. Trials should be logged. |
| Filled composites (wood, carbon fiber) | Not recommended | Abrasive fill accelerates barrel and nozzle wear; fibers promote clogging. |

**Segregation begins at the waste bin.** Maintain a separate, labeled waste container per polymer *before* shredding. Once granulated, mixed material cannot practically be re-sorted.

## 3.2 Feedstock preparation

1. **Granulation.** Shred failed prints, supports, and purge waste into small granules of uniform size, comparable to virgin pellets. Input uniformity is the single largest factor in extrusion stability. Scissors are adequate for thin waste; a shredder (or a dedicated, sacrificial blender) is required for bulk parts.
2. **Drying.** Moist feedstock extrudes with bubbles and audible popping, yielding brittle, dimensionally inconsistent filament. PETG and ABS are particularly hygroscopic. Current practice: dry granulated material as filament would be dried (filament dryer or low-temperature oven) if it has been exposed to ambient air for more than a few days.
3. **Blending.** Current recommended composition: **60% virgin pellets / 40% granulated waste, by weight**. Runs at up to 100% recycled content are feasible with reduced consistency; results are recorded in the Experiment Log.

## 3.3 Barrel temperature — current verified values

**Verification standard:** a value is marked *verified* only when an operator has produced usable filament at that setting on this machine and logged the run. Unverified entries are literature-derived starting ranges; when re-tuning, begin at the low end and increase in 5 °C increments.

| Material | Current verified setpoint | Starting range for tuning | Verified | Last updated by |
|----------|---------------------------|---------------------------|----------|-----------------|
| PLA | TBD — pending first tuned run | 160–190 °C | No | — |
| PETG | TBD | 200–230 °C | No | — |
| ABS | TBD | 220–250 °C | No | — |

**Note on setpoints vs. printing temperatures:** barrel extrusion at low screw speeds generally requires a *lower* temperature than the printing temperature stated on a filament spool. Residence time in the melt zone is far longer here than in a printer hotend; excessive temperature degrades the polymer (discoloration, burnt odor, brittle output).

## 3.4 Temperature tuning procedure

1. Set the barrel to the **low end** of the range for the material.
2. Run a small batch and observe the strand at the nozzle:
   - **Under-temperature:** motor strain, stalling, or a rough, matte strand with visible unmelted particles → increase by 5 °C.
   - **Over-temperature:** low-viscosity strand that sags immediately, discoloration, or burnt odor → decrease by 5 °C.
   - **Correct:** a steady, glossy, continuous strand that the puller holds at consistent diameter.
3. Once stable, record material, blend ratio, temperature, screw speed, puller speed, ambient temperature, and measured diameter range in the Experiment Log, then update the table in section 3.3 in the same pull request.

## 3.5 Diameter specification

- Target: **1.75 mm ± 0.05 mm** for reliable feeding in most printers.
- Filament within ± 0.10 mm is generally printable with some flow inconsistency.
- Measurement: calipers at multiple points over several meters, or the dial-indicator mount for continuous readings.

---

*Where a value in this document conflicts with logged results, the results take precedence and the document is to be updated.*
