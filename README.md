# Well Test Analysis of a Hydraulically Fractured Reservoir

Well test analysis of a pressure drawdown test to estimate reservoir permeability, skin factor, and fracture half-length, with results cross-validated using two independent interpretation methods: **semi-log analysis** and **log-log derivative analysis**.

## Problem Overview

A well is produced at a constant rate, and flowing bottom-hole pressure (FBHP) is recorded over time. The objective is to:

1. Estimate reservoir **permeability (k)** using conventional semi-log (pwf vs. log t) analysis.
2. Calculate the **skin factor (s)** from the semi-log straight line.
3. Diagnose the flow regime using a **pressure derivative (log-log) plot** of Δp and t·(dp/dt) vs. time, and identify the onset of infinite-acting radial flow.
4. Confirm the presence of a **hydraulic fracture** from the linear-flow signature (½-slope on the derivative plot).
5. Estimate **fracture half-length (Xf)** from the linear-flow period, using both the pwf vs. √t plot and the derivative plot.
6. Cross-check permeability and fracture half-length obtained from the two independent methods.

> **Note:** The skin factor is calculated, but the additional pressure drop caused by skin (Δp_skin) has not been evaluated in this version.

## Given Data

| Parameter | Symbol | Value | Units |
|---|---|---|---|
| Flow rate | q | 2000 | stb/day |
| Initial reservoir pressure | Pi | 5000 | psi |
| Formation thickness | h | 50 | ft |
| Porosity | φ | 0.24 | – |
| Total compressibility | Ct | 1.48 × 10⁻⁵ | psi⁻¹ |
| Oil formation volume factor | Bo | 1.5 | rb/stb |
| Oil viscosity | μo | 0.3 | cp |
| Wellbore/reference radius | rd | 0.29 | ft |

## Methodology

**1. Data preparation**
- Computed Δp = Pi − pwf, √t, and the pressure derivative t·(dp/dt) for each time step from the raw pwf vs. t data.

**2. Semi-log analysis (pwf vs. log t)**
- Plotted pwf against log(t) and identified the middle-time-region straight line.
- Calculated permeability and skin factor from the slope and intercept using the standard semi-log equations.

**3. Linear flow analysis (pwf vs. √t)**
- Plotted pwf against √t; the straight-line trend confirms linear flow into a hydraulic fracture.
- Back-calculated fracture half-length (Xf) from the slope of this line.

**4. Pressure derivative (log-log) analysis**
- Plotted Δp and the pressure derivative vs. time on a log-log scale.
- Identified the stabilization of the derivative at ~68.8 hours, marking the onset of infinite-acting radial flow.
- Confirmed linear flow by matching both curves to a common **½-slope** line (verified against two reference lines of slope 0.5).
- Independently recomputed permeability and fracture half-length from the derivative plot.

**5. Validation**
- Compared permeability and fracture half-length obtained from the semi-log/linear-flow method against the derivative method to confirm consistency.

## Results

| Quantity | Semi-log / Linear-flow method | Derivative method |
|---|---|---|
| Permeability, k (md) | 12.68 | 12.708 |
| Fracture half-length, Xf (ft) | 105.73 | 104.46 |
| Skin factor, s | −5.06 | – |

**Conclusion:** The skin factor is negative (s ≈ −5.06), and the fracture half-length (~105 ft) is confirmed by both methods, indicating a successful hydraulic fracturing operation. The close agreement between the two independent methods further validates the permeability and fracture half-length estimates.

## Repository Contents

- `Well_Test_Analysis_of_a_Hydraulically_Fractured_Reservoir.xlsx` — Full worked solution, containing:
  - **Question** sheet — raw well test data and calculated columns (Δp, √t, derivative).
  - **Parameter Calculation** sheet — semi-log plot, √t linear-flow plot, log-log derivative plot, and final reservoir parameter calculations (k, skin, Xf).

## Tools Used

- Microsoft Excel (data processing, plotting, and slope-based parameter estimation)

