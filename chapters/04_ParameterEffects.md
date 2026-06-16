# Parameter Effects

## Targets

For the dehydration of isopropanol, the distillate’s solution must be ≥ 99.75 mol% IPA, ≤ 0.55 mol% water, and ≤ 0.15 mol% dimethyl sulfoxide.
At the time of recovery, the water will be extracted as distillate. In this solution, less than 0.05 mol% IPA should be present, and less than 0.035 mol% DMSO.
After the whole process is finished, we will collect the remaining DMSO from the bottom of the column; We will use the same purity requirements stated for IPA, that is, ≥ 99.75 mol% DMSO, ≤ 0.55 mol% water, and ≤ 0.15 mol% IPA.

## Parameters studied

- Feed stage [-]
- Reflux ratio [-]
- Number of stages [-]
- Feed flow rate [kmol/h]
- Feed Temperature [°C]

Dependable variables:

- Mass of the IPA product
- Time
- Molar fraction (purity) of the product

Goals:

- Maximum mass
- Minimum time
- Maximum purity distillate (≥0.975 mole fraction IPA, ≤0.0025 water, ≤0.0015 DMSO)

Constant values:

- Volume of charge: 3500 dm3
- Charge temperature: 80֯C
- Reboiler duty: 1000 MJ/h
- Charge composition:
  - 0.66 mole fraction IPA
  - 0.34 mole fraction water
- Feed composition: 1 mole fraction DMSO (theoretically)

We have adhered to an interval of 15-30 for the number of stages, 5-10 kmol/h for the feed rate, 4-8 for the feed stage, 50-70 °C for the feed temperature, and 4-6 for the reflux ratio, as these are common industrial values that have showed good efficiency of separation in literature [@nemeth_hegely_lang_2019], [@gerbaud_rodriguez_donis_hegely_lang_denes_you_2019]. A quite difficult, azeotropic separation calls for several stages and a high R.

It is worth mentioning that, in simulations where the feed temperature is not being evaluated, a constant feed temperature value of 70֯C is chosen. All parameters were studied in the order in which they will be presented below. For parameters besides feed temperature, their constant values during the initial simulations were the averaged value of the ranges mentioned previously (22 stages, a feed rate of 7.5 kmol/h, a feed in stage number 6, and a reflux ratio of 5).

Below, we can see the purity results and total elapsed time of the last attempts tried with different parameter values; data obtained from sensitivity analyses. The final parameters were chosen through an iterative process, in which a sensitivity analysis is conducted, parameters were changed to achieve optimal results, and another sensitivity analysis is carried out until results are satisfactory.

Table: Feed Stage Data  
\label{tab:Feed Stage Data}

| Trial | Feed Stage | Mole Fraction | Time (h) | Mass (kg) |
| ----: | ---------: | ------------: | -------: | --------: |
|     1 |          1 |      0.727319 |  8.45001 |   3509.90 |
|     2 |    3.66667 |      0.997528 |  9.20002 |   2380.31 |
|     3 |    6.33333 |      0.997400 |  9.20002 |   2381.18 |
|     4 |          9 |      0.997040 |  9.20002 |   2380.57 |
|     5 |    11.6667 |      0.997273 |  9.15002 |   2370.28 |
|     6 |    14.3333 |      0.995347 |  8.50001 |   2225.38 |
|     7 |         17 |      0.986126 |  8.15001 |   2132.24 |
|     8 |    19.6667 |      0.970703 |  7.90001 |   2051.91 |
|     9 |    22.3333 |      0.904141 |  8.20001 |   2021.87 |
|    10 |         25 |      0.717659 |    13.55 |   2696.94 |

Which can be plotted as:

\begin{figure}[H]
\centering

    \begin{subfigure}{0.48\textwidth}
        \centering
        \includegraphics[width=\textwidth]{figs/feedstagepuritymass.png}
    \end{subfigure}
    \hfill
    \begin{subfigure}{0.48\textwidth}
        \centering
        \includegraphics[width=\textwidth]{figs/feedstagetime.png}
    \end{subfigure}

    \caption{Feed stage effect on purity, mass and time.}
    \label{fig:Feed stage effect on purity, mass}

\end{figure}

Table: Reflux Ratio Data  
\label{tab:Reflux Ratio Data}

