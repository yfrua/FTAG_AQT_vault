# SV Mass Fitting
Fitting formula:
![[Pasted image 20260226182700.png]]
- i stands for i-th NN discriminant interval.
- $N_{i, MC}$ is the predicted flavour-inclusive event yield for each discriminant interval; $C$ is a global normalization factor and $F^f$ are the jet-flavour fractions; $P^f_i (m_{SV})$ is the probability density function of $m_{SV}$ taken from simulation.
- The $C$, $F^f$ and $SF^{b,light}_i$ parameters are allowed to float in the fit, while $N_{i, MC}$ and $\epsilon^f_{i, MC}$ are fixed to the predictions from simulated events and $SF^c_i$ is set to $1.0 \pm 0.3$. 
- There are $5\times 3=15$ data points (100-85%, 85-77%, 77-70%, 70-65%, 65-0% for WPs and no SV, 0-3 GeV, 3-6 GeV for SV mass) with 2 constraint of $\sum_i \epsilon_{i, MC}^f \times SF_i^f = 1, f=l, b$ (data efficiency adds up to unity), and $1+3+6*2=16$ parameters to fit. And everything above goes down to a DoF of $15-16+2=1$.
	- ==Need to check correlation to avoid degeneracy.==

# Extrapolate Flip-Tagger to Nominal-Tagger
- 