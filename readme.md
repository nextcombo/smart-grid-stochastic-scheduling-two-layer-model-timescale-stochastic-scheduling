# [Smart Grid Stochastic Scheduling]Two-layer Model Timescale Stochastic Scheduling in Smart Grid (Matlab Code Implementation)

1. Overview
As the amount of renewable energy generation increases, the energy management of the distribution network has become a computationally challenging task. Solar power from photovoltaic (PV) devices can undergo significant changes in just one minute. Power inverters within PV systems can be commanded to reduce active power generation or adjust their power factor in seconds [1][2]. At slower timescales, distribution network operators exchange energy with the main grid every hour or every 10 minutes, and may suffer cost losses when deviating from the energy market schedule [3]. Additionally, voltage regulators and small diesel generators installed in microgrids respond at the same slower timescale. Therefore, optimizing the integrated design of such diverse tasks requires multi-level smart grid scheduling solutions.
Driven by demand response plans and the completion of various grid tasks using PV inverters, single-level scheduling schemes for distribution networks have been an active area of research. Power inverters can be controlled using local voltage regulation rules, see [5]–[8]. Assuming there is bidirectional communication between buses and utility operators, scheduling the distribution system can form an optimal power flow (OPF) problem. Centralized solutions use nonlinear program solvers [9]; or rely on balanced [10], [11] or unbalanced grid [12] AC models with complete convex relaxation. Distributed solvers with reduced computational complexity have been designed in [13]–[15].
However, the efficient and safe operation of the distribution network involves decisions at different time scales. [10] proposes a two-stage scheduling dynamic programming approach: the tap settings for the stabilizer are set on a slower time scale, maintaining a fixed configuration over short consecutive periods, with flexible loads being scheduled; however, the flexibility of the load is considered to be prioritized. Alternatively, centralized computational OPF decisions can be communicated to buses at the slower time scale, while photovoltaic power electronic devices can optimally track changes in renewable energy generation and demand at the faster time scale [16], [17]. Relying on an approximated grid model, which ignores the impact of uncertainty on slow-response unit scheduling, the latter approach generates partially decentralized real-time allocation of power flow between fast-response units.
Multi-level scheduling under uncertainty is commonly used in transmission systems and microgrids [18]. Robust methods find the best slow time scale decision for worst-case rapid time scale results; see [19] and its references. To avoid the conservativeness of robust schemes, probabilistic methods assume the probability density functions (pdfs) for demand, wind power generation, and system outages to find a one-day ahead grid schedule [20], [21]. The risk-limited scheduling framework adjusts multi-stage decisions as variance of involved random variables decreases towards actual time [3]. Only for convenient network constraints and risk-limited scheduling with congestion assumptions, pdfs, can effective decisions be computed [22]. As a third option, the sample average approximation (SAA) method uses samples extracted from assumed pdfs to produce the best slow time scale decisions; see [19], [23]. Recent work imposes limits on the probability of adverse events either relying on convex approximations based on opportunity constraints [24] or reducing computation by (sample-based) scenario approximation methods [25]; for example, [26].
Photovoltaic inverters, focusing on the distribution network, can occasionally overload on time and line to adapt to solar fluctuations and prevent overvoltages [27]. Consequently, temporal and spatial overloading of power system components (such as inverters, bus voltage, line current) may constitute an additional means for integrating renewable energy into smart grids. Nonetheless, ensuring that overloading occurs in a controlled manner couples decision-making with time is crucial. A single-level scheme can find the optimal PV setpoint while limiting the average time overload. The latter approach is also employed in this context, used to pre-set the transmission system dispatch one day/real-time market prior to load reduction.
Firstly, Section III describes the two-stage grid dispatch as a convex-concave problem: minimizing expected costs within slow control cycles while always satisfying relaxed voltage limits and on average or probabilistically. Secondly, in Section IV, the proven convergence algorithm for the average constraint formula is provided by the stochastic saddle point approximation scheme described in [30]. Unlike the SAA method, this stochastic approximation (SA) approach processes one random sample at a time to enhance computational efficiency. Thirdly, in Section V, we propose an algorithm to solve each of the two similar convex problems in the second stage under non-convex probability constraints. Although the expected cost enjoys zero dual gap [31], the overall two-stage dispatch is not convex-concave, which explains why the performance of the algorithms is verified numerically. Both approaches only require samples of load and solar power generation and can rely on either approximate or convex grid models. Numerical tests using the linearized distribution flow model on nodes 56 and 123 confirm the effectiveness found in Section 1.
Editor
Detailed mathematical models are available in the third part.
3. Matlab code and article detailed reading. This article only displays a part of the code, all and article code can be found in:
Editor
4. Running Results Editing
Editor
Editor
Editor
Editor
Editor
Editor
Editor
Editor
Editor
Editor
Editor
Editor
Editor
Editor
Editor
​  

