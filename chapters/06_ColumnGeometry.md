# Column Geometry

Our next step is to calculate the main dimensions of the column; that is, its column diameter, tank diameter, volume, height and thickness. In order to do this, we will need to obtain the flow rate of the vapour phase and the density of both the vapour and liquid phases in every stage throughout the column. This data was obtained from the ChemCAD software, given by the tray analysis report.

## F-factor and HETP value

The F factor is a parameter that represents the momentum of the vapour phase. From the Sulzer packing catalogue, the structured MellapakPlus 252.Y packing was chosen, as it offers a high operational efficiency and minimum hold-up for atmospheric pressure distillation [@sulzer_structured_packings_nd]. It is widely used in the pharmaceutical and food industry. In the same catalogue, it is possible to see the HETP-F factor graphs for each packing type. The F-factor will be picked so that it will not cause flooding or weeping in the column; 2 √Pa was selected (See Figure 6.1).

\begin{figure}[H]
\centering
\includegraphics[width=0.3\textwidth]{figs/packpic2.png}
\caption{Zoomed-in view of the structured packing MellapakPlus 252.Y.}
\label{fig:Zoomed-in view of the structured packing}
\end{figure}

In the same catalogue section, we have a graph indicating what HETP (Height Equivalent to one Theoretical Plate) value corresponds to an F factor of 2: 0.4 m (see Figure 6.2). The blue line refers to the distillation pressure 960 mbar.

\begin{figure}[H]
\centering
\includegraphics[width=0.4\textwidth]{figs/sulz.png}
\caption{HETP as a function of the F-factor for MellapakPlus 252.Y and 250.Y.}
\label{fig:HETP as a function of F-factor for MellapakPlus 252.Y}
\end{figure}

## Column Height

Since the HETP value is known, the calculation of the column height can be carried out directly. The HETP represents the height of packing required to achieve the separation effect of one theoretical stage.

The column height is calculated using the following equation [@bme_distillation_notes_v_nd]:

$$
H = N \times HETP
$$

where:

- $H$ = packed column height, in m
- $N$ = number of theoretical stages
- $HETP$ = height equivalent to one theoretical plate, in m

The column was chosen to have 24 theoretical stages, and the selected HETP value for the chosen packing is HETP = 0.4 m. Therefore, the required packed height is:

$$
H = 24 \times 0.4 = 9.6 \text{ m}
$$

The selected column height is 9.6 m, which can be rounded up to 10 m to allow for some extra safety space. This height is only representative of the column alone, without accounting for the reboiler, bottom tank or condenser.

## Pressure Drop

The pressure drop is the decrease in pressure that occurs as the vapour phase flows through the packing of the distillation column. In a packed column, this pressure loss is mainly caused by friction between the rising vapour, the descending liquid, and the surface of the packing. It is an important design parameter because excessive pressure loss can increase the pressure and temperature at the bottom of the column, which may negatively affect the separation and increase the operating requirements of the process. For a packed distillation column, the total pressure drop can generally be expressed as [@sulzer_structured_packings_nd]:

$\Delta P_{total} = \left(\frac{\Delta P}{H}\right) \cdot H$

where:

- $\Delta P_{total}$ = total pressure drop across the packed section, in mbar.
- $\frac{\Delta P}{H}$ = pressure drop per unit height of packing, in mbar/m.
- $H$ = total packed height of the column, in m.

For a distillation column, the bottom pressure can then be estimated from the top pressure and the total column pressure drop:

$P_{bottom} = P_{top} + \Delta P_{total}$

However, in the Sulzer catalogue's MellapakPlus 252.Y packing section, a relationship between the pressure drop and the F-factor is already provided:

\begin{figure}[H]
\centering
\includegraphics[width=0.3\textwidth]{figs/sulzp.png}
\caption{Pressure drop per meter of the column (mbar/m) as a function of the F-factor for MellapakPlus 252.Y and 250.Y.}
\label{fig:Pressure drop per meter of the column (mbar/m) as a function of the F-factor}
\end{figure}

$$
\frac{\Delta P}{H} = 1 \text{ mbar/m}
$$

Since the packed height of the column is H = 10 m, the total pressure drop is:

