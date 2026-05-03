# Pulsar Navigation Project

Pet project on pulsar signal analysis and X-ray pulsar navigation concepts.

The project demonstrates how photon arrival-time data can be processed to detect a pulsar period, build a folded pulse profile, and show how phase shifts may be used in navigation-related timing tasks.

## Goal

The goal of this project is to build a clear and reproducible pipeline for basic pulsar timing analysis:

- load and inspect photon arrival-time data;
- perform exploratory data analysis;
- preprocess the signal;
- detect the pulsation period;
- build an epoch-folded pulse profile;
- demonstrate the idea of timing-based navigation using phase shifts.

## Why This Project Matters

Pulsars are highly stable astrophysical sources. Because their pulse profiles repeat with very precise periods, they can be used as natural space navigation beacons.

This project is not a production-grade navigation system. It is an educational research-style project that shows the core logic behind pulsar timing analysis and its connection to X-ray navigation.

## Project Structure

~~~text
pulsar/
├── notebooks/
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
~~~

## Notebooks

| Notebook | Description |
|---|---|
| 01_data_loading.ipynb | Load pulsar photon data and inspect the raw dataset |
| 02_exploratory_analysis.ipynb | Explore photon arrival times, energy distribution and basic signal properties |
| 03_preprocessing.ipynb | Filter and prepare the data for period detection |
| 04_period_detection.ipynb | Apply period-search methods to detect the dominant pulsation period |
| 05_epoch_folding.ipynb | Build a folded pulse profile from photon arrival times |
| 06_xnav_demo.ipynb | Demonstrate how pulse phase shifts relate to timing and navigation concepts |

## Methods Used

- photon arrival-time analysis;
- exploratory data analysis;
- signal preprocessing;
- period detection;
- epoch folding;
- pulse profile visualization;
- simplified XNAV timing demonstration.

## Tech Stack

- Python
- NumPy
- Pandas
- Matplotlib
- SciPy
- Astropy
- Jupyter Notebook

## How to Run

Clone the repository:

~~~bash
git clone https://github.com/kva99kva-eng/pulsar.git
cd pulsar
~~~

Create and activate a virtual environment:

~~~bash
python -m venv .venv
.venv\Scripts\activate
~~~

Install dependencies:

~~~bash
pip install -r requirements.txt
~~~

Run Jupyter Lab:

~~~bash
jupyter lab
~~~

Then run the notebooks in order from 01 to 06.

## Results

The project shows a complete basic workflow for pulsar timing analysis:

- photon data is loaded and inspected;
- the signal is explored and preprocessed;
- the pulsation period is detected;
- a folded pulse profile is built;
- a simplified XNAV demonstration connects timing shifts with navigation logic.

## Limitations

This is a learning-oriented project. It does not include full spacecraft dynamics, relativistic corrections, onboard sensor fusion, or a production-grade navigation filter.

## License

This project is licensed under the MIT License.
