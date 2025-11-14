# WHO Tuberculosis Data Analysis

An interactive analysis exploring the relationship between GDP and tuberculosis (TB) incidence and mortality rates across countries from 2000-2023.

## Overview

This project analyzes World Health Organization (WHO) tuberculosis data merged with World Bank GDP data to investigate whether there's a correlation between a country's economic status and TB burden. The analysis includes interactive visualizations, statistical correlations, and animated maps showing TB trends over time.

## Data Sources

- **WHO TB Data**: TidyTuesday dataset (2025-11-11)
  - Contains TB incidence rates, mortality rates, and other TB statistics by country and year
  - Source: [TidyTuesday](https://github.com/rfordatascience/tidytuesday)

- **GDP Data**: World Bank GDP indicators
  - GDP in current US dollars by country and year
  - Source: [World Bank - GDP (current US$)](https://data.worldbank.org/indicator/NY.GDP.MKTP.CD)

## Key Findings

The analysis reveals:
- Correlation between GDP and TB incidence rates
- Correlation between GDP and TB mortality rates
- Geographic patterns in TB burden across WHO regions
- Temporal trends in TB rates from 2000-2023

## Visualizations

The notebook includes:

1. **Scatter Plots**: GDP vs TB incidence and mortality with trend lines and correlation coefficients
2. **Interactive Choropleth Maps**:
   - TB incidence by country
   - TB mortality by country
3. **Animated Map**: Year-by-year visualization of TB incidence changes (2000-2023)
4. **Animated GIF**: Exportable animation of TB trends over time

## Installation

### Prerequisites

- Python 3.8 or higher
- Jupyter Notebook or JupyterLab

### Required Packages

Install the required packages using pip:

```bash
pip install pandas matplotlib seaborn plotly pydytuesday nbformat kaleido Pillow
```

Or install from the requirements file (if provided):

```bash
pip install -r requirements.txt
```

## Usage

1. Clone this repository:
```bash
git clone <your-repo-url>
cd FallDatathon
```

2. Download the required data files:
   - The notebook automatically downloads WHO TB data using `pydytuesday`
   - Download the World Bank GDP data from [here](https://data.worldbank.org/indicator/NY.GDP.MKTP.CD) and save as `API_NY.GDP.MKTP.CD_DS2_en_csv_v2_216063.csv`

3. Open the Jupyter notebook:
```bash
jupyter notebook WHO_TB_Analysis.ipynb
```

4. Run all cells to reproduce the analysis

## File Structure

```
.
├── WHO_TB_Analysis.ipynb       # Main analysis notebook
├── README.md                    # This file
├── who_tb_data.csv             # WHO TB dataset (auto-downloaded)
├── API_NY.GDP.MKTP.CD_DS2_en_csv_v2_216063.csv  # GDP data (manual download)
├── tb_incidence_animation.gif  # Generated animated map (optional)
└── meta.yaml                   # TidyTuesday metadata (auto-downloaded)
```

## Key Variables

- `e_inc_100k`: Estimated TB incidence per 100,000 population
- `e_mort_100k`: Estimated TB mortality per 100,000 population
- `gdp`: GDP in current US dollars
- `iso3`: Three-letter country code
- `year`: Year of observation (2000-2023)

## Interactive Features

The Plotly visualizations are fully interactive:
- Hover over countries to see detailed statistics
- Use the animation controls to play/pause and scrub through years
- Zoom and pan on maps for detailed regional views

## Exporting the Animation

To generate an animated GIF of TB trends:
1. Run all cells up to and including the GIF generation cell
2. The GIF will be saved as `tb_incidence_animation.gif`
3. Adjust the `step` parameter to control frame count and file size
4. Adjust the `duration` parameter to control animation speed

## Contributing

Feel free to fork this repository and submit pull requests for improvements or additional analyses.

## License

This project is open source and available under the MIT License.

## Acknowledgments

- WHO for providing comprehensive tuberculosis data
- World Bank for GDP statistics
- TidyTuesday community for curating the dataset
- Plotly and Matplotlib communities for visualization tools

## Contact

For questions or feedback, please open an issue on GitHub.