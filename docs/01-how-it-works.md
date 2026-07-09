# 1. Machine Overview and Principle of Operation

## 1.1 Summary

The ExtrudeX is a single-screw filament extruder. It converts shredded thermoplastic waste — typically blended with virgin pellets — into continuous 1.75 mm filament suitable for FDM printing. Feedstock is gravity-fed into a heated barrel, melted, forced through a nozzle, drawn to final diameter by a motorized puller, cooled, and collected on a spool.

This document describes each subsystem in the order material passes through it. It assumes no prior experience with filament extrusion.

## 1.2 Process flow

```
Feedstock → Hopper → Barrel & auger (melt) → Nozzle → Cooling zone → Puller → Spool
```

## 1.3 Subsystems

### 1.3.1 Hopper (material intake)

A gravity-fed funnel mounted above the barrel inlet. Prepared feedstock — shredded waste, normally mixed with virgin pellets of the same polymer — is loaded here and descends into the barrel under its own weight. The hopper contains no active components; reliable feeding depends entirely on the feedstock being granulated to a small, uniform size (see [Materials & Temperatures](03-materials-and-temperatures.md), section on preparation).

### 1.3.2 Barrel and auger (melting and conveyance)

The core of the machine is a horizontal metal barrel containing a rotating screw (auger) driven by a DC gear motor. As the screw rotates, it conveys material along the barrel. External band heaters, regulated by a PID temperature controller, bring the barrel to the setpoint temperature; material is fully molten by the time it reaches the barrel outlet.

Two operator-adjustable parameters govern this stage:

| Parameter | Adjusted at | Effect |
|-----------|-------------|--------|
| Barrel temperature | PID controller | Melt viscosity; too low causes motor strain and incomplete melting, too high causes polymer degradation |
| Screw speed | Motor speed controller | Throughput; must remain matched to the melt rate the barrel can sustain |

The interaction between these two parameters accounts for most of the tuning effort on this machine. Documented setpoints are maintained in [Materials & Temperatures](03-materials-and-temperatures.md).

### 1.3.3 Nozzle (extrusion)

Molten material exits the barrel through a nozzle as a continuous strand. The strand leaves the nozzle oversized relative to the 1.75 mm target; final diameter is established downstream by drawing, not by the nozzle orifice.

### 1.3.4 Cooling zone and puller (diameter control)

A fan directs airflow across the strand as it exits the nozzle, solidifying its surface. The strand is then fed into the puller: a pair of motorized rollers that grip the filament and draw it away from the nozzle at a controlled rate.

**Puller speed — not nozzle geometry — determines final filament diameter.** While the strand is still soft, a higher draw rate stretches it thinner; a lower rate leaves it thicker. Matching puller speed to extrusion rate is the primary means of holding a consistent 1.75 mm diameter, and is covered step by step in the [operating procedure](04-operation.md).

An optional digital dial indicator can be mounted ahead of the puller to provide real-time diameter measurement. This is recommended whenever the output filament is intended for printers with tight diameter tolerances.

### 1.3.5 Spooling (collection)

Finished filament is wound onto a spool at the puller outlet. Depending on configuration this is performed manually or with assistance; the current documented workflow is described in the [operating procedure](04-operation.md).

## 1.4 Feedstock composition

Thermoplastics degrade slightly with each heat cycle: polymer chains shorten, reducing strength and flow consistency. Blending recycled material with virgin pellets offsets this degradation. The current recommended starting composition is **60% virgin pellets / 40% shredded waste by weight**. Compositions up to 100% recycled content are feasible but produce greater variation in diameter and mechanical properties; results from our own trials are recorded in the [experiment log](07-experiment-log.md).

## 1.5 Material compatibility constraint

**Polymer types must never be mixed.** PLA is processed with PLA, PETG with PETG, ABS with ABS. Dissimilar polymers have incompatible melt temperatures and do not form a homogeneous, usable material. A mixed batch produces unusable filament and leaves residue in the barrel that must be purged before the next run (see [Cleaning & Maintenance](05-cleaning-and-maintenance.md)). Feedstock segregation therefore begins at the waste bin, before shredding.

---

*This document reflects the community's current understanding of the machine's operation. Corrections and additions are welcome — see [CONTRIBUTING.md](../CONTRIBUTING.md).*
