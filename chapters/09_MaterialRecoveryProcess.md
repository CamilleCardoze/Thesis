# Material Recovery

After the main batch extractive distillation step, two secondary off-cut streams are produced: an IPA/water off-cut and a water/DMSO off-cut. These streams do not meet the purity requirements to be considered final products, but they still contain recoverable amounts of IPA, water, and DMSO. Therefore, instead of treating them as waste, their re-integration into later batches was studied in order to reduce material losses and improve the overall efficiency of the process.

Two recycling strategies were compared using ChemCAD simulations. In both cases, the results of one batch were used as input for the next batch. Batch 1 corresponds to the original reference batch, while Batches 2–6 represent five consecutive recycle batches. For each batch, the total moles, mass, purity of the off-cut streams, IPA distillate purity, distillate mass, elapsed time, and DMSO bottom-product purity were recorded.

In the first method, only the IPA/water off-cut is added to the pot charge of the next batch, while the recovered DMSO bottom product from the previous distillation is used as the solvent feed for the next batch. Since the amount of recovered DMSO is lower than the amount required for a complete new batch, the missing amount would be replaced in practice by externally supplied, theoretically pure DMSO. However, in the simulation, the additional pure DMSO was not included in the purity calculation. Instead, the purity of the recovered bottom DMSO was used as the next solvent-feed purity, representing the worst-case scenario. The water/DMSO off-cut is not directly recycled in this method and is instead kept for later recovery distillation.

In the second method, both the IPA/water off-cut and the water/DMSO off-cut are added directly to the pot charge of the next batch. This method has the advantage of immediately reusing all off-cut material, but it also introduces more water and DMSO into the next batch, which can influence the charge composition, separation time, and simulation convergence.

## Method 1, Water/IPA off-cut Recycling

In the first recycling method, the IPA/water off-cut from each batch was added to the pot charge of the following batch. The DMSO bottom product from the previous batch was reused as the next batch’s solvent feed. The water/DMSO off-cut was not added directly to the following batch, but was instead collected for later recovery. This approach aims to recover IPA-containing material without continuously increasing the amount of DMSO in the pot charge.

The initial charge molar amounts used for this recycle sequence were 41.18 kmol IPA and 21.21 kmol water. During the ChemCAD simulations, some operating adjustments were required to maintain convergence and product purity. For Batch 2, the reflux ratio in step 3 was changed from 4 to 5. For Batch 5, the reflux ratio in step 3 was further changed from 5 to 6. These changes were necessary to keep the distillate within the required purity range as the recycled material influenced the batch composition. The meaning of the abbreviations used in the tables' column titles are:

- B: batch number
- Chg.: charge
- Dist.: distillate
- OC: off-cut
- x: molar fraction
- m: mass

### IPA/Water off-cut and IPA Distillate Results

\footnotesize
Table: Results of the first material recovery method.
\label{tab: Results of the first material recovery method}

|   B | IPA OC | H₂O OC |   xIPA OC |  m OC | nIPA Chg. | nH₂O Chg. | xIPA Chg. | xH₂O Chg. | xIPA Dist. | mDist. |    t |
| --: | -----: | -----: | --------: | ----: | --------: | --------: | --------: | --------: | ---------: | -----: | ---: |
|     |   kmol |   kmol | mol frac. |    kg |      kmol |      kmol | mol frac. | mol frac. |  mol frac. |     kg |    h |
|   1 |   1.30 |   5.29 |    0.1975 | 173.6 |     42.48 |     26.51 |    0.6158 |    0.3842 |     0.9985 | 2397.4 | 16.1 |
|   2 |   1.71 |   7.04 |    0.1957 | 229.9 |     42.90 |     28.26 |    0.6029 |    0.3971 |     0.9989 | 2477.9 | 18.2 |
|   3 |   1.68 |   6.71 |    0.1999 | 221.6 |     42.86 |     27.92 |    0.6055 |    0.3945 |     0.9985 | 2477.2 | 18.5 |
|   4 |   1.65 |   6.73 |    0.1971 | 220.6 |     42.83 |     27.94 |    0.6052 |    0.3948 |     0.9985 | 2477.1 | 18.8 |
|   5 |   1.80 |   7.36 |    0.1963 | 240.6 |     42.98 |     28.57 |    0.6007 |    0.3993 |     0.9990 | 2466.7 | 19.5 |
|   6 |   1.74 |   7.04 |    0.1977 | 231.1 |     42.92 |     28.25 |    0.6030 |    0.3970 |     0.9987 | 2479.4 | 19.8 |

