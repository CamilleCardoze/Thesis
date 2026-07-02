# Heat Exchangers

## Column Condenser Design

The condenser was designed as a counter-current, one-pass shell-and-tube heat exchanger used to condense the IPA-rich vapour leaving the top of the distillation column. A one-pass shell-and-tube heat exchanger is suitable for the column condenser because it avoids unnecessary mechanical complexity, reduces the number of flow reversals, and helps keep the pressure drop low. Since the required heat transfer area can be achieved with a simple tube bundle, this arrangement is sufficient [@coulson_richardson_shell_tube_nd].

The total heat transfer area listed in the calculation corresponds to the total available outside tube surface area. The IPA properties used for the condensation-side calculation were obtained from ChemCAD's reports, while the cooling-water properties were taken from literature [@cengel_ghajar_2011]. These are listed below in Table 7.1.

Table: Material properties of isopropanol and cooling water.
\label{tab:Properties of cooling water and IPA}

| Property                                                   |     Value | Unit              |
| ---------------------------------------------------------- | --------: | ----------------- |
| thermal conductivity of IPA $\lambda_{IPA,film}$           |    0.1235 | $\text{W/(m*K)}$  |
| density of IPA $\rho_{IPA,film}$                           |   730.616 | $\text{kg/m}^3$   |
| dynamic viscosity of IPA $\mu_{IPA,film}$                  | 0.0005851 | $\text{N*s/m}^2$  |
| latent heat of IPA $r_{IPA,film}$                          |    680200 | $\text{J/kg}$     |
| specific heat capacity of IPA, const. pressure $c_{p,IPA}$ |    3296.2 | $\text{J/(kg*K)}$ |
| temperature of IPA $T_{dist}$                              |        80 | °C                |
| thermal conductivity of water $\lambda_{w}$                |     0.624 | $\text{W/(m*K)}$  |
| density of water $\rho_{w}$                                |     994.1 | $\text{kg/m}^3$   |
| dynamic viscosity of water $\mu_{w}$                       |  0.000719 | $\text{N*s/m}^2$  |
| specific heat capacity of water, const. pressure $c_{p,w}$ |    4175.5 | $\text{J/(kg*K)}$ |
| temperature of inlet water $T_{w, in}$                     |        25 | °C                |
| temperature of outlet water $T_{w, out}$                   |        50 | °C                |

\begin{figure}[H]
\centering
\includegraphics[width=0.8\textwidth]{figs/condT.png}
\caption{Minimum temperature of the distillate $T_{dist}$ (80°C), which was used in the condenser calculations.}
\label{fig:Minimum temperature of the distillate}
\end{figure}

\begin{figure}[H]
\centering
\includegraphics[width=0.6\textwidth]{figs/tprof.jpg}
\caption{Temperature profiles in the case of a condenser, where $T_{cond}$ is $T_{dist}$ in this case, and the x-axis represents the heat transfer surface length \cite{perry_green_2008_heat_mass_transfer}. Since the distillate vapour changes phase, the temperature can be assumed to be constant (non-sensible heat transfer).}
\label{fig:Temperature profiles in the case of a condenser}
\end{figure}

The main design equation used for the condenser was [@bme_heat_exchangers_2_2024]:

$$ Q = k A F \Delta T_m $$

Rearranging for the required heat transfer area:

$$ A = \frac{Q}{k F \Delta T_m} $$

where $Q$ is the condenser heat duty, $k$ is the overall heat transfer coefficient, $A$ is the total heat transfer area, $F$ is the correction factor and $\Delta T_m$ is the mean temperature difference. Since the temperature difference between the condensing vapour and cooling water changes along the exchanger, the logarithmic mean temperature difference was used:

$$
\Delta T_{log} = \frac{\Delta T_1 - \Delta T_2}{\ln \left(\frac{\Delta T_1}{\Delta T_2}\right)}
$$

The IPA vapour was assumed to condense at constant temperature since we are dealing with a phase change, while the cooling water was assumed to be heated up from 25°C (room temperature) to 50°C. Therefore:

$\Delta T_1 = T_{IPA} - T_{w,in}= 353.15 - 298.15 = 55 \text{ K}$

$\Delta T_2 = T_{IPA} - T_{w,out} = 353.15 - 323.15 = 30 \text{ K}$

Thus:

$\Delta T_{log} = \frac{55 - 30}{\ln \left(\frac{55}{30}\right)} = 41.24 \text{ K}$

