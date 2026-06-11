# Cost Estimation

The cost estimation of the distillation system was carried out using preliminary equipment cost correlations. This type of estimation is suitable for conceptual design because it allows the main process equipment costs to be estimated from the principal sizing parameters, such as heat-transfer area, column diameter, column height, tank dimensions, and compressor horsepower. The objective of this chapter is not to obtain a final vendor quotation, but to estimate the relative investment required for the main distillation system and for the two heat recycling alternatives.

The equipment cost correlations were taken from Douglas, where purchased equipment costs are estimated from equipment size and then corrected to installed costs using installation factors. Since the original correlations are based on an older cost index, the Marshall and Swift index correction was applied. The Marshall & Swift index used in this calculation, for the year 2020, was [cite]:

$MS = 2171.6$

Two tanks were assumed: one tank for the pot charge and one tank for the distillate.

## Heat Exchanger Cost Estimation

The heat-transfer areas used for the cost estimation were obtained from the previously calculated exchanger duties and temperature differences. The heat-transfer area was calculated using:

$A = \frac{Q}{K \Delta T}$

where:

- $A$ = heat-transfer area
- $Q$ = heat duty
- $K$ = overall heat-transfer coefficient
- $\Delta T$ = temperature difference or logarithmic mean temperature difference

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

[add high pressure steam cost] [cite]

The heat exchanger cost results are shown.

Table: Heat exchanger cost estimation results.
\label{tab:Heat exchanger cost estimation results.}

| Equipment    | Area [ft²] | $F_c$ | Purchased [$] | Installed [$] |
| ------------ | ---------: | ----: | ------------: | ------------: |
| Condenser    |     112.59 |  0.80 |      13545.58 |      52319.82 |
| Reboiler     |      84.04 |  1.60 |      22401.64 |      54463.99 |
| Inter-cooler |       5.39 |  0.80 |       1879.36 |       7259.03 |
| Pre-heater   |       6.65 |  0.80 |       2154.16 |       8320.45 |

The condenser and reboiler are part of the base distillation system. The inter-cooler is only required for the heat pump method, while the pre-heater is only required for the pre-heater heat recycling method.

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

$C_{p,tank} = 2 \frac{MS}{280} \left(101.9 D^{1.066} H^{0.82} F_c \right)$

Substituting the selected tank dimensions:

$C_{p,tank} = 65913.27 \text{\$}$

The installed cost of the two tanks was calculated as:

$C_{i,tank} = 2 \frac{MS}{280} \left(101.9 D^{1.066} H^{0.802}(F_c + 2.18)\right)$

Substituting the selected values:

$C_{i,tank} = 201814.01 \text{\$}$

Therefore, the total installed cost of the two tanks is:

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

$C_{p,col} = \frac{MS}{280} \left(101.9 D^{1.066} H^{0.82} F_c \right)$

Substituting the selected values:

$C_{p,col} = 32512.81 \text{\$}$

The installed cost of the column shell was calculated as [cite]:

$C_{i,col} = \frac{MS}{280} \left(101.9 D^{1.066} H^{0.802}(F_c + 2.18)\right)$

Substituting the selected values:

$C_{i,col} = 93925.17 \text{\$}$

Therefore, the total installed column cost is:

[add total column cost]

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

The compressor formula used in this calculation corresponds to the corrected version used in the Excel file. The formula from the book was not used directly because of a decimal point placement mistake in the original expression.

## Packing Cost Estimation

[add packing cost estimation] [cite]

## Vacuum Pump Cost Estimation

[add vacuum pump cost estimation] [cite]

## Charge and Feed Cost Estimation

[add cost estimation for cooling water] [cite book]

[add cost estimation for DMSO and IPA] [cite]

[compare material prices to material recovery energy prices (what would save more money and energy, buying new solvents or recycling?), conclude if it is financially advisable to recycle or not] [cite]

## Base Distillation System Cost

The base distillation system includes the two tanks, the column shell, column internals, condenser, and reboiler.

[add vacuum pump estimation and packing]

