# Mixture Composition

## Initial Conditions

Our mixture to be separated has a volume of 3500 liters, and a composition of 66.6 mol% isopropanol (IPA), and 33.4 mol% water. The time available to complete the distillation process is 22 hours.
Inside the batch distillation column, the temperature will gradually increase until it reaches the boiling point of the mixture, 80.2 °C. Our column was assigned a number of theoretical stages of n = 12 (not including the total condenser and the still pot). The feed stage initially is the 5th, counted from the top.
As for the entrainer, dimethyl sulfoxide (DMSO) will be fed to the column at 100% purity, room temperature (25 °C) and 1.013 bar in pressure. The chosen starting feed flow rate is 5 kmol/h. These parameters are to be changed depending on the results.

Table: Binary interaction parameters.
\label{tab:Binary interaction parameters}

|      I      |         J          | Bij [Cal/mol] | Bji [cal/mol] | Alpha [cal/mol] |
| :---------: | :----------------: | :-----------: | :-----------: | :-------------: |
| Isopropanol |       Water        |    20.0554    |    832.981    |     0.3255      |
| Isopropanol | Dimethyl Sulfoxide |    115.279    |   -25.0123    |       0.4       |
|    Water    | Dimethyl Sulfoxide |    1203.77    |   -524.822    |     0.6615      |

In Table 3.1 can be found the binary interaction parameters (BIPs) for the mixture, which are the coefficients to be used in the NRTL thermodynamic model to describe the interactions between pairs of molecules in the mixture. The BIPs describe the excess Gibbs free energy of mixing [@yao_ling_chien_2007].

The process will start with total reflux (R = ∞) and after the steady-state is reached, it will be working with an initial reflux ratio of R = 6, subject to change as the analysis progresses. In the same manner, It will start with an initial feed temperature of 20°C and 12 theoretical stages for the column.

## Residue Curves

Residue curves (Figure 3.2) depict how the liquid composition in the distillation still-pot evolves over time during simple batch distillation at 1.01 bar. Each vertex of the triangle represents a pure component, and for the IPA-water-DMSO system the curves start at the azeotrope, showing the need for DMSO to carry out the separation. They, too, illustrate the separation trajectory: the concentration of DMSO increases as time progresses for every case, revealing that the distillation of this mixture will generally lead to DMSO accumulation in the pot, while IPA and water are removed. Similarly, the diagram tells us that DMSO forms no azeotropes with the other two components.

\begin{figure}[H]
\centering
\includegraphics[width=0.8\textwidth]{figs/Picture2.png}
\caption{Residue curves of the mixture, obtained from ChemCAD.}
\label{fig:Residue curves of the mixture.}
\end{figure}

## Effect of DMSO on the Azeotrope

The altered activity coefficients increase the relative volatility of IPA compared to water. This shifts the VLE curve, eliminating the original azeotropic point where x = y. The high boiling point of DMSO (189°C) ensures it mostly remains in the liquid phase, accumulating in the column’s extractive section. This prevents IPA-water azeotrope reformation and allows IPA to distill overhead. As it can be seen in Figure 3.2, The IPA-water-DMSO system no longer exhibits an azeotrope, enabling distillation to achieve >99.75% IPA purity.

\begin{figure}[H]
\centering

    \begin{subfigure}{0.48\textwidth}
        \centering
        \includegraphics[width=\textwidth]{figs/Picture22.png}
    \end{subfigure}
    \hfill
    \begin{subfigure}{0.48\textwidth}
        \centering
        \includegraphics[width=\textwidth]{figs/Picture23.png}
    \end{subfigure}

    \par\medskip

    \begin{subfigure}{0.48\textwidth}
        \centering
        \includegraphics[width=\textwidth]{figs/Picture24.png}
    \end{subfigure}
    \hfill
    \begin{subfigure}{0.48\textwidth}
        \centering
        \includegraphics[width=\textwidth]{figs/Picture25.png}
    \end{subfigure}

    \caption{Effect the DMSO concentration (at 0.01, 0.05, 0.1 and 0.2 mole fraction, respectively) in the charge composition has on the azeotrope.}
    \label{fig:Effect the DMSO concentration in the charge composition has on the azeotrope}

\end{figure}

The VLE diagrams show that the addition of DMSO to a solvent-free concentration changes the phase-equilibrium behavior of the IPA-water system. Without an entrainer, the IPA-water mixture forms an azeotrope, which limits the maximum IPA purity attainable by ordinary distillation. When DMSO is added, the equilibrium curve is shifted away from the diagonal, meaning that the vapour and liquid compositions are no longer equal at the original azeotropic point. This confirms that DMSO successfully changes the relative volatility of IPA and water, allowing IPA to be concentrated beyond the azeotropic composition. The effect becomes more visible as the DMSO mole fraction increases, showing that the entrainer is essential for achieving the required high-purity IPA distillate.
