# Column Geometry

Our next step is to calculate the main dimensions of our column; that is, its column diameter, tank diameter, volume, height and thickness. In order to do this, we will need to obtain the flow rate of the vapour phase and the density of both the vapour and liquid phases in every stage throughout the column. This data was obtained from the ChemCAD software, given by the tray analysis report.

## F-factor and HETP value

The F factor is a parameter that represents the momentum of our vapour phase. From the Sulzer packing catalogue, we have picked the structured MellapakPlusTM 252.Y packing, as it offers a high operational efficiency (minimum hold-up) for atmospheric pressure distillation [add citation here]. It is widely used in the pharmaceutical and food industry. In the same catalogue, it is possible to see the HETP-F factor graphs for each packing type, from which we will pick a safe F factor that will not cause flooding or weeping in our column. We selected 2 √Pa [cite].

\begin{figure}[H]
\centering
\includegraphics[width=0.3\textwidth]{figs/packpic2.png}
\caption{Zoomed-in view of the structured packing MellapakPlus.}
\label{fig:Zoomed-in view of the structured packing}
\end{figure}

In the same catalogue section, we have a graph indicating what HETP (Height Equivalent to one Theoretical Plate) value corresponds to an F factor of 2: 0.4 m (see figure 8.2). The blue line refers to the distillation pressure in mbar.

\begin{figure}[H]
\centering
\includegraphics[width=0.4\textwidth]{figs/sulz.png}
\caption{HETP as a function of the F-factor for MellapakPlus}
\label{fig:HETP as a function of F-factor for MellapakPlus.}
\end{figure}

## Pressure Jump

Pressure jump, also referred to as pressure drop, is the decrease in pressure that occurs as the vapour phase flows through the packing of the distillation column. In a packed column, this pressure loss is mainly caused by friction between the rising vapour, the descending liquid, and the surface of the packing. It is an important design parameter because excessive pressure loss can increase the pressure and temperature at the bottom of the column, which may negatively affect the separation and increase the operating requirements of the process. For a packed distillation column, the total pressure jump can generally be expressed as [cite]:

$\Delta P_{total} = \left(\frac{\Delta P}{H}\right) \cdot H$

where:

- $\Delta P_{total}$ = total pressure jump across the packed section, in mbar.
- $\frac{\Delta P}{H}$ = pressure jump per unit height of packing, in mbar/m.
- $H$ = total packed height of the column, in m.

For a distillation column, the bottom pressure can then be estimated from the top pressure and the total column pressure jump:

$P_{bottom} = P_{top} + \Delta P_{total}$

However, in the Sulzer catalogue's MellapakPlus 252.Y packing section, a relationship between the pressure jump and the F-factor is already provided:

\begin{figure}[H]
\centering
\includegraphics[width=0.3\textwidth]{figs/sulzp.png}
\caption{Pressure jump per meter of the column (mbar/m) as a function of the F-factor for MellapakPlus}
\label{fig:Pressure jump per meter of the column (mbar/m) as a function of the F-factor}
\end{figure}

$\frac{\Delta P}{H} = 1 \text{ mbar/m}$

Since the packed height of the column is: $H = 10 \text{ m}$ the total pressure jump is:

$\Delta P_{total} = 1 \text{ mbar/m} \cdot 10 \text{ m} = 10 \text{ mbar}$

Therefore, the pressure at the bottom of the packed section is expected to be approximately 10 mbar higher than the pressure at the top of the column. The calculated pressure jump is small compared with the operating pressure of the distillation column. Therefore, the selected MellapakPlus™ structured packing is considered suitable, since it provides the required separation height while maintaining a low pressure drop. The 10 mbar pressure increase across the 10 m packed section is not expected to significantly affect the vapour-liquid equilibrium or the overall column operation.

## Column Height

Since the HETP value is known, the calculation of the column height can be carried out directly. HETP stands for Height Equivalent to one Theoretical Plate, and represents the height of packing required to achieve the separation effect of one theoretical stage.

The column height is calculated using the following equation [cite lecture]:

$H = N \times HETP$

where:

- $H$ = packed column height, in m
- $N$ = number of theoretical stages
- $HETP$ = height equivalent to one theoretical plate, in m

From the previous parameter selection, the column was chosen to have 24 theoretical stages. Therefore:

$N = 24$

The selected HETP value for the chosen packing is:

$HETP = 0.4 \text{m}$

