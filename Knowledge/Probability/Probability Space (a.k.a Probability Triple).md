A probability space is a triple $(\Omega, \mathcal{F}, P)$ consisting of:

- The sample space $\Omega$, an arbitrary non-empty set

- The $\sigma$-algebra (a.k.a $\sigma$-field), a set of subsets of $\Omega$, called events, such that:
	— $\mathcal{F}$ contains the sample space ($\Omega\in\mathcal{F}$), is closed under complements, countable unions, and countable intersections

- The probability measure $P:\mathcal{F}\to[0,1]$, a function on $\mathcal{F}$ such that:

	— $P$ is countably additive: if $\{A_i\}_{i=1}^{\infty}\subset \mathcal{F}$ is a countable collection of pairwise disjoint sets, then $P(\cup_{i=1}^{\infty} A_i)=\sum_{i=1}^{\infty}P(A_i)$
	— The measure of the entire sample space is equal to $1$: $P(\Omega)=1$.