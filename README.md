## Welcome to the JWST NIRSpec IFU Data Reduction Repository

This repository provides a structured, user-friendly pipeline for reducing and analyzing Integral Field Unit (IFU) data obtained from the James Webb Space Telescope (JWST). The workflow leverages the official jwst pipeline developed by the Space Telescope Science Institute (STScI), along with relevant scientific Python tools.

## Overview

This guide builds on the foundation outlined in this Astrobites article and expands it into a hands-on, step-by-step tutorial for reducing NIRSpec IFU data from JWST. While the focus is on data taken using the G395H/F290LP grating/filter configuration, the general methodology applies to a wide range of observing setups.
The reduction process uses the JWST Calibration Pipeline (version 1.13.2) - a Python based framework maintained by STScI. The pipeline processes data in three main stages:
	•	Stage 1: Performs detector-level corrections on uncalibrated exposures (e.g., bias subtraction, linearity correction, and saturation detection) and generates rate.fits and rateints.fits files.
	•	Stage 2: Applies flux and wavelength calibration to create flat-fielded 2D images.
	•	Stage 3: Combines multiple exposures into a final 3D spectral data cube for scientific analysis.

## Prerequisites

Before proceeding, ensure that:
	•	You have successfully retrieved your target data from MAST (Mikulski Archive for Space Telescopes).
	•	You are comfortable with basic Python scripting and using the terminal or command-line interface.
	•	You have set up a Python environment (e.g., via conda) with the JWST pipeline and its dependencies installed.

## Scientific Context

The NIRSpec IFU (Near-Infrared Spectrograph Integral Field Unit) enables high-contrast, spatially resolved spectroscopy across a range of scientific applications - such as:
	•	Galaxy formation and evolution studies
	•	Characterization of stellar populations
	•	Analysis of exoplanet atmospheres
	•	Spectroscopy of extended targets

More detailed information on the NIRSpec IFU and its science capabilities can be found in the JWST documentation.

In this project, we focused on IFU data for the galaxy targets SGAS-1723, SGAS-1226, SPT0418-47, and SPT2147-50. Following a public “cookbook” provided by the TEMPLATES ERS team, we installed and configured the JWST pipeline, reduced raw IFU data, and constructed 3D data cubes.
Throughout the process, we documented:
	•	Installation procedures
	•	Successful and failed steps
	•	Error messages and their resolutions
The result is a comprehensive how-to guide for reducing JWST NIRSpec IFU data. This resource is designed for users of all experience levels - from beginners to advanced researchers - who are interested in working with JWST IFU observations.

## References
1. Astrobites. (2023, October 3). UR: A Getting Started Guide for JWST NIRSpec IFU Data Reduction. https://astrobites.org/2023/10/03/ur-a-getting-started-guide-for-jwst-nirspec-ifu-data-reduction/
2. Space Telescope Science Institute (STScI). JWST NIRSpec Instrument Overview. https://jwst-docs.stsci.edu/jwst-near-infrared-spectrograph#gsc.tab=0
3. STScI. NIRSpec IFU Spectroscopy Observing Mode. https://jwst-docs.stsci.edu/jwst-near-infrared-spectrograph/nirspec-observing-modes/nirspec-ifu-spectroscopy#gsc.tab=0
4. JWST TEMPLATES ERS Team. (2023). JWST Notebooks – Public Cookbooks and Tutorials. GitHub Repository. https://github.com/JWST-Templates/Notebooks/blob/main/README.md
5. University of Cincinnati, Department of Physics. https://www.artsci.uc.edu/departments/physics.html