Therefore, the required packed height is:

$H = 24 \times 0.4$

$H = 9.6 \text{ m}$

The selected column height is 9.6 m, which can be rounded up to 10 m to allow for some extra safety space.

## Column Diameter

In order to calculate the diameter of the column, the vapour phase density in each stage must first be evaluated. This is necessary to determine the maximum allowable vapour velocity inside the column. The vapour velocity is calculated using the F-factor equation [cite]:

$$ F = v \sqrt{\rho_v} $$

Solving for the vapour velocity:

$$ v = \frac{F}{\sqrt{\rho_v}} $$

where:

- $F$ = F-factor, in $sqrt(Pa)$
- $v$ = maximum vapour velocity, in `m/s`
- $rho_v$ = vapour phase density, in $kg/m^3$

With the vapour velocity, the cross-sectional area of the column can be calculated by rearranging the continuity equation:

$$ A = \frac{\dot{V}}{v} $$

where:

- $A$ = cross-sectional area of the column, in $m^2$
- $V_dot$ = vapour volumetric flow rate, in $m^3/s$
- $v$ = vapour velocity, in `m/s`

The column diameter is then calculated from the circular area equation:

$$ A = \frac{\pi D^2}{4} $$

Solving for the diameter:

$$ D = \sqrt{\frac{4A}{\pi}} $$

For each stage of the process, the highest vapour volumetric flow rate and the lowest vapour density were considered in order to calculate the largest required column diameter, and these were obtained from ChemCAD's tray properties' reports. This approach was used for safety reasons, since the column must be able to operate under the most demanding vapour-flow conditions.

Table: Diameter calculation results.
\label{tab:Diameter calculation results}

| Vapour vol. flow rate [m^3/s] | Vapour density [kg/m^3] | F-factor [sqrt(Pa)] | Vapour velocity [m/s] | Area [m^2] | Diameter [m] | HETP [m] | Height [m] |
| ----------------------------- | ----------------------- | ------------------- | --------------------- | ---------- | ------------ | -------- | ---------- |
| 0.492                         | 1.625                   | 2                   | 1.5689                | 0.193      | 0.496        | 0.4      | 10.0       |
| 0.174                         | 0.853                   | 2                   | 2.1655                | 0.094      | 0.346        | 0.4      | 10.0       |
| 0.210                         | 0.595                   | 2                   | 2.5928                | 0.136      | 0.416        | 0.4      | 10.0       |
| 0.215                         | 0.593                   | 2                   | 2.5972                | 0.140      | 0.422        | 0.4      | 10.0       |
| 0.240                         | 2.100                   | 2                   | 1.3801                | 0.083      | 0.325        | 0.4      | 10.0       |

As shown in Table 8.1, the highest calculated diameter value is 0.495689 m. This value can be rounded up to 0.5 m. To provide an additional safety margin, a safety factor of 20% is applied [cite]:

$$ D = 0.50 \times 1.20 = 0.60 \text{ m} $$

Therefore, the final selected column diameter is 60 m.

## Column Thickness

The wall thickness of the distillation column was calculated by treating the column as a cylindrical pressure vessel under internal pressure. For safety purposes, the design pressure was selected as 6 bar, which is higher than the expected operating pressure of the column. The column is assumed to be made of carbon steel, with an allowable stress of $S = 120 \times 10^6 \text{ Pa}$ and a weld joint efficiency of $E = 0.85$. [cite]

The minimum required wall thickness was calculated using the cylindrical vessel equation [cite]:

$$ t = \frac{P R}{S E - 0.6P} $$

where:

- $t$ = minimum required wall thickness, in m
- $P$ = design pressure, in Pa
- $R$ = internal radius of the column, in m
- $S$ = allowable stress of the construction material, in Pa
- $E$ = weld joint efficiency

For this calculation, the following values were used:

Table: Parameters relevant to wall thickness.
\label{tab:wall thickness}

| Parameter                        | Symbol | Value             | Unit |
| -------------------------------- | ------ | ----------------- | ---- |
| Design pressure                  | $P$    | 600000            | Pa   |
| Column diameter                  | $D$    | 0.60              | m    |
| Column radius                    | $R$    | 0.30              | m    |
| Allowable stress of carbon steel | $S$    | $120 \times 10^6$ | Pa   |
| Weld joint efficiency            | $E$    | 0.85              | -    |

Substituting the values:

