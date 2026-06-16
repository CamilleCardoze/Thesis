# Cost Estimation

The cost estimation of the distillation system was carried out using preliminary equipment cost correlations. This type of estimation is suitable for conceptual design because it allows the main process equipment costs to be estimated from the principal sizing parameters, such as heat-transfer area, column diameter, column height, tank dimensions, and compressor horsepower. The objective of this chapter is not to obtain a final vendor quotation, but to estimate the relative investment required for the main distillation system and for the two heat recycling alternatives.

The equipment cost correlations were taken from Douglas, where purchased equipment costs are estimated from equipment size and then corrected to installed costs using installation factors. Since the original correlations are based on an older cost index, the Marshall and Swift index correction was applied. The Marshall & Swift index used in this calculation, for the year 2020, was [cite]:

$MS = 2171.6$

Two tanks were assumed: one tank for the pot charge and one tank for the distillate.

## Energy Cost estimation

The energy cost was estimated from the reboiler duty and the additional energy required to heat the DMSO feed from 20°C to 62°C. As of 2013 in the United States, literature reports a general electricity cost of approximately [cite]:

$$
C_{\mathrm{energy}} = 16.8\ \text{\$} / \mathrm{GJ}
$$

This value was used as the unit energy cost for the preliminary estimation. The energy cost was calculated by multiplying the total energy demand by this unit cost:

$$
C = Q_{\mathrm{total}} \cdot C_{\mathrm{energy}}
$$

For the main IPA distillation step, the reboiler operated for 9.05 h at 1000 MJ/h:

$$
Q_{\mathrm{reb,main}} = 1000 \cdot 9.05 = 9050\ \mathrm{MJ} = 9.05\ \mathrm{GJ}
$$

The DMSO feed-heating duty was approximately 50 MJ/h. Since the feed is heated during the main distillation step:

$$
Q_{\mathrm{feed}} = 50 \cdot 9.05 = 452.5\ \mathrm{MJ} = 0.4525\ \mathrm{GJ}
$$

Therefore, the total energy required for the main IPA distillation step was:

$$
Q_{\mathrm{main,total}} = 9.05 + 0.4525 = 9.5025\ \mathrm{GJ}
$$

$$
C_{\mathrm{main}} = 9.5025 \cdot 16.8 = 159.64\ \text{\$}
$$

For the complete process, with a total elapsed time of 16.15 h:

$$
Q_{\mathrm{reb,total}} = 1000 \cdot 16.15 = 16150\ \mathrm{MJ} = 16.15\ \mathrm{GJ}
$$

Adding the same feed-heating energy:

$$
Q_{\mathrm{process,total}} = 16.15 + 0.4525 = 16.6025\ \mathrm{GJ}
$$

$$
C_{\mathrm{process}} = 16.6025 \cdot 16.8 = 278.92\ \text{\$}
$$

Therefore, using the energy cost reported by literature [@kiss_2013], the estimated energy cost is approximately 159.64 $\text{\$}$ for the main IPA distillation step and 278.92 $\text{\$}$ for the complete process.

## Heat Exchanger Cost Estimation

The heat-transfer areas used for the cost estimation were obtained from the previously calculated exchanger duties and temperature differences.

The resulting areas were converted from square meters to square feet using:

$1 \text{ m}^2 = 10.764 \text{ ft}^2$

The corrected heat-transfer areas used in the cost estimation are shown in the table below, their values converted from meters to feet, in order to follow the calculations from our selected literature.

Table: Corrected heat-transfer areas used for cost estimation.
\label{tab:Corrected heat-transfer areas used for cost estimation.}

| Equipment    | Area [ft²] |
| ------------ | ---------: |
| Condenser    |     112.59 |
| Reboiler     |      84.04 |
| Inter-cooler |       5.39 |
| Pre-heater   |       6.65 |

The purchased cost of a heat exchanger was calculated as [cite]:

$C_{p,HX} = \frac{MS}{280} \left(101.3 A^{0.65} F_c \right)$

where:

- $C_{p,HX}$ = purchased heat exchanger cost, in $
- $A$ = heat-transfer area, in ft²
- $F_c$ = correction factor
- $MS$ = Marshall and Swift index

The installed cost was calculated using [cite]:

$C_{i,HX} = \frac{MS}{280} \left(101.3 A^{0.65}(F_c + 2.29)\right)$

Since high-pressure steam was used as the heating utility for the reboiler, its cost was added directly to the installed cost of the reboiler. According to Kiss, the cost of high-pressure steam at 42 bar is [cite]:

