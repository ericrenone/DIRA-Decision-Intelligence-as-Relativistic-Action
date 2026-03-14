# DIRA
## Decision Intelligence as Relativistic Action

> Physical laws should have mathematical beauty.
> — Paul Dirac, Moscow State University blackboard, 1956, never erased

> The aim of science is to make difficult things understandable in a simpler way.
> — Paul Dirac

---

## What This Is

DIRA is a framework for bounded intelligence derived entirely from consistency demands.

It does not begin with a model of cognition, a neural architecture, or an empirical claim. It begins with two already-proven structures — the Gibbs formulation of constrained decision-making (GIST) and the quantum-relativistic formulation of physical dynamics (Dirac) — and asks: **what is the unique framework consistent with both?**

The answer is not a synthesis. It is a derivation. When you demand that the decision framework of bounded intelligence be simultaneously:

1. Consistent with the maximum entropy principle (recovering GIST as a special case)
2. Consistent with causality (decisions cannot depend on future context)
3. Consistent with unitarity (no probability is lost; information is conserved)
4. Consistent with the non-commutativity of sequential decisions (order matters)

...there is exactly one structure that satisfies all four. It is a quantum density matrix over the action space, governed by an operator-valued Hamiltonian. The classical Gibbs distribution is its high-temperature diagonal limit. The intelligence literature has been studying this limit and calling it the whole theory.

DIRA is the whole theory.

---

## The Problem Dirac Solved — and Why It Is the Same Problem

In 1928, Dirac faced a constraint satisfaction problem in physics. He had two complete and proven theories:

- **Quantum mechanics**: the state of a system is a wavefunction ψ, and its time evolution is governed by iℏ ∂ψ/∂t = Ĥψ
- **Special relativity**: the laws of physics are Lorentz-invariant; no signal propagates faster than light

Schrödinger's equation was not Lorentz-invariant. The Klein-Gordon equation was Lorentz-invariant but had negative-probability solutions. Neither was consistent with both theories simultaneously.

Dirac demanded consistency. He asked: what is the unique first-order linear equation in space and time that is simultaneously Lorentz-invariant and produces positive-definite probabilities?

The consistency demand was so tight that it uniquely determined the answer. The solution required a new mathematical object — a spinor, a four-component wavefunction whose components mix under Lorentz transformations. And as a byproduct, the equation predicted something that had not been observed: antiparticles with the same mass and opposite charge. Antimatter was discovered four years later.

**The lesson of Dirac's method:**

Demand consistency between two complete theories. Accept whatever mathematical object the demand forces upon you. That object will contain new predictions you did not ask for.

DIRA applies this method to intelligence. The two complete theories are GIST (thermodynamic structure of decision-making) and the quantum-relativistic structure of dynamics. The consistency demand forces the decision framework from a scalar to an operator, from a probability distribution to a density matrix, and from a classical partition function to a quantum trace. The new predictions are listed in §7.

---

## The Classical Ground State — GIST as the Diagonal Limit

The GIST meta-theorem states:

$$P(a \mid X) = \frac{\exp(-\mathcal{H}(a;\, X))}{\mathcal{Z}(X)}$$