\normalsize

Results are listed in Table 9.1. The IPA distillate purity remained consistently above the required value in all six batches. The average IPA distillate purity was 0.9987 mol fraction, while the total recovered IPA distillate mass was 14775.70 kg. The total operating time for the six batches was approximately 111 h. A slight increase in operating time can be observed from Batch 1 to Batch 6, which is expected because the recycled IPA/water off-cut changes the initial pot composition of each new batch.

### Water/DMSO off-cut Obtained During Method 1

Table: Water/DMSO off-cut obtained during method 1.
\label{tab:Water/DMSO off-cut obtained uring method 1}

|   B |  H₂O |  DMSO |      xH₂O |     xDMSO | mTotal |
| --: | ---: | ----: | --------: | --------: | -----: |
|     | kmol |  kmol | mol frac. | mol frac. |     kg |
|   1 | 3.29 | 15.92 |    0.1713 |    0.8287 | 1302.9 |
|   2 | 2.47 | 15.75 |    0.1356 |    0.8644 | 1275.1 |
|   3 | 2.57 | 16.01 |    0.1382 |    0.8618 | 1297.5 |
|   4 | 2.60 | 15.98 |    0.1398 |    0.8602 | 1295.3 |
|   5 | 2.06 | 15.48 |    0.1176 |    0.8824 | 1246.8 |
|   6 | 2.00 | 15.56 |    0.1139 |    0.8861 | 1252.1 |

The water/DMSO off-cut contains a significant amount of DMSO, with an average DMSO mole fraction of 0.8639, as indicated in Table 9.2. Since this material is not directly returned to the next batch in Method 1, it remains available for a later recovery distillation. This prevents additional DMSO accumulation in the main IPA recovery process, but requires an additional recovery step.

### DMSO Bottom Product Obtained During Method 1

Table: DMSO bottom product obtained during method 1.
\label{tab:DMSO bottom product obtained during method 1}

|   B |  DMSO |    H₂O |     xDMSO |      xH₂O |  mTotal |
| --: | ----: | -----: | --------: | --------: | ------: |
|     |  kmol |   kmol | mol frac. | mol frac. |      kg |
|   1 | 51.96 | 0.0255 |    0.9995 |   0.00049 | 4060.02 |
|   2 | 53.20 | 0.0253 |    0.9995 |   0.00047 | 4157.48 |
|   3 | 53.70 | 0.0252 |    0.9995 |   0.00047 | 4195.97 |
|   4 | 53.73 | 0.0256 |    0.9995 |   0.00048 | 4198.89 |
|   5 | 53.85 | 0.0253 |    0.9995 |   0.00047 | 4207.86 |
|   6 | 54.14 | 0.0248 |    0.9995 |   0.00046 | 4230.33 |

The DMSO bottom product remained highly pure throughout the recycle sequence, with an average DMSO mole fraction of 0.9995 according to Table 9.3. This confirms that the recovered bottom DMSO can be reused as solvent feed in the following batch. However, the recovered amount is not enough to supply a full new batch, so external pure DMSO would still be required in practice.

The water/IPA off-cut re-integration method is stable and effective. It maintains the IPA distillate purity above the required specification, gives a high total recovered distillate mass, and produces a pure DMSO bottom product suitable for reuse. Its main disadvantage is that the water/DMSO off-cut is not immediately recycled and must be treated separately later. However, this also makes the main distillation sequence easier to control, since DMSO does not accumulate as strongly in the next batch charge.

## Method 2, Total off-cut Recycling

In the second recycling method, both the IPA/water off-cut and the water/DMSO off-cut were added directly to the next pot charge. This means that all off-cut material from the previous batch was immediately reused in the following batch. The purpose of this method was to determine whether direct recycling of all secondary material streams could improve material recovery and reduce the need for a separate recovery step.