The correction factor was calculated:

$F = 1$

From the formulas indicated in the correction factor chart for a single shell pass heat exchanger (Figure 7.3).

\begin{figure}[H]
\centering
\includegraphics[width=0.8\textwidth]{figs/Fgraph1.png}
\caption{Correction factor for a single shell pass heat exchanger \cite{coulson_richardson_shell_tube_nd}.}
\label{fig:Correction factor for a single shell pass heat exchanger}
\end{figure}

\begin{figure}[H]
\centering
\includegraphics[width=0.8\textwidth]{figs/condHD.png}
\caption{Graph indicating the maximum condenser heat duty (minimum value in the plot, since heat duty is negative) during the process (957.7 MJ/h).}
\label{fig:Minimum condenser heat duty}
\end{figure}

The highest condenser heat duty obtained from the simulation was $Q = 957.7 \text{ MJ/h}$. Converting to watts:

$Q = \frac{957.7 \times 10^6}{3600} = 266027.78 \text{ W}$

Using the initially assumed overall heat transfer coefficient for phase change $k = 850 \text{ W/m}^2\text{K}$ [@kiss_2013], the first estimated heat transfer area was:

$A = \frac{266027.78}{850 \times 41.24} = 7.59 \text{ m}^2$

This value was used only as an initial estimate. A corrected design was then obtained by calculating the individual heat transfer coefficients, the wall resistance, and the fouling resistance.

The clean overall heat transfer coefficient was calculated from the thermal resistance relationship [@perry_green_2008_heat_mass_transfer]:

$$
\frac{1}{k_{clean}} = \frac{1}{\alpha_{w,out}} + \frac{x_{tube}}{\lambda_{wall}} + \frac{1}{\alpha_{cond}}
$$

where $\alpha_{w,out}$ is the cooling-water heat transfer coefficient converted to the outside tube area, $x_{tube}$ is the tube wall thickness, $\lambda_{wall}$ is the thermal conductivity of the carbon-steel wall, and $\alpha_{cond}$ is the condensation-side heat transfer coefficient.

As it is a widely used, affordable material, it was decided to use carbon steel as the main material for the heat exchangers' tubes and shell walls. The wall thermal conductivity (the thermal conductivity of carbon steel) was then taken to be $\lambda_{wall} = 45 \text{ W/mK}$ [@perry_green_2008_heat_mass_transfer].

The water-side Reynolds number was calculated using [@bme_heat_exchangers_2_2024]:

$$
Re = \frac{\rho_{w} v D_{in}}{\mu}
$$

The Prandtl number was calculated using [@bme_heat_exchangers_2_2024]:

$$
Pr = \frac{\mu c_{p,w}}{\lambda}
$$

The Nusselt number used was [@bme_heat_exchangers_2_2024]:

$$
Nu = 0.3 Re^{0.5} Pr^{1/3}
$$

The water-side heat transfer coefficient was then calculated from [@bme_heat_exchangers_2_2024]:

$$
\alpha_{w,in} = \frac{Nu \lambda_{w}}{D_{in}}
$$

Since the total heat transfer area was based on the outside tube surface, the water-side coefficient was converted to the outside area basis:

$$
\alpha_{w,out} = \alpha_{w,in} \frac{D_{in}}{D_{out}}
$$

The calculated condenser heat transfer coefficients can be found in Table 7.2.

Table: Condenser heat transfer coefficients.
\label{tab:Condenser heat transfer coefficients.}

| Parameter                             |           Symbol |   Value |  Unit |
| ------------------------------------- | ---------------: | ------: | ----: |
| Condensation-side coefficient         |  $\alpha_{cond}$ | 1995.01 | W/m²K |
| Water-side coefficient, inside basis  |  $\alpha_{w,in}$ | 1514.09 | W/m²K |
| Water-side coefficient, outside basis | $\alpha_{w,out}$ | 1211.27 | W/m²K |
| Clean overall coefficient             |      $k_{clean}$ |  729.25 | W/m²K |
| Fouling resistance                    |            $R_f$ |  0.0005 | m²K/W |
| Dirty overall coefficient             |      $k_{dirty}$ |  534.40 | W/m²K |

Fouling resistance was obtained from literature [@perry_green_2008_heat_mass_transfer].

The dirty overall heat transfer coefficient was calculated by adding the fouling resistance:

$$
\frac{1}{k_{dirty}} = \frac{1}{k_{clean}} + R_f
$$

