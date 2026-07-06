# Cost Estimation

The cost estimation of the distillation system was carried out using preliminary equipment cost correlations. This type of estimation is suitable for conceptual design because it allows the main process equipment costs to be estimated from the principal sizing parameters, such as heat transfer area, column diameter, column height, tank dimensions, and compressor horsepower. The objective of this chapter is not to obtain a final vendor quotation, but to estimate the relative investment required for the main distillation system and for the two heat recycling alternatives. However, the costs of cooling water will be neglected in this estimation.

The equipment cost correlations were taken from literature [@douglas_1988], where purchased equipment costs are estimated from equipment size and then corrected to installed costs using installation factors. Since the original correlations are based on an older cost index, the Marshall and Swift index correction was applied. The Marshall & Swift index used in this calculation, for the year 2020, was [@mondal_jana_2022]:

$MS = 2171.6$

Two tanks were assumed: one tank for the pot charge and one tank for the distillate.

## Energy Cost Estimation

The heating energy cost was estimated from the reboiler duty and the additional energy required to heat the DMSO feed from 20°C to 62°C. Since the process heating duties are supplied by steam, the steam cost was used for these calculations instead of the electricity cost. Electricity is only used later for the compressor work required by the heat pump method. As of 2013 in the United States, literature reports high-pressure steam and electricity costs of approximately [@kiss_2013]:

$C_{\mathrm{HPS}} = \text{\$}\ 9.88 / \mathrm{GJ}$

$C_{\mathrm{electricity}} = \text{\$}\ 16.8 / \mathrm{GJ}$

where $C_{\mathrm{HPS}}$ is the cost of high-pressure steam and $C_{\mathrm{electricity}}$ is the cost of electricity. The heating cost was calculated by multiplying the required heat input by the steam cost:

$$
C = Q_{\mathrm{total}} \cdot C_{\mathrm{HPS}}
$$

where $C$ is the utility cost and $Q_{\mathrm{total}}$ is the total heating energy demand. The reboiler operated for 16.15 h at 1000 MJ/h:

$$
Q_{\mathrm{reb,main}} = 1000 \cdot 16.15 = 16150\ \mathrm{MJ} = 16.15\ \mathrm{GJ}
$$

The DMSO feed-heating duty was approximately 50 MJ/h, this value was obtained from simulation measurements. Since the feed is heated during the main distillation step, which lasts 9.05 h:

$Q_{\mathrm{feed}} = 50 \cdot 9.05 = 452.5\ \mathrm{MJ} = 0.4525\ \mathrm{GJ}$

Therefore, the total heating energy required for the complete base distillation sequence was:

$Q_{\mathrm{main,total}} = 16.15 + 0.4525 = 16.6025\ \mathrm{GJ}$

$C_{\mathrm{main}} = 16.6025 \cdot 9.88 = \text{\$}\ 164.03/\text{batch}$

The estimated operating cost of the complete base distillation heating duty is therefore $\text{\$}\ 164.03/\text{batch}$.

## Heat Exchanger Cost Estimation

The heat transfer areas used for the cost estimation were obtained from the previously calculated exchanger duties and temperature differences.

The resulting areas were converted from square meters to square feet using:

$1 \text{ m}^2 = 10.764 \text{ ft}^2$

The converted heat transfer areas used in the cost estimation are shown in Table 10.1, their values converted from meters to feet, in order to follow the calculations from the selected literature.

Table: Converted heat transfer areas used for cost estimation.
\label{tab:Converted heat transfer areas used for cost estimation.}

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

where $C_{i,HX}$ is the installed heat exchanger cost, in $. The operating steam cost was calculated separately in the energy-cost estimation section. The cost results for all heat exchangers used are shown in Table 10.2.

Table: Heat exchanger cost estimation results.
\label{tab:Heat exchanger cost estimation results.}

| Equipment    | Area [ft²] | $F_c$ | Purchased [$\text{\$}$] | Installed [$\text{\$}$] |
| ------------ | ---------: | ----: | ----------------------: | ----------------------: |
| Condenser    |     129.93 |  0.80 |                14867.20 |                57424.56 |
| Reboiler     |      84.04 |  1.60 |                22401.64 |                54463.99 |
| Inter-cooler |       5.39 |  0.80 |                 1879.36 |                 7259.03 |
| Pre-heater   |       6.65 |  0.80 |                 2154.16 |                 8320.45 |

