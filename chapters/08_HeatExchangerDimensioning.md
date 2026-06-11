# Heat Exchangers

## Column Condenser Design

The condenser was designed as a one-pass shell-and-tube heat exchanger used to condense the IPA-rich vapour leaving the top of the distillation column.

[add paragraph explaining why one pass heat exchanger is good]

The total heat-transfer area listed in the calculation corresponds to the total available outside tube surface area. The IPA properties used for the condensation-side calculation were obtained from ChemCAD's reports, while the cooling-water properties were taken at the average cooling-water temperature in a different ChemCAD simulation arrangement.

[add graph or reports from chemcad]

[add simulation arrangement picture]

The main design equation used for the condenser was:

$Q = K F A \Delta T_m$

Rearranging for the required heat-transfer area:

$A = \frac{Q}{F}{K \Delta T_m}$

where $Q$ is the condenser heat duty, $K$ is the overall heat-transfer coefficient, $A$ is the total heat-transfer area, $F$ is the correction factor and $\Delta T_m$ is the mean temperature difference. Since the temperature difference between the condensing vapour and cooling water changes along the exchanger, the logarithmic mean temperature difference was used:

$\Delta T_{log} = \frac{\Delta T_1 - \Delta T_2}{\ln \left(\frac{\Delta T_1}{\Delta T_2}\right)}$

The IPA vapour was assumed to condense at constant temperature since we are dealing with a phase change, while the cooling water was heated from 25°C (room temperature) to 50°C. Therefore:

$\Delta T_1 = T_{IPA} - T_{w,in}$

$\Delta T_1 = 353.15 - 298.15 = 55 \text{ K}$

$\Delta T_2 = T_{IPA} - T_{w,out}$

$\Delta T_2 = 353.15 - 323.15 = 30 \text{ K}$

Thus:

$\Delta T_{log} = \frac{55 - 30}{\ln \left(\frac{55}{30}\right)}$

$\Delta T_{log} = 41.24 \text{ K}$

The correction factor was calculated as:

$F_T = 1$

[add graph from book]

Therefore:

$\Delta T_m = F_T \Delta T_{log}$

$\Delta T_m = 41.24 \text{ K}$

The highest condenser heat duty obtained from the simulation was:

$Q = 957.7 \text{ MJ/h}$

[add picture of graph from chemcad]

Converting to watts:

$Q = \frac{957.7 \times 10^6}{3600}$

$Q = 266027.78 \text{ W}$

Using the initially assumed overall heat-transfer coefficient for phase change [cite]:

$K = 850 \text{ W/m}^2\text{K}$

the first estimated heat-transfer area was:

$A = \frac{266027.78}{850 \times 41.24}$

$A = 7.59 \text{ m}^2$

This value was used only as an initial estimate. A corrected design was then obtained by calculating the individual heat-transfer coefficients, the wall resistance, and the fouling resistance.

The clean overall heat-transfer coefficient was calculated from the thermal resistance relationship [cite lecture]:

$\frac{1}{K_{clean}} = \frac{1}{\alpha_{w,out}} + \frac{x_{tube}}{\lambda_{wall}} + \frac{1}{\alpha_{cond}}$

where $\alpha_{w,out}$ is the cooling-water heat-transfer coefficient converted to the outside tube area, $x_{tube}$ is the tube wall thickness, $\lambda_{wall}$ is the thermal conductivity of the carbon-steel wall, and $\alpha_{cond}$ is the condensation-side heat-transfer coefficient. The wall thermal conductivity was taken as [cite]:

$\lambda_{wall} = 45 \text{ W/mK}$

The water-side Reynolds number was calculated using [cite lecture]:

$Re = \frac{\rho v D_i}{\mu}$

The Prandtl number was calculated using [cite lecture]:

$Pr = \frac{\mu c_p}{\lambda}$

The Nusselt number used in the worksheet was [cite lecture]:

$Nu = 0.3 Re^{0.5} Pr^{1/3}$