$k_{dirty} = 534.40 \text{ W/m}^2\text{K}$

Using the dirty overall heat transfer coefficient, the final required heat transfer area was:

$A_{calc} = \frac{Q}{k_{dirty} \Delta T_{log}}$

$A_{calc} = \frac{266027.78}{534.40 \times 41.24} = 12.07 \text{ m}^2$

Therefore, the required total condenser heat transfer area is 12.07 $m^2$

The selected condenser geometry is shown in Table 7.3.

Table: Selected and calculated condenser geometry.
\label{tab:Selected and calculated condenser geometry}

| Parameter             |         Symbol |  Value | Unit |
| --------------------- | -------------: | -----: | ---: |
| Number of tubes       |            $N$ |     48 |    - |
| Tube outside diameter |      $D_{out}$ |  0.020 |    m |
| Tube inside diameter  |       $D_{in}$ |  0.016 |    m |
| Tube wall thickness   |     $x_{tube}$ |  0.002 |    m |
| Tube pitch            |          $p_t$ |  0.025 |    m |
| Tube length           |            $L$ |  4.002 |    m |
| Bundle diameter       |   $D_{bundle}$ |  0.232 |    m |
| Shell clearance       |    $C_{shell}$ |  0.011 |    m |
| Shell inside diameter | $D_{shell,in}$ |  0.243 |    m |
| Shell wall thickness  |    $x_{shell}$ | 0.0041 |    m |
| Shell length          |    $L_{shell}$ |  4.028 |    m |
| Baffle spacing        |              - |  0.049 |    m |

The tube outside diameter, tube thickness, tube pitch and shell clearance values were within those recommended by literature [@coulson_richardson_shell_tube_nd]. Similarly, the formulas for the bundle diameter, shell thickness, shell inside diameter and and shell length were given, respectively:

$$
D_{bundle} = D_{out} \left(\frac{N}{a}\right)^{1/b}
$$

For the selected one-pass square-pitch arrangement, the constants used were [@coulson_richardson_shell_tube_nd]:

- $a = 0.215$
- $b = 2.207$

$$
x_{shell} = \frac{P D_{shell,in}}{2S} + CA
$$

where:

- $P$ is the operating pressure (selected to be 600000 $\text{Pa}$)
- $S$ is the allowable stress of the shell material, (120 $\text{MPa}$ for carbon steel [@asme_bpvc_vii_d_metric_2025])
- $CA$ is the corrosion allowance (0.0035 m, recommended by literature [@coulson_richardson_shell_tube_nd])

$$
D_{shell,in} = D_{bundle} + C_{shell}
$$

$$
L_{shell} = L + 2C_{shell} + x_{shell}
$$

The number of tubes was arbitrarily selected to comply with length recommendations and the chosen array. Inversely, tube length was calculated with the following formula [@bme_heat_exchangers_2_2024]:

$$
L = \frac{A}{N \pi D_{out}}
$$

The selected tube layout for both heat exchangers is a square, 90° tube array [@coulson_richardson_shell_tube_nd] which is displayed in Figure 7.5. This arrangement is suitable for both the condenser and later, the reboiler because it gives a simple and compact tube bundle geometry, while also allowing easier mechanical cleaning between tube rows compared with triangular layouts. This is useful for a preliminary design, since the condenser may require periodic inspection or cleaning due to possible solvent impurities.

\begin{figure}[H]
\centering
\includegraphics[width=0.6\textwidth]{figs/array.png}
\caption{Selected tube array.}
\label{fig:Selected tube array}
\end{figure}

The available outside tube surface area was checked using:

$A = N \pi D_{out} L = 48 \pi (0.020)(4.002) = 12.07 \text{ m}^2$

Therefore, the selected condenser geometry provides the required total heat transfer area.

The cooling-water mass flow rate was calculated from the sensible heat balance equation[@bme_heat_exchangers_2_2024]:

$$
Q = \dot{m}_w c_{p,w} \Delta T_{w}
$$

Where $\Delta T_{w}$ is the temperature difference of the cooling water (25°C). The calculated cooling-water mass flow rate was, after rearranging the previous equation:

$\dot{m}_w = \frac{Q}{c_{p,w} \Delta T_w} = 2.55 \text{ kg/s}$

The main hydraulic results for the cooling water are given in Table 7.4.

Table: Cooling water hydraulic results.
\label{tab:Cooling water hydraulic results}