The same initial charge molar values were used as in Method 1: 41.18 kmol IPA and 21.214 kmol water. Since both off-cut streams were recycled, the DMSO content in the pot charge increased compared with Method 1. This made the simulation more difficult to converge in some cases. In Batch 2, the reflux ratio in step 3 was changed from 4 to 5. In Batch 3, the stop value in step 3 was changed from 0.9995 to 0.9997. In Batch 4, the reflux ratio in step 3 was increased from 5 to 6. In Batch 5, the reflux ratio was changed back from 6 to 5. These adjustments show that Method 2 required more operational changes than Method 1.

### Combined IPA/Water/DMSO off-cut and IPA Distillate Results

\footnotesize
Table: Results of the second material recovery method.
\label{tab:Results of the second material recovery method}

|   B | IPA OC | H₂O OC | DMSO OC |    mOC | nIPA Chg. | nH₂O Chg. | xIPA Chg. | xH₂O Chg. | xDMSO Chg. | xIPA Dist. | mDist. |    t |
| --: | -----: | -----: | ------: | -----: | --------: | --------: | --------: | --------: | ---------: | ---------: | -----: | ---: |
|     |   kmol |   kmol |    kmol |     kg |      kmol |      kmol | mol frac. | mol frac. |  mol frac. |  mol frac. |     kg |    h |
|   1 |   1.30 |   8.58 |   15.92 | 1476.5 |     42.48 |     29.80 |    0.4817 |    0.3378 |     0.1805 |     0.9985 | 2397.4 | 16.1 |
|   2 |   1.98 |  11.11 |   19.26 | 1824.0 |     43.17 |     32.32 |    0.4556 |    0.3411 |     0.2033 |     0.9989 | 2468.5 | 19.7 |
|   3 |   2.10 |   11.9 |   20.43 | 1936.6 |     43.28 |     33.08 |    0.4471 |    0.3417 |     0.2111 |     0.9988 | 2468.5 | 20.7 |
|   4 |   2.06 |  11.23 |   20.26 | 1909.2 |     43.24 |     32.44 |    0.4507 |    0.3381 |     0.2112 |     0.9985 | 2478.1 | 21.9 |
|   5 |   2.03 |  11.77 |   20.93 | 1969.6 |     43.21 |     32.98 |    0.4449 |    0.3396 |     0.2155 |     0.9985 | 2477.4 | 20.8 |
|   6 |   2.19 |  12.33 |   21.00 | 1994.2 |     43.37 |     33.54 |    0.4429 |    0.3426 |     0.2145 |     0.9989 | 2465.9 | 21.0 |

\normalsize

\begin{figure}[H]
\centering

    \begin{subfigure}{0.5\textwidth}
        \centering
        \includegraphics[width=\textwidth]{figs/massgraph.jpg}
    \end{subfigure}
    \hfill
    \begin{subfigure}{0.5\textwidth}
        \centering
        \includegraphics[width=\textwidth]{figs/timegraph.png}
    \end{subfigure}

    \caption{Comparison between the total distillate purity and total distillate mass results, respectively, of Method 1 and Method 2.}
    \label{fig:Comparison between the total distillate purity and total distillate mass results}

\end{figure}

Results are listed in Table 9.4. Both methods provided a distillate of sufficient purity, therefore all batches can be used; plotting was not needed. In Figure 9.1, can be seen when the reflux ratio is adjusted.

The IPA distillate purity remained above the target in all batches, with an average value of 0.9987 mol fraction. However, the total distillate mass was slightly lower than in Method 1, with 14755.93 kg recovered over the six batches. The total operating time increased to 120.20 h, which is 9.20 h longer than Method 1.

### DMSO Bottom Product Obtained During Method 2

Table: DMSO bottom product obtained during method 2.
\label{tab:DMSO bottom product obtained during method 2}