$C_{HPS} = 9.88\ \text{\$/GJ}$

The cost of high-pressure steam was estimated from the reboiler heat duty and the operating time [cite]:

$C_{steam} = Q_{reb} \cdot t \cdot C_{HPS}$

Using:

$Q_{reb} = 1000\ \text{MJ/h} = 1.00\ \text{GJ/h}$

$t = 16.15\ \text{h}$

$C_{HPS} = 9.88\ \text{\$/GJ}$

The high-pressure steam cost per batch is:

$C_{steam} = 1.00 \times 16.15 \times 9.88 = 159.56\ \text{\$/batch}$

Therefore, the corrected installed cost of the reboiler is:

$C_{i,reb,corr} = C_{i,reb} + C_{steam}$

$C_{i,reb,corr} = 54463.99 + 159.56 = 54623.55\ \text{\$}$

The heat exchanger cost results are shown.

Table: Heat exchanger cost estimation results.
\label{tab:Heat exchanger cost estimation results.}

| Equipment    | Area [ft²] | $F_c$ | Purchased [$\text{\$}$] | Installed [$\text{\$}$] |
| ------------ | ---------: | ----: | ----------------------: | ----------------------: |
| Condenser    |     112.59 |  0.80 |                13545.58 |                52319.82 |
| Reboiler     |      84.04 |  1.60 |                22401.64 |                54623.55 |
| Inter-cooler |       5.39 |  0.80 |                 1879.36 |                 7259.03 |
| Pre-heater   |       6.65 |  0.80 |                 2154.16 |                 8320.45 |

The condenser and reboiler are part of the base distillation system. The inter-cooler is only required for the heat pump method, while the pre-heater is only required for the pre-heater heat recycling method. The corrected installed reboiler cost includes the estimated high-pressure steam cost for one complete batch.

## Tank Cost Estimation

Two tanks were included in the cost estimation: one for the pot charge and one for the distillate. The tank dimensions used in the calculation are shown in the table below.

Table: Tank sizing values.
\label{tab:Tank sizing values.}

| Parameter         | Symbol | Value | Unit |
| ----------------- | -----: | ----: | ---: |
| Tank height       |    $H$ |  8.20 |   ft |
| Tank diameter     |    $D$ |  6.56 |   ft |
| Number of tanks   |    $N$ |     2 |    - |
| Correction factor |  $F_c$ |  1.00 |    - |

The purchased cost of the two tanks was calculated as [cite]:

$C_{p,tank} = 2 \frac{MS}{280} \left(101.9 D^{1.066} H^{0.802} F_c \right)$

Substituting the selected tank dimensions:

$C_{p,tank} = 63463.52 \text{\$}$

The installed cost of the two tanks was calculated as:

$C_{i,tank} = 2 \frac{MS}{280} \left(101.9 D^{1.066} H^{0.802}(F_c + 2.18)\right)$

Substituting the selected values:

$C_{i,tank} = 201814.01 \text{\$}$

## Column Cost Estimation

The cost of the distillation column was estimated using the column height and diameter. The column dimensions used in the cost estimation are shown in the following table:

Table: Column sizing values.
\label{tab:Column sizing values.}

| Parameter         | Symbol | Value | Unit |
| ----------------- | -----: | ----: | ---: |
| Column height     |    $H$ | 32.80 |   ft |
| Column diameter   |    $D$ |  2.13 |   ft |
| Correction factor |  $F_c$ |  1.05 |    - |

The purchased cost of the column shell was calculated using [cite]:

$C_{p,col} = \frac{MS}{280} \left(101.9 D^{1.066} H^{0.802} F_c \right)$

Substituting the selected values:

$C_{p,col} = 30532.95 \text{\$}$

The installed cost of the column shell was calculated as [cite]:

$C_{i,col} = \frac{MS}{280} \left(101.9 D^{1.066} H^{0.802}(F_c + 2.18)\right)$

Substituting the selected values:

$C_{i,col} = 93925.17 \text{\$}$

## Compressor Cost Estimation

The compressor costs correspond to the heat pump method. Two compressors are required, one for each compression stage. The compressor powers were obtained from the heat pump simulation and converted into horsepower, as shown in the following table:

Table: Compressor power values.
\label{tab:Compressor power values.}

| Equipment    | Power [hp] |
| ------------ | ---------: |
| Compressor 1 |      36.36 |
| Compressor 2 |      37.15 |

The purchased compressor cost was calculated using the formula [cite]:

