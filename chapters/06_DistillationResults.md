# Distillation Results

## Purity, Mass and Elapsed Time

We achieved a maximum purity of 99.856 mol% IPA, meeting our requirements; 0.14 ≤ 0.25 mol% water, 0.0012 ≤0.15 mol% DMSO.
The total elapsed time was 9.05 hours.

\begin{figure}[H]
\centering
\includegraphics[width=0.4\textwidth]{figs/Picture20.png}
\caption{Stream results.}
\label{fig:Stream results}
\end{figure}

## Distillate Graph

From the graphs produced by the ChemCAD simulation, it is possible to observe how the composition of the distillate changed with time, under our chosen parameter values:

\begin{figure}[H]
\centering
\includegraphics[width=\textwidth]{figs/Picture21.png}
\caption{Depiction of the distillate composition’s change with time.}
\label{fig:Depiction of the distillate composition’s change with time}
\end{figure}

The distillate composition graph shows that the IPA mole fraction remains very high during most of the main distillation step, while the water and DMSO mole fractions remain low. This confirms that the selected operating parameters allow IPA to be removed as the main overhead product with only small amounts of impurities. Near the end of the step, the IPA mole fraction begins to decrease while the impurity content increases, indicating that the useful IPA-rich distillation period is ending. Therefore, the stopping point was selected before a significant decrease in distillate purity occurs, in order to maintain the required product specification.

## Effect on the Azeotrope

The altered activity coefficients increase IPA’s relative volatility compared to water. This shifts the VLE curve, eliminating the original azeotropic point where x = y. DMSO’s high boiling point (189°C) ensures it mostly remains in the liquid phase, accumulating in the column’s stripping section. This prevents IPA-water azeotrope reformation and allows IPA to distill overhead. As we can see in graphs 14-17, The IPA-water-DMSO system no longer exhibits an azeotrope, enabling distillation to achieve >99.75% IPA purity.

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

The VLE diagrams show that the addition of DMSO changes the phase-equilibrium behavior of the IPA-water system. Without entrainer, the IPA-water mixture forms an azeotrope, which limits the maximum IPA purity attainable by ordinary distillation. When DMSO is added, the equilibrium curve is shifted away from the diagonal, meaning that the vapour and liquid compositions are no longer equal at the original azeotropic point. This confirms that DMSO successfully changes the relative volatility of IPA and water, allowing IPA to be concentrated beyond the azeotropic composition. The effect becomes more visible as the DMSO mole fraction increases, showing that the entrainer is essential for achieving the required high-purity IPA distillate.

## Additional Stages

After obtaining our desired product, the distillation column will still have liquid at the bottom, which composition is still rich in all three components: water, DMSO and IPA.

In an attempt to recover as much water as possible, as well as solvent, three more stages to the process were added: a water-IPA run-off stage, a water distillation stage, and a water-DMSO run-off stage.

In the water-IPA run-off stage, we will attempt to dispose of all leftover IPA in the bottom, in order to extract water more efficiently in the next phase. In the water distillation stage, we will separate as much water from the leftover mixture as possible, with the same purity parameters as IPA.Finally, for the water-DMSO run-off stage, we want to leave as little water in the bottom as possible in order to recover the solvent, again, following the same purity requirements as IPA.

In this case, extensive sensitivity analyses were not carried out, since our investigated parameters were now set to the chosen values for the whole process. Instead, the stop values for each stage were set as the following:

- stop value for step 2: 0.8 mole fraction water in the accumulator
- stop value for step 3: 0.9995 mole fraction water in the accumulator
- stop value for step 4: 0.9995 mole fraction DMSO in the bottom tank

The stop values were chosen according to the purpose of each additional distillation step. In step 2, the objective is not to obtain a final pure product, but to remove the remaining IPA-rich fraction before the main water recovery step. Therefore, the step is stopped when the accumulator reaches a high water content, indicating that most of the remaining IPA has already been removed from the bottom mixture. In step 3, the goal is to recover water as a final product, so a much stricter stop value is used: the accumulator must reach approximately pure water. In step 4, the objective is to recover the DMSO remaining in the bottom tank, so the process is continued until the bottom product reaches the required DMSO purity.

And our chosen reflux ratio for each step were chosen in a small iteration process, using values ranging from 2 to 5 R [cite source]. After 4 iterations were carried out for each step, the following values yielded the best results in the least possible amount of time:

- R for step 2: 5
- R for step 3: 4
- R for step 4: 2

A higher reflux ratio was used in step 2 because this step handles a transition mixture containing IPA and water, and stronger internal liquid-vapour contact is needed to remove the remaining IPA effectively. Step 3 uses a moderate reflux ratio because water is the main volatile component and can be recovered at high purity without excessive reflux. Step 4 uses the lowest reflux ratio because the target product is the DMSO-rich bottom stream rather than the distillate; therefore, very high reflux is not necessary and would only increase the operating time.

This will allow us to carry out our simulation until our desired purities for both water and DMSO are reached.

The resulting graphs of the additional distillation stages are showcased below:

\begin{figure}[H]
\centering
\includegraphics[width=0.8\textwidth]{figs/distgraph2.png}
\caption{Distillate composition in terms of time for step 2.}
\label{fig:Distillate composition in terms of time for step 2}
\end{figure}

\begin{figure}[H]
\centering
\includegraphics[width=0.8\textwidth]{figs/distgraph3.png}
\caption{Distillate composition in terms of time for step 3.}
\label{fig:Distillate composition in terms of time for step 3}
\end{figure}

\begin{figure}[H]
\centering
\includegraphics[width=0.8\textwidth]{figs/distgraph4.png}
\caption{Distillate composition in terms of time for step 4.}
\label{fig:Distillate composition in terms of time for step 4}
\end{figure}

After the process was finished, our results were:

- 226.52 kg of water, 0.9994 mol fraction water
- 4060.02 kg of DMSO, 0.9995 mol fraction DMSO

The results are satisfying and the liquids are usable for other applications. The total elapsed time was 16.15 hours, still under our 22 hour goal. Run-off stages will later be re-integrated into the system, further explained in Chapter 8, in order to recover as much material as possible. These results support the inclusion of material recovery steps in the overall process design, as they reduce waste formation and improve the reuse potential of both water and DMSO.