|   B |  DMSO |    H₂O |     xDMSO |      xH₂O |  mTotal |
| --: | ----: | -----: | --------: | --------: | ------: |
|     |  kmol |   kmol | mol frac. | mol frac. |      kg |
|   1 | 51.96 | 0.0255 |    0.9995 |   0.00049 | 4060.02 |
|   2 | 66.36 | 0.0323 |    0.9995 |   0.00049 | 5185.60 |
|   3 | 69.66 | 0.0331 |    0.9995 |   0.00048 | 5443.17 |
|   4 | 71.38 | 0.0343 |    0.9995 |   0.00048 | 5578.05 |
|   5 | 70.54 | 0.0330 |    0.9995 |   0.00047 | 5512.53 |
|   6 | 70.77 | 0.0328 |    0.9995 |   0.00046 | 5530.48 |

\begin{figure}[H]
\centering

    \begin{subfigure}{0.5\textwidth}
        \centering
        \includegraphics[width=\textwidth]{figs/dmsopurity.png}
    \end{subfigure}
    \hfill
    \begin{subfigure}{0.5\textwidth}
        \centering
        \includegraphics[width=\textwidth]{figs/dmsoamount.png}
    \end{subfigure}

    \caption{Comparison between the total bottom DMSO purity and total amount of DMSO recovered, respectively, with Method 1 and Method 2. Peaks can be seen when the reflux ratio is adjusted.}
    \label{fig:Comparison between the total bottom DMSO purity and total amount of DMSO recovered}

\end{figure}

As showcased in Figure 9.2, DMSO bottom purity remained high, with an average value of 0.9995 mol fraction. However, the total DMSO bottom mass increased significantly compared with Method 1. This is expected because the water/DMSO off-cut is recycled directly into the pot charge, causing more DMSO to remain within the main batch sequence (see Table 9.5).

## Comparison of the Two Recycling Methods

Table: Comparison between Method 1 and Method 2.
\label{tab:Comparison between Method 1 and Method 2}

| Parameter                   |            Method 1 |             Method 2 |
| --------------------------- | ------------------: | -------------------: |
| Avg. xIPA Dist. [mol frac.] |              0.9987 |               0.9987 |
| Total mDist. [kg]           |            14775.70 |             14755.93 |
| Total t [h]                 |              111.00 |               120.20 |
| Total Bottom m [kg]         |            25050.56 |             31309.85 |
| OC handled [kg]             | 7669.81 H₂O/DMSO OC | 11110.08 combined OC |
| Recycle batches studied     |                   5 |                    5 |
| Operating adjustments       |               Fewer |                 More |

Table 9.6 shows that both recycling strategies achieved the required IPA product purity. The average IPA distillate purity was practically the same for both methods, at approximately 0.9987 mol fraction. However, Method 1 produced a slightly larger total IPA distillate mass and required less total operating time. Method 2 required 120.20 h compared with 111.00 h for Method 1, which means that total off-cut re-integration increased the total process time by 9.30 h over the six simulated batches.

Method 2 also required more changes to the simulation settings to maintain convergence and product quality. This suggests that adding both off-cut streams directly to the next pot charge makes the process more sensitive to composition changes. The larger DMSO bottom mass in Method 2 also shows that DMSO accumulates more strongly in the batch sequence when the water/DMSO stream is directly recycled.

Total off-cut re-integration is technically possible, since it still achieves the required IPA purity and produces a high-purity DMSO bottom stream, and it actually allows us to recover more total DMSO (moles) from the bottom of the column. However, it is less favorable than Method 1 because it increases the operating time, requires more reflux ratio adjustments, and causes greater DMSO accumulation in the system; furthermore, even though more DMSO is recovered overall, each batch produces lower quality bottom compared to Method 1. Based on this comparison, the preferred material recovery strategy is Method 1: water/IPA off-cut re-integration combined with separate later treatment of the water/DMSO off-cut. This approach gives similar product purity, slightly higher IPA recovery, shorter operating time, and better process stability. Since the reboiler's heat duty is directly correlated to the elapsed time due to it being set at 1000 MJ/h, less time needed to complete the process means that it is more environmentally and financially affordable, not only less time consuming.

## Water/DMSO off-cut Distillation