| Parameter            |      Symbol |   Value | Unit |
| -------------------- | ----------: | ------: | ---: |
| Water mass flow rate | $\dot{m}_w$ |    2.55 | kg/s |
| Tube-side flow area  |  $A_{tube}$ | 0.00965 |   m² |
| Water velocity       |       $v_w$ |   0.270 |  m/s |
| Reynolds number      |      $Re_w$ | 5876.23 |    - |
| Prandtl number       |      $Pr_w$ |    4.81 |    - |
| Nusselt number       |      $Nu_w$ |   38.82 |    - |

As the IPA vapour changes phase, it will form a saturated liquid film along the surface of the tube walls. In order to accurately estimate the required temperature of the tube walls to carry out this heat transfer operation, the temperature difference across the film must be accounted for. The calculated wall and film temperatures can be observed in Table 7.5.

Table: Condenser wall and film temperatures.
\label{tab:Condenser wall and film temperatures}

| Parameter                        |                     Symbol | Value [°C] |
| -------------------------------- | -------------------------: | ---------: |
| Real mean wall temperature       | $\overline{T}_{wall,real}$ |      68.62 |
| Calculated mean wall temperature | $\overline{T}_{wall,calc}$ |      70.00 |
| Mean film temperature            |      $\overline{T}_{film}$ |      75.00 |
| Film temperature difference      |          $\Delta T_{film}$ |      10.00 |

The value of the film temperature difference was chosen by iteration, performed until the calculated wall temperature was close to the real wall temperature. A normal temperature difference interval between the film and wall temperatures is of around 5 to 15°C.

The calculated mean wall temperature could be obtained from the mean temperature of the condensed vapour or distillate $\overline{T}_{dist}$, and the film temperature difference:

$$
\overline{T}_{wall,calc} = \overline{T}_{dist} - \Delta T_{film}
$$

The real, mean wall temperature was calculated to be [@bme_heat_exchangers_2_2024]:

$$
\overline{T}_{wall,real} = T_{dist} - \frac{k_{dirty}}{\alpha_{cond}}(T_{dist} - \overline{T}_{w})
$$

Where $\overline{T}_{w}$ is the mean temperature of the water.

The small difference between the real and calculated wall temperatures shows that the assumed film temperature difference is acceptable for the preliminary condenser design. All other calculated parameters are realistic for the scale of the process and adequate for manufacturing.

## Column Reboiler Design

The reboiler was designed as a kettle reboiler. Although it is not a traditional shell-and-tube heat exchanger in the same way as the condenser, it still uses a tube bundle to transfer heat from condensing steam to the process liquid. The reboiler was designed as a two-pass heat exchanger arrangement, with the listed heat transfer area representing the total heat transfer area.

A kettle reboiler is more suitable for this project than a jacketed tank or internal coils since they are mainly used for heating agitated vessels, where the liquid temperature changes with time. In this case, the required duty is continuous vaporization at the bottom of the column. A kettle reboiler provides a submerged tube bundle with a large heat transfer surface, allowing the liquid to boil directly on the shell side while also providing enough volume for vapour-liquid disengagement [@perry_green_2008_heat_mass_transfer].

The DMSO-rich liquid properties were obtained from ChemCAD using the relevant column-bottom composition, while the steam-side properties were obtained from a saturated steam table [@cengel_ghajar_2011]. The obtained values are showcased below, in Table 7.6.

Table: Material properties of DMSO and steam.
\label{tab:Properties of DMSO and steam}

| Property                                          |     Value | Unit              |
| ------------------------------------------------- | --------: | ----------------- |
| vapor density of DMSO $\rho_{DMSO,vap}$           |       2.1 | $\text{kg/m}^3$   |
| liquid density of DMSO $\rho_{DMSO}$              |     927.4 | $\text{kg/m}^3$   |
| latent heat of DMSO $r_{DMSO}$                    |    605000 | $\text{J/kg}$     |
| specific heat capacity of DMSO $c_{p,DMSO}$       |      2323 | $\text{J/(kg*K)}$ |
| surface tension of DMSO $\sigma_{DMSO}$           |     0.022 | $\text{N/m}$      |
| thermal conductivity of DMSO $\lambda_{DMSO}$     |       0.1 | $\text{W/(m*K)}$  |
| dynamic viscosity of DMSO $\mu_{DMSO}$            |   0.00042 | $\text{N*s/m}^2$  |
| temperature of DMSO $T_{DMSO}$                    |       190 | °C                |
| thermal conductivity of steam $\lambda_{st,film}$ |   0.65455 | $\text{W/(m*K)}$  |
| liquid density of steam $\rho_{st,film}$          |     848.7 | $\text{kg/m}^3$   |
| vapor density of steam $\rho_{st,v}$              |    10.286 | $\text{kg/m}^3$   |
| dynamic viscosity of steam $\mu_{st,film}$        | 0.0001262 | $\text{N*s/m}^2$  |
| latent heat of steam $r_{st}$                     |   1887700 | $\text{J/kg}$     |
| specific heat capacity of steam $c_{p,st}$        |    4571.5 | $\text{J/(kg*K)}$ |
| temperature of steam $T_{st}$                     |       220 | °C                |