$C_{p,comp} = \frac{MS}{280} \left(51.75 HP^{0.82} F_t \right)$

Since two compressors are required:

$C_{p,comp,total} = \frac{MS}{280} \left(51.75 HP_1^{0.82} F_t \right) + \frac{MS}{280} \left(51.75 HP_2^{0.82} F_t \right)$

where:

- $HP_1$ = horsepower of compressor 1
- $HP_2$ = horsepower of compressor 2
- $F_t$ = compressor correction factor

Using:

$HP_1 = 36.36$

$HP_2 = 37.15$

$F_t = 1$

The total purchased compressor cost is:

$C_{p,comp,total} = 15420.85 \text{\$}$

The installed compressor cost was calculated using:

$C_{i,comp,total} = \frac{MS}{280} \left(51.75 HP_1^{0.82}(F_t + 2.11)\right) + \frac{MS}{280} \left(51.75 HP_2^{0.82}(F_t + 2.11)\right)$

Substituting the values:

$C_{i,comp,total} = 47958.84 \text{\$}$

Therefore, the installed cost of the two compressors required for the heat pump method is:

$C_{i,comp,total} = 47958.84 \text{\$}$

## Packing Cost Estimation

The selected column internal is MellapakPlus 252.Y structured packing. Since no vendor quotation was available, the packing cost was estimated from the random-packing cost data given by literature and then corrected with a structured-packing multiplier.

Stainless steel Pall rings are listed at approximately $1750-3200\ \text{€/m}^3$ [cite]. Since the selected packing is metallic, the average value was used as the reference random-packing cost:

$$
C_{random,unit} = 2475\ \text{€/m}^3
$$

The column has a selected diameter of $0.60\ \text{m}$ and a packed height of $10\ \text{m}$, giving a packing volume of:

$$
V_{packing} = 2.827\ \text{m}^3
$$

Therefore, the estimated equivalent random-packing cost is:

$$
C_{random} = 2.827 \times 2475 = 6997.90\ \text{€}
$$

Structured packing is reported to cost approximately $30-60\%$ more per cubic meter than comparable metal random packing [cite]. Therefore, the midpoint factor was used. The estimated structured-packing cost is therefore:

$$
C_{packing} = 6997.90 \times 1.45 = 10146.95\ \text{€}
$$

## Feed Cost Estimation

This subchapter estimates the cost of purchasing DMSO feed and compares it with the energy cost required to recover DMSO from the water/DMSO run-off stream. Since DMSO is the extractive solvent, recovering it reduces the amount of fresh solvent that must be purchased.

For the DMSO purchase price, a recent European market value was used [cite]. The price of DMSO in Germany was reported as:

$$
C_{DMSO} = 5.322\ \text{\$/kg}
$$

From the material recovery chapter, the water/DMSO run-off distillation recovered was 7401.16 kg Therefore, if this amount of DMSO were not recovered, the estimated cost of purchasing an equivalent amount of fresh DMSO would be:

$$
C_{DMSO,purchase} = 7401.16 \times 5.322 = 39388.97\ \text{\$}
$$

The water/DMSO recovery distillation required a total elapsed time of 6.55 h. Since the reboiler duty was set at $1000 MJ/h, the total energy required for this recovery step was:

$$
E_{recovery} = 1000 \times 6.55 = 6550\ \text{MJ} = 6.55\ \text{GJ}
$$

Using the general energy cost [cite]:

$$
C_{energy} = 16.8\ \text{\$/GJ}
$$

the energy cost of the DMSO recovery step is:

$$
C_{recovery} = 6.55 \times 16.8 = 110.04\ \text{\$}
$$

Table: Comparison of DMSO purchase cost and recovery energy cost.
\label{tab:DMSO purchase and recovery cost comparison.}

| Parameter                            |    Value |
| ------------------------------------ | -------: |
| DMSO purchase cost [$\text{\$}$]     | 39388.97 |
| Energy cost [$\text{\$}$/GJ]         |     16.8 |
| Recovery energy cost [$\text{\$}$]   |   110.04 |
| Net saving by recovery [$\text{\$}$] | 39278.93 |

The comparison shows that recovering DMSO is much cheaper than purchasing the same amount of fresh solvent. The energy cost required to recover 7401.16 kg of DMSO is approximately $ 110, while purchasing the same amount of DMSO would cost approximately $ 39388.97. Therefore, the estimated net saving is $ 39278.93. From a feed-cost perspective, DMSO recovery is financially advisable. In addition, it reduces solvent waste and improves the sustainability of the material recovery process.

