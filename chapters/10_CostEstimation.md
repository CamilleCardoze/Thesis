# Cost Estimation

The cost estimation of the distillation system was carried out using preliminary equipment cost correlations. This type of estimation is suitable for conceptual design because it allows the main process equipment costs to be estimated from the principal sizing parameters, such as heat transfer area, column diameter, column height, tank dimensions, and compressor horsepower. The objective of this chapter is not to obtain a final vendor quotation, but to estimate the relative investment required for the main distillation system and for the two heat recycling alternatives. However, the costs of cooling water will be neglected in this estimation.

The equipment cost correlations were taken from literature [@douglas_1988], where purchased equipment costs are estimated from equipment size and then corrected to installed costs using installation factors. Since the original correlations are based on an older cost index, the Marshall and Swift index correction was applied. The Marshall & Swift index used in this calculation, for the year 2020, was [@mondal_jana_2022]:

$MS = 2171.6$

Two tanks were assumed: one tank for the pot charge and one tank for the distillate.

## Energy Cost estimation

The energy cost was estimated from the reboiler duty and the additional energy required to heat the DMSO feed from 20°C to 62°C. As of 2013 in the United States, literature reports a general electricity cost of approximately [@kiss_2013]:

$C_{\mathrm{energy}} = 16.8\ \text{\$} / \mathrm{GJ}$

This value was used as the unit energy cost for the preliminary estimation. The energy cost was calculated by multiplying the total energy demand by this unit cost:

$$
C = Q_{\mathrm{total}} \cdot C_{\mathrm{energy}}
$$

The reboiler operated for 16.15 h at 1000 MJ/h:

$$
Q_{\mathrm{reb,main}} = 1000 \cdot 16.15 = 16150\ \mathrm{MJ} = 16.15\ \mathrm{GJ}
$$

The DMSO feed-heating duty was approximately 50 MJ/h, this value was obtained from simulation measurements. Since the feed is heated during the main distillation step, which lasts 9.05 h:

$Q_{\mathrm{feed}} = 50 \cdot 9.05 = 452.5\ \mathrm{MJ} = 0.4525\ \mathrm{GJ}$

Therefore, the total energy required for the main IPA distillation step was:

$Q_{\mathrm{main,total}} = 16.15 + 0.4525 = 16.6025\ \mathrm{GJ}$

$C_{\mathrm{main}} = 16.6025 \cdot 16.8 = 278.92\ \text{\$}$

## Heat Exchanger Cost Estimation

The heat transfer areas used for the cost estimation were obtained from the previously calculated exchanger duties and temperature differences.

The resulting areas were converted from square meters to square feet using:

$1 \text{ m}^2 = 10.764 \text{ ft}^2$

The corrected heat transfer areas used in the cost estimation are shown in the table below, their values converted from meters to feet, in order to follow the calculations from the selected literature.

Table: Corrected heat transfer areas used for cost estimation.
\label{tab:Corrected heat transfer areas used for cost estimation.}

| Equipment    | Area [ft²] |
| ------------ | ---------: |
| Condenser    |     129.93 |
| Reboiler     |      84.04 |
| Inter-cooler |       5.39 |
| Pre-heater   |       6.65 |

The purchased cost of a heat exchanger was calculated as [@douglas_1988]:

$$
C_{p,HX} = \frac{MS}{280} \left(101.3 A^{0.65} F_c \right)
$$

where:

- $C_{p,HX}$ = purchased heat exchanger cost, in $
- $A$ = heat transfer area, in ft²
- $F_c$ = correction factor
- $MS$ = Marshall and Swift index

The installed cost was calculated using [@douglas_1988]:

$$
C_{i,HX} = \frac{MS}{280} \left(101.3 A^{0.65}(F_c + 2.29)\right)
$$

Since high-pressure steam was used as the heating utility for the reboiler, its cost must also be accounted for. The cost of high-pressure steam in terms of the heat exchanger heat duty is [@kiss_2013]:

$C_{HPS} = 9.88\ \text{\$/GJ}$