The water/DMSO off-cut distillation serves as a following step to the water/IPA re-integration. The same column is to be used for this process. The goal of this extra step is to recover as much DMSO and water as possible, for it to be repurposed later. The obtained, total molar amount of water and DMSO from the water/DMSO off-cut were calculated after the 5 batches for Method 1, and this result was the pot charge for the distillation. There will be no feed or external entrainer. We created a separate ChemCAD simulation with the same column parameters and initial conditions, presented in Figure 9.3.

\begin{figure}[H]
\centering
\includegraphics[width=0.8\textwidth]{figs/DMSOdist.png}
\caption{Simulation layout for the Water-DMSO distillation.}
\label{fig:Simulation layout for the Water-DMSO distillation}
\end{figure}

Different stop values for the process were investigated, finally 0.998 mol frac. water in the accumulator (water is more volatile than DMSO), as well as reflux ratio values and internal column values. The reflux ratio was varied in the range R = 2 to R = 10 (see Figure 9.4), and the pressure was studied between 1 bar and 0.1 bar (see Figure 9.5) [@bme_distillation_notes_v_nd].

\begin{figure}[H]
\centering

    \begin{subfigure}{0.48\textwidth}
        \centering
        \includegraphics[width=\textwidth]{figs/R2.png}
    \end{subfigure}
    \hfill
    \begin{subfigure}{0.48\textwidth}
        \centering
        \includegraphics[width=\textwidth]{figs/R4.png}
    \end{subfigure}

    \par\medskip

    \begin{subfigure}{0.48\textwidth}
        \centering
        \includegraphics[width=\textwidth]{figs/R6.png}
    \end{subfigure}
    \hfill
    \begin{subfigure}{0.48\textwidth}
        \centering
        \includegraphics[width=\textwidth]{figs/R9.png}
    \end{subfigure}

    \caption{Distillate graphs demonstrating the effect of the reflux ratio, first parameter studied at 1 bar (at R = 2, 4, 6 and 9, respectively).}
    \label{fig:Distillate graphs demonstrating the effect of pressure}

\end{figure}

\begin{figure}[H]
\centering

    \begin{subfigure}{0.48\textwidth}
        \centering
        \includegraphics[width=\textwidth]{figs/1bar.png}
    \end{subfigure}
    \hfill
    \begin{subfigure}{0.48\textwidth}
        \centering
        \includegraphics[width=\textwidth]{figs/0.5bar.png}
    \end{subfigure}

    \par\medskip

    \begin{subfigure}{0.48\textwidth}
        \centering
        \includegraphics[width=\textwidth]{figs/0.25bar.png}
    \end{subfigure}
    \hfill
    \begin{subfigure}{0.48\textwidth}
        \centering
        \includegraphics[width=\textwidth]{figs/0.1 bar.png}
    \end{subfigure}

    \caption{Distillate graphs demonstrating the effect of pressure when the reflux ratio is set to 9 (at 1, 0.5, 0.25 and 0.1 bar, respectively).}
    \label{fig:Distillate graphs demonstrating the effect of pressure in Water/DMSO distillation}

\end{figure}

The reflux-ratio graphs must be interpreted together with the elapsed time and the actual distillate composition. At low reflux ratios, the separation may appear sharper because the operation is completed in a shorter time and the transition between composition regions is compressed on the time axis. However, this does not correspond to better separation, since the distillate obtained at lower reflux ratios contains a higher amount of DMSO. In contrast, at $R = 9$, the operation lasts longer, but the water-rich and DMSO-rich regions are more clearly separated, and DMSO carry-over into the distillate is reduced. Therefore, the high reflux ratio is required to provide sufficient rectification, not simply because of the longer operating time.

The pressure-variation graphs must be interpreted in the same way. DMSO has a non-zero vapour pressure throughout the distillation, so the relevant factor is not whether DMSO starts evaporating, but how the water/DMSO ratio in the vapour and distillate changes as the batch progresses. The profiles below 1 bar appear almost unchanged at first, but the slightly longer operating times give a clearer transition between the water-rich and DMSO-rich regions. The length and slope of the decreasing section remain approximately similar, while the total elapsed time increases, indicating a more gradual and better-resolved separation. Based on these results, the selected conditions were $R = 9$ and $P = 0.1$ bar, which gave the most suitable separation between the water-rich distillate and the DMSO-rich bottom product.

