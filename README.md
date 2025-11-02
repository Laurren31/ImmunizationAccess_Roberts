# ImmunizationAccess_Roberts
**Accessibility of Immunization Across Calgary**

---

## Project Overview
The access to vaccination sites indicator examines the spatial dimensions of public health equity, exploring whether income influences the accessibility of immunization services. This analysis compares the spatial distribution of vaccination sites with median household income across Calgary’s Community Service Areas (CSAs) to identify potential disparities in the availability of services. Namely, this indicator seeks to answer the question: To what extent does household income affect access to immunization within Calgary?

---

## Folder Structure

Within the main folder are three subfolders: `Data`, `Documents`, and `Output_Figures`.

- **`Data/`**
  - **`Raw_Data/`** – Contains all unedited raw data directly from the source.
  - **`Processed_Data/`** – Includes edited intermediate and final data, metadata, and schemas.
    - **`FinalCompositeFile`** – The final analysis table containing median income, vaccination sites, nearest distance, and all calculated fields.  
      A secondary sheet includes results from an *ANOVA: Single Factor* analysis.

- **`Documents/`**
  - Contains the written report titled *“WrittenReport_Accessibility_of_Immunization”*, including results and findings.  
  - Citations, references, and license information can be found in **Section 9** of this report.

- **`Output_Figures/`**
  - **`Graphs/`** – Holds output scatterplots and boxplots.
  - **`Maps/`** – Contains map layout outputs.

---

## CRS and Data Format

- Processed data: **CSV files**  
- Raw data: **Shapefiles**  
- All data projected using **NAD 1983 CSRS UTM Zone 11N**  
- The CEI (Calgary Equity Index) is completed over **Community Service Areas** — a custom geography formed by combining two adjacent census tracts to reach approximately 10,000 people.

---

## Data Sources

- **Vaccination Locations:** Calgary Open Data Portal (data provided by Blue Cross), accessed *October 16, 2025*  
- **Median Income:** Calgary Open Data Portal (data provided by Calgary Equity Index Overlay Statistics), accessed *October 16, 2025*  
- **2021 Federal Population and Dwelling Count by Community:** Statistics Canada, accessed *October 17, 2025*

---

## Methods Summary

This analysis was completed using **ArcGIS Pro** and **Excel** with a modified proximity-based approach.

- 1 km buffer zones were created around each immunization site.  
- Population counts were calculated per catchment under the assumption of uniform population distribution using Euclidean distance.  
- Accessibility scores were defined as the number of vaccination sites available per 1,000 individuals.  
- An **ANOVA: Single Factor** analysis tested whether there was a statistically significant relationship between median income and spatial access.

📄 Detailed methodology is available in **Section 4** of *“WrittenReport_Accessibility_of_Immunization”* (in the `Documents` folder).

---

## Alphabetical Field Dictionary

| **Field** | **Description** |
|------------|-----------------|
| **ANTIVIRAL** | Indicates if antiviral is offered at vaccination site |
| **AREA_Type** | Type of area measured (CSA) |
| **AREA_ID** | ID for area location |
| **ATTRIBUTE** | CEI indicator used (median income) |
| **BUFFER_DISTANCE** | Size of buffer around each vaccination site |
| **BUFF_SHAPE_LENGTH** | Shape length of buffer pieces |
| **BUFF_SHAPE_AREA** | Shape area of buffer pieces |
| **CATEGORY** | Class of indicator |
| **CEI_RANKING** | Quartile ranking determined by CEI for each CSA by median income |
| **CITY** | City vaccination site is located in |
| **COMMUNITY_ABRV** | Abbreviated community name |
| **COMMUNITY_FULL** | Full community name |
| **COVID_19** | If COVID-19 vaccinations are offered |
| **DA_AREA_m2** | Area of dissemination area (m²) |
| **DATA_CURRENCY** | Year/date data was obtained |
| **COVID-19 / RSV / TDAP / PNEUMOCOCCAL** | Indicates if this vaccine type is available at site |
| **Global_ID** | ID assigned to community by 2021 Census |
| **JOIN_COUNT** | Number of features matched from join layer |
| **JOIN_FID** | ID of the joined feature |
| **MEAN_VS_PER_1000** | Mean vaccination sites per 1,000 people |
| **OBJECTID** | CSA number (1–113) |
| **PHONE** | Phone number of vaccination site |
| **PNEUMOCOCCAL** | If Pneumococcal vaccinations are offered |
| **QUARTILE_RANKING** | Quartile ranking derived from Natural Breaks (Jenks) |
| **RSV** | If RSV vaccinations are offered |
| **SUM_POP_CATCHMENT_PIECE** | Population covered by each buffer |
| **SITES_PER_1000** | Vaccination sites per 1,000 individuals |
| **SITES_PER_1000_FILLED** | Same as above, with nulls replaced by 0 |
| **TARGET_FID** | ID of target feature from join |
| **TDAP** | If TDAP vaccinations are offered |
| **VALUE** | Median income value |
| **VALUE_LABEL** | Median income value with currency formatting |
| **NEAR_FID** | FID of nearest vaccination site |
| **NEAR_DIST** | Nearest distance (meters) |
| **VS_ID** | Lettered ID for vaccination sites |
| **VS_NAME** | Name of vaccination site |
| **VS_ADDRESS1** | Primary address |
| **VS_ADDRESS2** | Secondary address (if applicable) |
| **VS_PER_1000** | Raw vaccination sites per 1,000 people |
| **VS_PER_1000_FILLED** | Null values replaced with 0 |

---

##  Licence and Citation

- Full citation information available in **Section 9** of *“WrittenReport_Accessibility_of_Immunization”* (in the `Documents` folder).  
- **Citation:**  
  > Lauren Roberts (2025). *Accessibility of Immunization Across Calgary.*  
  > [https://github.com/Laurren31/ImmunizationAccess_Roberts](https://github.com/Laurren31/ImmunizationAccess_Roberts)

- **License:**  
  Accessibility of Immunization Across Calgary © 2025 by Lauren Roberts is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).

---

##  Contact

**Lauren Roberts**  
📧 [Lauren.c.Roberts31@gmail.com](mailto:Lauren.c.Roberts31@gmail.com)