Therefore, the total cost of high-pressure steam per batch was estimated from the reboiler heat duty and the operating time as follows:

$C_{steam} = Q_{reb} \cdot t \cdot C_{HPS} = C_{steam} = 1.00 \times 16.15 \times 9.88 = 159.56\ \text{\$/batch}$

The total capital needed to install and operate the reboiler is:

$C_{i,reb,corr} = C_{i,reb} + C_{steam}$

$C_{i,reb,corr} = 54463.99 + 159.56 = 54623.55\ \text{\$}$

The cost results for all heat exchangers used are shown below.

Table: Heat exchanger cost estimation results.
\label{tab:Heat exchanger cost estimation results.}

| Equipment    | Area [ft²] | $F_c$ | Purchased [$\text{\$}$] | Installed [$\text{\$}$] |
| ------------ | ---------: | ----: | ----------------------: | ----------------------: |
| Condenser    |     129.93 |  0.80 |                14867.20 |                57424.56 |
| Reboiler     |      84.04 |  1.60 |                22401.64 |                54623.55 |
| Inter-cooler |       5.39 |  0.80 |                 1879.36 |                 7259.03 |
| Pre-heater   |       6.65 |  0.80 |                 2154.16 |                 8320.45 |

The condenser and reboiler are part of the base distillation system. The inter-cooler is only required for the heat pump method, while the pre-heater is only required for the pre-heater heat recycling method. The installed reboiler cost includes the estimated high-pressure steam cost for one complete batch.

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

The purchased cost of the two tanks was calculated with [@douglas_1988]:

$$
C_{p,tank} = 2 \frac{MS}{280} \left(101.9 D^{1.066} H^{0.802} F_c \right)
$$

Substituting the selected tank dimensions:

$C_{p,tank} = 63463.52 \text{\$}$

The installed cost of the two tanks was calculated as well [@douglas_1988]:

$$
C_{i,tank} = 2 \frac{MS}{280} \left(101.9 D^{1.066} H^{0.802}(F_c + 2.18)\right)
$$

Substituting the selected values:

$C_{i,tank} = 201814.01 \text{\$}$

## Column Cost Estimation

The cost of the distillation column was estimated using the column height and diameter. The column dimensions used in the cost estimation are shown in the following table, converted to feet:

Table: Column sizing values.
\label{tab:Column sizing values.}

| Parameter         | Symbol | Value | Unit |
| ----------------- | -----: | ----: | ---: |
| Column height     |    $H$ | 32.80 |   ft |
| Column diameter   |    $D$ |  2.49 |   ft |
| Correction factor |  $F_c$ |  1.05 |    - |

The purchased cost of the column shell was calculated using [@douglas_1988]:

$$
C_{p,col} = \frac{MS}{280} \left(101.9 D^{1.066} H^{0.802} F_c \right) = C_{p,col} = 36217.64 \text{\$}
$$

The installed cost of the column shell was calculated to be [@douglas_1988]:

$$
C_{i,col} = \frac{MS}{280} \left(101.9 D^{1.066} H^{0.802}(F_c + 2.18)\right) = 111412.36 \text{\$}
$$

## Compressor Cost Estimation

The compressor costs correspond to the heat pump method. Two compressors are required, one for each compression stage. The compressor powers were obtained from the heat pump simulation and converted into horsepower, as shown in the following table:

Table: Compressor power values.
\label{tab:Compressor power values.}

| Equipment    | Power [hp] |
| ------------ | ---------: |
| Compressor 1 |      36.36 |
| Compressor 2 |      37.15 |

The purchased compressor cost was calculated using the formula [@douglas_1988]:

$$
C_{p,comp} = \frac{MS}{280} \left(51.75 HP^{0.82} F_t \right)
$$

Since two compressors are required:

$C_{p,comp,total} = \frac{MS}{280} \left(51.75 HP_1^{0.82} F_t \right) + \frac{MS}{280} \left(51.75 HP_2^{0.82} F_t \right)$

where:

- $HP_1$ = horsepower of compressor 1
- $HP_2$ = horsepower of compressor 2
- $F_t$ = compressor correction factor

