# 7. Experiment Log

Structured record of production runs, trials, and interventions. Every verified setting elsewhere in this repository must be traceable to an entry in this log. Entries are ordered newest first.

## 7.1 Logging standard

A full entry is required for any session producing a result of record: a verified setting, a rejected batch, a fault and its resolution, or a new technique. Routine runs at established settings may be recorded as a single line.

Entry template:

```markdown
### YYYY-MM-DD — <Material> — <one-line outcome>

- **Operator:**
- **Material and source:** (e.g., PLA — failed prints, single brand, mixed white/grey)
- **Blend ratio:** (e.g., 60/40 virgin/waste by weight)
- **Feedstock preparation:** (granulation method, particle size, drying method if any)
- **Barrel setpoint:** (PID value)
- **Screw speed:** (controller setting)
- **Puller speed:** (controller setting)
- **Ambient conditions:** (approximate room temperature, drafts, ventilation)
- **Measured diameter:** (min / max / typical over the run)
- **Output quality:** (surface finish, brittleness, test-print result)
- **Disposition:** Accepted / Marginal / Rejected
- **Notes and next experiment:** (planned changes for the following run)
```

An entry that establishes a new verified setting must be accompanied, in the same pull request, by the corresponding update to the table in [Materials and Temperature Settings, section 3.3](03-materials-and-temperatures.md).

## 7.2 Log

### YYYY-MM-DD — Placeholder

*(Remove this placeholder with the first recorded run.)*
