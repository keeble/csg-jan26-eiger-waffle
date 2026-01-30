---
marp: true
paginate: true
size: 16:9
backgroundImage: url('./assets/default.png')
style: |
  @import url('./assets/diamond.css');
  img[alt~='masked'] {
    mask-image: url('./assets/dls-mask.png');
    mask-repeat: no-repeat;
    mask-size: contain;
    mask-position: 100%, 0%;
    position: absolute;
    width: 1200px;

    /* Place to right-bottom */
    right: 0px;
    top: 0px;
    }

---
<!-- _class: lower-heading -->
![bg](./assets/h1.png)
# Waffle :waffle:
Dean Keeble
CSG Meeting, 2nd February 2026

---
<style scoped>
p, h3 {
  margin-right: 530px;
}
</style>

![masked](./assets/i15-1.png)

### What makes a _good_ PDF beamline? 
A good PDF measurement is usually characterised by accesing a large momentum transfer

---

<style scoped>
  p { text-align: center; }
</style>

![](./assets/form_factors.png)

---

### What makes a _good_ PDF beamline? 
A good PDF measurement is usually characterised by accesing a large momentum transfer

$$\begin{aligned}Q = \frac{4\pi\sin(\theta)}{\lambda}
\end{aligned} $$
---
<style scoped>
  p { text-align: center; }
</style>


![h:400px](./assets/TiO2_1mm_transmission.png)

#### Small wavelengths have another advantage: they go through the sample better
---

![bg right h:500](./assets/sensor_1mm_absorption.png)
problem is if they go through the sample then they also go through the detector


---

<style scoped>
  h2, p, li { color: white !important;  }
</style>

![bg](./assets/varex.png)

## Varex (_née_ Perkin Elmer) Detectors
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; :white_check_mark: big
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; :white_check_mark: heavy
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; :white_check_mark: cheap

---

## But... there are drawbacks
1. You're now wedded to high-energy photons
1. Have limited dynamic range
1. Have not fantastic resolution
2. Are susceptible to "burn-in" 

---
![](./assets/detectors.jpeg)
 <!-- _footer: https://doi.org/10.1148/radiol.2018172656--> 


---
On the 10th July 2018 the CEO signed a PPF for an ambitious angularly-resolved CdTe (ARC) hybrid photon counting detector

![bg left](./assets/i15-1.png)

---

&nbsp;

$$\begin{aligned}
Q &= \frac{4\pi\sin(\theta)}{\lambda} \\
&= \frac{4\pi\sin(70)}{0.161669} \\
&\approx 73.0 \text{ Å}^{-1} \\
&\approx \textit{ludicrous}
\end{aligned} $$

---
### But... there are drawbacks
![](./assets/arc_flat.png)

---
![bg w:1000](./assets/eigers.png)

---

<style scoped>
table {
  border: none !important;
  border-color:  rgba(255, 255, 255, 1) !important;
  position: absolute;
  top: 55%;
  left: 50%;
  transform: translate(-50%, -50%);
}
h2 {
  position: absolute;
  top: 7%;
} td, tr, tbody {
  background-color: rgba(255, 255, 255, 1) !important;
  border-color:  rgba(255, 255, 255, 1) !important;
  color: var(--diamond-primary) !important;
}
p {
  text-align: center;
  }
</style>

 &nbsp;| model | sensor <br>thickness | pixel<br>size | frame<br>rate |  coverage | width
:-----:|:------|:-----|:------|:------|:---|---
![h:150](./assets/arc.jpg)| ARC CdTe| 1000 um | 55 um | 25 Hz | 109° | 42.2 mm
![h:150](./assets/eiger.webp) | Eiger2 X CdTe | 750 um | 75 um | 2.2 kHz | 17° | 38.4 mm

---
<style scoped>
h3 {
    position: absolute;
    top: 60px;
    left: 75px;
    right: 75px;
  }
</style>

### Simulations of scattering from LaB<sub>6</sub>

![bg h:500](./assets/lab6.png)

![bg h:450](./assets/eiger_coverage_76keV.png)

---


And that's why we ordered an Eiger?
<span data-marpit-fragment>... not entirely.</span>


---

![bg](./assets/bricks.png)

---

- bluesky, ophyd, ophyd-async, dodal
- sample, experiment definition services
- UIs, web interfaces
- containerised analysis platform

---

we happen to have a run off this year for some upgrades of our motion controllers

so March - June we'll be trying to throw as much of this stuff together as we can

---

## New Possibilities / Conclusiojns? 
- Can we utilise the frame rate? 
- Can we utilise the 2 threshold energies? 
- _Will we be able to collect samples faster?_
- Will the new Diamond-II software stack potentially help with any of these? 

---
---
<style scoped>
  h2,p {color: white !important;}
  </style>
![bg](./assets/h2.png)

## acknowledgements / project team
&nbsp;
&nbsp;
i15-1 team 
scm-x controls & daq teams
ulims
analysis platform team
project management team
too many other people to mention! 

---
