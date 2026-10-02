\# 2-Stage Miller-Compensated OTA — TSMC 180nm



A two-stage operational transconductance amplifier (OTA) designed 

in TSMC 180nm technology as part of my analog circuits course project.



\## Key Specifications



| Parameter          | Value        |

|--------------------|--------------|

| Technology         | TSMC 180nm   |

| Supply Voltage     | 1.8 V        |

| Open-Loop DC Gain  | 67.16 dB     |

| Phase Margin       | 58.36°       |

| Unity-Gain BW      | 20.04 MHz    |

| Power Consumption  | 518.4 µW     |

| Load Capacitance   | 5 pF         |

| Closed-Loop Gain   | 2 (non-inverting) |



\## Circuit Overview



\- \*\*Stage 1:\*\* Differential pair (M1, M2) with PMOS current mirror 

&#x20; load (M3, M4) and tail current source (M0)

\- \*\*Stage 2:\*\* Common-source amplifier (M5) with current source (M6)

\- \*\*Compensation:\*\* Miller capacitor Cc = 2.5 pF with series 

&#x20; resistor Rz = 500 Ω to cancel RHP zero

\- \*\*Bias:\*\* M7 generates reference; tail current = 10× Iref = 80 µA



\## Transistor Sizing



| Transistor | Role                   | W (µm) | L (µm) | ID (µA) |

|------------|------------------------|--------|--------|---------|

| M0         | Tail current source    | 8.695  | 0.5    | 67.15   |

| M1, M2     | Input diff pair        | 4.348  | 0.5    | 33.57   |

| M3, M4     | Active load (PMOS)     | 10     | 0.5    | 33.57   |

| M5         | 2nd stage amp (PMOS)   | 50     | 0.5    | 176.68  |

| M6         | 2nd stage source (NMOS)| 21.75  | 0.5    | 176.68  |

| M7         | Bias reference (NMOS)  | 0.869  | 0.5    | 8.00    |



\## Simulation Results



\### AC Response (Open Loop)

!\[AC Response](simulations/screenshots/ac\_response.png)



\### Transient Response (Closed Loop, 0.2V step)

!\[Transient](simulations/screenshots/transient\_response.png)



\## Tools Used

\- \*\*Simulator:\*\* LTSpice

\- \*\*PDK:\*\* TSMC 180nm (model file not included — proprietary)



\## How to Run

1\. Clone this repo

2\. Obtain TSMC 180nm model file (`tsmc018.lib`) from your institution

3\. Place it in the schematics/ folder

4\. Open the `.asc` file in LTSpice and run


## Course

Analog Circuits – Electrical and Electronics Engineering, IIT Guwahati