Table: Base distillation system installed cost.
\label{tab:Base distillation system installed cost.}

| Equipment           | Installed Cost [$] |
| ------------------- | -----------------: |
| Two tanks           |          201814.01 |
| Column shell        |           89520.16 |
| Condenser           |           52319.82 |
| Reboiler            |           54463.99 |
| Base installed cost |              [add] |

[modify table according to new data]

The total installed cost of the base system is:

[modify this]

$C_{base} = 201814.01 + 89520.16 + 3706.97 + 52319.82 + 54463.99$

$C_{base} = 401824.94 \text{\$}$

## Cost of the Pre-heater Method

The pre-heater method requires one additional heat exchanger. The installed cost of the pre-heater is:

$C_{i,pre} = 8320.45 \text{\$}$

Therefore, the total installed cost of the system with the pre-heater method is:

$C_{pre,total} = C_{base} + C_{i,pre}$

$C_{pre,total} = 401824.94 + 8320.45$

$C_{pre,total} = 410145.39 \text{\$}$

## Cost of the Heat Pump Method

The heat pump method requires two compressors and an inter-cooler. The installed cost of the two compressors is:

$C_{i,comp,total} = 47958.84 \text{\$}$

The installed cost of the inter-cooler is:

$C_{i,int} = 7259.03 \text{\$}$

Therefore, the total additional installed cost of the heat pump system is:

$C_{HP,add} = C_{i,comp,total} + C_{i,int}$

$C_{HP,add} = 47958.84 + 7259.03$

$C_{HP,add} = 55217.87 \text{\$}$

The total installed cost of the system with the heat pump method is:

$C_{HP,total} = C_{base} + C_{HP,add}$

$C_{HP,total} = 401824.94 + 55217.87$

$C_{HP,total} = 457042.82 \text{\$}$

## Comparison of Heat Recycling Alternatives

The two heat recycling alternatives were compared by considering the additional equipment required by each method. The pre-heater method requires only one additional heat exchanger, while the heat pump method requires two compressors and an inter=cooler.

Table: Cost comparison of heat recycling methods.
\label{tab:Cost comparison of heat recycling methods.}

| Method            | Additional Equipment         | Add. Installed Cost [$] | Total Installed Cost [$] |
| ----------------- | ---------------------------- | ----------------------: | -----------------------: |
| Pre-heater method | Pre-heater                   |                 8320.45 |                410145.39 |
| Heat pump method  | 2 compressors + inter-cooler |                55217.87 |                457042.82 |

The heat pump method requires a higher total installed cost than the pre-heater method:

$\Delta C = C_{HP,total} - C_{pre,total}$

$\Delta C = 457042.82 - 410145.39$

$\Delta C = 46897.43 \text{\$}$

The additional installed cost of the heat pump method is also higher than that of the pre-heater method:

$\frac{C_{HP,add}}{C_{pre}} = \frac{55217.87}{8320.45}$

$\frac{C_{HP,add}}{C_{pre}} = 6.64$

Therefore, the heat pump method requires approximately 6.64 times more additional installed equipment cost than the pre-heater method.

From a capital cost perspective, the pre-heater method is the more economical heat recycling option. It requires only one additional heat exchanger, with an installed cost of 8320.45 $. In contrast, the heat pump method requires two compressors and an inter-cooler, increasing the additional installed cost to 55217.87 $.

Although the heat pump method can upgrade the temperature level of the overhead vapour and help reduce the reboiler duty, it requires significantly more equipment and therefore has a higher installed cost. In addition, the heat pump method was found to be suitable only during the first part of the distillation operation. The pre-heater method is simpler, cheaper, and easier to implement, although it provides a smaller degree of heat recovery. Therefore, based on the preliminary cost estimation, the pre-heater method is the preferred heat recycling alternative.

[compare amount of money saved via heat recycling (pre-heater method and compressor method). For this, compare amount of total energy saved]

[compare amount of money it takes to install heat recycling methods with 10 years of energy saved (if heat recycling is viable)] [cite]

[review all numbers]