## Images

![(Smart Grid Stochastic Scheduling)Two-layer Model Timescale Stochastic Scheduling in Smart Grid (Matlab Code Implementation)](01.png)
![(Smart Grid Stochastic Scheduling)Two-layer Model Timescale Stochastic Scheduling in Smart Grid (Matlab Code Implementation)](02.png)
![(Smart Grid Stochastic Scheduling)Two-layer Model Timescale Stochastic Scheduling in Smart Grid (Matlab Code Implementation)](03.png)
![(Smart Grid Stochastic Scheduling)Two-layer Model Timescale Stochastic Scheduling in Smart Grid (Matlab Code Implementation)](04.png)
![(Smart Grid Stochastic Scheduling)Two-layer Model Timescale Stochastic Scheduling in Smart Grid (Matlab Code Implementation)](05.png)
![(Smart Grid Stochastic Scheduling)Two-layer Model Timescale Stochastic Scheduling in Smart Grid (Matlab Code Implementation)](06.png)
![(Smart Grid Stochastic Scheduling)Two-layer Model Timescale Stochastic Scheduling in Smart Grid (Matlab Code Implementation)](07.png)
![(Smart Grid Stochastic Scheduling)Two-layer Model Timescale Stochastic Scheduling in Smart Grid (Matlab Code Implementation)](08.png)
![(Smart Grid Stochastic Scheduling)Two-layer Model Timescale Stochastic Scheduling in Smart Grid (Matlab Code Implementation)](09.png)
![(Smart Grid Stochastic Scheduling)Two-layer Model Timescale Stochastic Scheduling in Smart Grid (Matlab Code Implementation)](10.png)
![(Smart Grid Stochastic Scheduling)Two-layer Model Timescale Stochastic Scheduling in Smart Grid (Matlab Code Implementation)](11.png)
![(Smart Grid Stochastic Scheduling)Two-layer Model Timescale Stochastic Scheduling in Smart Grid (Matlab Code Implementation)](12.png)
![(Smart Grid Stochastic Scheduling)Two-layer Model Timescale Stochastic Scheduling in Smart Grid (Matlab Code Implementation)](13.png)
![(Smart Grid Stochastic Scheduling)Two-layer Model Timescale Stochastic Scheduling in Smart Grid (Matlab Code Implementation)](14.png)
![(Smart Grid Stochastic Scheduling)Two-layer Model Timescale Stochastic Scheduling in Smart Grid (Matlab Code Implementation)](15.png)
![(Smart Grid Stochastic Scheduling)Two-layer Model Timescale Stochastic Scheduling in Smart Grid (Matlab Code Implementation)](16.png)
![(Smart Grid Stochastic Scheduling)Two-layer Model Timescale Stochastic Scheduling in Smart Grid (Matlab Code Implementation)](17.png)
![(Smart Grid Stochastic Scheduling)Two-layer Model Timescale Stochastic Scheduling in Smart Grid (Matlab Code Implementation)](18.png)
![(Smart Grid Stochastic Scheduling)Two-layer Model Timescale Stochastic Scheduling in Smart Grid (Matlab Code Implementation)](19.png)
![(Smart Grid Stochastic Scheduling)Two-layer Model Timescale Stochastic Scheduling in Smart Grid (Matlab Code Implementation)](20.png)
![(Smart Grid Stochastic Scheduling)Two-layer Model Timescale Stochastic Scheduling in Smart Grid (Matlab Code Implementation)](21.png)
![(Smart Grid Stochastic Scheduling)Two-layer Model Timescale Stochastic Scheduling in Smart Grid (Matlab Code Implementation)](22.png)
![(Smart Grid Stochastic Scheduling)Two-layer Model Timescale Stochastic Scheduling in Smart Grid (Matlab Code Implementation)](23.png)

<!-- PAYMENT_BLOCK -->

## Get this dataset

- Payment link (Stripe): [Buy now](https://buy.stripe.com/3cs8yP7sY87d0vu9AB)
- Payment QR code: ![Payment QR code](pay.png)

<!-- /PAYMENT_BLOCK -->