The water-side heat-transfer coefficient was then calculated from [cite lecture]:

$\alpha_{w,in} = \frac{Nu \lambda_w}{D_i}$

Since the total heat-transfer area was based on the outside tube surface, the water-side coefficient was converted to the outside area basis:

$\alpha_{w,out} = \alpha_{w,in} \frac{D_i}{D_o}$

The calculated condenser coefficients were:

Table: Condenser heat transfer coefficients.
\label{tab:Condenser heat transfer coefficients.}

| Parameter                             |           Symbol |   Value |  Unit |
| ------------------------------------- | ---------------: | ------: | ----: |
| Condensation-side coefficient         |  $\alpha_{cond}$ | 1995.01 | W/m²K |
| Water-side coefficient, inside basis  |  $\alpha_{w,in}$ | 1514.09 | W/m²K |
| Water-side coefficient, outside basis | $\alpha_{w,out}$ | 1211.27 | W/m²K |
| Clean overall coefficient             |      $K_{clean}$ |  729.25 | W/m²K |
| Fouling resistance                    |            $R_f$ |  0.0005 | m²K/W |
| Dirty overall coefficient             |      $K_{dirty}$ |  534.40 | W/m²K |

Fouling resistance was obtained from literature [cite book].

The dirty overall heat-transfer coefficient was calculated by adding the fouling resistance:

$\frac{1}{K_{dirty}} = \frac{1}{K_{clean}} + R_f$

$K_{dirty} = 534.40 \text{ W/m}^2\text{K}$

Using the dirty overall heat-transfer coefficient, the final required heat-transfer area was:

$A_{calc} = \frac{Q}{K_{dirty} \Delta T_{log}}$

$A_{calc} = \frac{266027.78}{534.40 \times 41.24}$

$A_{calc} = 12.07 \text{ m}^2$

Therefore, the required total condenser heat-transfer area is:

$A_{cond} = 12.07 \text{ m}^2$

The selected condenser geometry was:

Table: Selected and calculated condenser geometry.
\label{tab:Selected and calculated condenser geometry}

| Parameter             |         Symbol |   Value | Unit |
| --------------------- | -------------: | ------: | ---: |
| Number of tubes       |            $N$ |      48 |    - |
| Tube outside diameter |          $D_o$ |   0.020 |    m |
| Tube inside diameter  |          $D_i$ |   0.016 |    m |
| Tube wall thickness   |     $x_{tube}$ |   0.002 |    m |
| Tube pitch            |          $p_t$ |   0.025 |    m |
| Tube length           |            $L$ |   4.002 |    m |
| Bundle diameter       |   $D_{bundle}$ |   0.232 |    m |
| Shell clearance       |              - |   0.011 |    m |
| Shell inside diameter | $D_{shell,in}$ |   0.243 |    m |
| Shell wall thickness  |    $x_{shell}$ | 0.00423 |    m |
| Shell length          |    $L_{shell}$ |   4.028 |    m |
| Baffle spacing        |              - |  0.0486 |    m |

The tube outside diameter, tube thickness, tube pitch and shell clearance values were amongst those recommended by literature [cite book]. Similarly, the formulas for the bundle diameter, shell thickness, shell diameter and and shell length were given:

[give four formulas]

The number of tubes was arbitrarily selected to comply with length recommendations and the chosen arrangement. Inversely, tube length was calculated with the following formula [cite lecture]:

$$L = \frac{A}{N \pi D_o}$$

The tube arrangement [add explanation indicating why 2x2 is suitable].

[add picture of chosen arrangement]

The available outside tube surface area was checked using:

$A = N \pi D_o L$

$A = 48 \pi (0.020)(4.002)$

$A = 12.07 \text{ m}^2$

Therefore, the selected condenser geometry provides the required total heat-transfer area.

The cooling-water mass flow rate was calculated from the sensible heat balance [cite lecture]:

