# Heat Recycling

Distillation is an energy-intensive separation process because heat must be supplied to the reboiler while it is simultaneously removed from the overhead vapour in the condenser. In the original configuration, a significant part of the thermal energy contained in the top vapour is rejected during condensation. For this reason, heat recycling was studied as a way to reduce the external heating demand of the column and improve the energetic efficiency of the process.

In this chapter, two heat recovery methods are investigated. The first method is the pre-heater method, in which the vapour leaving the top of the column during the IPA distillation is used as a heat source in a heat exchanger. This recovered heat is transferred to the DMSO feed stream before it enters the column, eliminating external energy required to pre-heat the feed. This method was simulated in ChemCAD using a simple heat exchanger model, as can be seen in Figure 8.1.

The second method is the heat pump method, in which the top vapour from the column is compressed in order to increase its temperature and make it suitable for heat recovery at the bottom of the column. The simulated arrangement includes two compressors with an inter-cooler, a heat exchanger, an expansion valve, and a second heat exchanger. In this configuration, heat is extracted from the compressed overhead vapour and used to help heat the column bottom, reducing the required reboiler heat load. This method was studied using a dynamic ChemCAD simulation. The top-vapour composition was introduced into the model at time steps of 0.05 h over the distillation operation.

The purpose of comparing these two methods is to determine how effectively the available overhead-vapour heat can be reused in the process. The pre-heater method represents a simpler and more direct heat-recovery option, while the heat pump method represents a more complex but potentially more powerful heat-integration strategy. Both methods are evaluated based on their ability to reduce external heat requirements and improve the energetic performance of the distillation process.

## Pre-heater Method

In the pre-heater method, the heat contained in the vapour leaving the top of the distillation column is used to pre-heat the DMSO feed before it enters the column. This reduces the amount of external heat required to bring the solvent feed to the selected inlet temperature. The simulation was carried out in ChemCAD using a heat exchanger, where the hot side corresponds to the overhead vapour and the cold side corresponds to the feed stream.

\begin{figure}[H]
\centering
\includegraphics[width=0.7\textwidth]{figs/preh.png}
\caption{ChemCAD simulation arrangement for the pre-heater calculations.}
\label{fig:ChemCAD simulation arrangement for the pre-heater calculation}
\end{figure}

We used the main design equation for the heat exchangers is, and the logarithmic mean temperature difference was calculated from the two terminal temperature differences:

$\Delta T_{log} = \frac{\Delta T_1 - \Delta T_2}{\ln \left(\frac{\Delta T_1}{\Delta T_2}\right)}$

where:

$\Delta T_1 = T_{1,1} - T_{2,1}$

$\Delta T_2 = T_{1,2} - T_{2,2}$

\begin{figure}[H]
\centering
\includegraphics[width=0.8\textwidth]{figs/prehT.png}
\caption{ChemCAD plot displaying the top vapour temperature during step 1. It was determined to be 82.4 °C.}
\label{fig:hemCAD plot displaying the top vapour temperature during step 1}
\end{figure}

We need to heat up the feed to increase its temperature from 20°C (room temperature) to 62°C. Since the vapour, which is almost pure IPA, experiences a phase change (condensation), its temperature can be assumed to remain constant [@bme_heat_exchangers_1_2024]. The temperatures used in the pre-heater calculation, in Kelvin, are shown in Table 8.1.

Table: Pre-heater temperatures.
\label{tab:Pre-heater temperatures}

| Parameter               |    Symbol |  Value | Unit |
| ----------------------- | --------: | -----: | ---: |
| Hot inlet temperature   | $T_{1,1}$ | 355.55 |    K |
| Hot outlet temperature  | $T_{1,2}$ | 355.55 |    K |
| Cold inlet temperature  | $T_{2,1}$ | 293.15 |    K |
| Cold outlet temperature | $T_{2,2}$ | 335.15 |    K |

Replacing the logarithmic mean temperature difference formula with these values:

$\Delta T_{log} = 37.57 \text{ K}$

The value of the total heat duty of this process, obtained from the ChemCAD heat-exchanger simulation, was:

$Q = 45.1324 \text{ MJ/h}$

This value was converted into watts:

$Q = \frac{45.1324 \times 10^6}{3600} = 12536.78 \text{ W}$

The calculated temperature differences and heat duty are summarized in Table 8.2.

Table: Pre-heater heat duty.
\label{tab:Pre-heater heat duty}

| Parameter               |           Symbol | Value | Unit |
| ----------------------- | ---------------: | ----: | ---: |
| Terminal T difference 1 |     $\Delta T_1$ | 62.40 |    K |
| Terminal T difference 2 |     $\Delta T_2$ | 20.40 |    K |
| LMTD                    | $\Delta T_{log}$ | 37.57 |    K |
| Heat duty               |              $Q$ | 45.13 | MJ/h |

