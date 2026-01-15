# 🌟 Vela Pulsar Analysis for XNAV Demonstration

**Author:** Victoria Kupina  
**Role:** Data Analyst / Junior Data Scientist  

## 🚀 Problem Statement

Pulsars are rapidly rotating neutron stars emitting **periodic signals**, acting as cosmic lighthouses.  
This project demonstrates how **Vela Pulsar's γ-ray signals** can be used as **timing references** for ultra-precise **space navigation (XNAV)**.  

**Objectives:**
- Analyze photon arrival times and energies  
- Detect the dominant pulsation period  
- Build folded pulse profiles  
- Demonstrate phase shifts and timing errors affecting navigation  

## 📊 Data Source

- [Fermi LAT Photon Events for Vela Pulsar](https://fermi.gsfc.nasa.gov/cgi-bin/ssc/LAT/QueryResults.cgi?id=L2601141734299D7B0BD279)  
- **Raw format:** FITS  
- **Preprocessed:** filtered by energy > 100 MeV  

## 🛠 Methods

- **Data Loading & Preprocessing** (`01_data_loading.ipynb`, `02_preprocessing.ipynb`)  
- **Period Detection with Lomb–Scargle** (`03_period_detection.ipynb`)  
- **Folded Pulse Profiles** (`04_epoch_folding.ipynb`)  
- **XNAV Phase Shift Demo** (`05_xnav_demo.ipynb`) 

## 📈 Visuals

### Photon Arrival Times
![Arrival Times](images/hist_arrival_times.png)

### Energy Distribution
![Energy Distribution](images/hist_energy.png)

### Energy Distribution After Filtering
![Filtered Energy](images/hist_energy_filtered.png)

### Lomb–Scargle Periodogram
![Lomb–Scargle](images/lomb_scargle.png)

### Folded Pulse Profile (50 bins)
![Folded 50 bins](images/folded_profile_50bins.png)

### Folded Pulse Profile - Different Binnings
![Different Binnings](images/folded_profile_bins.png)

### XNAV Phase Shift Demo
![XNAV Demo](images/xnav_shift.png)

**Numbers:**
- Dominant period ≈ 0.0893 s  
- Filtered photons: 278,459 events  
- Phase shift 2% → ~1.78 ms time delay  
- Period error δP = 1e-4 s over 1000 s → ~1.0 ms timing error  

## 🌌 Business / Engineering Relevance

- Pulsar-based timing enables **autonomous spacecraft navigation**  
- Real-world example of **time-series analysis in astrophysics**  
- Demonstrates **data analyst skills**: cleaning, period detection, visualization, reproducible pipelines  

## 📂 Notebooks

| Notebook | Description |
|----------|-------------|
| `01_data_loading.ipynb` | Load Fermi LAT photon data, initial inspection |
| `02_preprocessing.ipynb` | Filter photons by energy, reduce background noise |
| `03_period_detection.ipynb` | Lomb–Scargle periodogram, dominant frequency detection |
| `04_epoch_folding.ipynb` | Folded pulse profile, comparison of different binning |
| `05_xnav_demo.ipynb` | Phase shift → time delay, XNAV demonstration |

## ⚡ How to Run

1. Clone this repository  
2. Install Python ≥ 3.10, packages: `numpy`, `pandas`, `matplotlib`, `astropy`, `psrqpy`  
3. Open notebooks in **JupyterLab / Jupyter Notebook**  
4. Execute cells in order (`01 → 05`)  

## 📝 License
MIT License
