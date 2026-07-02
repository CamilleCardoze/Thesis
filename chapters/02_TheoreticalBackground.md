# Theoretical Background

## Batch Extractive Distillation

In batch extractive distillation, a mixture made up of a more volatile and a less volatile component is heated up to achieve the component separation, by causing the more volatile component to evaporate in a higher concentration and then condensate for its recovery. This process is done in batch, where only a portion of the mixture is treated in a single cycle; a fixed amount of it is to be separated at a time [@bme_distillation_notes_v_nd].

The distillate of the mixture is separated from the less volatile substances that are left in the residue or at the bottom of the tanks, by being brought back to its liquid phase by a condenser and then collected. However, part of this condensate will return to the column as reflux to improve the mass transfer between phases and therefore the efficiency of the column, at a ratio called reflux ratio (R). It is the quotient of the liquid used as reflux and the total liquid withdrawn (distillate). Under constant reflux ratio, the composition of the distillate will steadily change (the more volatile component’s mole fraction will decrease in the distillate) as the procedure progresses.

\begin{figure}[H]
\centering
\includegraphics[width=0.5\textwidth]{figs/batchex.png}
\caption{A diagram illustrating batch extractive distillation \cite{hilmen_skogestad_doherty_malone_1997}.}
\label{fig:A diagram illustrating batch extractive distillation}
\end{figure}

## Azeotropes

An azeotrope is a specific mixture composition where the liquid and vapour phases in vapour–liquid equilibrium have the same composition. In ordinary distillation, the vapour phase is usually richer in the more volatile component than the liquid phase, which allows separation to occur. At the azeotropic composition, however, the vapour produced during boiling has the same composition as the liquid, meaning that no further enrichment of one component is achieved by simple vaporization and condensation. As a result, conventional distillation cannot separate the mixture beyond the azeotropic composition without changing the operating conditions or introducing an additional separating agent.

Both phases meet on the main diagonal line of the equilibrium curve diagram; this would mean that x = y (Figure 2.2). This condition prevents any more separation from happening, since the equilibrium reached eliminates the gradient needed for further change in the concentrations [@bme_distillation_notes_v_nd]. In the case, the azeotrope presents at a mass fraction of 87-88% and a temperature of 80.2 – 80.4 °C. This is due to the interactions between the molecules (see Table 3.1) of each component in the solution.

\begin{figure}[H]
\centering
\includegraphics[width=0.8\textwidth]{figs/azeotropepic.png}
\caption{Visual representation of an azeotropic mixture \cite{bhattacharyya_2025}.}
\label{fig:Visual representation of an azeotropic mixture}
\end{figure}

\begin{figure}[H]
\centering
\includegraphics[width=0.8\textwidth]{figs/ipaaz.png}
\caption{Azeotrope present in the water/IPA mixture; obtained from ChemCAD.}
\label{fig:Water-IPA azeotrope}
\end{figure}

## Material Recovery in Extractive Distillation

Material recovery is an important part of extractive distillation, since the process requires the addition of a third component. The purpose of this component is to change the relative volatility of the original components and make the separation possible. However, because the solvent is not the desired final product, it should be recovered and reused whenever possible. This reduces the amount of fresh solvent required, lowers operating costs, and decreases waste formation. In extractive distillation, the solvent is usually chosen to have a much higher boiling point than the components being separated, so it is mostly recovered from the bottom product rather than from the distillate. [@seader_henley_roper_2011].

In batch extractive distillation, the recovery of materials is especially relevant because the composition of the liquid in the still pot changes continuously with time. As the operation progresses, different fractions may be obtained: some fractions may meet the desired purity specification, while others may contain valuable amounts of IPA, water, or DMSO but not be pure enough to be considered final products. These intermediate or run-off streams can often be recycled to a later batch or treated in a separate recovery step.

For this project, material recovery is studied through the recycling of run-off material and the recovery of DMSO from previous distillation residues. Since DMSO acts as the extractive solvent, its recovery is especially necessary for improving the economic and environmental performance of the process.

## Heat Exchangers

Heat exchangers are devices used to transfer heat between two fluids at different temperatures. In most industrial heat exchangers, the fluids do not mix directly, but are separated by a solid wall through which heat is transferred. The heat transfer process usually involves convection from the hot fluid to the wall, conduction through the wall, and convection from the wall to the cold fluid. Heat exchangers are widely used in chemical and mechanical engineering for heating, cooling, condensation, evaporation, and heat recovery [@kern_1950]. The most common configuration in the case of condensers and boilers is the shell and tube, single-pass heat exchanger; see Figure 2.4 for an illustration.

In distillation systems, the two most important heat exchangers are the condenser and the reboiler. The condenser removes heat from the vapor leaving the top of the column and converts it into liquid. Part of this liquid may be withdrawn as distillate, while the remaining part is returned to the column as reflux. The reboiler, on the other hand, supplies heat to the liquid at the bottom of the column, producing vapor that rises through the column and allows mass transfer between vapor and liquid phases.

The design of a heat exchanger depends mainly on the required heat duty, the temperature difference between the fluids, the heat transfer coefficient, and the available heat transfer area. A common design equation is:

$$
Q = k A F \Delta T_{lm}
$$

where Q is the heat duty, k is the overall heat transfer coefficient, A is the heat transfer area, $\Delta T_{lm}$ is the logarithmic mean temperature difference, and F is a correction factor. In this project, this theory is applied to the design of the distillation column's condenser and reboiler.

\begin{figure}[H]
\centering
\includegraphics[width=0.6\textwidth]{figs/simpleshell.png}
\caption{Diagram of a single-pass shell and tube heat exchanger \cite{zohuri_2017}.}
\label{fig:Diagram of a single-pass shell and tube heat exchanger}
\end{figure}

## Heat Recycling in the Industry

Heat recycling, also called heat recovery, is the reuse of heat that would otherwise be rejected from a process. In many industrial systems, some streams must be cooled while others must be heated. Instead of using only external utilities, such as cooling water and steam, heat can be transferred from hot process streams to cold process streams. This reduces the energy demand of the plant and improves overall process efficiency. [@kemp_2007].

In distillation, heat recycling is especially important because the process usually requires significant energy input in the reboiler and significant heat removal in the condenser. One simple form of heat recycling is feed preheating, where heat from a hot stream, such as overhead vapor or bottom product, is used to increase the temperature of the feed before it enters the column. This decreases the amount of heat that must later be supplied by the reboiler.

A more advanced method is vapor recompression. In this method, the vapor leaving the top of the column is compressed, which increases its temperature and pressure. The compressed vapor can then be used as a heating medium in the reboiler. The goal is for the net output thermal energy of the recycling system to be higher than the required input energy.