Three possible heat transfer areas were calculated using different overall heat transfer coefficients. The first value, $k_{vap} = 850 \text{ W/m}^2\text{K}$, represents the assumed overall heat transfer coefficient for a change of phase in a heat exchanger. The second value, $k_{dist} = 570 \text{ W/m}^2\text{K}$ [@kiss_2013], represents an estimation of the required heat transfer coefficient for the condensation of IPA vapour. The third value, $k_{calc} = 534.4 \text{ W/m}^2\text{K}$, represents the calculated overall heat transfer coefficient used for the final conservative sizing. This is the heat transfer coefficient that was calculated for the main condenser of this column.

The highest calculated heat transfer area is obtained using the lowest overall heat transfer coefficient:

For $k_{calc} = 534.4 \text{ W/m}^2\text{K}$:

$A_{calc} = \frac{12536.78}{534.4 \times 37.57}$

$A_{calc} = 0.6245 \text{ m}^2$

Therefore, the selected required heat transfer area for the pre-heater is $0.6245 \text{ m}^2$.

The pre-heater therefore allows the feed to enter the distillation column at the selected feed temperature of 62°C using recovered heat from the overhead vapour. This decreases the amount of additional external energy that would otherwise be required to heat the feed before it enters the column. Not only would it efficiently save on energy, but also on costs. It provides a simple and practical way to recycle part of the heat contained in the overhead vapour, while its required size area is relatively small.

## Heat Pump Method

The second heat recycling method studied was the heat pump method. In this configuration, the vapour leaving the top of the distillation column is compressed. This makes the overhead vapour suitable for heat recovery at a higher temperature level. The recovered heat is then transferred to the bottom of the column, helping the reboiler supply the energy required for vaporization.

Before the final arrangement was selected, different compression ratios were investigated using a single compressor. The purpose of these trials was to determine whether the overhead vapour could be compressed sufficiently in one step to reach a useful temperature level for reboiler heat recovery. Several pressure ratios were tested, but the results showed that a single compressor was not suitable. Lower compression ratios did not increase the temperature enough for useful heat recovery over a sufficient part of the operation, while higher compression ratios produced excessively high outlet temperatures and unsuitable vapour-fraction behavior (the stream does not remain in the vapour phase during compression;condensation should occur only in the heat exchanger where useful heat is released to the reboiler.). Therefore, the final selected configuration used two compressors with an inter-cooler between them. Each compressor was operated with a compression ratio of 1:4.

The simulated heat pump arrangement in ChemCAD is displayed in Figure 8.3. It included two compressors, a first heat exchanger that acted as an inter-cooler between them (unit 1 in the figure), a second heat exchanger (unit 3 in the figure) with a set heat duty of -1000 MJ/h to represent the heat taken out by the reboiler (the heat duty of the reboiler for the all distillation simulations was set to 1000 MJ/h; therefore, theoretically, this amount of energy per hour that will be demanded), an expansion valve, and a third heat exchanger (unit 5 in the figure) that was used to calculate the amount of energy that could be recovered. After supplying heat to the reboiler, the remaining heat indicated by the heat exchanger could theoretically be used for secondary heating duties, such as pre-heating process streams, feed streams, or utility water.
The inter-cooler was required to reduce the vapour temperature between compression stages and to avoid excessively high temperatures after the second compressor. It was set to superheat the compressed vapour stream in order to keep the working fluid in gaseous state, and cooling was assumed to be done with room-temperature cooling water (25°C). The heat transfer coefficient of the IPA-rich fluid was given as k = 150 $\text{ W/m}^2\text{K}$ by literature [@perry_green_2008_heat_mass_transfer], which was applied as the inter-cooler heat transfer coefficient.

\begin{figure}[H]
\centering
\includegraphics[width=0.9\textwidth]{figs/heatp.png}
\caption{ChemCAD heat pump simulation arrangement.}
\label{fig:ChemCAD heat pump simulation arrangement}
\end{figure}

The simulation was carried out dynamically using ChemCAD data maps and Excel coding. The input vapour composition and temperature at each time step was obtained from ChemCAD reports for the top vapour stream, these values were out-putted as a large excel table. Our excel file was programmed to transfer the data values to a specific cell in the document every 0.05 h. ChemCAD then read these values through a data map and used them as inputs for the heat pump simulation. In the same way, the output values from ChemCAD were exported back into Excel every 0.05 h and stored in a second table.

The main outputs recorded were the temperature after compression, vapour fraction after compression, temperature after the first heat exchanger, vapour fraction after the first heat exchanger, heat duty of the second heat exchanger, inter-cooler heat duty, compressor duties, cooling-water outlet temperature, and logarithmic mean temperature difference. Although the full simulation was carried out over the complete operation, the heat pump was found to be suitable only during the first 4.5 h of the distillation. As the batch progressed, the recoverable heat decreased, and later the temperature difference became too small for practical heat transfer; in some later intervals, heat input would even be required instead of useful heat recovery. Therefore, only this time interval was considered for the useful heat recovery evaluation.

