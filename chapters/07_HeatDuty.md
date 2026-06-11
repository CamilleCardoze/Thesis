# Heat Duty

The distillation process requires energy, which we will want to keep at a minimum in order not to spend resources unnecessarily. Each parameter changes the heat duty of the operation in a different way; however, we have set the column re-boiler’s duty to be 1000 MJ/h, therefore we will focus on how heating up the DMSO feed will affect the outcomes, which we will calculate using a controller and a heat exchanger (via ChemCAD simulation). We will gather data relating to the amount of energy it takes to heat up the DMSO to a desired temperature, and how much energy it takes to feed the column. We will add our obtained quantities to the overall column duty and multiply by the number of hours it takes for the process to be complete.

\begin{figure}[H]
\centering
\includegraphics[width=0.5\textwidth]{figs/heatd.png}
\caption{Layout of the heat duty measurement equipment in ChemCAD.}
\label{fig:Layout of the heat duty measurement equipment in ChemCAD.}
\end{figure}

Below are the results of the conducted simulations:

Table: Feed Heating Duty  
\label{tab:Feed Heating Duty}

| Trial | Temperature (°C) | Calculated Heat Duty (MJ/h) |
| ----: | ---------------: | --------------------------: |
|     1 |               20 |                           0 |
|     2 |               32 |                     12.8504 |
|     3 |               44 |                     25.7242 |
|     4 |               56 |                     38.6459 |
|     5 |               68 |                       51.64 |
|     6 |               80 |                     64.7311 |

We can observe that raising the feed temperature from 20֯C to 62֯C will require a heat duty of around 50 MJ/h, and it will be heated up during the entire dIPA distillation process, which is 9.05 hours. Adding this to our reboiler duty, which will work for 16.15 hours, we obtain 16600 MJ in total for the distillation of IPA.

## Energy Cost Estimation

The energy cost was estimated from the reboiler duty and the additional energy required to heat the DMSO feed from 20°C to 62°C. As of 2012 in the United States, literature reports a general electricity cost of approximately:

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

Therefore, using the energy cost reported by literature [cite], the estimated energy cost is approximately 159.64 $\text{\$}$ for the main IPA distillation step and 278.92 $\text{\$}$ for the complete process.
