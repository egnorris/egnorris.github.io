---
title: "Prediction of Optical Scattering from Plasmonic Nanostructures using Convolutional Neural Networks"
excerpt: "<br/><img src='https://i.imgur.com/Qx94UWD.png'>"
collection: projects
---

<br/><img src='https://i.imgur.com/Qx94UWD.png'>
[Abstract](https://doi.org/10.1364/CLEO_FS.2023.FW3C.3)

Finite Difference Time Domain (FDTD) simultions are a commonly used and indispensible tool in computational optics but even with the aid of High Performance Computing (HPC) these simulations can still take on the order of tens of minutes, which is perfectly reasonable when only a small number of simulations need to be completed. This time scale in the context of inverse design where hundreds of thousands of simulations are required to adequately explore parameter space is however quite long. To address this we have utilized convolutional neural networks to assemble a surrogate model that can quickly explore parameter space with reasonably high accuracy requiring for only a limited number of potential candidate designs to be rigorously simulated by FDTD. 

Electromagnetic Fields in free-space can be expressed as a sum of electric and magnetic multipoles, this provides a convenient framework for modelling far-field scattering from a nanoparticle in a homogenous medium, these multipole terms are entirely defined by particle geometry and fully describe the radiated field. Since these mutipole terms are scalars they are an ideal candidate for prediction by a machine learning system. Our previously mentioned surrogate model is able to take in a 2D profile of plasmonic nanostructure geometry and predict one of these multipole terms as a function of wavelength, for full field reconstruction we use neural networks trained to predict each component, for plamonics only the dipole and quadrupole terms are necessary for a high quality reconstruction, so we train six networks. The training time for all of these networks is on the order of hours and the prediction time is on the order of fractions of a second per geometry. 