$Q = \dot{m}_w c_{p,w} \Delta T_w$

$\dot{m}_w = \frac{Q}{c_{p,w} \Delta T_w}$

The calculated cooling-water mass flow rate was:

$\dot{m}_w = 2.55 \text{ kg/s}$

The main hydraulic results for the cooling water were:

Table: Cooling water properties.
\label{tab:Cooling water properties}

| Parameter            |      Symbol |   Value | Unit |
| -------------------- | ----------: | ------: | ---: |
| Water mass flow rate | $\dot{m}_w$ |    2.55 | kg/s |
| Tube-side flow area  |  $A_{tube}$ | 0.00965 |   m² |
| Water velocity       |       $v_w$ |   0.266 |  m/s |
| Reynolds number      |      $Re_w$ | 5876.23 |    - |
| Prandtl number       |      $Pr_w$ |    4.81 |    - |
| Nusselt number       |      $Nu_w$ |   38.82 |    - |

The calculated wall and film temperatures were:

Table: Condenser wall and film temperatures.
\label{tab:Condenser wall and film temperatures}

| Parameter                   |                     Symbol | Value | Unit |
| --------------------------- | -------------------------: | ----: | ---: |
| Real wall temperature       | $\overline{T}_{wall,real}$ | 68.62 |   °C |
| Calculated wall temperature | $\overline{T}_{wall,calc}$ | 70.00 |   °C |
| Film temperature            |      $\overline{T}_{film}$ | 75.00 |   °C |

From the formulas [cite lectures]:

[add 2 formulas]

The value of the film temperature was chosen by iteration, performed until the calculated wall temperature was close to the real wall temperature. A normal temperature difference interval between the film and wall temperatures is of around 5 to 10 degrees.

The small difference between the real and calculated wall temperatures shows that the assumed film temperature is acceptable for the preliminary condenser design. All other calculated parameters are realistic for the scale of our process and adequate for manufacturing [cite].

## Column Reboiler Design

The reboiler was designed as a kettle reboiler. Although it is not a traditional shell-and-tube heat exchanger in the same way as the condenser, it still uses a tube bundle to transfer heat from condensing steam to the process liquid. The reboiler was designed as a two-pass heat exchanger arrangement, with the listed heat-transfer area representing the total heat-transfer area.

[add paragraph explaining why kettle reboiler is good] [cite]

The DMSO-rich liquid properties were obtained from ChemCAD using the relevant column-bottom composition, while the steam-side properties were obtained from a saturated steam table by interpolation [cite steam table].

In this case, it was not necessary to calculate the logarithmic temperature difference, since we chose the steam temperature. Furthermore, the heat duty is known.

[add picture of chemcad graph for reboiler]

[add picture of steam stable]

[add interpolation formula]

The design equation used for the reboiler was:

$Q = K A \Delta T$ F

Rearranging for heat-transfer area:

$A = \frac{Q}{K \Delta T}$

The DMSO-rich liquid temperature was taken as:

$T_{DMSO} = 190^\circ C$

The heating steam temperature was taken as:

$T_{steam} = 220^\circ C$

For an adequate temperature difference of:

$\Delta T = T_{steam} - T_{DMSO}$

$\Delta T = 220 - 190$

$\Delta T = 30 \text{ K}$

This will allow for proper heat transfer without overheating the DMSO, which properties we will take as reference since it possesses the highest heat transfer resistance ([add heat transfer coefficients of water, IPA and DMSO]) [add citation]. For stages where DMSO does not make up most of the bottom liquid, the pressure of steam (and therefore the temperature) is to be decreased with a control system. At higher temperatures, a peak and then a rapid decrease in the value of the heat transfer coefficient can be observed [cite hegelys book from picture].

[add picture of graph from book]

The reboiler heat duty was:

$Q = 1000 \text{ MJ/h}$

Converting to watts:

$Q = \frac{1000 \times 10^6}{3600}$

$Q = 277777.78 \text{ W}$

