# 🌍 Global Population Pressure Index Dashboard

An interactive data visualization project designed to analyze and understand **population pressure across countries** using key demographic, economic, and environmental indicators.

---

## 📊 Overview

The **Global Population Pressure Index Dashboard** provides a comprehensive view of how population growth interacts with resources, economy, and sustainability factors.

The dashboard combines multiple datasets to create an **index that reflects population stress/pressure** on a country or region.

Such dashboards are commonly used to explore relationships between population and development indicators using global datasets like World Bank or similar sources 0.

---

## 🎯 Objectives

- Measure and visualize **population pressure across countries**
- Identify **high-risk regions** facing resource strain
- Enable **comparative analysis** between countries
- Support **data-driven insights** for planning and policy

---

## 📁 Project Structure

Global_Population_Pressure_Index-Dashboard/
│ 
├── data/                 # Raw and processed datasets 
├── dashboard/            # Dashboard files (Power BI)  
├── images/               # Screenshots or visuals  
├── notebooks/            # Data preprocessing / analysis  
├── README.md             # Project documentation  
└── requirements.txt     

---

## 📌 Features

- 🌐 **Global Coverage** — Multi-country dataset
- 📈 **Interactive Visualizations** — Charts, maps, filters
- 🔍 **Drill-down Analysis** — Country-level insights
- ⚖️ **Composite Index** — Population Pressure Index calculation
- 📊 **Comparative Analytics** — Cross-country comparisons

---

## 📊 Key Metrics Used

The index may include combinations of:

- Population density
- Growth rate
- GDP per capita
- Resource availability
- Urbanization rate
- Environmental indicators

---

## 🛠️ Tools & Technologies

- **Power BI / Tableau / Python (Dash/Plotly)** *(depending on implementation)*
# 📦 Data Sources

All datasets used in the **Global Population Pressure Index Dashboard** are publicly available and free to download. Below is the complete list organized by category.

---

## 🌍 Population & Demographics

| Dataset | Source | Format | Link |
|---|---|---|---|
| World Population by Country (1960–2023) | United Nations (via World Bank) | CSV | [Download](https://data.worldbank.org/indicator/SP.POP.TOTL) |
| Population Growth Rate | United Nations Population Division | CSV | [Download](https://data.worldbank.org/indicator/SP.POP.GROW) |
| Population Density (people/km²) | World Bank | CSV | [Download](https://data.worldbank.org/indicator/EN.POP.DNST) |

---

## 🌱 Food Security & Hunger

| Dataset | Source | Format | Link |
|---|---|---|---|
| Suite of Food Security Indicators | FAO / World Bank Data360 | CSV | [Download](https://data360.worldbank.org/en/dataset/FAO_FS) |
| Global Hunger Index Scores (2000–2025) | Welthungerhilfe & Concern Worldwide | XLSX | [Download](https://www.globalhungerindex.org/) |

---

## 🏭 CO₂ Emissions & Energy

| Dataset | Source | Format | Link |
|---|---|---|---|
| CO₂ & Greenhouse Gas Emissions (full dataset) | Our World in Data (OWID) | CSV | [Download](https://github.com/owid/co2-data) |
| CO₂ Emissions per Capita (AR5 standard) | World Bank | CSV | [Download](https://data.worldbank.org/indicator/EN.GHG.CO2.PC.CE.AR5) |

---

## 💧 Water Access

| Dataset | Source | Format | Link |
|---|---|---|---|
| Access to Safe Drinking Water (Rural & Urban) | WHO / UNICEF JMP via World Bank | CSV | [Download](https://data.worldbank.org/indicator/SH.H2O.SMDW.ZS) |

---

## 📊 Human Development

| Dataset | Source | Format | Link |
|---|---|---|---|
| Human Development Index (HDI) — Complete Time Series | UNDP Human Development Reports | CSV | [Download](https://hdr.undp.org/data-center/documentation-and-downloads) |
| Statistical Annex HDI Table (2025 Report) | UNDP | XLSX | [Download](https://hdr.undp.org/data-center/documentation-and-downloads) |

---

## 💰 Economics & Trade

| Dataset | Source | Format | Link |
|---|---|---|---|
| GDP (constant 2015 USD) | World Bank / IMF | CSV | [Download](https://data.worldbank.org/indicator/NY.GDP.MKTP.KD) |
| GDP per Capita (constant 2015 USD) | World Bank / IMF | CSV | [Download](https://data.worldbank.org/indicator/NY.GDP.PCAP.KD) |
| Exports & Imports Volume | IMF World Economic Outlook | CSV | [Download](https://www.imf.org/en/Publications/WEO/weo-database/2024/October) |
| Inflation (Average Consumer Prices) | IMF | CSV | [Download](https://www.imf.org/en/Publications/WEO/weo-database/2024/October) |

---

## 🗺️ Geography & Country Metadata

| Dataset | Source | Format | Link |
|---|---|---|---|
| Country Region & Income Group Classification | World Bank | XLSX | [Download](https://datahelpdesk.worldbank.org/knowledgebase/articles/906519) |
| Total Land Area (km²) | World Bank | CSV | [Download](https://data.worldbank.org/indicator/AG.LND.TOTL.K2) |
| World Regions (Our World in Data) | Our World in Data | CSV | [Download](https://ourworldindata.org/grapher/world-regions-according-to-the-world-bank) |

---

## 🗂️ Cleaned Files (used in Power BI)

The following cleaned and transformed files are used directly in the Power BI data model:

| File | Description |
|---|---|
| `dim_country_region.csv` | Country → ISO3 code, Region, Income Group lookup |
| `fact_population_un.csv` | Population & growth rate by country and year |
| `fact_population_density.csv` | Population density (people/km²) by country and year |
| `fact_land_area.csv` | Total land area (km²) by country and year |
| `fact_water_access.csv` | Rural, urban and total safe water access (%) |
| `fact_economics_imf.csv` | GDP, GDP per capita, exports, imports, inflation |
| `fact_hdi.csv` | HDI score, life expectancy, GNI per capita (2000–2023) |
| `fact_co2_owid.csv` | CO₂, GHG, energy per capita (OWID, 2000–2024) |
| `fact_co2_wb.csv` | CO₂ per capita — World Bank (AR5, 2000–2024) |
| `fact_food_security.csv` | Undernourishment %, food insecurity %, protein supply |
| `fact_hunger_index.csv` | Global Hunger Index scores (2000, 2008, 2016, 2025) |

---

## 📝 License & Attribution

All datasets are publicly available under their respective open data licenses:

- **World Bank**: [Creative Commons Attribution 4.0 (CC BY 4.0)](https://datacatalog.worldbank.org/public-licenses)
- **Our World in Data**: [Creative Commons Attribution 4.0 (CC BY 4.0)](https://ourworldindata.org/faqs#how-can-i-use-our-worlds-content)
- **UNDP HDR**: [Creative Commons Attribution 3.0 IGO](https://hdr.undp.org/copyright-and-terms-use)
- **FAO**: [Creative Commons Attribution-NonCommercial-ShareAlike 3.0 IGO](https://www.fao.org/contact-us/terms/en/)
- **IMF**: [IMF Copyright & Usage Terms](https://www.imf.org/external/terms.htm)
- **Global Hunger Index**: [Creative Commons Attribution-NonCommercial-NoDerivs 4.0](https://www.globalhungerindex.org/)

> 💡 If you use this project or its data pipeline, please credit the original data providers above.

---

## 🚀 Getting Started

### 1. Clone the repository

git clone https://github.com/6thAce/Global_Population_Pressure_Index-Dashboard.git
cd Global_Population_Pressure_Index-Dashboard
