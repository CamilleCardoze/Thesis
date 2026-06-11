# Material Recovery

After the main batch extractive distillation step, two secondary run-off streams are produced: an IPA/water run-off and a water/DMSO run-off. These streams do not meet the purity requirements to be considered final products, but they still contain recoverable amounts of IPA, water, and DMSO. Therefore, instead of treating them as waste, their re-integration into later batches was studied in order to reduce material losses and improve the overall efficiency of the process.

Two recycling strategies were compared using ChemCAD simulations. In both cases, the results of one batch were used as input for the next batch. Batch 1 corresponds to the original reference batch, while Batches 2–6 represent five consecutive recycle batches. For each batch, the total moles, mass, purity of the run-off streams, IPA distillate purity, distillate mass, elapsed time, and DMSO bottom-product purity were recorded.

In the first method, only the IPA/water run-off is added to the pot charge of the next batch, while the recovered DMSO bottom product from the previous distillation is used as the solvent feed for the next batch. Since the amount of recovered DMSO is lower than the amount required for a complete new batch, the missing amount would be replaced in practice by externally supplied, theoretically pure DMSO. However, in the simulation, the additional pure DMSO was not included in the purity calculation. Instead, the purity of the recovered bottom DMSO was used as the next solvent-feed purity, representing the worst-case scenario. The water/DMSO run-off is not directly recycled in this method and is instead kept for later recovery distillation.

In the second method, both the IPA/water run-off and the water/DMSO run-off are added directly to the pot charge of the next batch. This method has the advantage of immediately reusing all run-off material, but it also introduces more water and DMSO into the next batch, which can influence the charge composition, separation time, and simulation convergence.

Abbreviations:

- `B` = batch
- `RO` = run-off
- `x` = mole fraction
- `m` = mass
- `n` = amount of substance
- `Chg.` = charge
- `Dist.` = distillate
- `t` = time

## Method 1, Water/IPA Run-off Re-integration

In the first recycling method, the IPA/water run-off from each batch was added to the pot charge of the following batch. The DMSO bottom product from the previous batch was reused as the next batch’s solvent feed. The water/DMSO run-off was not added directly to the following batch, but was instead collected for later recovery. This approach aims to recover IPA-containing material without continuously increasing the amount of DMSO in the pot charge.

The initial charge values used for this recycle sequence were 41.18112 kmol IPA and 21.21452 kmol water. During the ChemCAD simulations, some operating adjustments were required to maintain convergence and product purity. For Batch 2, the reflux ratio in step 3 was changed from 4 to 5. For Batch 5, the reflux ratio in step 3 was further changed from 5 to 6. These changes were necessary to keep the distillation within the required purity range as the recycled material influenced the batch composition.

### IPA/Water Run-off and IPA Distillate Results

Table: Results of the first material recovery method.
\label{tab: Results of the first material recovery method}

|         B | IPA RO | H₂O RO | xIPA RO |    mRO | nIPA Chg. | nH₂O Chg. | xH₂O Chg. | xIPA Chg. | xIPA Dist. |   mDist. |      t |
| --------: | -----: | -----: | ------: | -----: | --------: | --------: | --------: | --------: | ---------: | -------: | -----: |
|           |   kmol |   kmol |       - |     kg |      kmol |      kmol |         - |         - |          - |       kg |      h |
|         1 |   1.30 |   5.29 |  0.1975 | 173.55 |     42.48 |     26.51 |    0.3842 |    0.6158 |     0.9985 |  2397.36 |  16.15 |
|         2 |   1.71 |   7.04 |  0.1957 | 229.91 |     42.90 |     28.26 |    0.3971 |    0.6029 |     0.9989 |  2477.95 |  18.25 |
|         3 |   1.68 |   6.71 |  0.1999 | 221.58 |     42.86 |     27.92 |    0.3945 |    0.6055 |     0.9985 |  2477.15 |  18.55 |
|         4 |   1.65 |   6.73 |  0.1971 | 220.56 |     42.83 |     27.94 |    0.3948 |    0.6052 |     0.9985 |  2477.15 |  18.80 |
|         5 |   1.80 |   7.36 |  0.1963 | 240.61 |     42.98 |     28.57 |    0.3993 |    0.6007 |     0.9990 |  2466.74 |  19.55 |
|         6 |   1.74 |   7.04 |  0.1977 | 231.09 |     42.92 |     28.25 |    0.3970 |    0.6030 |     0.9987 |  2479.36 |  19.80 |
| Tot./Avg. |      - |      - |       - |      - |         - |         - |         - |         - |     0.9987 | 14775.70 | 111.10 |