$\Delta P_{total} = 1 \text{ mbar/m} \cdot 10 \text{ m} = 10 \text{ mbar}$

Therefore, the pressure at the bottom of the packed section is expected to be approximately 10 mbar higher than the pressure at the top of the column. The calculated pressure drop is small compared with the operating pressure of the distillation column. Therefore, the selected MellapakPlus 252.Y structured packing is considered suitable, since it provides the required separation height while maintaining a low pressure drop. The 10 mbar pressure increase across the 10 m packed section is not expected to significantly affect the vapour-liquid equilibrium or the overall column operation.

## Column Diameter

In order to calculate the diameter of the column, the vapour phase velocity on each stage must first be evaluated by rearranging the F-value equation, whose value we selected: [@sulzer_structured_packings_nd]:

$$ F = v \sqrt{\rho_v} $$

Solving for the vapour velocity:

$$ v = \frac{F}{\sqrt{\rho_v}} $$

where:

- $F$ = F-factor, in $\sqrt{Pa}$
- $v$ = maximum vapour velocity, in $m/s$
- $\rho_v$ = vapour phase density, in $kg/m^3$

With the vapour velocity, the cross-sectional area of the column can be calculated by rearranging the continuity equation:

$$ A = \frac{\dot{V}}{v} $$

where:

- $A$ = cross-sectional area of the column, in $m^2$
- $\dot{V}$ = vapour volumetric flow rate, in $m^3/s$
- $v$ = vapour velocity, in $m/s$

The column diameter is then calculated from the circular area equation:

$$ A = \frac{\pi D^2}{4} $$

Solving for the diameter:

$$ D = \sqrt{\frac{4A}{\pi}} $$

For each step of the process, the highest vapour volumetric flow rate and the lowest vapour density were considered in order to calculate the largest required column diameter, and these were obtained from ChemCAD's tray properties' reports (see Table 6.1). This approach was used for safety, since the column must be able to operate under the most demanding vapour-flow conditions.

Table: Diameter calculation results.
\label{tab:Diameter calculation results}

| Simulation Steps | Vapour vol. flow rate [$m^3/s$] | Vapour density [$kg/m^3$] | Vapour velocity [m/s] | Area [m^2] | Diameter [m] |
| ---------------- | ------------------------------- | ------------------------- | --------------------- | ---------- | ------------ |
| 0                | 0.492                           | 1.625                     | 1.5689                | 0.314      | 0.632        |
| 1                | 0.174                           | 0.853                     | 2.1655                | 0.0803     | 0.320        |
| 2                | 0.210                           | 0.595                     | 2.5928                | 0.0810     | 0.321        |
| 3                | 0.215                           | 0.593                     | 2.5972                | 0.0828     | 0.324        |
| 4                | 0.240                           | 2.100                     | 1.3801                | 0.1739     | 0.471        |

As shown in Table 6.1, the highest calculated diameter value is 0.632 m. To provide an additional safety margin, a safety factor of 20% is applied:

$$ D = 0.632 \times 1.20 = 0.758 \text{ m} $$

Therefore, the final selected column diameter is 0.76 m after rounding up the second decimal, for the sake of simplicity.

## Column Thickness

The wall thickness of the distillation column was calculated by treating the column as a cylindrical pressure vessel under internal pressure. For safety purposes, the design pressure was selected as 6 bar, which is higher than the expected operating pressure of the column. The column is assumed to be made of carbon steel, with an allowable stress of $S = 120 \times 10^6 \text{ Pa}$ and a weld joint efficiency of $E = 0.85$. [@asme_bpvc_viii_div1_2025]

The minimum required wall thickness was calculated using the cylindrical vessel equation [@asme_bpvc_viii_div1_2025]:

$$ x = \frac{P R}{S E - 0.6P} $$

where:

- $x$ = minimum required wall thickness, in m
- $P$ = design pressure, in Pa
- $R$ = internal radius of the column, in m
- $S$ = allowable stress of the construction material, in Pa
- $E$ = weld joint efficiency, dimensionless

For this calculation, the following values used can be found in Table 6.2.

Table: Parameters relevant to wall thickness.
\label{tab:wall thickness}

