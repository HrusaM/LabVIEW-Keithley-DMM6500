# LabVIEW Keithley DMM6500 Acquisition and Control Software

## Overview

This repository contains LabVIEW drivers and a control application developed for communication with the **Keithley DMM6500 6½-digit digital multimeter**. The software was initially developed for resistance measurements of **chemiresistors (gas chemosensors)**, which operate based on changes in the resistance of their active semiconducting layers.

The application supports continuous time-resolved acquisition of the sensor response \( R(t) \) and can perform multiple resistance (and, in general, other) measurements across up to **four channels** by utilising the **Keithley 2000-SCAN scanner card**.

Target hardware links:
- Keithley DMM6500 digital multimeter: https://www.tek.com/en/products/keithley/digital-multimeter/dmm6500-6-5-digit-multimeter
- Keithley 2000-SCAN scanner card: https://www.tek.com/en/default-accessory-series-manual/model-2000-scan-scanner-card

---

## Buy Me a Coffee

If you find this project useful, you can optionally support my work by buying me a coffee.

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/Y8Z020CFC6)

## Disclaimer

This project is **not an official Keithley / Tektronix product**.  
The drivers and application were developed independently and are provided without any affiliation with, or endorsement by, Keithley or Tektronix.

The software is provided *as is*, without warranty of any kind.

---

## Hardware and Communication Requirements

- Keithley DMM6500 digital multimeter
- Keithley 2000-SCAN scanner card (for multi-channel switching, up to 4 channels in the current implementation)
- Communication via NI-VISA (e.g., USB-TMC or LAN, depending on the instrument configuration)

---

## Software Requirements

- LabVIEW 23.0 SP1
- NI-VISA
- Official LabVIEW driver package for the Keithley DMM6500 (NI Instrument Driver Network):
  - https://sine.ni.com/apps/utf8/niid_web_display.model_page?p_model_id=27985

---

## Data Storage

Measurement data are continuously saved during acquisition to a dedicated folder created under the user’s Documents directory:

- `Documents\KeithleyDMM6500\`

The application creates the folder automatically if it does not exist.

---

## Repository Structure

- src/Application – Main control application 
- src/Application/SubVIs - UI-related VIs
- project – LabVIEW project file (.lvproj)

---

## Research Context and Use

This software was developed for experimental work involving chemiresistive gas sensors and time-dependent resistance measurements at **UCT Prague (University of Chemistry and Technology, Prague)** by **Martin Hruska (hruskaa@vscht.cz, hruska.marti@gmail.com)**. Users are encouraged to use, modify, and adapt the code for their own research and experimental work.

For context and illustrative examples of experimental use cases related to this type of instrumentation, users may refer to the author’s research output:

- ORCID: https://orcid.org/0000-0002-7931-4955  
- Google Scholar: https://scholar.google.com/citations?hl=en&user=IRiKHXIAAAAJ

If this software contributes significantly to published work, appropriate citation of related publications is encouraged.

---

## Licence

This project is released under the MIT Licence. See the `LICENSE` file for details.