## Base Distillation System Cost

The base distillation system includes the two tanks, the column shell, the column internals, condenser, and reboiler. The column internals correspond to the selected structured packing, with an estimated packing cost of:

$$
C_{packing} = 10146.95\ \text{\$}
$$

Table: Base distillation system installed cost.
\label{tab:Base distillation system installed cost.}

| Equipment    | Installed Cost [$\text{\$}$] |
| ------------ | ---------------------------: |
| Two tanks    |                    201814.01 |
| Column shell |                     93925.17 |
| Packing      |                     10146.95 |
| Condenser    |                     52319.82 |
| Reboiler     |                     54463.99 |

The total installed cost of the base system is:

$$
C_{base} = 201814.01 + 93925.17 + 10146.95 + 52319.82 + 54463.99 = 412669.94
$$

## Cost of the Pre-heater Method

The pre-heater method requires one additional heat exchanger. The installed cost of the pre-heater is:

$C_{i,pre} = 8320.45 \text{\$}$

Therefore, the total installed cost of the system with the pre-heater method is:

$C_{pre,total} = C_{base} + C_{i,pre}$

$C_{pre,total} = 402522.99 + 8320.45 = 410843.44 \text{\$}$

## Cost of the Heat Pump Method

The heat pump method requires two compressors and an inter-cooler. The compressor cost was estimated using the compressor cost correlation, where compressor cost is expressed as a function of horsepower.

The total purchased compressor cost is:

$C_{p,comp,total} = 15420.85 \text{\$}$

The installed cost of the two compressors is:

$C_{i,comp,total} = 47958.84 \text{\$}$

The installed cost of the inter-cooler is:

$C_{i,int} = 7259.03 \text{\$}$

Therefore, the total additional installed cost of the heat pump system is:

$C_{HP,add} = C_{i,comp,total} + C_{i,int}$

$C_{HP,add} = 47958.84 + 7259.03 = 55217.87 \text{\$}$

## Comparison of Heat Recycling Alternatives

The two heat recycling alternatives were compared by considering their additional installed costs and their long-term energy savings. The pre-heater method requires only one additional heat exchanger, while the heat pump method requires two compressors and an inter-cooler.

Table: Cost comparison of heat recycling methods.
\label{tab:Cost comparison of heat recycling methods.}

| Method     | Additional Equipment         | Add. Installed Cost [$\text{\$}$] | Total Installed Cost [$\text{\$}$] |
| ---------- | ---------------------------- | --------------------------------: | ---------------------------------: |
| Pre-heater | heat exch.                   |                           8320.45 |                          410843.44 |
| Heat pump  | 2 compressors + inter-cooler |                          55217.87 |                          457740.86 |

The heat pump method requires a higher additional installed cost than the pre-heater method:

$$
\Delta C = 457740.86 - 410843.44 = 46897.43\ \text{\$}
$$

Therefore, from a capital cost perspective, the pre-heater method is the cheaper heat-recycling option. Its additional installed cost is $8320.45$, while the heat pump method requires $55217.87$, which is approximately 6.64 times higher.

However, the long-term energy savings must also be considered. Assuming one distillation cycle per day and a life expectancy of 10 years:

$$
N_{cycles} = 365 \times 10 = 3650\ \text{cycles}
$$

Using the energy cost:

$$
C_{energy} = 16.8\ \text{\$/GJ}
$$

the estimated 10-year savings are shown below.

Table: Ten-year comparison of heat recycling methods.
\label{tab:Ten-year heat recycling comparison.}

| Method            | Energy Saved [GJ/batch] | Saving [$\text{\$}$/batch] | 10-year Saving [$\text{\$}$] | Add. Installed Cost [$\text{\$}$] | Net 10-year Saving [$\text{\$}$] | Payback [years] |
| ----------------- | ----------------------: | -------------------------: | ---------------------------: | --------------------------------: | -------------------------------: | --------------: |
| Pre-heater method |                   0.408 |                       6.86 |                     25044.90 |                           8320.45 |                         16724.45 |            3.32 |
| Heat pump method  |                   3.504 |                      58.86 |                    214844.00 |                          55217.87 |                        159626.13 |            2.57 |

The pre-heater method saves less energy, but it also requires a much smaller investment. Over 10 years, it gives an estimated net saving of approximately $ 16724.45, meaning that the installation cost is recovered and the method is financially justified. The heat pump method has a much higher installation cost, but it also saves much more energy. Over the same 10-year period, it gives an estimated net saving of approximately $ 159626.13.
