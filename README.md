# EGRET & BATSE Gamma-Ray Catalog Analysis

This repository provides a comprehensive Python-based analysis of gamma-ray sources detected by EGRET and BATSE, two major instruments onboard NASA’s Compton Gamma-Ray Observatory (CGRO). The code and documentation demonstrate advanced catalog querying, data manipulation, classification, and all-sky visualization of high-energy astrophysical sources.

---

## 🚀 What’s Included?

- **Automated catalog retrieval** from Vizier using `astroquery` for:
  - Third EGRET Catalog ([Hartman et al. 1999](https://vizier.cds.unistra.fr/viz-bin/VizieR?-source=J/ApJS/123/79))
  - BATSE Burst and Transient Source Experiment database

- **Conversion of astronomical tables to Pandas DataFrames** for analysis and visualization

- **Source type classification** using identification flags and notes in the catalog

- **Manual vs. pandas-based approaches** for counting and analyzing object types

- **Handling of unclassified and ambiguous sources**

- **Coordinate transformations:** Equatorial (RA/Dec) to Galactic, using `astropy`

- **All-sky visualization:**
  - Static sky maps with Mollweide projections (`matplotlib`)
  - Optional interactive maps using [PyWWT](https://pywwt.readthedocs.io/en/stable/)

- **Source property exploration:** 
  - Fluxes and uncertainties
  - Spectral indices

- **Comparison of EGRET and BATSE detection capabilities**

---

## 📋 Step-by-Step Workflow

1. **Library Imports and Setup:**  
   Loads all required scientific and astronomy libraries, sets up plotting.

2. **Catalog Querying and Retrieval:**  
   - Searches Vizier for the "Third EGRET Catalog" and BATSE database
   - Downloads the catalogs in their entirety, removing any row limits

3. **Table Inspection and Conversion:**  
   - Explores catalog contents and columns (IDs, coordinates, fluxes, errors, notes, etc.)
   - Converts `astropy.table.Table` to Pandas DataFrames for flexible manipulation

4. **Source Classification:**  
   - Interprets the meaning of 'ID' and 'Note' columns (e.g., pulsars, AGN, unidentified)
   - Counts and displays source types with both loop-based and `value_counts()` approaches

5. **Coordinate Handling:**  
   - Creates `SkyCoord` objects for positions
   - Transforms and visualizes sources in both equatorial and galactic coordinates

6. **All-Sky Mapping:**  
   - Generates Mollweide-projected all-sky maps of source locations
   - Differentiates source types and marks extended/compact sources
   - Adds optional background surveys (e.g., galactic plane)

7. **Interactive Visualization (Optional):**  
   - Uses PyWWT for interactive, multi-layered exploration of sources on the sky

8. **Comparison of EGRET and BATSE:**  
   - Contrasts source classes and spatial distributions from both catalogs
   - Discusses observational selection effects and detection limits


---

## ⚙️ Dependencies

- Python 3.8+
- [pandas](https://pandas.pydata.org/)
- [numpy](https://numpy.org/)
- [matplotlib](https://matplotlib.org/)
- [astropy](https://www.astropy.org/)
- [astroquery](https://astroquery.readthedocs.io/en/latest/)
- (Optional) [pywwt](https://pywwt.readthedocs.io/en/stable/) for interactive sky maps

Install with:

```bash
pip install pandas numpy matplotlib astropy astroquery
# For interactive visualization
pip install pywwt