In this case, it was not necessary to calculate the logarithmic temperature difference, since the steam temperature was chosen and the temperature of the bottoms is known (see Figure 7.6). Furthermore, the heat duty is known.

\begin{figure}[H]
\centering
\includegraphics[width=0.8\textwidth]{figs/bottomT.png}
\caption{Bottom temperature as a function of time, highest temperature was selected (190°C).}
\label{fig:Bottom temperature as a function of time}
\end{figure}

\begin{figure}[H]
\centering
\includegraphics[width=\textwidth]{figs/steam.png}
\caption{Steam table.}
\label{fig:steam table}
\end{figure}

The steam table used can be seen in Figure 7.7. A saturated steam pressure of 23.2 bar corresponds to the selected saturated steam temperature. A design steam pressure of 24 bar was selected for wall thickness selection, to provide an extra margin of safety.

The design equation used for the reboiler was:

$$ Q = k A F \Delta T $$

Rearranging for heat transfer area:

$$ A = \frac{Q}{k F \Delta T} $$

The DMSO-rich liquid temperature was taken to be $T_{DMSO} = 190^\circ C$. The heating steam temperature was then chosen as $T_{st} = 220^\circ C$, for an adequate temperature difference of $\Delta T = 30^\circ C$. This will allow for proper heat transfer without overheating the DMSO, which properties are to be taken as reference since it possesses the highest boiling resistance. For stages where DMSO does not make up most of the bottom liquid, the pressure of steam (and therefore the temperature) is to be decreased with a control system. At higher temperatures, a peak and then a rapid decrease in the value of the heat transfer coefficient can be observed [@fonyo_fabry_2004]. An illustration of this phenomenon with water as an example is illustrated in Figure 7.7.

\begin{figure}[H]
\centering
\includegraphics[width=0.6\textwidth]{figs/bookgraph.png}
\caption{Heat-transfer coefficient during the boiling of water. Small values of $T$ ($\theta$ in the plot) correspond to free-convective boiling up to point A in the figure. For larger values of $T$, nucleate boiling occurs. The maximum point marked as B in the figure occurs at a critical value of $T$ characteristic of the liquid, which is around $25^\circ C$ for water.}
\label{fig:Heat-transfer coefficient during the boiling of water.}
\end{figure}

The reboiler heat duty was $Q = 1000 \text{ MJ/h}$. Converting to watts:

$Q = \frac{1000 \times 10^6}{3600} = 277777.78 \text{ W}$

Using the initially assumed overall heat transfer coefficient for phase change $k = 850 \text{ W/m}^2\text{K}$, the preliminary heat transfer area was:

$A = \frac{277777.78}{850 \times 30} = 10.89 \text{ m}^2$

This initial estimate was corrected by calculating the individual boiling-side and steam-condensation-side heat transfer coefficients.

The boiling-side heat transfer coefficient for the process was calculated using the pool-boiling correlation [@perry_green_2008_heat_mass_transfer]:

$$
\alpha_{boiling} = 0.225 \left[\left(\frac{Q \cdot c_p}{A \cdot r}\right)^{0.69}
\left(\frac{P \cdot \lambda}{\sigma}\right)^{0.31}
\left(\frac{\rho_l}{\rho_v}\right)^{0.33}\right]
$$

where:

- $\alpha_{boiling}$ = boiling-side heat transfer coefficient, W/m²K
- $Q$ = heat duty, W
- $A$ = heat transfer area, m²
- $c_p$ = liquid specific heat capacity, J/kgK
- $r$ = latent heat of vaporization, J/kg
- $P$ = operating pressure, Pa
- $\lambda$ = liquid thermal conductivity, W/mK
- $\sigma$ = surface tension, N/m
- $\rho_l$ = liquid density, kg/m³
- $\rho_v$ = vapour density, kg/m³

