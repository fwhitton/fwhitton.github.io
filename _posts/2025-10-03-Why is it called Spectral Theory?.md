---
title: "Why is it called Spectral Theory?"
date: 2025-10-03
---
When I meet other PhD students and the unavoidable question 'What area of research are you in?' is asked, my answer varies between 'Analysis', 'Partial differential equations', 'Laplacian eigenvalues' and 'Spectral theory'. For now I'm sticking with the latter. But to someone who has never studied maths (and to many who have), it's not at all clear from the name what spectral theory entails. 

To begin with, what actually is a spectrum? The word comes from the Latin *specere* meaning to view and so a spectrum is an image. Originally this was the term given to the band of light which has been split by a prism; the term was later extended beyond visible wavelengths to the entire electromagnetic spectrum and later loosened to just mean the entire range, such as the autistic spectrum.

When heated, each element emits specific wavelengths of light. These wavelengths of light are like a fingerprint, uniquely identifying the element (the identification is called spectroscopy). In fact this is how Helium got its name: an unknown spectral line was detected during an eclipse. 

<img src="/assets/images/spectrum.png" alt="spectrum" width = 300>

Let's look at the spectrum of the Hydrogen. Hydrogen is a fairly simple quantum system, consisting of an electron orbiting a proton. It was Max Planck who realised that the electron can only orbit at certain distances from the nucleus and so requires 'packets' energy (or *quanta*) to move between levels. Thus when an electron drops down a level it emits a photon with a particular amount of energy and the amount of energy is related (inversely proportionally) to the wavelength of emitted light. The gaps between energy levels are different, explaining why there are different wavelengths in the spectrum. 

For a better idea of why the electron can only orbit at certain distances from the orbit, we need to remember that an electron is both a particle and a wave. This wave is wrapped around the nucleus so must oscillate some whole number of times in order to match up. The further away the electron sits, the more oscillations can be fit around its orbit. This can also be thought of as the quantisation of angular momentum. 

But I don't study electrons, I study functional analysis so how are quantum systems related to analysis? In quantum mechanics we treat quantities like energy and momentum no longer as numbers but as operators (in reality this involves putting a hat on a quantity like the position $x$ to make it an operator $\hat{x}$). Specifically, observable quantities are represented by Hermitian, linear operators. For the sake of simplicity we can think of them as matrices and when we make a measurement, for example an energy measurement, we can only get an eigenvalue of the matrix which corresponds to the energy of the system. Now it becomes very important to understand the eigenvalues of operators and especially those which correspond to physical observables.

Returning to the example of light, we can write down concretely the operator corresponding to the energy of an electron orbiting a proton and we can find its eigenvalues. Not every value can be an eigenvalue: the spectral theorem states that the spectrum of a (self-adjoint, compact, linear) operator is discrete so contains a countable sequence of values and QM tells us that the differences between them are the energies of photons which are emitted when electrons move between energy levels.

While the name only refers to light, the applications of spectral theory are much broader. Often we can cast a partial differential equation, for example the time independent Schrodinger equation, the heat equation or the wave equation, as an eigenvalue problem and employ the tools of spectral theory to synthesise the problem.

Aside 1: while writing this I realised that not a single common quantity has an operator which begins with the same letter: energy gets H, position gets x, momentum gets p and angular momentum gets L.


Aside 2, for those inclined:  spectral theory in finite dimensional vector spaces is a little dull. We form the characteristic polynomial for a matrix and by the fundamental theorem of algebra we are guaranteed n roots, counted with multiplicity. Things get far more interesting in the infinite dimensional case: lets examine the equation $(T- \lambda I)x = 0$ a little more closely. In finite dimensions we have a theorem about when this equation has a non-trivial solution: precisely when the map $T-\lambda I$ has determinant 0. But in infinite dimensions we have no such criteria as to when the map $T-\lambda I$ is not invertible: not being bijective entails failing to be injective or surjective. In finite dimensions these concepts are equivalent but no longer. As a result we define firstly the resolvent set:

$$
\rho(T) = \{ \lambda \in \mathbb{C} : T - \lambda I\text{ is bijective}\}
$$

and the complement of the resolvent set in the complex numbers is the spectrum. Specifically if the map $T-\lambda I$ is not injective then there is a non-zero $x$ such that $(T-\lambda I)x = 0$, precisely the statement that $x$ is an eigenvector. The spectrum contains eigenvalues but also other points which only appear in infinite dimensional spaces, called the residual and continuous spectra. Further reading is left for the curious reader.
