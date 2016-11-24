## Tank drainage

(c) 2016 Mathias Vangö, JKU/PFM

##### Testcase Source

[CFDEMcoupling-PFM github repo](https://github.com/ParticulateFlow/CFDEMcoupling/tree/feature/cfdemSolverMultiphase/tutorials/cfdemSolverMultiphase/TankDrainage)

##### Software Sources

* [CFDEMcoupling-PFM branch feature/cfdemSolverMultiphase](https://github.com/ParticulateFlow/CFDEMcoupling/tree/feature/cfdemSolverMultiphase)
* [LIGGGHTS-PFM branch develop](https://github.com/ParticulateFlow/LIGGGHTS/tree/develop)
* [OpenFOAM-2.3.x commit 4d6f4a3115ff76ec4154c580eb041bc95ba4ec09](https://github.com/OpenFOAM/OpenFOAM-2.3.x)

##### CiteMe

N/A

##### Technology Readiness Level

7

##### Abstract

The developed solver is based on a coupled Volume of Fluid (VOF) and Discrete Element Method (DEM), similar as described in Sun et al. [[1]](#ref1) and Jing et al. [[2]](#ref2). The model is extended to handle n-amount of continuous phases, thus it is not limited to two continuous phases only. This testcase simulates the drainage of a stratified water-oil-air system through a dense packed particle bed. Atmospheric pressure is set at the top as well as at the outlet, thus the flow is driven by gravity only. The images below shows the domain and how such a 4-phase system can look like, as well as the obtained volumetric outflow rate of the individual phases over time.

![domain](domain.png =300x "Water-oil-air-particle system") ![volFlow](volFlow.png =300x "Volumetric flow rate over time")

##### Output

Volumetric flow rate

##### References

<a name="ref1">\[1\]</a> Sun, Xiaosong, and Mikio Sakai. "Three-dimensional simulation of gas–solid–liquid flows using the DEM–VOF method." Chemical Engineering Science 134 (2015): 531-548.

<a name="ref2">\[2\]</a> Jing, L., et al. "Extended CFD–DEM for free‐surface flow with multi‐size granules." International Journal for Numerical and Analytical Methods in Geomechanics 40.1 (2016): 62-79.

##### Known Limitations

* Smoothing of the exchange fields is necessary to keep the volume fractions bound to 1.
* Simulating lightweight dense particle beds leads to severe stability issues. Additional treatment is necessary.

##### Tested By

Mathias Vangö (JKU/PFM), 24.11.2016

##### Extended Documentation

N/A