| Parameter                        | Symbol | Value             | Unit |
| -------------------------------- | ------ | ----------------- | ---- |
| Design pressure                  | $P$    | 600000            | Pa   |
| Column radius                    | $R$    | 0.38              | m    |
| Allowable stress of carbon steel | $S$    | $120 \times 10^6$ | Pa   |
| Weld joint efficiency            | $E$    | 0.85              | -    |

Substituting the values:

$$
x = \frac{600000 \times 0.38}{(120 \times 10^6)(0.85) - 0.6(600000)} = 0.00224 \text{ m} = 2.24 \text{ mm}
$$

The calculated theoretical wall thickness is therefore 2.44 mm. However, this value only represents the minimum thickness required to withstand the selected internal design pressure. A corrosion allowance must also be included, especially because carbon steel is used as the construction material. Assuming a corrosion allowance of 3.2 mm [@coulson_richardson_shell_tube_nd]:

$x_{\text{final}} = t + C_A = 2.24 + 3.2 = 5.44 \text{ mm}$

The practical wall thickness is rounded up to 6 mm in order to guarantee safety.

The column is later planned to operate at a pressure of 0.1 bar. Since the outside of the column is assumed to be at atmospheric pressure, this condition creates an external pressure difference of approximately $P_{\text{external}} = 1.013 - 0.1 = 0.913 \text{ bar} = 91300 \text{ Pa}$

A preliminary external pressure check shows that a 6 mm wall thickness can withstand the vacuum condition if the full 5 mm thickness is available structurally. To check for shell buckling, the following expression was used [@nasa_sp_8007_2020]:

$$
P_{cr} = \frac{2E}{\sqrt{3(1-\nu^2)}} \left(\frac{x}{R}\right)^3
$$

where $P_{cr}$ is the critical external pressure, $E$ is Young’s modulus, $\nu$ is Poisson’s ratio, $t$ is the wall thickness, and $R$ is the column radius.

Using carbon steel properties [@asme_bpvc_vii_d_metric_2025]:

$E = 200 \cdot 10^9 \text{ Pa}$

$\nu = 0.30$

and the selected column dimensions:

$x = 0.006 \text{ m}$

$R = 0.38 \text{ m}$

the critical external pressure is:

$$
P_{cr} = \frac{2(200 \cdot 10^9)}{\sqrt{3(1-0.30^2)}} \left(\frac{0.006}{0.38}\right)^3 = 9.82 \cdot 10^5 \text{ Pa} = 9.82 \text{ bar}
$$

Since the estimated critical external pressure is higher than the vacuum pressure difference, the selected 6 mm wall thickness is acceptable for this preliminary vacuum check.

## Tank Geometry

The tank geometry was determined based on the maximum liquid volume obtained from the ChemCAD simulation reports. From the tank's liquid volume values, the maximum required liquid volume was found at the end of step 1, due to the addition of DMSO feed. This value is approximately $V_{\text{max}} = 6 \text{ m}^3$.

In order to provide an additional safety margin for bubbling and avoid operating the tank exactly at its maximum capacity, a larger geometrical volume was selected. The tank was designed as a vertical cylindrical vessel with a height of 2.5 m and a diameter of 2.0 m.

The volume of a cylindrical tank is calculated as:

$$ V = \frac{\pi D^2}{4}H $$

where:

- $V$ = tank volume, in m³
- $D$ = tank diameter, in m
- $H$ = tank height, in m

Substituting with the selected dimensions:

$$
V = \frac{\pi (2.0)^2}{4}(2.5) = 7.85 \text{ m}^3
$$

Since this value is greater than the maximum required process volume of 6 m³, the tank geometry provides sufficient additional capacity for safe operation. The final selected tank dimensions are displayed in Table 6.3.

Table: Final Dimensions of the selected tank.
\label{tab:Final Dimensions of the selected tank}

| Parameter               |            Symbol | Value |  Unit |
| ----------------------- | ----------------: | ----: | ----: |
| Maximum required volume |  $V_{\text{max}}$ |  6.00 | $m^3$ |
| Selected tank diameter  |               $D$ |  2.00 |   $m$ |
| Selected tank height    |               $H$ |  2.50 |   $m$ |
| Selected tank volume    | $V_{\text{tank}}$ |  7.85 | $m^3$ |