[add graph]

The IPA distillate purity remained consistently above the required value in all six batches. The average IPA distillate purity was 0.9987 mol fraction, while the total recovered IPA distillate mass was 14775.70 kg. The total operating time for the six batches was 111.10 h. A slight increase in operating time can be observed from Batch 1 to Batch 6, which is expected because the recycled IPA/water run-off changes the initial pot composition of each new batch.

### Water/DMSO Run-off Obtained During Method 1

Table: Water/DMSO run-off obtained during method 1.
\label{tab:Water/DMSO run-off obtained uring method 1}

|         B |   H₂O |  DMSO |   xH₂O |  xDMSO |  mTotal |
| --------: | ----: | ----: | -----: | -----: | ------: |
|           |  kmol |  kmol |      - |      - |      kg |
|         1 |  3.29 | 15.92 | 0.1713 | 0.8287 | 1302.96 |
|         2 |  2.47 | 15.75 | 0.1356 | 0.8644 | 1275.15 |
|         3 |  2.57 | 16.01 | 0.1382 | 0.8618 | 1297.51 |
|         4 |  2.60 | 15.98 | 0.1398 | 0.8602 | 1295.26 |
|         5 |  2.06 | 15.48 | 0.1176 | 0.8824 | 1246.89 |
|         6 |  2.00 | 15.56 | 0.1139 | 0.8861 | 1252.03 |
| Tot./Avg. | 14.99 | 94.70 |      - | 0.8639 | 7669.81 |

The water/DMSO run-off contains a significant amount of DMSO, with an average DMSO mole fraction of 0.8639. Since this stream is not directly returned to the next batch in Method 1, it remains available for a later recovery distillation. This prevents additional DMSO accumulation in the main IPA recovery process, but requires an additional recovery step.

### DMSO Bottom Product Obtained During Method 1

Table: DMSO bottom product obtained during method 1.
\label{tab:DMSO bottom product obtained during method 1}

|         B |  DMSO |    H₂O |  xDMSO |    xH₂O |   mTotal |
| --------: | ----: | -----: | -----: | ------: | -------: |
|           |  kmol |   kmol |      - |       - |       kg |
|         1 | 51.96 | 0.0255 | 0.9995 | 0.00049 |  4060.02 |
|         2 | 53.20 | 0.0253 | 0.9995 | 0.00047 |  4157.48 |
|         3 | 53.70 | 0.0252 | 0.9995 | 0.00047 |  4195.97 |
|         4 | 53.73 | 0.0256 | 0.9995 | 0.00048 |  4198.89 |
|         5 | 53.85 | 0.0253 | 0.9995 | 0.00047 |  4207.86 |
|         6 | 54.14 | 0.0248 | 0.9995 | 0.00046 |  4230.33 |
| Tot./Avg. |     - |      - | 0.9995 |       - | 25050.56 |

[add graph]

The DMSO bottom product remained highly pure throughout the recycle sequence, with an average DMSO mole fraction of 0.9995. This confirms that the recovered bottom DMSO can be reused as solvent feed in the following batch. However, the recovered amount is not enough to supply a full new batch, so external pure DMSO would still be required in practice.

The water/IPA run-off re-integration method is stable and effective. It maintains the IPA distillate purity above the required specification, gives a high total recovered distillate mass, and produces a very pure DMSO bottom stream suitable for reuse. Its main disadvantage is that the water/DMSO run-off is not immediately recycled and must be treated separately later. However, this also makes the main distillation sequence easier to control, since DMSO does not accumulate as strongly in the next batch charge.

## Method 2, Total Run-off Re-integration

In the second recycling method, both the IPA/water run-off and the water/DMSO run-off were added directly to the next pot charge. This means that all run-off material from the previous batch was immediately reused in the following batch. The purpose of this method was to determine whether direct recycling of all secondary material streams could improve material recovery and reduce the need for a separate recovery step.