Using the initially assumed overall heat-transfer coefficient for phase change [cite book]:

$K = 850 \text{ W/m}^2\text{K}$

the preliminary heat-transfer area was:

$A = \frac{277777.78}{850 \times 30}$

$A = 10.89 \text{ m}^2$

This initial estimate was corrected by calculating the individual boiling-side and steam-condensation-side heat-transfer coefficients.

The boiling-side heat-transfer coefficient for the process was calculated using the pool-boiling correlation [cite book]:

[add formula]

$\alpha_{shell} = 2261.06 \text{ W/m}^2\text{K}$

The steam-side condensation coefficient was calculated using the filmwise-condensation method. The inside coefficient was first calculated and then converted to the outside tube surface basis [cite book]:

$\alpha_{st,out} = \alpha_{st,in} \frac{D_i}{D_o}$

The calculated reboiler heat-transfer coefficients were:

Table: Reboiler heat transfer coefficients.
\label{tab:Reboiler heat transfer coefficients}

| Parameter                                     |            Symbol |    Value |  Unit |
| --------------------------------------------- | ----------------: | -------: | ----: |
| Boiling-side coefficient                      |  $\alpha_{shell}$ |  2261.06 | W/m²K |
| Steam condensation coefficient, inside basis  |  $\alpha_{st,in}$ | 12152.33 | W/m²K |
| Steam condensation coefficient, outside basis | $\alpha_{st,out}$ | 10194.74 | W/m²K |
| Clean overall coefficient                     |       $K_{clean}$ |  1708.92 | W/m²K |
| Fouling resistance                            |             $R_f$ |  0.00026 | m²K/W |
| Dirty overall coefficient                     |       $K_{dirty}$ |  1183.20 | W/m²K |

The clean overall heat-transfer coefficient was calculated as:

$\frac{1}{K_{clean}} = \frac{1}{\alpha_{st,out}} + \frac{x_{tube}}{\lambda_{wall}} + \frac{1}{\alpha_{shell}}$

The dirty overall heat-transfer coefficient was calculated by including the fouling resistance [cite book]:

$\frac{1}{K_{dirty}} = \frac{1}{K_{clean}} + R_f$

$K_{dirty} = 1183.20 \text{ W/m}^2\text{K}$

The correction factor was calculated for a two-pass heat exchanger:

[add correction factor formula]

[add picture of graph from book]

Using the dirty overall coefficient, the corrected reboiler heat-transfer area was:

$A_{calc} = \frac{Q}{F}{K_{dirty} \Delta T}$

$A_{calc} = \frac{277777.78}{1}{1183.20 \times 30}$

$A_{calc} = 7.83 \text{ m}^2$

Therefore, the required total reboiler heat-transfer area is:

$A_{reb} = 7.83 \text{ m}^2$

The selected reboiler geometry was:

Table: Selected and calculated reboiler geometry.
\label{tab:Selected and calculated reboiler geometry}

| Parameter             |         Symbol |   Value | Unit |
| --------------------- | -------------: | ------: | ---: |
| Number of tubes       |            $N$ |      28 |    - |
| Tube outside diameter |          $D_o$ |  0.0250 |    m |
| Tube inside diameter  |          $D_i$ |  0.0210 |    m |
| Tube wall thickness   |     $x_{tube}$ | 0.00202 |    m |
| Tube pitch            |          $p_t$ |  0.0313 |    m |
| Tube length           |            $L$ |   1.777 |    m |
| Bundle diameter       |   $D_{bundle}$ |   0.227 |    m |
| Shell clearance       |              - |   0.011 |    m |
| Shell inside diameter | $D_{shell,in}$ |   0.477 |    m |
| Shell wall thickness  |    $x_{shell}$ | 0.00493 |    m |

The tube length was calculated from the total required heat-transfer area:

$L = \frac{A}{2N \pi D_o}$

The factor of 2 is included because the reboiler was designed with a two-pass tube arrangement [cite lecture].