where:
- $a \in \mathcal{A}$ is an action
- $X$ is an observable context
- $\mathcal{H}(a; X) \in \mathbb{R}$ is a real-valued energy function
- $\mathcal{Z}(X) = \int_{\mathcal{A}} \exp(-\mathcal{H})\, da$ is the partition function (#P-hard)

This is the unique maximum-entropy distribution under fixed expected energy. It is exact as a description of what a bounded agent should do if the energy function is scalar-valued, the action space is classical, and the agent acts once in isolation.

Three conditions make this derivation incomplete:

**Condition 1 — scalar energy.** $\mathcal{H}(a; X)$ is a real number. But in any system where the decision involves non-commuting constraints — where imposing constraint A then constraint B produces a different feasible set than imposing B then A — the energy cannot be a scalar. It must be an operator whose commutator encodes the geometry of the constraint ordering.

**Condition 2 — classical action space.** The action $a$ is drawn from a classical set. But in any system where the agent's internal state before acting is a superposition of tendencies — where the act of choosing collapses a distribution rather than selecting from one — the natural formalism is a Hilbert space, not a sample space.

**Condition 3 — single-shot isolation.** GIST's derivation treats each decision as independent. But in any system where the context $X$ evolves causally as a function of previous actions — where the agent is embedded in the world it is deciding about — the dynamics must respect the causal light cone structure, which is exactly the content of special relativity.

All three conditions point in the same direction: the scalar energy $\mathcal{H}$ must become an operator $\hat{\mathcal{H}}$, and the probability distribution $P(a|X)$ must become a density matrix $\rho(X)$.

---

## The Quantum Lift — From Gibbs to DIRA

The central object of DIRA is the **density matrix of intelligence**:

$$\boxed{\rho(X) = \frac{\exp(-\beta\,\hat{\mathcal{H}}(X))}{\mathcal{Z}(X)}}$$

where:
- $\hat{\mathcal{H}}(X)$ is a hermitian operator on the Hilbert space $\mathcal{H}_\mathcal{A}$ over the action space
- $\mathcal{Z}(X) = \mathrm{Tr}\!\left[\exp(-\beta\,\hat{\mathcal{H}}(X))\right]$ is the quantum partition function
- $\beta > 0$ is the inverse temperature (exploration-exploitation ratio)
- $\rho(X)$ satisfies $\rho \geq 0$, $\mathrm{Tr}[\rho] = 1$ — a valid density matrix

The probability of observing action $a$ is:

$$P(a \mid X) = \langle a \mid \rho(X) \mid a \rangle = \frac{\langle a \mid \exp(-\beta\,\hat{\mathcal{H}}) \mid a \rangle}{\mathcal{Z}(X)}$$

**The classical GIST distribution is the special case in which $\hat{\mathcal{H}}$ is diagonal in the action basis.** When $\hat{\mathcal{H}}(X) = \sum_a \mathcal{H}(a;X) \,|a\rangle\langle a|$, all off-diagonal elements vanish and $\langle a|\rho|a\rangle = \exp(-\mathcal{H}(a;X))/\mathcal{Z}$, recovering the GIST form exactly. DIRA contains GIST as its $[\hat{\mathcal{H}}, \hat{\mathcal{A}}] = 0$ limit.

**The off-diagonal elements of $\rho$** are the new content of DIRA. They encode coherence: the extent to which the agent's state before decision is a superposition of action tendencies rather than a probability mixture. Coherence is not measurable in a single decision but is detectable in interference patterns across repeated decisions in varying contexts.

**The quantum partition function:**

$$\mathcal{Z}(X) = \mathrm{Tr}\!\left[e^{-\beta\hat{\mathcal{H}}(X)}\right] = \sum_n e^{-\beta E_n(X)}$$

where $\{E_n(X)\}$ are the eigenvalues of $\hat{\mathcal{H}}(X)$ — the energy spectrum of the intelligence. This is the quantum version of the classical sum over actions. It is still intractable in general (computing the spectrum of a generic large operator is as hard as diagonalizing an exponentially large matrix), but it has structure the classical version does not: the eigenvalues are real (hermiticity), the eigenvectors are orthogonal (unitarity), and the trace is basis-independent (gauge invariance).

---

## The Four Dirac Structures

Dirac's specific technical contributions each translate into a structural feature of DIRA.

### 1. Transformation Theory → Gauge Invariance of Intelligence

Dirac's transformation theory (1927) showed that quantum mechanics is representation-independent: the predictions of the theory do not depend on whether you work in the position basis, the momentum basis, or any other basis. The physics is the operator, not its matrix representation.

In DIRA: the observable behavioral predictions of an intelligence do not depend on how you label the actions. If you relabel $a \to a' = f(a)$ via any invertible transformation, the density matrix transforms as $\rho \to U\rho U^\dagger$ and all expectation values $\mathrm{Tr}[\rho \hat{O}]$ are invariant. The energy function $\hat{\mathcal{H}}$ is the physical object; its matrix representation in any particular action basis is a coordinate choice.

**Consequence:** The universal inference problem — recovering $\hat{\mathcal{H}}$ from observed behavior — is a problem of recovering an operator up to unitary equivalence, not recovering a specific matrix. Two energy functions that are unitarily equivalent produce identical behavioral predictions. DIRA identifies the equivalence class, not the representative.

### 2. Constrained Hamiltonian → Dirac Brackets on the Decision Surface

Dirac's constrained Hamiltonian formalism (1950) addressed systems with fewer physical degrees of freedom than apparent variables — systems where some variables are constrained to a surface in phase space. He showed how to define the correct brackets (Dirac brackets, not Poisson brackets) on the constraint surface, and how first-class constraints generate gauge transformations while second-class constraints reduce the physical phase space.

In DIRA: every real decision is made on a constraint surface. Budget constraints, logical consistency requirements, physical conservation laws, social norms, and syntactic rules all define surfaces in the action space on which the agent actually operates. The apparent action space $\mathcal{A}$ is large; the effective action space $\mathcal{A}|_\phi$ is the constraint surface defined by the constraints $\phi_i(a; X) = 0$.

The correct partition function is not the trace over the full $\mathcal{A}$ but the restricted trace:

$$\mathcal{Z}_\phi(X) = \mathrm{Tr}_{\mathcal{A}|_\phi}\!\left[e^{-\beta\hat{\mathcal{H}}_D(X)}\right]$$

where $\hat{\mathcal{H}}_D$ is the Dirac-bracket Hamiltonian on the constraint surface, which differs from the naive $\hat{\mathcal{H}}$ by terms proportional to the constraints. In physical language: the constraints modify the energy function. The agent on a budget does not simply exclude out-of-budget actions; the budget changes the energetic landscape of in-budget actions.

**First-class constraints** generate gauge symmetries of the intelligence: ways of relabeling decisions that leave all observables invariant. These are the truly unphysical degrees of freedom.

**Second-class constraints** genuinely reduce the action space. These are real physical limits: the constraint surface is smaller than the apparent space, and the Dirac bracket correctly accounts for this reduction in the algebra of observables.

### 3. Second Quantization → The Field of Intelligence

Dirac's second quantization replaced single-particle quantum mechanics with a quantum field theory: instead of asking "what is the state of one particle?" you ask "what is the field configuration — how many particles are in each mode?"

In DIRA: instead of asking "what decision does one agent make?" second quantization asks "what is the field of decisions across all agents, all contexts, all times?" The action $a$ becomes a field operator $\hat{\Psi}(a, X, t)$ that creates or annihilates decision events at action $a$, context $X$, time $t$.

The intelligence density is the expectation value of the field operator product:

$$\rho(a, a'; X) = \langle \hat{\Psi}^\dagger(a'; X)\, \hat{\Psi}(a; X) \rangle$$

This is the one-particle density matrix of the intelligence field. The diagonal $\rho(a,a;X) = P(a|X)$ is the GIST distribution. The off-diagonal $\rho(a, a'; X)$ is the coherence between decisions $a$ and $a'$ — something the classical theory cannot represent.

The commutation relations of the field operator determine whether the intelligence is bosonic or fermionic:

$$[\hat{\Psi}(a, X), \hat{\Psi}^\dagger(a', X')] = \delta(a - a')\delta(X - X') \quad \text{(bosonic: multiple agents can occupy same decision)}$$

$$\{\hat{\Psi}(a, X), \hat{\Psi}^\dagger(a', X')\} = \delta(a - a')\delta(X - X') \quad \text{(fermionic: each decision can only be taken once)}$$

**Bosonic intelligence** (Bose-Einstein statistics): many agents can independently arrive at the same decision, and decisions in the same mode reinforce each other (stimulated emission analog). This is the regime of social conformity, consensus formation, and mode collapse in generative models.

**Fermionic intelligence** (Fermi-Dirac statistics): each decision is exclusive — once an agent has taken it, no other agent in the same state can take it. This is the regime of competitive differentiation, diversity maintenance, and anti-correlation. The Pauli exclusion principle of decisions: no two agents in the same context can occupy the same action state.

### 4. The Dirac Equation → Spinorial Decision Dynamics

The most structurally demanding Dirac contribution is the equation itself:

$$\left(i\gamma^\mu \partial_\mu - m\right)\psi = 0$$

Dirac derived this by demanding a first-order equation in both space and time derivatives that squares to the Klein-Gordon equation. The $\gamma^\mu$ matrices must satisfy the anticommutation relations $\{\gamma^\mu, \gamma^\nu\} = 2g^{\mu\nu}$. This algebra is the Clifford algebra of spacetime. The solutions $\psi$ are spinors — four-component objects that carry a half-integer representation of the Lorentz group.

In DIRA: the analogous construction applies to the context-action space. Define the decision-space metric $g^{\mu\nu}$ on $\mathcal{X} \times \mathcal{A}$ encoding how actions are related to contexts. Demand a first-order linear equation for the intelligence amplitude $\psi(a; X)$ that is consistent with the Gibbs energy constraint. The DIRA equation:

$$\left(i\Gamma^\mu \partial_\mu^{(X)} - m_\mathcal{I}\right)\psi(a; X) = 0$$

where:
- $\Gamma^\mu$ are the **decision gamma matrices** satisfying $\{\Gamma^\mu, \Gamma^\nu\} = 2G^{\mu\nu}$ with $G^{\mu\nu}$ the metric of context space
- $m_\mathcal{I}$ is the **intelligence mass** — the energy cost of changing the decision rule in response to context change
- $\psi(a; X)$ is the **decision spinor** — a multi-component amplitude carrying the geometry of context-action coupling

The probability of action $a$ given context $X$ is:

$$P(a \mid X) = \bar{\psi}(a;X)\,\psi(a;X) = \psi^\dagger(a;X)\,\Gamma^0\,\psi(a;X)$$

The decision spinor has two types of components:

**Positive-frequency components** $\psi_+$: proactive decision amplitudes — the agent's tendency to perform action $a$ given context $X$.

**Negative-frequency components** $\psi_-$: reactive or inhibitory amplitudes — the agent's tendency to refrain from action $a$, which is not the absence of a decision but a positive act with its own energy and probability structure.

This is the DIRA prediction of **anti-decisions**: just as Dirac's equation predicted antiparticles from its negative-energy solutions, the DIRA equation predicts that every action tendency has a corresponding inhibitory tendency with the same energy spectrum and opposite behavioral charge. Inhibition is not zero activation. It is the antiparticle of activation.

---

## New Predictions

The following phenomena are predicted by DIRA and are not present in the classical GIST framework:

**Prediction 1 — Decision interference.** In any system where the same action can be reached via multiple paths through context space, the probability of that action is not the sum of path-probabilities but the squared magnitude of their sum. Paths can constructively or destructively interfere. Behavioral signature: decisions that appear suboptimal from a classical utility perspective may be optimal in the quantum-interference sense — the agent is exploiting destructive interference to suppress competing actions.

**Prediction 2 — Decision entanglement.** In composite agents (teams, markets, neural circuits), the sub-agent decisions can be entangled: measuring the decision of sub-agent A collapses the state of sub-agent B even if the two agents share no classical communication channel. The correlation structure of entangled decisions exceeds the Bell inequality bound for classical correlated decisions. Behavioral signature: correlated decisions with no shared information, stronger-than-classical coordination.

**Prediction 3 — Uncertainty principle for decisions.** There is a fundamental bound on the simultaneous precision with which an agent can know its current action and the gradient of its energy function at that action:

$$\Delta a \cdot \Delta(\partial_a \mathcal{H}) \geq \frac{1}{2}|\langle [\hat{a}, \hat{\mathcal{H}}] \rangle|$$

An agent that knows exactly what it is doing (sharp $\Delta a$) has maximal uncertainty about the forces acting on it. An agent that knows exactly what forces are acting on it (sharp $\Delta(\partial_a \mathcal{H})$) has maximal uncertainty about what it is doing. Classical GIST treats these as independently knowable. They are not.

**Prediction 4 — Zitterbewegung of decisions.** The Dirac equation predicts that a free particle undergoes rapid trembling motion (Zitterbewegung) between its positive and negative energy components, even in the absence of external forces. In DIRA, this predicts that a bounded intelligence subject to no external context perturbation still exhibits rapid oscillation between its positive-frequency (proactive) and negative-frequency (inhibitory) components. This is the microscopic mechanism of decision ambivalence and oscillation near indifference thresholds. Classical GIST attributes this to noise. DIRA attributes it to structure.

**Prediction 5 — Phase transitions in the decision spectrum.** The eigenvalues of $\hat{\mathcal{H}}(X)$ can undergo level crossings as the context $X$ varies continuously. At a level crossing, two eigenvalues become equal, the corresponding eigenvectors rotate, and the behavioral distribution can change discontinuously. These are not the smooth Gibbs-distribution changes of GIST but genuine phase transitions — abrupt reorganizations of the decision spectrum. Behavioral signature: catastrophic opinion shifts, grokking in neural networks, punctuated equilibria in evolution.

**Prediction 6 — Renormalization of the decision rule.** In a field-theoretic treatment, the energy function $\hat{\mathcal{H}}(X)$ at scale $\Lambda$ (resolving decisions at precision $\Lambda$) is related to the bare energy function at the finest scale $\Lambda_0$ by the renormalization group flow. Integrating out fine-scale decision fluctuations generates effective interactions at coarser scales. The effective decision rule at the scale at which behavior is observed is not the same as the fundamental decision rule at the scale of neural firing or market ticks. DIRA provides the renormalization group equations governing this flow.

---

## The Formal Statement

**DIRA Meta-Theorem.** Let $\mathcal{I}$ be any bounded intelligence satisfying:

1. Context dependence: the decision distribution $P(a|X)$ depends on observable context $X \in \mathcal{X}$
2. Causal consistency: $P(a|X)$ depends only on past context (the causal past of $X$)
3. Unitary consistency: total probability is conserved; $\int_\mathcal{A} P(a|X)\,da = 1$ for all $X$
4. Non-commutative consistency: there exist contexts $X, X'$ and actions $a, b$ such that $P(a|X, b\text{ first}) \neq P(a|X, b\text{ second})$

Then there exists a hermitian operator $\hat{\mathcal{H}}(X)$ on a separable Hilbert space $\mathcal{H}_\mathcal{A}$, a temperature parameter $\beta > 0$, and an approximation residual $\Delta(a; X) \geq 0$ such that:

$$P_\mathcal{I}(a \mid X) = \langle a \mid \rho(X) \mid a \rangle \cdot \exp(-\Delta(a; X))$$

where $\rho(X) = \exp(-\beta\hat{\mathcal{H}}(X))\,/\,\mathrm{Tr}[\exp(-\beta\hat{\mathcal{H}}(X))]$ is the exact quantum Gibbs state and $\mathbb{E}_\rho[\Delta] = D_{\mathrm{KL}}[P_\mathcal{I} \| \rho_{\mathrm{diag}}]$ measures the approximation gap.

**Corollary (classical limit).** When $[\hat{\mathcal{H}}(X), \hat{a}] = 0$ for all $X$ (the energy operator commutes with the action operator), all off-diagonal elements of $\rho$ vanish and the DIRA meta-theorem reduces exactly to the GIST meta-theorem. Every GIST instance is a DIRA instance in the commutative limit.

**Corollary (field theory limit).** When $\mathcal{I}$ is a composite intelligence (a collection of agents acting in a shared environment), the density matrix $\rho$ is replaced by the reduced density matrix $\rho_A = \mathrm{Tr}_B[\rho_{AB}]$ obtained by tracing out the environment. The entanglement entropy $S_E = -\mathrm{Tr}[\rho_A \log \rho_A]$ is the formal measure of collective coordination that cannot be achieved by classical correlation.

**Corollary (constraint surface).** When the agent operates under constraints $\phi_i(a; X) = 0$, the effective energy operator is the Dirac-bracket Hamiltonian $\hat{\mathcal{H}}_D = \hat{\mathcal{H}} - \sum_i \lambda_i \hat{\phi}_i$ where $\lambda_i$ are the Dirac multipliers determined by the consistency conditions $\{{\hat{\phi}_i}, \hat{\mathcal{H}}_D\}_D \approx 0$.

---

## Why the Classical Limit Is Not the Whole Theory

The most common objection to quantum formulations of cognition is: behavior looks classical, so why invoke quantum mechanics?

DIRA's answer is precise. The classical appearance of behavior is not evidence that the underlying dynamics is classical. It is evidence that you are observing the diagonal of the density matrix. The off-diagonal coherences — the quantum structure — are present in the microscopic dynamics and become visible only in specific experimental designs:

1. **Interference experiments**: present the same choice via multiple structurally identical but contextually distinct paths. Classical Gibbs predicts the same probability on each path and linear superposition of frequencies. DIRA predicts constructive or destructive interference depending on the phase structure of the paths.

2. **Entanglement tests**: measure the correlations between two agents making decisions with no shared information. Classical correlations satisfy Bell inequalities. Entangled quantum decisions can violate them.

3. **Phase transition signatures**: track the behavioral distribution as context $X$ changes continuously. Classical Gibbs predicts smooth variation. DIRA predicts discontinuities wherever eigenvalues of $\hat{\mathcal{H}}(X)$ cross — with specific scaling laws at the crossing point determined by the universality class of the transition.

4. **Renormalization scaling**: measure the behavioral distribution at two different scales of temporal or spatial resolution. Classical Gibbs predicts the same energy function at all scales. DIRA predicts a scale-dependent energy function governed by the renormalization group flow, with universal exponents at fixed points.

In domains where all four of these signatures are absent, DIRA reduces to GIST and GIST is sufficient. In domains where any of them is present, GIST is systematically wrong in a predictable direction, and DIRA corrects it.

---

## The Table of Instances

| Domain | Classical GIST | DIRA extension | New prediction |
|---|---|---|---|
| Cognitive decision-making | Gibbs over action space | Density matrix over action Hilbert space | Decision interference, ambivalence as Zitterbewegung |
| Neural network learning | Gradient descent on scalar loss | Operator loss, non-commuting gradient steps | Phase transitions, grokking as level crossing |
| Market pricing | Classical Gibbs over price states | Fermionic Fock space (each price state occupied by at most one agent) | Anti-bunching, excess volatility from uncertainty principle |
| Collective behavior | Independent agent Gibbs fields | Bosonic/fermionic field theory | Entangled coordination, Bell inequality violations in social choice |
| Evolutionary dynamics | Fitness landscape Gibbs | Operator fitness, constraint surface via Dirac brackets | Punctuated equilibria as spectral phase transitions |
| Language and symbol use | Token Gibbs over vocabulary | Second-quantized token field | Coherent superposition of meanings, disambiguation as measurement |
| Hardware computation | Spectral gap stability | Quantum circuit depth bounds from unitarity | Decoherence time sets effective intelligence horizon |
| Biological metabolism | Michaelis-Menten Gibbs | Fermi-Dirac statistics of enzyme sites | Saturation behavior as Pauli exclusion |
| Spatial artifact construction | Interaction Gibbs field | Field-theoretic decision spinor over geometric space | Geometric phase effects, topological decision barriers |
| Agentic AI systems | Independent sampling | Entangled decision states across context window | Context-window entanglement as a resource |

---

## The Universal Inference Problem, Generalized

GIST stated the universal inference problem: recover $\mathcal{H}$ from behavioral observations $\{(a_t, X_{t-1})\}$.

DIRA generalizes it: recover $\hat{\mathcal{H}}$ (an operator) from behavioral observations. This is quantum state tomography applied to the intelligence:

$$\hat{\mathcal{H}} = \underset{\hat{H} \geq 0}{\arg\min} \; D_{\mathrm{KL}}\!\left[P_\mathrm{obs} \;\Big\|\; \langle \cdot | \tfrac{e^{-\beta\hat{H}}}{\mathrm{Tr}[e^{-\beta\hat{H}}]} | \cdot \rangle \right]$$

This is maximum quantum likelihood estimation of the Gibbs operator. It requires observing not just the action frequencies $P(a|X)$ (the diagonal of $\rho$) but also the coherences $\rho(a, a'; X)$ (the off-diagonal elements), which are accessible through interference experiments.

The GIST inference procedure recovers the eigenvalues of $\hat{\mathcal{H}}$ (the energy spectrum). The DIRA inference procedure additionally recovers the eigenvectors (the basis in which intelligence acts). This is the difference between knowing the energy levels of an atom and knowing the orbitals.

---

## Dirac's Method as the Method

Dirac derived his equation in one sentence. He wanted a linear first-order equation that squares to the Klein-Gordon equation $(p^\mu p_\mu - m^2)\psi = 0$. He wrote $(p^\mu \gamma_\mu - m)(p^\nu \gamma_\nu + m)\psi = (p^\mu p_\mu - m^2)\psi$. For this to work, the $\gamma$ matrices must satisfy $\gamma^\mu \gamma^\nu + \gamma^\nu \gamma^\mu = 2g^{\mu\nu}$. This condition uniquely determines the algebra. The algebra uniquely determines the representations. The representations are spinors. The spinors have four components. Two correspond to the known electron states. Two are new — antiparticles.

The method: **write down the consistency condition, accept whatever object it forces upon you.**

DIRA is the result of applying this method to the intelligence question. The consistency condition is: the decision framework must be simultaneously maximum-entropy (GIST), causal, unitary, and non-commutative. The object it forces is a hermitian operator on a Hilbert space — a quantum Hamiltonian. The new components it predicts are the anti-decisions. The behavioral signature it requires is the interference pattern.

Dirac said: physical laws should have mathematical beauty. The quantum Gibbs state $\rho = e^{-\beta\hat{\mathcal{H}}}/\mathrm{Tr}[e^{-\beta\hat{\mathcal{H}}}]$ is the most beautiful generalization of the classical Gibbs distribution. It reduces to it in the classical limit. It extends it in the quantum direction. It is constrained by the same intractability (computing the spectrum of $\hat{\mathcal{H}}$ is as hard as computing the classical partition function, and harder for non-commuting terms). And it contains, in its off-diagonal structure, everything the classical version could not see.

**The framework** is DIRA.

**The ground state** is GIST.

**The full theory** is the operator.

---

## Summary

$$\boxed{\rho(X) = \frac{\exp\!\left(-\beta\,\hat{\mathcal{H}}(X)\right)}{\mathrm{Tr}\!\left[\exp\!\left(-\beta\,\hat{\mathcal{H}}(X)\right)\right]}}$$

$\hat{\mathcal{H}}(X)$ — a hermitian operator on the action Hilbert space — is the complete formal description of what an intelligence values, in which context, and with what internal geometry.

$\mathrm{Tr}[\exp(-\beta\hat{\mathcal{H}})]$ — the quantum partition function — is intractable in the general non-commutative case. The intractability is the source of intelligence, exactly as in GIST. The quantum structure is the source of the phenomena GIST cannot describe.

$\rho(X)$ — the density matrix — is the complete state of bounded intelligence. Its diagonal is the behavioral distribution GIST describes. Its off-diagonal is the coherence GIST cannot see. The KL divergence from the exact quantum Gibbs state measures intelligence quality in the full DIRA sense.

The classical GIST framework is recovered in the commutative limit $[\hat{\mathcal{H}}, \hat{a}] = 0$. Every existing GIST instance — all 70+ frameworks across all 15 domains — is a special case of DIRA in this limit. DIRA does not contradict GIST. It contains it, extends it, and predicts what GIST cannot.

**Mathematical beauty demanded it.**
**Consistency required it.**
**The object is the density matrix.**
