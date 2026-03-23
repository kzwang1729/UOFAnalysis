# Use of Force Analysis

Analysis of police use-of-force incidents across multiple states using NIBRS and state-level datasets.

## Notebooks

- **`states_uof_dataset_creation.ipynb`** — Cleans and standardizes state-level UOF data (CA, NJ, NY, OH) into a common format
- **`creating_final_dataset.ipynb`** — Merges state UOF data with NIBRS incident data and agency metadata
- **`nibrs_eda.ipynb`** — Exploratory data analysis on NIBRS data
- **`nibrs_temporal_search.ipynb`** — Temporal analysis of NIBRS incidents

## Setup

```bash
conda env create -f environment.yml
```

## Data

Data files are not included in this repository. Place them in a `data/` directory with the following structure:

```
data/
├── nibrs.csv                                  # Compiled NIBRS incidents (see NIBRS section below)
├── incidents.csv                              # Final merged incidents output
├── agency_info_2024.csv                       # FBI agency info (2024)
├── all oris 2024.csv                          # FBI ORI list (2024)
├── pra-request_clets_agencies_04282015.xls    # California CLETS agency list
├── California/
│   └── Final files/                           # California RIPA stop data
├── NewJersey/
│   └── nj_data.csv                            # New Jersey UOF data
├── NewYork/
│   ├── UOF Case Level File_Nov2020-Dec2024.xlsx
│   ├── NYPD_Use_of_Force_Incidents_20260211.csv
│   └── NYPD_Use_of_Force__Subjects_20260211.csv
└── Ohio/
    └── OIBRSUOF.csv                           # Ohio Incident-Based Reporting System UOF data
```

### Data Sources

| Dataset | Source |
|---|---|
| **NIBRS** | [FBI Crime Data Explorer](https://cde.fbi.gov/dataexplorer) — National Incident-Based Reporting System |
| **Agency Info / ORI List** | Avaliable Upon Request to Author |
| **California** | [CA DOJ RIPA Open Data Portal](https://openjustice.doj.ca.gov/data) |
| **New Jersey** | [NJ State Police Use of Force Portal](https://www.njoag.gov/force/) |
| **New York** | [NY State CJS](https://www.criminaljustice.ny.gov/crimnet/ojsa/stats.htm) / [NYPD Use of Force Data Link](https://data.cityofnewyork.us/Public-Safety/NYPD-Use-of-Force-Incidents/f4tj-796d/about_data) / [NYPD Use of Force Data Link 2](https://data.cityofnewyork.us/Public-Safety/NYPD-Use-of-Force-Subjects/dufe-vxb7/about_dataa)  |
| **Ohio** | [Ohio Office of Criminal Justice Services](https://dpsoibrspext.azurewebsites.net/UOF) |
| **California CLETS Agencies** | [Electronic Frontier Foundation Public Records Act request](https://www.eff.org/files/2015/11/18/pra-request_clets_agencies_04282015.xls)|
