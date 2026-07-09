# 4. Operating Procedure

Complete operating sequence from cold machine to spooled filament. This is the currently documented optimal procedure; refinements are adopted through the standard contribution process.

**Prerequisites:** [Safety](02-safety.md) has been read in full; feedstock is sorted, granulated, dried, and blended per [Materials and Temperature Settings](03-materials-and-temperatures.md).

## 4.1 Pre-operation checklist

- [ ] Ventilation active (mandatory for ABS; standard practice for all materials)
- [ ] Heat-resistant gloves and pliers/tweezers within reach
- [ ] Hopper and barrel confirmed free of foreign or incompatible material (if uncertain, purge per [Cleaning and Maintenance](05-cleaning-and-maintenance.md))
- [ ] Empty spool staged at the puller outlet
- [ ] Session log opened: operator, date, material, blend ratio
- [ ] Operator will remain present for the full run — **the machine is never left running unattended**

## 4.2 Startup sequence

1. **Energize the machine** at the power supply. Do not start the drive motor.
2. **Set the barrel temperature** on the PID controller per the current verified value for the material ([section 3.3](03-materials-and-temperatures.md)).
3. **Allow full heat soak.** After the PID display reaches setpoint, wait an additional **5 minutes** for the barrel interior to equalize. Extruding into a partially soaked barrel is the most common cause of a stalled first run.

## 4.3 Production run

4. **Load the hopper** with prepared feedstock. Do not overfill; a hopper at approximately two-thirds capacity feeds more reliably than a full one.
5. **Start the drive motor** at low speed and increase gradually. A smooth, even motor note indicates normal operation; straining or clicking indicates insufficient temperature or excessive screw speed.
6. **Allow extrusion to stabilize.** Initial output is typically discolored or inconsistent (residual and heat-soaked material). Extrude and discard the first 30–60 cm.
7. **Capture the strand with pliers** — never by hand; it is molten — and guide it through the cooling airflow to the puller.
8. **Feed the strand into the puller rollers** and start the puller at low speed.
9. **Tune puller speed to the target diameter**, measuring with calipers or the dial indicator:
   - Diameter above target → increase puller speed incrementally.
   - Diameter below target → decrease puller speed incrementally.
   - Make small adjustments and allow several seconds of lag before evaluating the effect at the measurement point.
10. **Begin spooling** once diameter is stable. Maintain light, even winding tension. Re-check diameter periodically during the run and replenish the hopper before it empties to avoid flow interruption.

## 4.4 Shutdown sequence

The objective of a correct shutdown is a clean, predictable startup for the next operator. The order of steps matters.

1. **Stop feeding material** and allow the barrel to run until output slows, minimizing the quantity of material left to degrade in the barrel.
2. **Purge if a material change is expected next** (recommended) — see [Cleaning and Maintenance](05-cleaning-and-maintenance.md).
3. **Stop the drive motor and puller.**
4. **Set the heater setpoint to zero / heaters off.**
5. **Allow the machine to cool completely** before covering, relocating, or cleaning it. Burn-hazard temperatures persist for 30 minutes or more.
6. **De-energize at the power supply.**
7. **Complete the session log:** material, temperature, screw and puller settings, measured diameter, meters produced, and any anomalies. A complete log entry routinely saves the next operator a full re-tuning cycle.

## 4.5 Output acceptance criteria

Before a spool is placed in usable stock, verify it against the current acceptance standard:

| Check | Acceptance criterion |
|-------|----------------------|
| Diameter | 1.75 ± 0.05 mm at a minimum of 5 sample points |
| Surface | Smooth and continuous; no bubbles, lumps, or rough sections |
| Brittleness | A 20 cm length bends around a finger without fracturing (PLA is stiffer but must not shatter) |
| Test print | A small calibration print completes without under-extrusion or jamming |

Spools failing any criterion are labeled accordingly and routed to the re-recycle bin; rejected filament re-enters the process as feedstock.

---

*A step that consistently causes difficulty is a documentation defect. Report or correct it.*