The condenser and reboiler are part of the base distillation system. The inter-cooler is only required for the heat pump method, while the pre-heater is only required for the pre-heater heat recycling method. The installed reboiler cost is therefore only the installed capital cost of the reboiler.

## Tank Cost Estimation

Two tanks were included in the cost estimation: one for the pot charge and one for the distillate. The tank dimensions used in the calculation are shown in Table 10.3.

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

where $C_{p,tank}$ is the purchased cost of the two tanks, $D$ is the tank diameter, $H$ is the tank height, $F_c$ is the correction factor, and $MS$ is the Marshall and Swift index. Substituting the selected tank dimensions:

$C_{p,tank} = \text{\$}\ 63463.52$

The installed cost of the two tanks was calculated as well [@douglas_1988]:

$$
C_{i,tank} = 2 \frac{MS}{280} \left(101.9 D^{1.066} H^{0.802}(F_c + 2.18)\right)
$$

where $C_{i,tank}$ is the installed cost of the two tanks. Substituting the selected values:

$C_{i,tank} = \text{\$}\ 201814.01$

## Column Cost Estimation

The cost of the distillation column was estimated using the column height and diameter. The column dimensions used in the cost estimation are shown in Table 10.4, converted to feet:

Table: Column sizing values.
\label{tab:Column sizing values.}

| Parameter         | Symbol | Value | Unit |
| ----------------- | -----: | ----: | ---: |
| Column height     |    $H$ | 32.80 |   ft |
| Column diameter   |    $D$ |  2.49 |   ft |
| Correction factor |  $F_c$ |  1.05 |    - |

The purchased cost of the column shell was calculated using [@douglas_1988]:

$$
C_{p,col} = \frac{MS}{280} \left(101.9 D^{1.066} H^{0.802} F_c \right) = \text{\$}\ 36217.64
$$

where $C_{p,col}$ is the purchased cost of the column shell, $D$ is the column diameter, $H$ is the column height, $F_c$ is the correction factor, and $MS$ is the Marshall and Swift index. The installed cost of the column shell was calculated to be [@douglas_1988]:

$$
C_{i,col} = \frac{MS}{280} \left(101.9 D^{1.066} H^{0.802}(F_c + 2.18)\right) = \text{\$}\ 111412.36
$$

where $C_{i,col}$ is the installed cost of the column shell.

## Compressor Cost Estimation

The compressor costs correspond to the heat pump method. Two compressors are required, one for each compression stage. The compressor powers were obtained from the heat pump simulation and converted into horsepower, as shown in Table 10.5.

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

where $C_{p,comp}$ is the purchased compressor cost, $HP$ is the compressor power in horsepower, $F_t$ is the compressor correction factor, and $MS$ is the Marshall and Swift index. Since two compressors are required:

$C_{p,comp,total} = \frac{MS}{280} \left(51.75 HP_1^{0.82} F_t \right) + \frac{MS}{280} \left(51.75 HP_2^{0.82} F_t \right)$

where:

- $HP_1$ = horsepower of compressor 1
- $HP_2$ = horsepower of compressor 2
- $F_t$ = compressor correction factor

Using $F_t = 1$, the total purchased compressor cost is:

$C_{p,comp,total} = \text{\$}\ 15420.85$

The installed compressor cost was calculated using:

$$
C_{i,comp,total} = \frac{MS}{280} \left(51.75 HP_1^{0.82}(F_t + 2.11)\right) + \frac{MS}{280} \left(51.75 HP_2^{0.82}(F_t + 2.11)\right)
$$

where $C_{i,comp,total}$ is the installed cost of the two compressors. The resulting installed compressor cost for the heat pump method is $\text{\$}\ 47958.84$.

## Packing Cost Estimation

The selected column internal is MellapakPlus 252.Y structured packing. Since no vendor quotation was available, the packing cost was estimated from the random-packing cost data given by literature and then corrected with a structured-packing multiplier.

Stainless steel Pall rings are listed at approximately $\text{\$}\ 1750-3200 / \text{m}^3$ [@kiss_2013]. Since the selected packing is metallic, the average value was used as the reference random-packing cost (after EUR to USD conversion, as of June 2026):

$C_{random,unit} = \text{\$}\ 2475 / \text{m}^3$

The column has a selected diameter of $0.76\ \text{m}$ and a packed height of $10\ \text{m}$, giving a packing volume of:

$V_{packing} = 4.54\ \text{m}^3$

Therefore, the estimated equivalent random-packing cost is:

$C_{random} = 4.54 \times 2475 = \text{\$}\ 11236.50$