| Trial | Reflux Ratio | Mole Fraction | Time (h) | Mass (kg) |
| ----: | -----------: | ------------: | -------: | --------: |
|     1 |            3 |      0.996872 |    16.15 |   2393.41 |
|     2 |            4 |      0.997535 |    18.05 |   2406.52 |
|     3 |            5 |      0.997973 |    19.95 |   2413.92 |
|     4 |            6 |      0.997399 |    21.90 |   2424.64 |
|     5 |            7 |      0.997836 |  23.7999 |   2426.82 |

Which can be plotted as:

\begin{figure}[H]
\centering

    \begin{subfigure}{0.48\textwidth}
        \centering
        \includegraphics[width=\textwidth]{figs/Rpuritymass.png}
    \end{subfigure}
    \hfill
    \begin{subfigure}{0.48\textwidth}
        \centering
        \includegraphics[width=\textwidth]{figs/Rtime.png}
    \end{subfigure}

    \caption{Reflux ratio effect on purity, mass and time.}
    \label{fig:Reflux ratio effect on purity, mass and time}

\end{figure}

Table: Feed Rate Data  
\label{tab:Feed Rate Data}

| Trial | Feed Rate (kmol/h) | Mole Fraction | Time (h) | Mass (kg) |
| ----: | -----------------: | ------------: | -------: | --------: |
|     1 |                  5 |      0.987313 |  8.60001 |   2375.32 |
|     2 |            6.11111 |      0.995814 |  8.65001 |   2356.56 |
|     3 |            7.22222 |      0.997105 |  8.95002 |   2381.33 |
|     4 |            8.33334 |      0.996503 |  9.20002 |   2387.23 |
|     5 |            9.44445 |      0.997112 |  9.40002 |   2380.46 |
|     6 |            10.5556 |      0.996768 |  9.65002 |   2379.43 |
|     7 |            11.6667 |      0.996776 |  9.90002 |   2375.50 |
|     8 |            12.7778 |      0.997171 |    10.15 |   2368.91 |
|     9 |            13.8889 |      0.996996 |    10.45 |   2367.03 |
|    10 |                 15 |      0.997244 |    10.75 |   2362.07 |

Which can be plotted as:

\begin{figure}[H]
\centering

    \begin{subfigure}{0.48\textwidth}
        \centering
        \includegraphics[width=\textwidth]{figs/feedratepuritymass.png}
    \end{subfigure}
    \hfill
    \begin{subfigure}{0.48\textwidth}
        \centering
        \includegraphics[width=\textwidth]{figs/feedratetime.png}
    \end{subfigure}

    \caption{Feed rate effect on purity, mass and time.}
    \label{fig:Feed rate effect on purity, mass and time}

\end{figure}

Table: Stage Number Data  
\label{tab:Stage Number Data}

| Trial | Stage Number | Mole Fraction | Time (h) | Mass (kg) |
| ----: | -----------: | ------------: | -------: | --------: |
|     1 |           10 |      0.907955 |  8.15001 |   2016.42 |
|     2 |      12.2222 |      0.958189 |  7.85001 |   2022.11 |
|     3 |      14.4444 |      0.980373 |  8.05001 |   2100.75 |
|     4 |      16.6667 |      0.990602 |  8.30001 |   2173.13 |
|     5 |      18.8889 |      0.995448 |  8.50001 |   2225.54 |
|     6 |      21.1111 |      0.997299 |  9.15002 |   2370.32 |
|     7 |      23.3333 |      0.997048 |  9.20002 |   2380.59 |
|     8 |      25.5556 |      0.997349 |  9.20002 |   2381.05 |
|     9 |      27.7778 |      0.997496 |  9.20002 |   2381.28 |
|    10 |           30 |      0.997590 |  9.20002 |   2381.42 |

Which can be plotted as:

\begin{figure}[H]
\centering

    \begin{subfigure}{0.48\textwidth}
        \centering
        \includegraphics[width=\textwidth]{figs/stageNpuritymass.png}
    \end{subfigure}
    \hfill
    \begin{subfigure}{0.48\textwidth}
        \centering
        \includegraphics[width=\textwidth]{figs/stageNtime.png}
    \end{subfigure}

    \caption{Stage number effect on purity, mass and time.}
    \label{fig:Stage number effect on purity, mass and time}