However, the ChemCAD simulation needed additional aid in order to converge. Hold-up values were added: 5 dm3 for the condenser and 3 dm3 for the stages [@kiss_2013]. These represent the liquid volume that gets held up back due to the geometry of the condenser and the type of packing. Adding hold up values also makes the process more accurate and realistic.

In order to maintain realism, several batches for both recycling methods were performed again, with the same hold-up values for the column as in the water/DMSO distillation. Our products (composition, mass, time) only slightly changed, affecting the values only after 2-3 decimal points. Purity of the distillate products remained acceptable. It was then concluded that it is not necessary to add hold-up values in a more complex ChemCAD simulation for accurate results.

The recovered product is summarized below:

- Mass of recovered water: 268.72 kg
- Purity of recovered water: 0.9975 mole fraction water
- Mass of recovered DMSO: 7401.16 kg
- Purity of recovered DMSO: 0.9975 mole fraction DMSO
- Total elapsed time: 6.55 h

As it can be seen, with Method 1 the yields are still better than Method 2, and the new elapsed time is still inferior (117.55 h compared to 120.2 h). Therefore, even though it includes more steps, it can be concluded that Method 1 is the most efficient.

Since this distillation process is under vacuum, a proper vacuum pump was selected for this application. A breakdown of the selection is carried out in the next sub-chapter.

## Vacuum Pump Selection

A vacuum pump was required to evacuate the distillation system prior to the start of each batch. The objective was to reduce the system pressure from atmospheric pressure (1.0 bar absolute) to the operating pressure of 0.1 bar absolute before heating commenced. Since the vacuum pump is only used during the initial evacuation stage and not during normal distillation operation, the pump was sized based on the required pump-down time and the total gas volume contained within the equipment.

The total volume to be evacuated consists of the vapor space in the feed tank and the internal volume of the distillation column. The feed tank has a total volume of 7.85 m³ and contains approximately 6 m³ of liquid before the start of the distillation, resulting in a vapor space of 1.85 m³. The distillation column has a height of 10 m and a diameter of 0.76 m, corresponding to an internal volume of approximately 6.39 m³. To allow for additional system volume, the total gas volume to be evacuated was approximated as 6.5 m³.

The required pumping speed was calculated using the standard vacuum pump-down equation [@pfeiffer_vacuum_basic_calculations]:

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

$V = 6.5\ \mathrm{m^3}$

We want the pump-down time to be approximately 20 minutes:

$t = 20 \times 60 = 1200\ \mathrm{s}$

This gives:

$S=\frac{6.5}{1200}\ln\left(\frac{1.0}{0.1}\right) = 0.01247\ \mathrm{m^3/s} = 44.9\ \mathrm{m^3/h}$

Therefore, the vacuum system must provide a minimum pumping speed of approximately 45 m³/h to achieve the required vacuum level under the desired time.

A liquid ring vacuum pump was selected due to its suitability for handling condensable vapors and traces of process fluids. Compared to oil-sealed rotary vane pumps, liquid ring pumps are more tolerant to water vapor and solvent carryover, making them well suited for vacuum distillation applications. Since the process involves water and dimethyl sulfoxide (DMSO), a liquid ring design provides increased operational robustness and reliability [@busch_dolphin_vx_0030_0055].

The selected vacuum pump is the Busch DOLPHIN VX 0055, a total recirculation liquid ring vacuum pump
(see Figure 9.6). The manufacturer specifies a nominal pumping speed of 47 m³/h at 50 Hz and an ultimate pressure of 33 mbar absolute. Since the required operating pressure is 100 mbar absolute and the required pumping speed is 45 m³/h, the selected pump satisfies both requirements.

\begin{figure}[H]
\centering
\includegraphics[width=0.9\textwidth]{figs/pumpspecs.png}
\caption{Dimensional drawing, pumping speed vs flow rate plot, and specifications of the selected pump \cite{busch_dolphin_vx_0030_0055}.}
\label{fig:specifications of the selected pump}
\end{figure}
