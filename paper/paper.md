---
title: 'AnalyZe: A MATLAB Application GUI for Visualizing and Analyzing Electrical Impedance Spectroscopy data in Biological Applications'
tags:
  - Electrical Impedance Spectroscopy
  - Equivalent Circuit
  - Bioimpedance
  - System Identification
  - MATLAB
authors:
  - given-names: Douglas C.
    dropping-particle: van
    surname: Niekerk
    orcid: 0000-0002-6449-7808
    equal-contrib: true
    affiliation: 1
  - name: Róisín M. Owens
	orcid: 0000-0001-7856-2108
    corresponding: true 
    affiliation: 1
affiliations:
   index: 1
 - name: Dept. Chemical Engineering & Biotechnology, University of Cambridge, UK
date: 25 March 2024
bibliography: paper.bib

# Introduction
Electrical currents in the biological context are almost exclusively realised as ionic flux and therefore, in order to monitor (and stimulate) biological systems using electronics, electronic flow needs to be coupled ionic flow; this is the province of electrochemistry. Electrodes, inserted into the ionic conducting phase (inhabited by the biology), serve as the interface between ionic flow and electronic flow. However, the voltage-curent relationship in electrochemical systems is notoriously non-linear - in particular, the measured current is a non-linear combination of the current (modulations) contributions from each physical process within the electrochemical cell, including the biological system [REF]. 

Small-signal linearization is a common technique when treating with non-linear systems, wherein a small (sinusoidal) perterbation is applied to the system. If the perterbation (i.e. the applied voltage in a potentiostatic scenario) is sufficiently small, relative to the non-linearity of the system, then the corresponding output of the system can be approximated as linearly related to the input perterbation. A linear approximation of the system, in the region of an operating (bias) point, can therefore be measured. For a sinusoidal voltage-current, input-output pair, the the ratio of the voltage to current yields the impedance of the net system. The impedance is a linear combination of the physical phenomena in the system, and can therefore be more easily decomposed into its constituent parts. In the field of electrochemistry, this measurement is known as electrical impedance spectroscopy (EIS) [REF] and the process of decomposing the measurement using an appropriate model of the system, is known as system identification. The most common form of system identification involves modelling the linear system as an equivalent circuit, where each circuit element models the voltage-current relaitonship exhibited by the linear approximation of one of the physical processes participating in the measurment. 

# Statement of Need

Fiting equivalent circuits to impedance data is a common exercise and various software solutions exist to meet this need, incuding paid (or 'freemium') software, such as 'EC-lab', 'ZView', 'Nova' and 'PSTrace' as well as open-source solutions such as 'impedance.py' and 'ZFit' [REFS]. In general, the GUI-based solutions are proprietary and closed-source, while open source solutions are implemented as software packages. There therefore exists an accessiblity concern, wherein researchers with a preference for graphical software are limited to the use of inflexible, proprietary solutions, while those with the prerequisite coding skillset, who wish to develop bespoke variations of the impedance post-processing process, are limited to implementing sripted solutions which have a reduced apeal to other researchers in the field. We believe that, in order to democratize the knowledge being developed in the field of impedance data processing and minimize the barrier to adoption of community-driven advancement is the field, a flexible, open-source, GUI based solution is needed. 

'AnalyZe' was initially developed specifically for bioimpedance applications, although the design flexiblity is such that it can be retooled or extended for a variety of applications. In order to maximize utility of this first iteration of the software, the most common bioimpedance scenario is targeted, wherein a collection of biological cells mediate the ionic flux; the flow of ions is considered to follow two paths, the paracellular path (flow between cells) which is primarily resistive, and the trancellular path (flow through cells) which is primarily capactive [REF]. This biological barrier (to current flow) is commonly modelled as a parallel resitance and capactiance. as shown in \autoref{fig:Intro_BarrierImpedance }, the net impedance is, in the most general case, a linear combination of this barrier, the series (electrolyte) resistance of the system, and the impedance contribution of the electrode-electrolyte interfaces. 

![In an generic bioimpedance scenario, ionic flux is induced between two electrodes (conventionally reffered to as the counter and working electodes), such that the flux is impeded by the biological system situated within the applied field. The ionic current flows between the cells, via the paracellular pathway and accross the cells, via the trancellular pathway. Ionic flux in the case of the former is impeded by intercellular junctions resistively, while current flow via the trancellular pathway is impeded primarily capacitvely due to the low permittivity (and subsequent polarization) of the cell membranes. \label{fig:Intro_BarrierImpedance }](Intro_BarrierImpedance .png)

# Current Functionality of 'AnalyZe'

## Data Handling

## Equivalent Circuit Fitting

## Transfer Function System Identification

## 

# Example Text

`Gala` is an Astropy-affiliated Python package for galactic dynamics. Python
enables wrapping low-level languages (e.g., C) for speed without losing
flexibility or ease-of-use in the user-interface. The API for `Gala` was
designed to provide a class-based and user-friendly interface to fast (C or
Cython-optimized) implementations of common operations such as gravitational
potential and force evaluation, orbit integration, dynamical transformations,
and chaos indicators for nonlinear dynamics. `Gala` also relies heavily on and
interfaces well with the implementations of physical units and astronomical
coordinate systems in the `Astropy` package [@astropy] (`astropy.units` and
`astropy.coordinates`).

`Gala` was designed to be used by both astronomical researchers and by
students in courses on gravitational dynamics or astronomy. It has already been
used in a number of scientific publications [@Pearson:2017] and has also been
used in graduate courses on Galactic dynamics to, e.g., provide interactive
visualizations of textbook material [@Binney:2008]. The combination of speed,
design, and support for Astropy functionality in `Gala` will enable exciting
scientific explorations of forthcoming data releases from the *Gaia* mission
[@gaia] by students and experts alike.

# Mathematics

Single dollars ($) are required for inline mathematics e.g. $f(x) = e^{\pi/x}$

Double dollars make self-standing equations:

$$\Theta(x) = \left\{\begin{array}{l}
0\textrm{ if } x < 0\cr
1\textrm{ else}
\end{array}\right.$$

You can also use plain \LaTeX for equations
\begin{equation}\label{eq:fourier}
\hat f(\omega) = \int_{-\infty}^{\infty} f(x) e^{i\omega x} dx
\end{equation}
and refer to \autoref{eq:fourier} from text.

# Citations

Citations to entries in paper.bib should be in
[rMarkdown](http://rmarkdown.rstudio.com/authoring_bibliographies_and_citations.html)
format.

If you want to cite a software repository URL (e.g. something on GitHub without a preferred
citation) then you can do it with the example BibTeX entry below for @fidgit.

For a quick reference, the following citation commands can be used:
- `@author:2001`  ->  "Author et al. (2001)"
- `[@author:2001]` -> "(Author et al., 2001)"
- `[@author1:2001; @author2:2001]` -> "(Author1 et al., 2001; Author2 et al., 2002)"

# Figures

Figures can be included like this:
![Caption for example figure.\label{fig:example}](figure.png)
and referenced from text using \autoref{fig:example}.

Figure sizes can be customized by adding an optional second parameter:
![Caption for example figure.](figure.png){ width=20% }

# References
