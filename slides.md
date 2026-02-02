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
### Diamond-II WBS 1.3 - Core Software, Controls and Computing
- Hardware Infrastructure
- Software Infrastructure
- Data to Information
- Real-time Data
- Experiment Management
- Information Management

---

![bg](./assets/bricks.png)

---
We'll be using the D-II software stack for Eiger collections
- bluesky, ophyd, ophyd-async, dodal
- sample, experiment definition services
- UIs, web interfaces
- containerised analysis platform

---

# Waffle &nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;![ w:150](./assets/software_Waffle.jpg)

[ **wof**-uhl ]
**noun**
*In user interface design, "waffle" refers to a grid-like menu or app launcher, often used as a navigation element, resembling a waffle's squares.*

---

## New Possibilities / Conclusions? 
- March - June we'll be trying to build new scans
- Benefit to I15-1:
  - new detector
  - better metadata management
- Benefit to Diamond: 
  - prototype _how_ to put new software on existing beamline

---
<style scoped>
  h2,p {color: white !important;}
  </style>
![bg](./assets/h2.png)

## Acknowledgements / Project Team
&nbsp;
&nbsp;
i15-1 team 
scm-x controls & daq teams
ulims
analysis platform team
project management team
too many other people to mention! 

---
## Quiz time! 
![bg right:60% h:400](./assets/image.png)

---
![bg](./assets/intranet.png)

---

![bg h:760](./assets/germany.png)

---

![bg h:760](./assets/a_beamline.jpg)