These values for DMSO were obtained from ChemCAD reports and listed at the beginning of the subchapter.

$\alpha_{shell} = 2261.06 \text{ W/m}^2\text{K}$

The steam-side condensation coefficient was calculated using the filmwise-condensation method. The inside coefficient was first calculated and then converted to the outside tube surface basis [@bme_heat_exchangers_2_2024]:

$\alpha_{st,out} = \alpha_{st,in} \frac{D_{in}}{D_{out}}$

The calculated reboiler heat transfer coefficients are displayed in Table 7.7.

Table: Reboiler heat transfer coefficients.
\label{tab:Reboiler heat transfer coefficients}

| Parameter                                     |            Symbol |    Value |  Unit |
| --------------------------------------------- | ----------------: | -------: | ----: |
| Boiling-side coefficient                      |  $\alpha_{shell}$ |  2261.06 | W/m²K |
| Steam condensation coefficient, inside basis  |  $\alpha_{st,in}$ | 12152.33 | W/m²K |
| Steam condensation coefficient, outside basis | $\alpha_{st,out}$ | 10194.74 | W/m²K |
| Clean overall coefficient                     |       $k_{clean}$ |  1708.92 | W/m²K |
| Fouling resistance                            |             $R_f$ |  0.00026 | m²K/W |
| Dirty overall coefficient                     |       $k_{dirty}$ |  1183.20 | W/m²K |

The clean overall heat transfer coefficient was calculated as:

$\frac{1}{k_{clean}} = \frac{1}{\alpha_{st,out}} + \frac{x_{tube}}{\lambda_{wall}} + \frac{1}{\alpha_{shell}}$

The dirty overall heat transfer coefficient was calculated by including the fouling resistance [@perry_green_2008_heat_mass_transfer]:

$\frac{1}{k_{dirty}} = \frac{1}{k_{clean}} + R_f$

$k_{dirty} = 1183.20 \text{ W/m}^2\text{K}$

The correction factor for the two-pass heat exchanger was possible to compute:

$F = 1$

From the correction factor diagram for a two-pass heat exchanger (see Figure 7.9).

\begin{figure}[H]
\centering
\includegraphics[width=0.8\textwidth]{figs/Fgraph1.png}
\caption{Correction factor for a two-pass heat exchanger.}
\label{fig:Correction factor for a two-pass heat exchanger}
\end{figure}

Using the dirty overall coefficient, the corrected reboiler heat transfer area was:

$A_{calc} = \frac{Q}{k_{dirty} F \Delta T} = \frac{277777.78}{1183.20 \times 30} = 7.83 \text{ m}^2$

Therefore, the required total reboiler heat transfer area is 7.83 $\text{ m}^2$

The selected reboiler geometry is shown below, in Table 7.8. The same formulas and values obtained from literature used in subchapter 7.1, were applied in this subchapter [@coulson_richardson_shell_tube_nd]. Tube wall thickness was selected to be compatible with high pressure steam.

Table: Selected and calculated reboiler geometry.
\label{tab:Selected and calculated reboiler geometry}

| Parameter             |         Symbol |   Value | Unit |
| --------------------- | -------------: | ------: | ---: |
| Number of tubes       |            $N$ |      28 |    - |
| Tube outside diameter |      $D_{out}$ |  0.0250 |    m |
| Tube inside diameter  |       $D_{in}$ |  0.0210 |    m |
| Tube wall thickness   |     $x_{tube}$ | 0.00202 |    m |
| Tube pitch            |          $p_t$ |  0.0313 |    m |
| Tube length           |            $L$ |    1.78 |    m |
| Bundle diameter       |   $D_{bundle}$ |   0.227 |    m |
| Shell clearance       |    $C_{shell}$ |   0.011 |    m |
| Shell inside diameter | $D_{shell,in}$ |   0.477 |    m |
| Shell wall thickness  |    $x_{shell}$ | 0.00493 |    m |

The tube length was calculated from the total required heat transfer area, dividing the result by 2 since the configuration will have two tube passes. This means that the length of the tubes need to be half the size as for a single pass, while the shell diameter will double [@bme_heat_exchangers_2_2024]. The formula used to compute the tube length was:

$$
L = \frac{A}{2N \pi D_{out}} = \frac{7.83}{2(28)\pi(0.0250)} = 1.78 \text{ m}
$$

