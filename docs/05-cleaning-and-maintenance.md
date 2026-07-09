# 5. Cleaning and Maintenance

Current documented practice. The machine responds well to brief, frequent care; deferred maintenance manifests primarily as clogging and diameter instability.

## 5.1 Principle

An extruder barrel cannot practically be emptied; residual material is **displaced** by new material. Nearly all cleaning on this machine therefore takes the form of *purging*: running fresh material through the barrel until the output runs clean.

## 5.2 Purging between materials

Required for every change of polymer type (e.g., PLA → PETG); recommended after any run producing discolored or contaminated output.

Current procedure:

1. Complete the run with the barrel at operating temperature.
2. **Transition to a higher-temperature material** (PLA → PETG → ABS): raise the barrel to the *new* material's setpoint, then feed virgin pellets of the **new** material until the output strand is clean and exhibits only the new material's color and behavior.
3. **Transition to a lower-temperature material** (e.g., ABS → PLA): purge at the *old* material's setpoint first — residual high-temperature polymer will not melt at the new setpoint. Feed virgin pellets of the new material at the old temperature until output runs clean, then reduce to the new setpoint and purge briefly again.
4. Discard all purge output to general waste. Purge material is mixed-polymer and **must not** re-enter the feedstock stream.

Default purge medium when in doubt: inexpensive virgin PLA pellets.

## 5.3 Per-session tasks (approximately 2 minutes)

- Empty the hopper completely; residual granules absorb moisture and impede the next run.
- Brush the nozzle exterior with a brass brush **while warm** (gloves required) to remove drool and buildup.
- Clear filament fragments from the puller rollers and cooling zone.
- Wipe granules and dust from the machine and work surface.

## 5.4 Weekly / every ~10 sessions

Perform with the machine **cold and unplugged** where inspection involves wiring:

- Inspect band heater wiring and thermistor leads for damage or looseness.
- Inspect puller roller surfaces for plastic buildup; clean to restore even grip.
- Confirm the cooling fan rotates freely and is free of dust.
- Inspect the hopper mounting and all printed structural parts for heat deformation or cracking. Printed parts adjacent to the heated zone are the machine's consumable components; log and replace as required.
- Check fasteners near the motor and barrel for vibration loosening.

## 5.5 Periodic / condition-based tasks

- **Thermistor drift check.** Displayed and actual barrel temperatures can diverge over time. If a previously verified setpoint begins producing different behavior, suspect the sensor before revising the setpoint.
- **Severe clog recovery.** If the motor stalls at full operating temperature, do not apply force. Heat-soak at the upper end of the stuck material's range for 10–15 minutes, attempt slow extrusion, and purge. Barrel disassembly is a last resort; if performed, document the procedure fully so a repeatable method exists for future incidents.
- **Spares.** Maintain printed spares for known wear components. (Print spares from your own licensed copy of the design files; this repository does not and cannot supply them.)

## 5.6 Maintenance records

Every non-routine intervention — clog clearance, part replacement, wiring repair — is recorded in the [Experiment Log](07-experiment-log.md) or as a GitHub issue: the fault, the corrective action taken, and any recommended changes to procedure.

---

*Where a documented method proves inferior to a tested alternative, replace it, citing the supporting evidence.*