Structured packing is reported to cost approximately $30-60\%$ more per cubic meter than comparable metal random packing [@sutong_structured_vs_random_packing]. Therefore, the midpoint ($45\%$) was used. The estimated structured-packing cost is therefore:

$$
C_{packing} = 11236.5 \times 1.45 = \text{\$}\ 16292.92
$$

where $C_{packing}$ is the estimated cost of the selected structured packing.

## Solvent Cost Estimation

This subchapter estimates the cost of purchasing the DMSO solvent and compares it with the steam cost required to recover DMSO from the water/DMSO off-cut stream. Recovering it reduces the amount of fresh solvent that must be purchased.

For the DMSO purchase price, a recent European market value was used [@imarc_dmso_pricing_2026]. The price of DMSO in Germany was reported as, after converting the price from EUR to USD as of June 2026:

$C_{DMSO} = \text{\$}\ 5.322/\text{kg}$

From the material recovery chapter, the water/DMSO off-cut distillation recovered 7401.16 kg of usable DMSO. The estimated cost of purchasing an equivalent amount of fresh DMSO would be:

$$
C_{DMSO,purchase} = 7401.16 \times 5.322 = \text{\$}\ 39388.97
$$

The water/DMSO recovery distillation required a total elapsed time of 6.55 h. Since the reboiler duty was set at $1000\ \mathrm{MJ/h}$, the total energy required for this recovery step was:

$E_{recovery} = 1000 \times 6.55 = 6550\ \text{MJ} = 6.55\ \text{GJ}$

where $E_{recovery}$ is the energy required for the recovery distillation step. Since this is a reboiler heating duty, the cost was calculated using the high-pressure steam cost [@kiss_2013]:

$C_{\mathrm{HPS}} = \text{\$}\ 9.88/\text{GJ}$

The steam cost of the DMSO recovery step is:

$C_{recovery} = 6.55 \times 9.88 = \text{\$}\ 64.71$

Table 10.6 compares the cost of purchasing fresh DMSO with the steam cost required for DMSO recovery.

Table: Comparison of DMSO purchase cost and recovery energy cost.
\label{tab:DMSO purchase and recovery cost comparison.}

| Parameter                            |    Value |
| ------------------------------------ | -------: |
| DMSO purchase cost [$\text{\$}$]     | 39388.97 |
| Steam cost [$\text{\$}$/GJ]          |     9.88 |
| Recovery steam cost [$\text{\$}$]    |    64.71 |
| Net saving by recovery [$\text{\$}$] | 39324.26 |

The comparison shows that recovering DMSO is much cheaper than purchasing the same amount of fresh solvent. The steam cost required to recover 7401.16 kg of DMSO is approximately $\text{\$}\ 64.71$, while purchasing the same amount of DMSO would cost approximately $\text{\$}\ 39388.97$. Therefore, the estimated net saving is $\text{\$}\ 39324.26$. From a feed-cost perspective, DMSO recovery is financially advisable. In addition, it reduces solvent waste and improves the sustainability of the material recovery process.

## Base Distillation System Cost

The base distillation system includes the two tanks, the column shell, the column internals, condenser, and reboiler. The column internals correspond to the selected structured packing, with an estimated packing cost of:

$C_{packing} = \text{\$}\ 16292.92$

The installed costs used to calculate the base system cost are summarized in Table 10.7.

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
C_{base} = 201814.01 + 111412.36 + 16292.92 + 57424.56 + 54463.99 =  \text{\$}\ 441407.84
$$

where $C_{base}$ is the total installed cost of the base distillation system. This is a capital cost only and does not include the batch operating cost of steam.

## Cost of the Pre-heater Method

The pre-heater method only requires one additional heat exchanger; its installed cost was calculated earlier in this chapter:

$C_{i,pre} = \text{\$}\ 8320.45$

where $C_{i,pre}$ is the installed cost of the pre-heater. Therefore, the total installed cost of the system with the pre-heater method is $\text{\$}\ 449728.29$.

## Cost of the Heat Pump Method

The heat pump method requires two compressors and an inter-cooler. The compressor cost was estimated earlier in this chapter using the compressor cost correlation [@douglas_1988]. The total purchased compressor cost is:

$C_{p,comp,total} = \text{\$}\ 15420.85$

The installed cost of the two compressors is:

$C_{i,comp,total} = \text{\$}\ 47958.84$

The installed cost of the inter-cooler is:

$C_{i,int} = \text{\$}\ 7259.03$