Using $F_t = 1$, the total purchased compressor cost is:

$C_{p,comp,total} = 15420.85 \text{\$}$

The installed compressor cost was calculated using:

$$
C_{i,comp,total} = \frac{MS}{280} \left(51.75 HP_1^{0.82}(F_t + 2.11)\right) + \frac{MS}{280} \left(51.75 HP_2^{0.82}(F_t + 2.11)\right)
$$

Resulting in a cost for the heat pump method of $47958.84\ \text{\$}$.

## Packing Cost Estimation

The selected column internal is MellapakPlus 252.Y structured packing. Since no vendor quotation was available, the packing cost was estimated from the random-packing cost data given by literature and then corrected with a structured-packing multiplier.

Stainless steel Pall rings are listed at approximately $1750-3200\ \text{\$} / \text{m}^3$ [@kiss_2013]. Since the selected packing is metallic, the average value was used as the reference random-packing cost (after EUR to USD conversion, as of June 2026):

$C_{random,unit} = 2475\ \text{\$} / \text{m}^3$

The column has a selected diameter of $0.76\ \text{m}$ and a packed height of $10\ \text{m}$, giving a packing volume of:

$V_{packing} = 4.54\ \text{m}^3$

Therefore, the estimated equivalent random-packing cost is:

$C_{random} = 4.54 \times 2475 = 11236.50\ \text{\$}$

Structured packing is reported to cost approximately $30-60\%$ more per cubic meter than comparable metal random packing [@sutong_structured_vs_random_packing]. Therefore, the midpoint ($45\%$) was used. The estimated structured-packing cost is therefore:

$$
C_{packing} = 11236.5 \times 1.45 = 16292.92\ \text{\$}
$$

## Feed Cost Estimation

This subchapter estimates the cost of purchasing DMSO feed and compares it with the energy cost required to recover DMSO from the water/DMSO off-cut stream. Since DMSO is the extractive solvent, recovering it reduces the amount of fresh solvent that must be purchased.

For the DMSO purchase price, a recent European market value was used [@imarc_dmso_pricing_2026]. The price of DMSO in Germany was reported as, after converting the price from EUR to USD as of June 2026:

$C_{DMSO} = 5.322\ \text{\$/kg}$

From the material recovery chapter, the water/DMSO off-cut distillation recovered 7401.16 kg of usable DMSO. The estimated cost of purchasing an equivalent amount of fresh DMSO would be:

$$
C_{DMSO,purchase} = 7401.16 \times 5.322 = 39388.97\ \text{\$}
$$

The water/DMSO recovery distillation required a total elapsed time of 6.55 h. Since the reboiler duty was set at $1000 MJ/h, the total energy required for this recovery step was:

$E_{recovery} = 1000 \times 6.55 = 6550\ \text{MJ} = 6.55\ \text{GJ}$

Using the general energy cost [@kiss_2013]:

$C_{energy} = 16.8\ \text{\$/GJ}$

the energy cost of the DMSO recovery step is:

$C_{recovery} = 6.55 \times 16.8 = 110.04\ \text{\$}$

Table: Comparison of DMSO purchase cost and recovery energy cost.
\label{tab:DMSO purchase and recovery cost comparison.}

| Parameter                            |    Value |
| ------------------------------------ | -------: |
| DMSO purchase cost [$\text{\$}$]     | 39388.97 |
| Energy cost [$\text{\$}$/GJ]         |     16.8 |
| Recovery energy cost [$\text{\$}$]   |   110.04 |
| Net saving by recovery [$\text{\$}$] | 39278.93 |

The comparison shows that recovering DMSO is much cheaper than purchasing the same amount of fresh solvent. The energy cost required to recover 7401.16 kg of DMSO is approximately $110 \text{\$}$, while purchasing the same amount of DMSO would cost approximately $39388.97 \text{\$}$. Therefore, the estimated net saving is $39278.93 \text{\$}$. From a feed-cost perspective, DMSO recovery is financially advisable. In addition, it reduces solvent waste and improves the sustainability of the material recovery process.