### Input Vapour Stream

The input vapour stream composition changes continuously during the batch distillation. The dynamic heat pump simulation therefore required the vapour composition to be updated at each time step. Table 8.3 shows representative values from the input table, using 0.5 h intervals up to 4.5 h. After 4.5 hours had passed, the output results from the simulation were not good enough for efficient heat recycling anymore.

Table: Heat pump input values.
\label{tab:Heat pump input values}

| Time [h] | Bottom Temperature [°C] | IPA vapour flow rate [kmol/h] | H₂O vapour flow rate [kmol/h] | DMSO vapour flow rate [kmol/h] |
| -------: | ----------------------: | ----------------------------: | ----------------------------: | -----------------------------: |
|     0.50 |                   81.82 |                       23.6395 |                        0.0129 |                       0.000263 |
|     1.00 |                   83.57 |                       23.5455 |                        0.0116 |                       0.000263 |
|     1.50 |                   85.44 |                       23.4585 |                        0.0106 |                       0.000263 |
|     2.00 |                   87.43 |                       23.3680 |                        0.0098 |                       0.000263 |
|     2.50 |                   89.56 |                       23.2690 |                        0.0092 |                       0.000263 |
|     3.00 |                   91.82 |                       23.1535 |                        0.0085 |                       0.000263 |
|     3.50 |                   94.26 |                       23.0215 |                        0.0080 |                       0.000262 |
|     4.00 |                   96.89 |                       22.8661 |                        0.0075 |                       0.000262 |
|     4.50 |                   99.75 |                       22.6821 |                        0.0070 |                       0.000262 |

As shown in Table 5, the IPA vapour flow rate slowly decreases during the first 4.5 h, while the bottom temperature increases from approximately 80°C to nearly 100°C. The DMSO vapour flow rate remains very small compared with the IPA vapour flow rate. This is expected because DMSO has a much higher boiling point and remains mainly in the liquid phase.

### Heat Pump Output Results

Table 8.3 shows the main output values obtained from the ChemCAD heat pump simulation. The table includes only the useful operating region up to 4.5 h. The abbreviations shown in the column titles stand for:

- VF: Vapour fraction
- IC: inter-cooler
- HX1: second heat exchanger (first if the inter-cooler is not counted)
- HX2: third heat exchanger (second of the inter-cooler is not counted)
- C1: first compressor
- C2: second compressor

Table: Heat pump output values.
\label{tab:Heat pump output values}

| Time [h] | T after comp. [°C] | VF after C2 | T after HX1 [°C] | VF after HX1 | HX2 duty [MJ/h] | IC duty [MJ/h] | C1 duty [MJ/h] | C2 duty [MJ/h] | LMTD [K] |
| -------: | -----------------: | ----------: | ---------------: | -----------: | --------------: | -------------: | -------------: | -------------: | -------: |
|     0.50 |             177.21 |        1.00 |           114.36 |         0.00 |          164.31 |          23.97 |          97.18 |          99.29 |    89.36 |
|     1.00 |             177.21 |        1.00 |           113.62 |         0.00 |          159.62 |          23.87 |          96.79 |          98.89 |    89.41 |
|     1.50 |             177.21 |        1.00 |           112.93 |         0.00 |          155.30 |          23.77 |          96.43 |          98.52 |    89.46 |
|     2.00 |             177.20 |        1.00 |           112.20 |         0.00 |          150.79 |          23.68 |          96.05 |          98.13 |    89.51 |
|     2.50 |             177.20 |        1.00 |           111.39 |         0.00 |          145.88 |          23.57 |          95.64 |          97.71 |    89.57 |
|     3.00 |             177.20 |        1.00 |           110.45 |         0.00 |          140.18 |          23.45 |          95.17 |          97.23 |    89.64 |
|     3.50 |             177.20 |        1.00 |           109.36 |         0.00 |          133.65 |          23.32 |          94.62 |          96.67 |    89.71 |
|     4.00 |             177.20 |        1.00 |           108.05 |         0.00 |          125.97 |          23.16 |          93.98 |          96.01 |    89.80 |
|     4.50 |             177.20 |        1.00 |           106.47 |         0.00 |          116.89 |          22.97 |          93.22 |          95.24 |    89.90 |

The results show that the vapour fraction after compression remains equal to 1.00 during the useful period, meaning that the stream remains fully vapour after compression. After the first heat exchanger, the vapour fraction becomes 0.00, meaning that the compressed vapour is condensed and heat is successfully extracted. This confirms that the heat pump arrangement works properly during the first 4.5 h.