$t = \frac{600000 \times 0.30}{(120 \times 10^6)(0.85) - 0.6(600000)}$

$t = 0.00177 \text{ m}$

$t = 1.77 \text{ mm}$

The calculated theoretical wall thickness is therefore 1.77 mm. However, this value only represents the minimum thickness required to withstand the selected internal design pressure. A corrosion allowance must also be included, especially because carbon steel is used as the construction material. Assuming a corrosion allowance of 3.2 mmc[cite book]:

$t_{\text{final}} = t + C_A$

$t_{\text{final}} = 1.77 + 3.2$

$t_{\text{final}} = 4.97 \text{ mm}$

Therefore, the selected practical wall thickness is rounded up to:

$t_{\text{selected}} = 5 \text{ mm}$

The final selected wall thickness of the column for the 6 bar internal pressure case is therefore 5 mm.

The column is also later planned to withstand an internal pressure of 0.1 bar. Since the outside of the column is assumed to be at atmospheric pressure, this condition creates an external pressure difference of approximately $P_{\text{external}} = 1.013 - 0.1 = 0.913 \text{ bar}$.

A preliminary external pressure check shows that a 5 mm wall thickness can withstand the vacuum condition if the full 5 mm thickness is available structurally:

the external pressure difference is:

$P_{external} = 1.013 - 0.1 = 0.913 \text{ bar} = 91300 \text{ Pa}$

For a preliminary thin cylindrical shell buckling check, the following expression was used [cite]:

$P_{cr} = \frac{2E}{\sqrt{3(1-\nu^2)}} \left(\frac{t}{R}\right)^3$

where $P_{cr}$ is the critical external pressure, $E$ is Young’s modulus, $\nu$ is Poisson’s ratio, $t$ is the wall thickness, and $R$ is the column radius.

Using carbon steel properties [cite]:

$E = 200 \cdot 10^9 \text{ Pa}$

$\nu = 0.30$

and the selected column dimensions:

$t = 0.005 \text{ m}$

$R = 0.30 \text{ m}$

the critical external pressure is:

$P_{cr} = \frac{2(200 \cdot 10^9)}{\sqrt{3(1-0.30^2)}} \left(\frac{0.005}{0.30}\right)^3$

$P_{cr} = 1.12 \cdot 10^6 \text{ Pa} = 11.2 \text{ bar}$

Since the estimated critical external pressure is much higher than the vacuum pressure difference, the selected 5 mm wall thickness is acceptable for this preliminary vacuum check.

However, if the 5 mm thickness includes a 3.2 mm corrosion allowance, the effective structural thickness would be only 1.8 mm, which is not sufficient for the 0.1 bar internal pressure case. Therefore, if vacuum operation at 0.1 bar must be guaranteed while keeping the 3.2 mm corrosion allowance, a larger nominal wall thickness, such as 7 mm, is recommended.

## Tank Geometry

The tank geometry was determined based on the maximum liquid volume obtained from the simulation results. From the tank volume values, the maximum required volume was approximately:

$V_{\text{max}} = 6 \text{ m}^3$

In order to provide an additional safety margin for bubbling and avoid operating the tank exactly at its maximum capacity, a larger geometrical volume was selected. The tank was designed as a vertical cylindrical vessel with a height of 2.5 m and a diameter of 2.0 m.

The volume of a cylindrical tank is calculated as:

$$ V = \frac{\pi D^2}{4}H $$

where:

- $V$ = tank volume, in m³
- $D$ = tank diameter, in m
- $H$ = tank height, in m

Substituting the selected dimensions:

$V = \frac{\pi (2.0)^2}{4}(2.5)$

$V = 7.85 \text{ m}^3$

Therefore, the selected tank dimensions provide a total geometrical volume of approximately 7.85 m^3.

Since this value is greater than the maximum required process volume of 6 m³, the selected tank geometry provides sufficient additional capacity for safe operation. The final selected tank dimensions are therefore:

Table: Final Dimensions of the column tank.
\label{tab:Final Dimensions of the column tank}

| Parameter               |            Symbol | Value | Unit |
| ----------------------- | ----------------: | ----: | ---: |
| Maximum required volume |  $V_{\text{max}}$ |  6.00 |   m³ |
| Selected tank diameter  |               $D$ |  2.00 |    m |
| Selected tank height    |               $H$ |  2.50 |    m |
| Selected tank volume    | $V_{\text{tank}}$ |  7.85 |   m³ |