## Base Distillation System Cost

The base distillation system includes the two tanks, the column shell, the column internals, condenser, and reboiler. The column internals correspond to the selected structured packing, with an estimated packing cost of:

$C_{packing} = 10146.95\ \text{\$}$

Table: Base distillation system installed cost.
\label{tab:Base distillation system installed cost.}

| Equipment    | Installed Cost [$\text{\$}$] |
| ------------ | ---------------------------: |
| Two tanks    |                    201814.01 |
| Column shell |                    111412.36 |
| Packing      |                     16292.92 |
| Condenser    |                     57424.56 |
| Reboiler     |                     54463.99 |

The total installed cost of the base system is:

$$
C_{base} = 201814.01 + 111412.36 + 16292.92 + 57424.56 + 54463.99 =  441407.84 \text{\$}
$$

## Cost of the Pre-heater Method

The pre-heater method only requires one additional heat exchanger; its installed cost was calculated earlier in this chapter:

$C_{i,pre} = 8320.45 \text{\$}$

Therefore, the total installed cost of the system with the pre-heater method is $449728.29 \text{\$}$.

## Cost of the Heat Pump Method

The heat pump method requires two compressors and an inter-cooler. The compressor cost was estimated earlier in this chapter using the compressor cost correlation [@douglas_1988]. The total purchased compressor cost is:

$C_{p,comp,total} = 15420.85 \text{\$}$

The installed cost of the two compressors is:

$C_{i,comp,total} = 47958.84 \text{\$}$

The installed cost of the inter-cooler is:

$C_{i,int} = 7259.03 \text{\$}$

Therefore, the total additional installed cost of the heat pump system is $55217.87 \text{\$}$, making the grand total $496625.71 \text{\$}$

## Comparison of Heat Recycling Alternatives

The two heat recycling alternatives were compared by considering their additional installed costs and their long-term energy savings. The pre-heater method requires only one additional heat exchanger, while the heat pump method requires two compressors and an inter-cooler.

Table: Cost comparison of heat recycling methods.
\label{tab:Cost comparison of heat recycling methods.}

| Method     | Additional Equipment         | Add. Installed Cost [$\text{\$}$] |
| ---------- | ---------------------------- | --------------------------------: |
| Pre-heater | heat exch.                   |                           8320.45 |
| Heat pump  | 2 compressors + inter-cooler |                          55217.87 |

From a capital cost perspective, the pre-heater method is the cheaper heat-recycling option. Its additional installed cost is $8320.45 \text{\$}$, while the heat pump method requires $55217.87 \text{\$}$, which is approximately 6.64 times higher. However, the long-term energy savings must also be considered; assuming one distillation cycle per day and a life expectancy of 10 years:

$N_{cycles} = 365 \times 10 = 3650\ \text{cycles}$

Using the energy cost:

$C_{energy} = 16.8\ \text{\$/GJ}$

the estimated 10-year savings are shown below.

Table: Ten-year comparison of heat recycling methods.
\label{tab:Ten-year heat recycling comparison.}

| Method            | Energy Saved [GJ/batch] | Saving [$\text{\$}$/batch] | 10-year Saving [$\text{\$}$] | Add. Installed Cost [$\text{\$}$] | Net 10-year Saving [$\text{\$}$] | Payback [years] |
| ----------------- | ----------------------: | -------------------------: | ---------------------------: | --------------------------------: | -------------------------------: | --------------: |
| Pre-heater method |                   0.408 |                       6.86 |                     25044.90 |                           8320.45 |                         16724.45 |            3.32 |
| Heat pump method  |                   3.612 |                      58.86 |                    214844.00 |                          55217.87 |                        159626.13 |            2.57 |

The pre-heater method saves less energy, but it also requires a much smaller investment. Over 10 years, it gives an estimated net saving of approximately $16724.45 \text{\$}$, meaning that the installation cost is recovered and the method is financially justified. The heat pump method has a much higher installation cost, but it also saves much more energy. Over the same 10-year period, it gives an estimated net saving of approximately $159626.13 \text{\$}$.
