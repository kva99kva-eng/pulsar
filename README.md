# Vela Pulsar Analysis for XNAV Demonstration

Author: Victoria Kupina  
Role: Data Analyst / Junior Data Scientist

## Problem Statement

Pulsars are rapidly rotating neutron stars that emit highly periodic signals.  
This project demonstrates how photon arrival-time data from the Vela pulsar can be analyzed to detect a dominant pulsation period, build a folded pulse profile, and illustrate the basic timing logic behind X-ray pulsar navigation.

## Objectives

- load and inspect photon event data;
- explore photon arrival times and energy distribution;
- preprocess the dataset and filter low-energy events;
- detect the dominant pulsation period;
- build folded pulse profiles;
- demonstrate how phase shifts can be interpreted as timing errors in an XNAV-style example.

## Project Structure

```text
pulsar/
├── data/
│   └── README.md
├── notebooks/
│   ├── images/
│   ├── 01_data_loading.ipynb
│   ├── 02_exploratory_analysis.ipynb
│   ├── 03_preprocessing.ipynb
│   ├── 04_period_detection.ipynb
│   ├── 05_epoch_folding.ipynb
│   └── 06_xnav_demo.ipynb
├── .gitignore
├── LICENSE
├── requirements.txt
└── README.md
Data

Raw FITS data is not included in this repository because large data files are ignored by Git.

To run the notebooks, place the photon event file at:

data/raw/vela_photons.fits

Additional details are provided in data/README.md.

Methods
photon arrival-time analysis;
exploratory data analysis;
signal preprocessing;
Lomb-Scargle period detection;
epoch folding;
pulse profile visualization;
simplified XNAV timing demonstration.
Notebooks
NotebookDescription
01_data_loading.ipynbLoad FITS photon event data and inspect the dataset
02_exploratory_analysis.ipynbExplore photon arrival times, energy distribution and signal properties
03_preprocessing.ipynbFilter photon events and prepare the data for period detection
04_period_detection.ipynbDetect the dominant pulsation period
05_epoch_folding.ipynbBuild folded pulse profiles using the detected period
06_xnav_demo.ipynbDemonstrate phase shifts, timing errors and XNAV logic
Results

The project demonstrates a complete basic workflow for pulsar timing analysis:

photon event data is loaded and inspected;
low-energy events are filtered to reduce background noise;
the dominant pulsation period is detected;
folded pulse profiles are built for different binning strategies;
timing and phase-shift examples are connected to the concept of X-ray pulsar navigation.

Key result:

Dominant period ≈ 0.0893 s
Tech Stack
Python
NumPy
Pandas
Matplotlib
SciPy
Astropy
psrqpy
Jupyter Notebook
How to Run

Clone the repository:

git clone https://github.com/kva99kva-eng/pulsar.git
cd pulsar

Create and activate a virtual environment:

python -m venv .venv
.venv\Scripts\activate

Install dependencies:

pip install -r requirements.txt

Place the FITS file here:

data/raw/vela_photons.fits

Run Jupyter Lab:

jupyter lab

Then run the notebooks in order from 01 to 06.

Limitations

This is a learning-oriented project. It does not include full spacecraft dynamics, relativistic corrections, onboard sensor fusion, or a production-grade navigation filter.

License

This project is licensed under the MIT License.