The steam mass flow rate was calculated from the latent heat balance formula [@bme_heat_exchangers_2_2024]:

$$
\dot{m}_{st} = \frac{Q}{r_{st}} = \frac{277777.78}{1887700} = 0.147 \text{ kg/s}
$$

The main steam-side values related to flow rate were also computed, using the same formula for flow cross-sectional area and velocity as in the previous chapter. Results are listed in Table 7.9

Table: Steam flow rate parameters.
\label{tab:Steam flow rate parameters}

| Parameter            |         Symbol |   Value | Unit |
| -------------------- | -------------: | ------: | ---: |
| Steam mass flow rate | $\dot{m}_{st}$ |   0.147 | kg/s |
| Tube-side flow area  |     $A_{tube}$ | 0.00485 |   m² |
| Steam velocity       |       $v_{st}$ |    2.95 |  m/s |

Similarly, film and wall mean temperature results could be obtained by utilizing the same formulas as in the case of the condenser, but assuming that this time it will be steam forming a film around the tubes as it condenses. The calculated and selected film and wall temperatures are found in Table 7.10.

Table: Reboiler wall and film temperatures.
\label{tab:Reboiler wall and film temperatures}

| Parameter                   |                     Symbol | Value [°C] |
| --------------------------- | -------------------------: | ---------: |
| Real wall temperature       | $\overline{T}_{wall,real}$ |     204.30 |
| Calculated wall temperature | $\overline{T}_{wall,calc}$ |     205.00 |
| Film temperature            |      $\overline{T}_{film}$ |     212.50 |
| Film temperature difference |          $\Delta T_{film}$ |      15.00 |

The small difference between the real and calculated wall temperatures confirms that the assumed film temperature is acceptable for the preliminary kettle reboiler calculation.

All calculated parameters are realistic for the scale of the process and adequate for the manufacturing of parts for this reboiler.

## Selection of Heat Exchanger Construction Types

The condenser was selected as a conventional one-pass shell-and-tube heat exchanger. Since the exchanger is relatively small and the temperature difference is moderate, a fixed-tube-sheet construction is suitable. For the front-end stationary head, a removable channel and cover is selected so that the tube side can be accessed for inspection and cleaning. The selected front-end type is therefore TEMA type A [@coulson_richardson_shell_tube_nd]. The shell is selected as a one-pass shell, corresponding to TEMA shell type E. The rear-end head is selected as a fixed-tube-sheet rear channel with removable cover, corresponding to TEMA rear-end type L. Therefore, the selected condenser construction is:

$AEL$

where:

- $A$ = front-end stationary head with removable channel and cover
- $E$ = one-pass shell
- $L$ = fixed-tube-sheet rear end with removable cover

\begin{figure}[H]
\centering
\includegraphics[width=0.8\textwidth]{figs/arrange.png}
\caption{TEMA-type designations for shell-and-tube heat exchangers.}
\label{fig:TEMA-type designations for shell-and-tube heat exchangers}
\end{figure}

This construction is appropriate for a normal one-pass condenser because it is mechanically simple, allows tube-side access, and provides the required heat transfer area.

The reboiler was selected as a kettle-type reboiler rather than a conventional shell-and-tube heat exchanger. For this reason, the shell type must correspond to a kettle arrangement. The selected shell type is therefore TEMA type K [@coulson_richardson_shell_tube_nd]. Since the reboiler uses a two-pass tube arrangement and must allow thermal expansion of the tube bundle, a U-tube rear-end construction is suitable. The selected rear-end type is TEMA type U. For the front-end stationary head, a bonnet-type head is selected because the tube-side fluid is condensing steam, which is relatively clean compared with process liquids. The selected front-end type is therefore TEMA type B. Therefore, the selected reboiler construction is:

$BKU$

where:

- $B$ = bonnet-type front-end stationary head
- $K$ = kettle-type shell
- $U$ = U-tube rear-end construction

This construction is appropriate for the kettle reboiler because the kettle shell provides space for boiling and vapour-liquid disengagement, while the U-tube arrangement allows thermal expansion and provides the required two-pass tube-side flow path.

\begin{figure}[H]
\centering
\includegraphics[width=0.6\textwidth]{figs/ket.png}
\caption{Diagram of a kettle-type reboiler \cite{processphase_2020}.}
\label{fig:Diagram of a kettle-type reboiler}
\end{figure}