The time-zero value is treated as a start-up point and is not considered representative of stable heat pump operation, therefore 0.05 h is the initial time value. The heat duty of the second heat exchanger decreases in magnitude during the useful operating period, from approximately 169.40 MJ/h at 0.05 h to 116.89 MJ/h at 4.5 h. This shows that the amount of useful recoverable heat decreases as the batch distillation progresses, and that the method would be most efficient when only applied during the first 4.5 hours. During the time interval 7.5 h - 9.5 h, the heat duty becomes negative, meaning that the expanded working fluid remains sub-cooled liquid, and heating would be required to obtain a saturated liquid reflux. This would make recovery definitely not viable during this range. The compressor heat duties also decrease slightly over time, while the logarithmic mean temperature difference remains almost constant, close to 89–90 °C. Furthermore, the temperature difference between the input vapour and output liquid after heat recovery decreases to less than 10 °C, which is not suitable for efficient heat transfer applications [@kiss_2013], [@kemp_2007].

### Useful Heat Pump Operation

The useful heat pump operating period and the energy demand of the whole configuration can be summarized in Table 8.4.

Table: Useful heat pump period.
\label{tab:Useful heat pump period}

| Parameter              |  Value | Unit |
| ---------------------- | -----: | ---: |
| Start time             |   0.05 |    h |
| End time               |   4.50 |    h |
| Max. HX2 duty          | 169.40 | MJ/h |
| Max. inter-cooler duty |  24.08 | MJ/h |
| Max. compressor 1 duty |  97.61 | MJ/h |
| Max. compressor 2 duty |  99.72 | MJ/h |
| Avg. LMTD              |  89.57 |    K |

Using the maximum compressor duties as a conservative estimate, the energy needed to operate the heat pump for 4.5 h is:

$$
(97.61 + 99.72)\times 4.5 = 888\ \text{MJ}
$$

However, the heat pump will replace the duty of the reboiler duty during this time period, which was assumed to be $1000\ \text{MJ/h}$ throughout the entire process. Therefore, the total energy demand in this period is:

$$
1000\times 4.5 = 4500\ \text{MJ}
$$

The net energy saving is therefore approximately:

$$
4500 - 887.985 = 3612.015\ \text{MJ}
$$

This means that, from an energy-balance point of view, the heat pump is viable since the energy recovered for the reboiler is much greater than the compressor energy required. This method can be considered energetically beneficial as a partial heat-recovery option, but its final practical viability must also consider its higher equipment complexity and capital cost, since it requires two compressors, an inter-cooler, an expansion valve, and additional heat exchangers.

For future cost estimation, the inter-cooler's maximum heat duty and heat transfer area were used.

Conversion to watts:

$Q_{max} = \frac{24.08 \times 10^6}{3600} = 6688.01 \text{ W}$

Assuming cooling water is heated from 25°C to 50°C:

$\dot{m}_{w} = \frac{Q}{c_p \Delta T}$

Using $c_p = 4180 \text{ J/kgK}$ and $\Delta T = 25 \text{ K}$:

$\dot{m}_{w} = \frac{6688.01}{4180 \times 25} = 0.0640 \text{ kg/s}$

$\dot{m}_{w} = 230.40 \text{ kg/h}$

The logarithmic mean temperature difference calculated was:

$\Delta T_{log} = 88.46 \text{ K}$

Assuming the inter-cooler is a single pass heat exchanger, the correction factor F was calculated to be 1 from correction factor chart for a single-pass heat exchanger [@coulson_richardson_shell_tube_nd].

Using $k = 150 \text{ W/m}^2\text{K}$ as the heat transfer coefficient for this application [@perry_green_2008_heat_mass_transfer], The heat transfer area was calculated using the heat transfer area equation for heat exchangers:

$A = \frac{6688.01}{150 \times 88.46} = 0.501 \text{ m}^2$

## Method Comparison

For the pre-heater method, the recovered overhead-vapour heat is used to heat the feed before it enters the column. The total recovered energy is $45 \times 9.05 = 407.25\ \text{MJ}$. Therefore, only about $(50-45)\times 9.05 = 45.25\ \text{MJ}$ of additional external feed-heating energy would still be required. In comparison, the heat pump method can replace $1000 \times 4.5 = 4500\ \text{MJ}$ of reboiler energy during its useful 4.5 h operating period. It requires more energy to operate, but the net energy saving is around 3600 MJ. Therefore, the heat pump method is clearly superior from a net energy-saving perspective. However, the heat pump method is much more complex and requires additional equipment, including two compressors, an inter-cooler, an expansion valve, and additional heat exchangers. Its main disadvantage is that it is only useful for a limited part of the batch operation and requires significant compressor work. For this reason, the heat pump method may be useful as a partial heat-recovery option, but it is more complicated and less broadly applicable than the pre-heater method, as well as more costly.
