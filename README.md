# NHS Prescription Data Analysis

### Objective
This project analyzes a massive dataset of NHS general practice prescriptions to identify the highest dispensing clinics and understand the distribution of medical items across 8,000+ practices. 

### Phase 1: Data Engineering & Memory Optimization
The raw NHS dataset consisted of highly memory-intensive CSV files. I built a Python pipeline to:
* Extract and concatenate multiple large datasets.
* Downcast data types (`float32`, `int32`) to minimize RAM footprint.
* Merge clinic geographic/index data.
* Convert the final cleaned pipeline into `.parquet` format, achieving a 10x improvement in read-speed and memory efficiency.

### Phase 2: Exploratory Data Analysis (EDA)
With the dataset optimized, I utilized `matplotlib` and `seaborn` to query the data and visualize the "Mega-Clinics" driving the highest dispensation costs.

### Key Findings
* **The Long Tail Distribution:** The vast majority of practices dispense a standard, low volume of items, while a fractional percentage of "Mega-Clinics" dispense millions of units.
* **Top Spenders:** The top 10 clinics account for a disproportionately massive segment of the total actual cost (`act_cost`).
* 
<img width="3502" height="1451" alt="dispensation_practices" src="https://github.com/user-attachments/assets/610c0136-82d1-40be-bc4e-1bf2f0a34478" />

### Tech Stack
* **Language:** Python
* **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Glob
* **Storage:** Parquet
