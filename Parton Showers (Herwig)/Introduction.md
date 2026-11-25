Event generators are key tools in high-energy physics. General-purpose event generators describe high energy reactions across vastly different energy scales, multiplicity regimes, and at all levels of detail which allows for direct comparison with measurements carried out at colliders.

Multi-purpose event generators like HERWIG describe high energy particle collisions in several stages, expecting factorisation due to the disparate energy and length scales:

1. Elementary hard subprocesses - Incoming particles interact to produce primary outgoing states, generally calculated at LO or NLO. The energy scale of hard scattering sets the initial conditions for QCD and EW parton showers.

2. initial and final state parton showers - coloured particles are perturbatively evolved evolved from the hard scale to an IR cutoff. QCD coherence can be implemented through angular ordering, and dipole showers provide an alternative way to describe QCD parton showers in the large $N_{c}$ limit, and logarithmic accuracy can also pose additional constraints. QED and EW emission can also be incorporated in these showers.

3. Decay of heavy objects - Massive particles such as the top quark, EW bosons, Higgs, and other BSM states decay on similar timescales to parton to parton showers. Radiation from both production and decay needs to be simulated consistently, with full spin correlations preserved between stages.

4. Multiple scattering - At high energies, multiple partonic interactions within a single hadron-hadron collision are significant, and essential to Herwig.

5. Hadronisation - After perturbative evolution, coloured partons are projected into hadrons. This can be done using the string model, or through projections on colour-singlet clusters, which decay into hadrons and resonances.

6. Hadron decay - Hadronic decays are typically modelled with matrix element techniques, including off-shell effects and spin correlations, fully consistant with those in perturbative production and decay.

Herwig provides full simulation of high-energy lepton-lepton, lepton-hadron, hadron-hadron collisions, with components:#
- Initial and final state QCD showers
- EW showers
- Matching and merging to higher-order calculations
- Colour matrix element corrections
- Hadronisation and non-perturbative dynamics
- Decays of partons and hadrons
- BSM physics
- Underlying event and soft physics

