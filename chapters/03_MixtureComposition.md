# Mixture Composition

## Initial Conditions

Our mixture to be separated has a volume of 3500 liters, and a composition of 66.6 mol% isopropanol, and 33.4 mol% water. The time available to complete the distillation process is 22 hours.
Inside the batch distillation column, the temperature will gradually increase until it reaches the boiling point of the mixture, 80.2 ֯C. Our column was assigned a number of theoretical stages n=12 (including the total condenser and the still pot). The feed stage initially is the 5th counted from the top.
As for our entrainer, dimethyl sulfoxide (DMSO) will be fed to the column at 100% purity, room temperature (25 ֯C) and 1.013 bar in pressure. The chosen starting feed flow rate is 5 kmol/h. These parameters are to be changed depending on the results.

Table: Binary interaction parameters.
\label{tab:Binary interaction parameters}

|      I      |         J          | Bij [Cal/mol] | Bji [Cal/mol] | Alpha [Cal/mol] |
| :---------: | :----------------: | :-----------: | :-----------: | :-------------: |
| Isopropanol |       Water        |    20.0554    |    832.981    |     0.3255      |
| Isopropanol | Dimethyl Sulfoxide |    115.279    |   -25.0123    |       0.4       |
|    Water    | Dimethyl Sulfoxide |    1203.77    |   -524.822    |     0.6615      |

In the table above we can find the binary interaction parameters (BIPs) for our mixture, which are the coefficients to be used in the NRTL thermodynamic model to describe the interactions between pairs of molecules in our mixture. The BIPs describe the excess Gibbs free energy of mixing[@yao_ling_chien_2007].

At the beginning of the process, we will start with total reflux (R=∞). After the steady-state is reached, we will be working with an initial reflux ratio of R=6, subject to change as the analysis progresses. In the same manner, we will start with an initial feed temperature of 20°C, 12 stages, feed stage 4, and a feed flow rate of 5 kmol/h.

## Azeotrope Condition

In our case, our azeotrope presents at a mass fraction of 87-88% and a temperature of 80.2 – 80.4 °C. This is due to the interactions between the molecules (see Table 1) of each component in the solution.

\begin{figure}[H]
\centering
\includegraphics[width=0.9\textwidth]{figs/Picture1.png}
\caption{Graphical representation of the azeotrope present in the water/IPA mixture.}
\label{fig:Graphical representation of the azeotrope present in the water/IPA mixture}
\end{figure}

## Residue Curves

Our residue curves depict how the liquid composition in the distillation still-pot evolves over time during simple batch distillation at 1.01 bar. Each vertex of the triangle represents 100% of the component, and for the IPA-water-DMSO system the curves start at the azeotrope, showing the need for DMSO to carry out the separation. They, too, illustrate the separation trajectory: the concentration of DMSO increases as time progresses for every case, revealing that the distillation of this mixture will generally lead to DMSO accumulation in the pot, while IPA and water are removed. Similarly, the diagram tells us that DMSO forms no azeotropes with the other two components.

\begin{figure}[H]
\centering
\includegraphics[width=0.8\textwidth]{figs/Picture2.png}
\caption{Residue curves of our mixture.}
\label{fig:Residue curves of our mixture.}
\end{figure}