The same initial charge values were used as in Method 1: 41.18112 kmol IPA and 21.21452 kmol water. Since both run-off streams were recycled, the DMSO content in the pot charge increased compared with Method 1. This made the simulation more difficult to converge in some cases. In Batch 2, the reflux ratio in step 3 was changed from 4 to 5. In Batch 3, the stop value in step 3 was changed from 0.9995 to 0.9997. In Batch 4, the reflux ratio in step 3 was increased from 5 to 6. In Batch 5, the reflux ratio was changed back from 6 to 5. These adjustments show that Method 2 required more operational changes than Method 1.

### Combined IPA/Water/DMSO Run-off and IPA Distillate Results

Table: Results of the second material recovery method.
\label{tab:Results of the second material recovery method}

|         B | IPA RO | H₂O RO | DMSO RO |      mRO | nIPA Chg. | nH₂O Chg. | xIPA Chg. | xH₂O Chg. | xDMSO Chg. | xIPA Dist. |   mDist. |      t |
| --------: | -----: | -----: | ------: | -------: | --------: | --------: | --------: | --------: | ---------: | ---------: | -------: | -----: |
|           |   kmol |   kmol |    kmol |       kg |      kmol |      kmol |         - |         - |          - |          - |       kg |      h |
|         1 |   1.30 |   8.58 |   15.92 |  1476.51 |     42.48 |     29.80 |    0.4817 |    0.3378 |     0.1805 |     0.9985 |  2397.36 |  16.15 |
|         2 |   1.98 |  11.11 |   19.26 |  1824.00 |     43.17 |     32.32 |    0.4556 |    0.3411 |     0.2033 |     0.9989 |  2468.51 |  19.75 |
|         3 |   2.10 |  11.86 |   20.43 |  1936.60 |     43.28 |     33.08 |    0.4471 |    0.3417 |     0.2111 |     0.9988 |  2468.52 |  20.75 |
|         4 |   2.06 |  11.23 |   20.26 |  1909.22 |     43.24 |     32.44 |    0.4507 |    0.3381 |     0.2112 |     0.9985 |  2478.15 |  21.90 |
|         5 |   2.03 |  11.77 |   20.93 |  1969.56 |     43.21 |     32.98 |    0.4449 |    0.3396 |     0.2155 |     0.9985 |  2477.41 |  20.85 |
|         6 |   2.19 |  12.33 |   21.00 |  1994.18 |     43.37 |     33.54 |    0.4429 |    0.3426 |     0.2145 |     0.9989 |  2465.97 |  21.00 |
| Tot./Avg. |      - |      - |       - | 11110.08 |         - |         - |         - |         - |          - |     0.9987 | 14755.93 | 120.40 |

[add graph]

The IPA distillate purity remained above the target in all batches, with an average value of 0.9987 mol fraction. However, the total distillate mass was slightly lower than in Method 1, with 14755.93 kg recovered over the six batches. The total operating time increased to 120.40 h, which is 9.30 h longer than Method 1.

### DMSO Bottom Product Obtained During Method 2

Table: DMSO bottom product obtained during method 2.
\label{tab:DMSO bottom product obtained during method 2}

|         B |  DMSO |    H₂O |  xDMSO |    xH₂O |  mTotal |
| --------: | ----: | -----: | -----: | ------: | ------: |
|           |  kmol |   kmol |      - |       - |      kg |
|         1 | 51.96 | 0.0255 | 0.9995 | 0.00049 | 4060.02 |
|         2 | 66.36 | 0.0323 | 0.9995 | 0.00049 | 5185.60 |
|         3 | 69.66 | 0.0331 | 0.9995 | 0.00048 | 5443.17 |
|         4 | 71.38 | 0.0343 | 0.9995 | 0.00048 | 5578.05 |
|         5 | 70.54 | 0.0330 | 0.9995 | 0.00047 | 5512.53 |
|         6 | 70.77 | 0.0328 | 0.9995 | 0.00046 | 5530.48 |
| Tot./Avg. |     - |      - | 0.9995 |         |         |

[add graph]

The DMSO bottom purity remained high, with an average value of 0.9995 mol fraction. However, the total DMSO bottom mass increased significantly compared with Method 1. This is expected because the water/DMSO run-off is recycled directly into the pot charge, causing more DMSO to remain within the main batch sequence.