Substituting the values:

$L = \frac{7.83}{2(28)\pi(0.0250)}$

$L = 1.78 \text{ m}$

Therefore, the selected tube length is 1.78 m.

The steam mass flow rate was calculated from the latent heat balance:

$Q = \dot{m}_{st} r_{st}$

$\dot{m}_{st} = \frac{Q}{r_{st}}$

The latent heat of the heating steam was obtained from the steam table by interpolation:

$r_{st} = 1887700 \text{ J/kg}$

Therefore:

$\dot{m}_{st} = \frac{277777.78}{1887700}$

$\dot{m}_{st} = 0.147 \text{ kg/s}$

The main steam-side hydraulic values were:

Table: Steam parameters.
\label{tab:Steam parameters}

| Parameter            |         Symbol |   Value | Unit |
| -------------------- | -------------: | ------: | ---: |
| Steam mass flow rate | $\dot{m}_{st}$ |   0.147 | kg/s |
| Tube-side flow area  |     $A_{tube}$ | 0.00485 |   m² |
| Steam velocity       |       $v_{st}$ |    2.95 |  m/s |

The calculated wall and film temperatures were obtained from the formula [cite lecture]:

[add formula]

The results could be summarized below:

Table: Reboiler wall and film temperatures.
\label{tab:Reboiler wall and film temperatures}

| Parameter                   |                     Symbol |  Value | Unit |
| --------------------------- | -------------------------: | -----: | ---: |
| Real wall temperature       | $\overline{T}_{wall,real}$ | 204.30 |   °C |
| Calculated wall temperature | $\overline{T}_{wall,calc}$ | 205.00 |   °C |
| Film temperature            |      $\overline{T}_{film}$ | 212.50 |   °C |

The small difference between the real and calculated wall temperatures confirms that the assumed film temperature is acceptable for the preliminary kettle reboiler calculation.

All calculated parameters are realistic for the scale of our process and adequate for the manufacturing of parts for this reboiler [cite].

## Selection of Heat Exchanger Construction Types

The condenser was selected as a conventional one-pass shell-and-tube heat exchanger. Since the exchanger is relatively small and the temperature difference is moderate, a fixed-tube-sheet construction is suitable. For the front-end stationary head, a removable channel and cover is selected so that the tube side can be accessed for inspection and cleaning. The selected front-end type is therefore TEMA type A [cite book]. The shell is selected as a one-pass shell, corresponding to TEMA shell type E. The rear-end head is selected as a fixed-tube-sheet rear channel with removable cover, corresponding to TEMA rear-end type L. Therefore, the selected condenser construction is:

$AEL$

where:

- $A$ = front-end stationary head with removable channel and cover
- $E$ = one-pass shell
- $L$ = fixed-tube-sheet rear end with removable cover

[add picture of table]

This construction is appropriate for a normal one-pass condenser because it is mechanically simple, allows tube-side access, and provides the required heat-transfer area.

The reboiler was selected as a kettle-type reboiler rather than a conventional shell-and-tube heat exchanger. For this reason, the shell type must correspond to a kettle arrangement. The selected shell type is therefore TEMA type K. Since the reboiler uses a two-pass tube arrangement and must allow thermal expansion of the tube bundle, a U-tube rear-end construction is suitable. The selected rear-end type is TEMA type U. For the front-end stationary head, a bonnet-type head is selected because the tube-side fluid is condensing steam, which is relatively clean compared with process liquids. The selected front-end type is therefore TEMA type B. Therefore, the selected reboiler construction is:

$BKU$

where:

- $B$ = bonnet-type front-end stationary head
- $K$ = kettle-type shell
- $U$ = U-tube rear-end construction

This construction is appropriate for the kettle reboiler because the kettle shell provides space for boiling and vapour-liquid disengagement, while the U-tube arrangement allows thermal expansion and provides the required two-pass tube-side flow path.

[add picture of kettle reboiler]