\end{figure}

Table: Feed Temperature Data  
\label{tab:Feed Temperature Data}

| Trial | Feed Temperature (°C) | Mole Fraction | Time (h) | Mass (kg) |
| ----: | --------------------: | ------------: | -------: | --------: |
|     1 |                    20 |      0.996916 |  9.90002 |   2391.57 |
|     2 |                    32 |      0.996842 |  9.70002 |   2390.15 |
|     3 |                    44 |      0.996943 |  9.50002 |   2387.46 |
|     4 |                    56 |      0.997194 |  9.30002 |   2383.51 |
|     5 |                    68 |      0.997534 |  9.10002 |   2378.27 |
|     6 |                    80 |      0.996955 |  8.95002 |   2381.23 |

Which can be plotted as:

\begin{figure}[H]
\centering

    \begin{subfigure}{0.48\textwidth}
        \centering
        \includegraphics[width=\textwidth]{figs/feedTpuritymass.png}
    \end{subfigure}
    \hfill
    \begin{subfigure}{0.48\textwidth}
        \centering
        \includegraphics[width=\textwidth]{figs/feedTtime.png}
    \end{subfigure}

    \caption{Feed temperature effect on purity, mass and time.}
    \label{fig:Feed temperature effect on purity, mass and time}

\end{figure}

## Conclusion on Parameter Effects

The sensitivity analyses show that each parameter affects the IPA distillate purity, recovered mass, and elapsed time through different mechanisms. The feed stage strongly influences the contact between the DMSO feed and the internal vapour-liquid flows. If the feed is introduced too high, the solvent does not interact sufficiently with the liquid phase; if it is introduced too low, it cannot modify the relative volatility across enough of the column. For this reason, the best results occur at intermediate feed stages, while the extremes show clear drops in purity and, in one case, a strong increase in time. The reflux ratio improves separation by returning more condensed liquid to the column, increasing vapour-liquid contact. However, after a certain point, higher reflux gives only small purity improvements while greatly increasing the operating time, so the purity peak at the middle reflux values is more useful than simply choosing the highest reflux ratio. The feed flow rate mainly controls how much DMSO is available to break the IPA-water azeotropic behavior. Too low a flow rate gives insufficient solvent action, while too high a flow rate increases the elapsed time and can slightly reduce the recovered mass; therefore, an intermediate feed rate is preferred. Increasing the number of stages improves purity and mass because more equilibrium contacts are available, but the effect reaches a plateau at higher stage numbers, meaning that additional stages give diminishing returns and would mainly increase column size and cost. Finally, increasing feed temperature reduces the elapsed time because the feed enters closer to column conditions, but excessive heating can disturb the internal temperature and composition profiles. The purity peak occurs at a moderately high feed temperature, while the recovered mass tends to decrease as temperature rises. Overall, the selected parameter values should represent a compromise between high purity, high recovered mass, and low elapsed time, rather than the maximum value of only one dependent variable.

Table: Selected parameter values.
\label{tab:Selected parameter values}

| Feed Stage | Reflux Ratio | Feed Flow Rate | Number of Stages | Feed Temperature |
| :--------: | :----------: | :------------: | :--------------: | :--------------: |
|     4      |      4       |   7.5 kmol/h   |        24        |      62 °C       |

These final parameters were chosen taking maximum efficiency into consideration; they produce the best, balanced results regarding purity, elapsed time and mass.
We selected 24 stages for our column because, even though the elapsed time is high, it will give us the best purity results and the most amount of mass.
A feed stage of 4 gives us a good balance between distillate purity and mass, while keeping time at a minimum. A feed stage higher than 22 will give us good purity results too, but it will increase the time significantly.
As for the selected feed flow rate, a value between 6 and 7 kmol/h will be best, since we are able to complete the process at the shortest possible time and obtain the maximum amount of mass, with highest purity. Therefore, we have settled on 7.5 kmol/h, or 586.012 kg/h.
A reflux ratio of 6 would give us the best results according to our graph; however, the time a high reflux ratio needs and the energy it consumes are significantly higher. A reflux ratio of 4 gives us good enough results, while making up for time.
Feed temperature is chosen to be 62°C because, even though we won’t obtain the highest amount of distillate possible, it will reduce our elapsed time and give us the highest possible IPA purity.