### Comparison of the Two Recycling Methods

Table: Comparison between method 1 and method 2.
\label{tab:Comparison between method 1 and method 2}

| Parameter                |            Method 1 |             Method 2 |
| ------------------------ | ------------------: | -------------------: |
| Avg. xIPA Dist. [-]      |              0.9987 |               0.9987 |
| Total mDist. [kg]        |            14775.70 |             14755.93 |
| Total t [h]              |              111.00 |               120.30 |
| Total DMSO Bottom m [kg] |            25050.56 |             31309.85 |
| RO handled [kg]          | 7669.81 H₂O/DMSO RO | 11110.08 combined RO |
| Recycle batches studied  |                   5 |                    5 |
| Operating adjustments    |               Fewer |                 More |

[add graph]

Both recycling strategies achieved the required IPA product purity. The average IPA distillate purity was practically the same for both methods, at approximately 0.9987 mol fraction. However, Method 1 produced a slightly larger total IPA distillate mass and required less total operating time. Method 2 required 120.30 h compared with 111.00 h for Method 1, which means that total run-off re-integration increased the total process time by 9.30 h over the six simulated batches.

Method 2 also required more changes to the simulation settings to maintain convergence and product quality. This suggests that adding both run-off streams directly to the next pot charge makes the process more sensitive to composition changes. The larger DMSO bottom mass in Method 2 also shows that DMSO accumulates more strongly in the batch sequence when the water/DMSO stream is directly recycled.

Total run-off re-integration is technically possible, since it still achieves the required IPA purity and produces a high-purity DMSO bottom stream. However, it is less favorable than Method 1 because it increases the operating time, requires more simulation adjustments, and causes greater DMSO accumulation in the system. Based on the comparison, the preferred material recovery strategy is Method 1: water/IPA run-off re-integration combined with separate later treatment of the water/DMSO run-off. This approach gives similar product purity, slightly higher IPA recovery, shorter operating time, and better process stability. Since our reboiler's heat duty is directly correlated to the elapsed time due to it being set at 1000 MJ/h, less time needed to complete our process means that it is more environmentally and financially affordable, not only less time consuming.

## Water/DMSO Run-off Distillation

As a following step to the water/IPA re-integration, we have the water/DMSO run-off distillation. The same column is to be used for this process. The goal of this extra step is to recover as much DMSO and water as possible, for it to be repurposed later. The obtained, total amount of water moles and DMSO moles from the water/DMSO run-off were calculated after the 5 batches for Method 1, and this result was the pot charge for our distillation. There will be no feed or external entrainer. We created a separate ChemCAD simulation with the same column parameters and initial conditions.

[add picture of chemcad layout]

Different stop values for the process were investigated, finally falling at 0.998 mol frac. water in the accumulator (water is more volatile than DMSO), as well as reflux values and internal pot pressure values.

[add pictures of pressure graphs]

After many trials, it was determined that a high reflux ratio paired with vacuum conditions will be needed. This is due to the fact that, as the last traces of water begin to evaporate, at this temperature DMSO starts turning into vapour as well, rapidly, since the reboiler keeps providing heat. To obtain a purity of more than 99.75 mol% for both water and DMSO, we must take the pressure down to 0.1 bar to stimulate quick water evaporation and make the gap between water's and DMSO's volatility bigger.

[add pictures of reflux ratio graphs]

In the same way, it was determined that a reflux ratio of [] will be needed. As the cold reflux liquid flows downward, it meets the hot, rising DMSO vapor. This forces DMSO condense back into liquid, while water continues to vaporize and rise. The reason for the need behind such a high R value is time. Just as with pressure, the more time it takes to complete the operation, the more DMSO gets heated up and evaporated.

However, our ChemCAD simulation needed additional aid in order to converge. Hold-up values were added:[add holdup values] . These represent the liquid that gets "held up" in the packing, as well as inside the condenser. Adding hold up values also makes our process more accurate and realistic.

In order to maintain realism, several batches for both recycling methods were performed again, with the same hold-up values for the column as in the water/DMSO distillation. However, our results (composition, mass, time) only slightly changed, affecting the values only after two decimal points. Purity of the distillate products remained acceptable. It was then concluded that it is not necessary to add hold-up values in a more complex ChemCAD simulation for accurate results.

