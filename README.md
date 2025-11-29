This repository contains the complete experimental dataset used in the accompanying data article on surface pressure measurements over stepped airfoils tested in a low-speed subsonic wind tunnel. The dataset provides high-resolution, time-series pressure data generated under controlled turbulent inflow conditions.

About the Dataset

The experiments were performed on three airfoil configurations:

Stepped airfoil M1 – 3 discrete steps

Stepped airfoil M2 – 6 discrete steps

Stepped airfoil M3 – 8 discrete steps

Controlled turbulence levels were introduced using upstream passive turbulence-generating grids. Surface pressure measurements were obtained from distributed pressure taps connected to a Scanivalve MPS4264 miniature pressure scanner, ensuring accurate acquisition of pressure data.

Contents

The repository includes:

Raw time-series surface pressure data acquired under various inflow turbulence intensities collected at multiple pressure ports

File Name Convention:
Each file name follows a structured code describing the test condition: 
•	WG/G – without grid/passive grid for turbulence generation (Flow condition)
•	1000-Wind tunnel RPM, corresponding to Re=2.14x105.
•	TI-turbulence intensity
•	0.44/6.81-turbulence intensity 
•	PS-Pressure side step
•	SA-symmetrical airfoil
•	0/5/10- angles of attack in degrees.
For example: WG1000TI6.81PSSA0.csv represents Without Grid, 1000 RPM,TI=6.81%, Pressure-side step, Symmetrical airfoil, 0° AoA.

Description of the Excel File:

Each experimental dataset file contains 10,007 rows and 77 columns. The structure of the file is as follows:

1. Rows 1–6: Metadata / Instrument Information

The first six rows contain metadata automatically logged by the MPS4264 Scanivalve pressure scanner.
These entries normally include:

Sampling rate (700 Hz)

Units (e.g., psi, mmH₂O, Pa)

Conversion factor

Date and timestamp of acquisition

The scanner’s internal timing information

These rows do not contain pressure measurements or useful data for analysis. They are typically skipped during preprocessing.

2. Row 7: Column Headers

The seventh row contains the complete column headers for all 77 columns. This row must be treated as the formal header row for parsing.

3. Rows 8–10007: Time-Series Pressure Measurements

The remaining 10,000 rows contain the actual time-series pressure measurements collected during wind tunnel testing.

Each row corresponds to a single timestamp.

Column Organization

The dataset has 77 columns, grouped functionally as follows:

A. Columns 1–12: Non-pressure channels
The first 12 columns appear to store:

Frame 

Valve 

XTime 

Temp1–Temp8 – Temperature readings from the scanner

FTime – Floating timestamp

Possibly additional system parameters and these columns are not pressure data. They are housekeeping parameters recorded by the scanner for calibration and synchronization.

B. Columns 13–76: Surface Pressure Measurements (Primary Data)

These columns contain the actual surface pressure time-series data measured using tubing from the stepped airfoil connected to the Scanivalve.

M1 Model Readings (64 pressure ports)

Column 13 → Press01 → Pressure Port 1

Column 14 → Press02

…

Column 76 → Press64 → Pressure Port 64
Total usable ports = 64

M2 & M3 Model Readings (61 pressure ports)

Column 13 → Press01

…

Column 73 → Press61
Total usable ports = 61

C. Columns 74-76: Additional Unused Channels (only for M2 & M3 model readings)

These channels represent extra Scanivalve ports beyond the connected pneumatic tubings from the test model. They are typically discarded during analysis.