where $C_{i,int}$ is the installed cost of the inter-cooler. Therefore, the total additional installed cost of the heat pump system is $\text{\$}\ 55217.87$, making the grand total $\text{\$}\ 496625.71$.

## Comparison of Heat Recycling Alternatives

The two heat recycling alternatives were compared by considering both their additional installed cost and their operating utility saving. The additional installed costs calculated in the previous subchapters are summarized in Table 10.8.

Table: Cost comparison of heat recycling methods.
\label{tab:Cost comparison of heat recycling methods.}

| Method     | Additional Equipment         | Add. Installed Cost [$\text{\$}$] |
| ---------- | ---------------------------- | --------------------------------: |
| Pre-heater | heat exch.                   |                           8320.45 |
| Heat pump  | 2 compressors + inter-cooler |                          55217.87 |

For the operating comparison, one batch per operating day and 330 operating days per year were assumed. Therefore, over a 10-year period:

$$
N_{cycles} = 330 \cdot 10 = 3300\ \text{batches}
$$

where $N_{cycles}$ is the number of batches operated during the 10-year period. This value is used to calculate the total 10-year saving from the saving per batch.

For the pre-heater method, the recovered heat duty from the ChemCAD heat-exchanger simulation was $45.1324\ \text{MJ/h}$. Since this heat is recovered during the $9.05\ \text{h}$ DMSO feed-heating period:

$$
E_{pre} = 45.1324 \cdot 9.05 = 408.45\ \text{MJ} = 0.40845\ \text{GJ/batch}
$$

where $E_{pre}$ is the heat recovered by the pre-heater per batch. Since this replaces external steam heating, the saving is calculated using the high-pressure steam cost:

$$
C_{pre,saving} = 0.40845 \cdot 9.88 = \text{\$}\ 4.04/\text{batch}
$$

For the heat pump method, the useful operating period was $4.5\ \text{h}$. During this time, the heat pump replaces the reboiler steam duty of $1000\ \text{MJ/h}$:

$$
E_{HP,steam} = 1000 \cdot 4.5 = 4500\ \text{MJ} = 4.5\ \text{GJ/batch}
$$

The value of this saved steam is:

$$
C_{HP,steam\ saved} = 4.5 \cdot 9.88 = \text{\$}\ 44.46/\text{batch}
$$

However, the heat pump also requires electricity for the two compressors. Their duties were $97.61\ \text{MJ/h}$ and $99.72\ \text{MJ/h}$, both operating for $4.5\ \text{h}$:

$$
E_{HP,electricity} = (97.61 + 99.72) \cdot 4.5 = 887.99\ \text{MJ} = 0.888\ \text{GJ/batch}
$$

The electricity cost is:

$$
C_{HP,electricity} = 0.888 \cdot 16.8 = \text{\$}\ 14.92/\text{batch}
$$

Therefore, the net saving of the heat pump method is:

$$
C_{HP,saving} = 44.46 - 14.92 = \text{\$}\ 29.54/\text{batch}
$$

The 10-year utility saving was calculated by multiplying the saving per batch by $N_{cycles}$. The net 10-year saving was then obtained by subtracting the additional installed cost. The results are shown in Table 10.9.

Table: Ten-year comparison of heat recycling methods.
\label{tab:Ten-year heat recycling comparison.}

| Method            | Steam Saved [GJ/batch] | Electricity Used [GJ/batch] | Net Saving [$\text{\$}$/batch] | 10-year Saving [$\text{\$}$] | Add. Installed Cost [$\text{\$}$] | Net 10-year Saving [$\text{\$}$] | Payback [years] |
| ----------------- | ---------------------: | --------------------------: | -----------------------------: | ---------------------------: | --------------------------------: | -------------------------------: | --------------: |
| Pre-heater method |                  0.408 |                       0.000 |                           4.04 |                     13317.10 |                           8320.45 |                          4996.65 |            6.25 |
| Heat pump method  |                  4.500 |                       0.888 |                          29.54 |                     97488.11 |                          55217.87 |                         42270.24 |            5.66 |

The pre-heater method has the lower installed cost, because it only requires one additional heat exchanger. It also gives a smaller utility saving, because it only recovers part of the DMSO feed-heating duty. The heat pump method has a higher installed cost, because it requires two compressors and an inter-cooler, but it gives a larger utility saving by replacing part of the reboiler steam duty. The electricity required by the compressors was subtracted from the saved steam cost because steam and electricity have different unit costs. Therefore, both methods are economically justifiable over the assumed 10-year operating period, while the heat pump method gives the larger net saving.