The recovered product is summarized below:

- Mass of recovered water:
- Purity of recovered water:
- Mass of recovered DMSO:
- Purity of recovered DMSO:
- Total elapsed time:

[add updated comparison between methods 1 and 2]

Since we are working under vacuum in this distillation process, a proper vacuum pump was selected for this application. A breakdown of the selection is carried out in the next sub-chapter.

## Vacuum Pump Selection

A vacuum pump was required to evacuate the distillation system prior to the start of each batch. The objective was to reduce the system pressure from atmospheric pressure (1.0 bar absolute) to the operating pressure of 0.1 bar absolute before heating commenced. Since the vacuum pump is only used during the initial evacuation stage and not during normal distillation operation, the pump was sized based on the required pump-down time and the total gas volume contained within the equipment.

The total volume to be evacuated consists of the vapor space in the feed tank and the internal volume of the distillation column. The feed tank has a total volume of approximately 8 m³ and contains approximately 6 m³ of liquid before the start of the distillation, resulting in a vapor space of 2 m³. The distillation column has a height of 9.6 m and a diameter of 0.60 m, corresponding to an internal volume of approximately 3.15 m³. Accounting for additional piping and system volume, the total gas volume to be evacuated was approximated as 6.0 m³ [cite].

The required pumping speed was calculated using the standard vacuum pump-down equation [cite]:

$$
S=\frac{V}{t}\ln\left(\frac{P_1}{P_2}\right)
$$

where:

- $S$ = required pumping speed (m³/s)
- $V$ = gas volume to be evacuated (m³)
- $t$ = desired pump-down time (s)
- $P_1$ = initial pressure (bar abs)
- $P_2$ = final pressure (bar abs)

Substituting the design values:

$$
V = 6.0\ \mathrm{m^3}
$$

$$
t = 20 \times 60 = 1200\ \mathrm{s}
$$

$$
P_1 = 1.0\ \mathrm{bar}
$$

$$
P_2 = 0.1\ \mathrm{bar}
$$

gives:

$$
S=\frac{6.0}{1200}\ln\left(\frac{1.0}{0.1}\right)
$$

$$
S=0.0115\ \mathrm{m^3/s}
$$

$$
S=41.4\ \mathrm{m^3/h}
$$

Therefore, the vacuum system must provide a minimum pumping speed of approximately 41 m³/h to achieve the required vacuum level within 20 minutes.

A liquid ring vacuum pump was selected due to its suitability for handling condensable vapors and traces of process fluids. Compared to oil-sealed rotary vane pumps, liquid ring pumps are more tolerant to water vapor and solvent carryover, making them well suited for vacuum distillation applications. Since the process involves water and dimethyl sulfoxide (DMSO), a liquid ring design provides increased operational robustness and reliability [cite].

The selected vacuum pump is the Busch DOLPHIN VX 0055 A Total Recirculation liquid ring vacuum pump. The manufacturer specifies a nominal pumping speed of 47 m³/h at 50 Hz and an ultimate pressure of 33 mbar absolute. Since the required operating pressure is 100 mbar absolute and the required pumping speed is 41.4 m³/h, the selected pump satisfies both requirements.

The selected pump specifications were summarized:

Table: Vacuum pump specifications.
\label{tab:Vacuum pump specifications}

| Parameter                   |                   Value |
| --------------------------- | ----------------------: |
| Pump model                  | Busch DOLPHIN VX 0055 A |
| Pump type                   | Liquid ring vacuum pump |
| Pumping speed               |                 47 m³/h |
| Ultimate pressure           |             33 mbar abs |
| Required operating pressure |            100 mbar abs |
| Required pumping speed      |               41.4 m³/h |
| Estimated pump-down time    |                  20 min |

[add picture of pump graph]

Based on the calculated evacuation requirements and the manufacturer's performance data, the Busch DOLPHIN VX 0055 A was determined to be suitable for achieving the desired vacuum level within the specified pump-down time while providing reliable operation in the presence of water and DMSO vapors.

We will need to account for the energy this pump will require to operate for 20 minutes, in order to accurately compare the affordability of Method 1 compared to Method 2.

[add energy estimation]

[add comparison conclusion]

[add picture of pump]
