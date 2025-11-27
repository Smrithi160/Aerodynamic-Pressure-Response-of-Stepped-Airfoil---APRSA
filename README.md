This repository contains the complete experimental dataset used in the accompanying data article on surface pressure measurements over stepped airfoils tested in a low-speed subsonic wind tunnel. The dataset provides high-resolution, time-series pressure data generated under controlled turbulent inflow conditions.

About the Dataset

The experiments were performed on three airfoil configurations:

Stepped airfoil M1 – 3 discrete steps

Stepped airfoil M2 – 6 discrete steps

Stepped airfoil M3 – 8 discrete steps

Controlled turbulence levels were introduced using upstream passive turbulence-generating grids. Surface pressure measurements were obtained from distributed pressure taps connected to a Scanivalve MPS4264 miniature pressure scanner, ensuring accurate acquisition of pressure data.

Contents

The repository includes:

Raw time-series surface pressure data acquired under various inflow turbulence intensities
collected at multiple pressure ports

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

