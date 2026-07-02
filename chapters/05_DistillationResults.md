# Distillation Results

A maximum purity of 99.856 mol% IPA was achieved, meeting the requirements; 0.14 ≤ 0.25 mol% water, 0.0012 ≤ 0.15 mol% DMSO; these results calculated by ChemCAD are shown in Figure 5.1.
The total elapsed time was 9.05 hours.

\begin{figure}[H]
\centering
\includegraphics[width=0.3\textwidth]{figs/Picture20.png}
\caption{Calculated properties of the IPA product.}
\label{fig:Calculated properties of the IPA product}
\end{figure}

In Figure 5.2, it is possible to observe how the composition of the distillate changed with time, under the chosen parameter values. This plot was produced by the ChemCAD simulation.

\begin{figure}[H]
\centering
\includegraphics[width=0.8\textwidth]{figs/Picture21.png}
\caption{Depiction of the distillate composition’s change with time.}
\label{fig:Depiction of the distillate composition’s change with time}
\end{figure}

The distillate composition graph shows that the IPA mole fraction remains very high during most of the main distillation step, while the water and DMSO mole fractions remain low. This confirms that the selected operating parameters allow IPA to be removed as the main overhead product with only small amounts of impurities. Near the end of the step, the IPA mole fraction begins to decrease while the impurity content increases, indicating that the useful IPA-rich distillation period is ending. Therefore, the stopping point was selected before a significant decrease in distillate purity occurs, in order to maintain the required product specification.

## Additional Steps

After obtaining the desired product, the distillation column will still have liquid at the bottom, whose composition is still rich in all three components: water, DMSO and IPA.

In an attempt to recover as much water as possible, as well as solvent, three more steps to the process were added: a water-IPA run-off step, a water distillation step, and a water-DMSO run-off step. The new simulation layout, after adding the necessary equipment for these additional steps, is illustrated in Figure 5.3.

\begin{figure}[H]
\centering
\includegraphics[width=0.9\textwidth]{figs/newsim.png}
\caption{New ChemCAD simulation layout.}
\label{fig:New ChemCAD simulation layout}
\end{figure}

In the water-IPA run-off step, the goal is to dispose of all leftover IPA in the bottom, in order to produce water more efficiently in the next step. In the water distillation step, as much water as possible will be separated from the leftover mixture (less than 0.05 mol% IPA should be present, and less than 0.035 mol% DMSO). Finally, for the water-DMSO run-off step, it is attempted to leave as little water in the bottom as possible in order to recover the solvent.

In this case, extensive sensitivity analyses were not carried out, since the investigated parameters were now set to the chosen values for the whole process. Instead, the stop values for each step were set as the following:

- stop value for step 2: 0.8000 mole fraction water in the accumulator
- stop value for step 3: 0.9995 mole fraction water in the accumulator
- stop value for step 4: 0.9995 mole fraction DMSO in the still pot

The stop values were chosen according to the purpose of each additional distillation step. In step 2, the objective is not to obtain a final pure product, but to remove the remaining IPA-rich fraction before the main water recovery step. Therefore, the step is stopped when the accumulator reaches a high water content, indicating that most of the remaining IPA has already been removed from the bottom mixture. In step 3, the goal is to recover water as a final product, so a much stricter stop value is used: the accumulator must reach approximately pure water. In step 4, the objective is to recover the DMSO remaining in the still pot, so the process is continued until the bottom product reaches the required DMSO purity.

The reflux ratios for each step were chosen in a small iteration process, using values ranging from R = 2 to 5 [@bme_distillation_notes_v_nd]. After four simulations (corresponding to the four integer values selected) were carried out for each step, the following values yielded the best results in the least possible amount of time:

- R for step 2: 5
- R for step 3: 4
- R for step 4: 2

A higher reflux ratio was used in step 2 because this step handles a transition mixture containing IPA and water, and stronger internal liquid-vapour contact is needed to remove the remaining IPA effectively. Step 3 uses a moderate reflux ratio because water is the main volatile component and can be recovered at high purity without excessive reflux. Step 4 uses the lowest reflux ratio because the target product is the DMSO-rich bottom stream rather than the distillate; therefore, very high reflux is not necessary and would only increase the operating time.

This will allow us to carry out the simulation until the desired purity for both water and DMSO are reached.

The resulting graphs of the additional distillation steps are showcased in Figures 5.4, 5.5 and 5.6.

\begin{figure}[H]
\centering
\includegraphics[width=0.8\textwidth]{figs/distgraph2.png}
\caption{Distillate composition as a function of time for step 2.}
\label{fig:Distillate composition as a function of time for step 2}
\end{figure}

\begin{figure}[H]
\centering
\includegraphics[width=0.8\textwidth]{figs/distgraph3.png}
\caption{Distillate composition as a function of time for step 3.}
\label{fig:Distillate composition as a function of time for step 3}
\end{figure}

\begin{figure}[H]
\centering
\includegraphics[width=0.8\textwidth]{figs/distgraph4.png}
\caption{Distillate composition as a function of time for step 4.}
\label{fig:Distillate composition as a function of time for step 4}
\end{figure}

After the process was finished, the results were:

- Water distillate:
  - 226.52 kg, 0.9994 mol fraction water, 0.0004432 mol fraction IPA, 0.0001375 mol fraction DMSO
- DMSO bottom:
  - 4060.02 kg, 0.9995 mol fraction DMSO, 0.0004904 mol fraction water, 7.226e-18 mol fraction IPA

The results are satisfying and the liquids are usable for other applications. The total elapsed time was 16.15 hours, still under the 22 hour goal. Run-off steps will later be re-integrated into the system, further explained in Chapter 8, in order to recover as much material as possible. These results support the inclusion of material recovery steps in the overall process design, as they reduce waste formation and improve the reuse potential of both water and DMSO.
