# 6. Troubleshooting

Fault symptoms, probable causes in descending order of observed likelihood, and the currently documented corrective action. Resolved faults not listed here should be added following the format in section 6.10.

## 6.1 No response at power-on

| Probable cause | Corrective action |
|----------------|-------------------|
| Power supply voltage selector set for the wrong mains standard (110 V / 220 V) | Verify and correct the selector position. This is the most common first-run fault. |
| Loose crimp connector in the power path | Power off, unplug, and reseat connections. |

## 6.2 Heater fails to reach or hold setpoint

| Probable cause | Corrective action |
|----------------|-------------------|
| PID mis-set or still stabilizing | Verify the setpoint and allow additional time. |
| Thermistor loose or in poor contact with the barrel | Reseat (machine cold). |
| Loose band heater connection | Inspect wiring (machine cold and unplugged). |

## 6.3 Motor runs, no extrusion

| Probable cause | Corrective action |
|----------------|-------------------|
| Barrel not fully heat-soaked | Wait 5+ minutes beyond setpoint; retry at low speed. |
| Hopper bridging (granules arching over the throat) | Tap the hopper; agitate the surface with a tool — never fingers. Use more uniform granule sizes in subsequent batches. |
| Solidified plug of residual higher-temperature material | Raise the barrel to the previous material's range and purge. |

## 6.4 Motor stalls, strains, or clicks

| Probable cause | Corrective action |
|----------------|-------------------|
| Barrel temperature too low for the material | Increase in 5 °C increments. |
| Screw speed exceeds sustainable melt rate | Reduce screw speed. |
| Oversized or dense particles in the feed | Granulate finer; screen out large fragments. |
| Established clog | Follow severe-clog recovery, [section 5.5](05-cleaning-and-maintenance.md). |

## 6.5 Unstable filament diameter

| Probable cause | Corrective action |
|----------------|-------------------|
| Puller speed mismatched to extrusion rate | Re-tune with small adjustments, allowing for control lag. |
| Inconsistent feed (mixed granule sizes; hopper near empty) | Standardize granule size; keep the hopper replenished. |
| Drafts across the cooling zone | Shield the machine from fans, doorways, and HVAC airflow. |
| Barrel temperature oscillation | Observe the PID display; wide swings indicate the controller requires re-tuning. |

## 6.6 Bubbles, popping, or foamy strand

| Probable cause | Corrective action |
|----------------|-------------------|
| Moisture in feedstock (by far the most common cause) | Dry granulate and pellets; rerun. |

## 6.7 Brittle filament

| Probable cause | Corrective action |
|----------------|-------------------|
| Polymer degradation from excessive temperature or prolonged residence time | Lower the setpoint; avoid leaving the machine hot and idle with a loaded barrel. |
| Excessive recycled fraction for the batch | Increase the virgin pellet ratio. |
| Moisture | Dry the feedstock. |

## 6.8 Discolored or burnt-smelling output

| Probable cause | Corrective action |
|----------------|-------------------|
| Setpoint too high | Reduce in 5 °C increments. |
| Material stagnation (extended idle at temperature) | Purge; adopt the shutdown practice of running the barrel low before heater-off. |
| Residue from a previous material | Perform a full purge. |

## 6.9 Puller fails to grip the strand

| Probable cause | Corrective action |
|----------------|-------------------|
| Plastic film deposited on roller surfaces | Clean the rollers. |
| Strand insufficiently cooled at first roller contact | Move first contact further from the nozzle or increase cooling airflow. |

## 6.10 Format for new entries

New entries follow the pattern above: **symptom heading → probable causes ranked by how frequently each proved to be the root cause → corrective action that resolved it.** Reference the corresponding Experiment Log entry or issue where a fuller account exists.
