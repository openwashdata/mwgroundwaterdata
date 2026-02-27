
<!-- README.md is generated from README.Rmd. Please edit that file -->

# Malawi Groundwater Monitoring Time-Series Dataset (2024–2025)

<!-- badges: start -->

[![License: CC BY
4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

<!-- badges: end -->

This dataset contains groundwater monitoring data collected from
monitoring wells across 10 districts in Malawi between 2024 and 2025.
The data were captured using automated data loggers installed in
monitoring wells and were collected and managed by BASEflow.

The dataset provides time-series measurements of key groundwater
parameters, enabling detailed analysis of aquifer behavior across
multiple geographic locations.

Variables Included

- Date – Date of measurement

- Waterpoint Name – Name of the monitoring site

- District – Administrative district where the monitoring well is
  located

- Latitude & Longitude – Geographic coordinates of the monitoring well

- Source – Data collection method (automated data logger)

- Water Level – Groundwater level measurement (typically meters below
  ground level, depending on installation reference)

- Temperature – Groundwater temperature (°C)

- Conductivity – Electrical conductivity (µS/cm), indicating dissolved
  ion concentration and groundwater quality characteristics

The use of automated loggers ensures high-frequency, consistent, and
reliable measurements suitable for time-series analysis and
hydrogeological assessment.

1.  **Purpose and Use Cases 1. Groundwater Resource Monitoring**

- Tracking spatial and temporal groundwater level variations across
  districts

- Assessing seasonal recharge and depletion patterns

- Identifying long-term aquifer trends

2.  **Water Quality Surveillance**

- Monitoring conductivity trends as a proxy for salinity and
  mineralization

- Detecting potential contamination or quality shifts

3.  **Climate and Drought Analysis**

- Supporting drought early warning systems

- Evaluating groundwater resilience to climate variability

4.  **Infrastructure Management**

- Informing borehole design and pump installation depths

- Supporting preventive maintenance planning

- Assessing borehole performance over time

5.  **Hydrogeological Research and Modelling**

- Input data for groundwater flow and recharge models

- Calibration of aquifer simulations

- Comparative inter-district hydrogeological analysis

6.  **Policy, Regulation, and Planning**

- Evidence base for district-level and national water resource planning

- Supporting groundwater abstraction regulation

- Informing investment decisions in rural and urban water supply

**Potential Users**

- Ministry responsible for Water and district water offices

- Hydrologists and hydrogeologists

- WASH sector NGOs and implementing partners

- Academic and research institutions

- Climate and environmental analysts

- Development partners supporting water security and resilience programs

This dataset provides a structured, multi-district groundwater evidence
base to support sustainable groundwater management and water security
planning in Malawi.

## Installation

You can install the development version of mwgroundwaterdata from
[GitHub](https://github.com/) with:

``` r
# install.packages("devtools")
devtools::install_github("openwashdata/mwgroundwaterdata")
```

``` r
## Run the following code in console if you don't have the packages
## install.packages(c("dplyr", "knitr", "readr", "stringr", "gt", "kableExtra"))
library(dplyr)
library(knitr)
library(readr)
library(stringr)
library(gt)
library(kableExtra)
```

Alternatively, you can download the individual datasets as a CSV or XLSX
file from the table below.

1.  Click Download CSV. A window opens that displays the CSV in your
    browser.
2.  Right-click anywhere inside the window and select “Save Page As…”.
3.  Save the file in a folder of your choice.

| dataset | CSV | XLSX |
|:---|:---|:---|
| mwgroundwatta.rda | [Download CSV](https://github.com/openwashdata/mwgroundwaterdata/raw/main/inst/extdata/mwgroundwatta.rda.csv) | [Download XLSX](https://github.com/openwashdata/mwgroundwaterdata/raw/main/inst/extdata/mwgroundwatta.rda.xlsx) |

## Data

The package provides access to This dataset contains groundwater
monitoring data collected from monitoring wells across 10 districts in
Malawi between 2024 and 2025. The data were captured using automated
data loggers installed in monitoring wells and were collected and
managed by BASEflow.

``` r
library(mwgroundwaterdata)
```

### metadata

The dataset `mwgroundwaterdata` contains 1415 observations and 9
variables

``` r
mwgroundwaterdata |> 
  head(3) |> 
  gt::gt() |>
  gt::as_raw_html()
```

<div id="elcspaouav" style="padding-left:0px;padding-right:0px;padding-top:10px;padding-bottom:10px;overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
  &#10;  <table class="gt_table" data-quarto-disable-processing="false" data-quarto-bootstrap="false" style="-webkit-font-smoothing: antialiased; -moz-osx-font-smoothing: grayscale; font-family: system-ui, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol', 'Noto Color Emoji'; display: table; border-collapse: collapse; line-height: normal; margin-left: auto; margin-right: auto; color: #333333; font-size: 16px; font-weight: normal; font-style: normal; background-color: #FFFFFF; width: auto; border-top-style: solid; border-top-width: 2px; border-top-color: #A8A8A8; border-right-style: none; border-right-width: 2px; border-right-color: #D3D3D3; border-bottom-style: solid; border-bottom-width: 2px; border-bottom-color: #A8A8A8; border-left-style: none; border-left-width: 2px; border-left-color: #D3D3D3;" bgcolor="#FFFFFF">
  <thead style="border-style: none;">
    <tr class="gt_col_headings" style="border-style: none; border-top-style: solid; border-top-width: 2px; border-top-color: #D3D3D3; border-bottom-style: solid; border-bottom-width: 2px; border-bottom-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3;">
      <th class="gt_col_heading gt_columns_bottom_border gt_right" rowspan="1" colspan="1" scope="col" id="date" style="border-style: none; color: #333333; background-color: #FFFFFF; font-size: 100%; font-weight: normal; text-transform: inherit; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: bottom; padding-top: 5px; padding-bottom: 6px; padding-left: 5px; padding-right: 5px; overflow-x: hidden; text-align: right; font-variant-numeric: tabular-nums;" bgcolor="#FFFFFF" valign="bottom" align="right">date</th>
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="waterpoint_name" style="border-style: none; color: #333333; background-color: #FFFFFF; font-size: 100%; font-weight: normal; text-transform: inherit; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: bottom; padding-top: 5px; padding-bottom: 6px; padding-left: 5px; padding-right: 5px; overflow-x: hidden; text-align: left;" bgcolor="#FFFFFF" valign="bottom" align="left">waterpoint_name</th>
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="district" style="border-style: none; color: #333333; background-color: #FFFFFF; font-size: 100%; font-weight: normal; text-transform: inherit; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: bottom; padding-top: 5px; padding-bottom: 6px; padding-left: 5px; padding-right: 5px; overflow-x: hidden; text-align: left;" bgcolor="#FFFFFF" valign="bottom" align="left">district</th>
      <th class="gt_col_heading gt_columns_bottom_border gt_right" rowspan="1" colspan="1" scope="col" id="latitude" style="border-style: none; color: #333333; background-color: #FFFFFF; font-size: 100%; font-weight: normal; text-transform: inherit; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: bottom; padding-top: 5px; padding-bottom: 6px; padding-left: 5px; padding-right: 5px; overflow-x: hidden; text-align: right; font-variant-numeric: tabular-nums;" bgcolor="#FFFFFF" valign="bottom" align="right">latitude</th>
      <th class="gt_col_heading gt_columns_bottom_border gt_right" rowspan="1" colspan="1" scope="col" id="longitude" style="border-style: none; color: #333333; background-color: #FFFFFF; font-size: 100%; font-weight: normal; text-transform: inherit; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: bottom; padding-top: 5px; padding-bottom: 6px; padding-left: 5px; padding-right: 5px; overflow-x: hidden; text-align: right; font-variant-numeric: tabular-nums;" bgcolor="#FFFFFF" valign="bottom" align="right">longitude</th>
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="source" style="border-style: none; color: #333333; background-color: #FFFFFF; font-size: 100%; font-weight: normal; text-transform: inherit; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: bottom; padding-top: 5px; padding-bottom: 6px; padding-left: 5px; padding-right: 5px; overflow-x: hidden; text-align: left;" bgcolor="#FFFFFF" valign="bottom" align="left">source</th>
      <th class="gt_col_heading gt_columns_bottom_border gt_right" rowspan="1" colspan="1" scope="col" id="water_level" style="border-style: none; color: #333333; background-color: #FFFFFF; font-size: 100%; font-weight: normal; text-transform: inherit; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: bottom; padding-top: 5px; padding-bottom: 6px; padding-left: 5px; padding-right: 5px; overflow-x: hidden; text-align: right; font-variant-numeric: tabular-nums;" bgcolor="#FFFFFF" valign="bottom" align="right">water_level</th>
      <th class="gt_col_heading gt_columns_bottom_border gt_right" rowspan="1" colspan="1" scope="col" id="temperature" style="border-style: none; color: #333333; background-color: #FFFFFF; font-size: 100%; font-weight: normal; text-transform: inherit; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: bottom; padding-top: 5px; padding-bottom: 6px; padding-left: 5px; padding-right: 5px; overflow-x: hidden; text-align: right; font-variant-numeric: tabular-nums;" bgcolor="#FFFFFF" valign="bottom" align="right">temperature</th>
      <th class="gt_col_heading gt_columns_bottom_border gt_right" rowspan="1" colspan="1" scope="col" id="conductivity" style="border-style: none; color: #333333; background-color: #FFFFFF; font-size: 100%; font-weight: normal; text-transform: inherit; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: bottom; padding-top: 5px; padding-bottom: 6px; padding-left: 5px; padding-right: 5px; overflow-x: hidden; text-align: right; font-variant-numeric: tabular-nums;" bgcolor="#FFFFFF" valign="bottom" align="right">conductivity</th>
    </tr>
  </thead>
  <tbody class="gt_table_body" style="border-style: none; border-top-style: solid; border-top-width: 2px; border-top-color: #D3D3D3; border-bottom-style: solid; border-bottom-width: 2px; border-bottom-color: #D3D3D3;">
    <tr style="border-style: none;"><td headers="date" class="gt_row gt_right" style="border-style: none; padding-top: 8px; padding-bottom: 8px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: right; font-variant-numeric: tabular-nums;" valign="middle" align="right">31/12/2024</td>
<td headers="waterpoint_name" class="gt_row gt_left" style="border-style: none; padding-top: 8px; padding-bottom: 8px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Balaka Water Office</td>
<td headers="district" class="gt_row gt_left" style="border-style: none; padding-top: 8px; padding-bottom: 8px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Balaka</td>
<td headers="latitude" class="gt_row gt_right" style="border-style: none; padding-top: 8px; padding-bottom: 8px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: right; font-variant-numeric: tabular-nums;" valign="middle" align="right">-14.9923</td>
<td headers="longitude" class="gt_row gt_right" style="border-style: none; padding-top: 8px; padding-bottom: 8px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: right; font-variant-numeric: tabular-nums;" valign="middle" align="right">34.95948</td>
<td headers="source" class="gt_row gt_left" style="border-style: none; padding-top: 8px; padding-bottom: 8px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Logger</td>
<td headers="water_level" class="gt_row gt_right" style="border-style: none; padding-top: 8px; padding-bottom: 8px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: right; font-variant-numeric: tabular-nums;" valign="middle" align="right">3.1000</td>
<td headers="temperature" class="gt_row gt_right" style="border-style: none; padding-top: 8px; padding-bottom: 8px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: right; font-variant-numeric: tabular-nums;" valign="middle" align="right">27.415</td>
<td headers="conductivity" class="gt_row gt_right" style="border-style: none; padding-top: 8px; padding-bottom: 8px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: right; font-variant-numeric: tabular-nums;" valign="middle" align="right">896.8</td></tr>
    <tr style="border-style: none;"><td headers="date" class="gt_row gt_right" style="border-style: none; padding-top: 8px; padding-bottom: 8px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: right; font-variant-numeric: tabular-nums;" valign="middle" align="right">31/12/2024</td>
<td headers="waterpoint_name" class="gt_row gt_left" style="border-style: none; padding-top: 8px; padding-bottom: 8px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Balaka Water Office</td>
<td headers="district" class="gt_row gt_left" style="border-style: none; padding-top: 8px; padding-bottom: 8px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Balaka</td>
<td headers="latitude" class="gt_row gt_right" style="border-style: none; padding-top: 8px; padding-bottom: 8px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: right; font-variant-numeric: tabular-nums;" valign="middle" align="right">-14.9923</td>
<td headers="longitude" class="gt_row gt_right" style="border-style: none; padding-top: 8px; padding-bottom: 8px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: right; font-variant-numeric: tabular-nums;" valign="middle" align="right">34.95948</td>
<td headers="source" class="gt_row gt_left" style="border-style: none; padding-top: 8px; padding-bottom: 8px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Logger</td>
<td headers="water_level" class="gt_row gt_right" style="border-style: none; padding-top: 8px; padding-bottom: 8px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: right; font-variant-numeric: tabular-nums;" valign="middle" align="right">2.7012</td>
<td headers="temperature" class="gt_row gt_right" style="border-style: none; padding-top: 8px; padding-bottom: 8px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: right; font-variant-numeric: tabular-nums;" valign="middle" align="right">27.415</td>
<td headers="conductivity" class="gt_row gt_right" style="border-style: none; padding-top: 8px; padding-bottom: 8px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: right; font-variant-numeric: tabular-nums;" valign="middle" align="right">895.8</td></tr>
    <tr style="border-style: none;"><td headers="date" class="gt_row gt_right" style="border-style: none; padding-top: 8px; padding-bottom: 8px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: right; font-variant-numeric: tabular-nums;" valign="middle" align="right">1/1/2025</td>
<td headers="waterpoint_name" class="gt_row gt_left" style="border-style: none; padding-top: 8px; padding-bottom: 8px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Balaka Water Office</td>
<td headers="district" class="gt_row gt_left" style="border-style: none; padding-top: 8px; padding-bottom: 8px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Balaka</td>
<td headers="latitude" class="gt_row gt_right" style="border-style: none; padding-top: 8px; padding-bottom: 8px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: right; font-variant-numeric: tabular-nums;" valign="middle" align="right">-14.9923</td>
<td headers="longitude" class="gt_row gt_right" style="border-style: none; padding-top: 8px; padding-bottom: 8px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: right; font-variant-numeric: tabular-nums;" valign="middle" align="right">34.95948</td>
<td headers="source" class="gt_row gt_left" style="border-style: none; padding-top: 8px; padding-bottom: 8px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: left;" valign="middle" align="left">Logger</td>
<td headers="water_level" class="gt_row gt_right" style="border-style: none; padding-top: 8px; padding-bottom: 8px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: right; font-variant-numeric: tabular-nums;" valign="middle" align="right">3.3367</td>
<td headers="temperature" class="gt_row gt_right" style="border-style: none; padding-top: 8px; padding-bottom: 8px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: right; font-variant-numeric: tabular-nums;" valign="middle" align="right">27.416</td>
<td headers="conductivity" class="gt_row gt_right" style="border-style: none; padding-top: 8px; padding-bottom: 8px; padding-left: 5px; padding-right: 5px; margin: 10px; border-top-style: solid; border-top-width: 1px; border-top-color: #D3D3D3; border-left-style: none; border-left-width: 1px; border-left-color: #D3D3D3; border-right-style: none; border-right-width: 1px; border-right-color: #D3D3D3; vertical-align: middle; overflow-x: hidden; text-align: right; font-variant-numeric: tabular-nums;" valign="middle" align="right">895.7</td></tr>
  </tbody>
  &#10;</table>
</div>

For an overview of the variable names, see the following table.

<div style="border: 1px solid #ddd; padding: 0px; overflow-y: scroll; height:200px; ">

<table class="table table-striped" style="margin-left: auto; margin-right: auto;">

<thead>

<tr>

<th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;">

variable_name
</th>

<th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;">

variable_type
</th>

<th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;">

description
</th>

</tr>

</thead>

<tbody>

<tr>

<td style="text-align:left;">

date
</td>

<td style="text-align:left;">

character
</td>

<td style="text-align:left;">

Date when data was captured
</td>

</tr>

<tr>

<td style="text-align:left;">

waterpoint_name
</td>

<td style="text-align:left;">

character
</td>

<td style="text-align:left;">

The name of the water point
</td>

</tr>

<tr>

<td style="text-align:left;">

district
</td>

<td style="text-align:left;">

character
</td>

<td style="text-align:left;">

Administrative district the water point is located
</td>

</tr>

<tr>

<td style="text-align:left;">

latitude
</td>

<td style="text-align:left;">

numeric
</td>

<td style="text-align:left;">

GPS latitude coordinate
</td>

</tr>

<tr>

<td style="text-align:left;">

longitude
</td>

<td style="text-align:left;">

numeric
</td>

<td style="text-align:left;">

GPS longitude coordinate
</td>

</tr>

<tr>

<td style="text-align:left;">

source
</td>

<td style="text-align:left;">

character
</td>

<td style="text-align:left;">

The device that captured the information
</td>

</tr>

<tr>

<td style="text-align:left;">

water_level
</td>

<td style="text-align:left;">

numeric
</td>

<td style="text-align:left;">

Water level of the water
</td>

</tr>

<tr>

<td style="text-align:left;">

temperature
</td>

<td style="text-align:left;">

numeric
</td>

<td style="text-align:left;">

Temperature of the data
</td>

</tr>

<tr>

<td style="text-align:left;">

conductivity
</td>

<td style="text-align:left;">

numeric
</td>

<td style="text-align:left;">

Electical conductivity of the water
</td>

</tr>

</tbody>

</table>

</div>

## Example

``` r
library(mwgroundwaterdata)

# Visualization: Geospatial Map
# Import the libraries to be used
library(tidyverse)
library(lubridate)
library(leaflet)

# Create summary dataset INSIDE the README
well_summary <- mwgroundwaterdata %>%
  group_by(waterpoint_name, latitude, longitude, district) %>%
  summarise(
    avg_water_level = mean(water_level, na.rm = TRUE),
    avg_conductivity = mean(conductivity, na.rm = TRUE),
    .groups = "drop"
  )

leaflet(well_summary) %>%
  addTiles() %>%  # OpenStreetMap tiles
  addCircleMarkers(~longitude, ~latitude,
                   radius = ~avg_conductivity/400,
                   color = ~colorNumeric("plasma", avg_water_level)(avg_water_level),
                   popup = ~paste0(waterpoint_name, "<br>Avg Water Level: ", round(avg_water_level,2),
                                   "<br>Avg Conductivity: ", round(avg_conductivity,1))) %>%
  addLegend("bottomright",
            pal = colorNumeric("plasma", well_summary$avg_water_level),
            values = well_summary$avg_water_level,
            title = "Avg Water Level (m)")
```

<div class="leaflet html-widget html-fill-item" id="htmlwidget-6f381d13155b4c2f42b1" style="width:100%;height:480px;"></div>
<script type="application/json" data-for="htmlwidget-6f381d13155b4c2f42b1">{"x":{"options":{"crs":{"crsClass":"L.CRS.EPSG3857","code":null,"proj4def":null,"projectedBounds":null,"options":{}}},"calls":[{"method":"addTiles","args":["https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png",null,null,{"minZoom":0,"maxZoom":18,"tileSize":256,"subdomains":"abc","errorTileUrl":"","tms":false,"noWrap":false,"zoomOffset":0,"zoomReverse":false,"opacity":1,"zIndex":1,"detectRetina":false,"attribution":"&copy; <a href=\"https://openstreetmap.org/copyright/\">OpenStreetMap<\/a>,  <a href=\"https://opendatacommons.org/licenses/odbl/\">ODbL<\/a>"}]},{"method":"addCircleMarkers","args":[[-14.9923017,-15.5008809,-16.0224384,-15.81389694,-15.76980952,-15.3200048,-15.72544722,-15.4958948,-16.0168375,-15.0456152,-15.18922812,-15.7062856,-16.02450517,-15.6074859,-15.79386089,-16.45533904,-15.774954,-16.92180746,-14.8676492],[34.95948,34.5033563,34.7906859,35.59344396,34.98733313,35.3988751,35.32192842,35.04738728,35.2797201,35.1841628,34.82364619,34.7364662,35.50426657,34.5161009,35.60694735,34.89122404,34.4642941,35.25727741,35.5283082],[2.233276315789474,0.5635974025974025,14.21542333333333,0.84684375,1.148153333333333,0.7561795774647888,3.412704861111111,1.901413333333333,0.8256780821917807,2.291543333333333,3.010180921052632,2.280207792207792,0.3046423611111111,0.8302142857142857,2.349430555555556,5.359946666666668,0.8731348684210526,1.051574324324324,0.3981266666666666],null,null,{"interactive":true,"className":"","stroke":true,"color":["#0D0887","#9814A0","#F9983E","#5601A4","#F0F921","#39049A","#900EA3","#44039E","#360499","#6600A7","#C33D80","#D14E72","#7501A8","#370499","#2B0594","#5102A3","#C7427C","#7B02A8","#6F00A8"],"weight":5,"opacity":0.5,"fill":true,"fillColor":["#0D0887","#9814A0","#F9983E","#5601A4","#F0F921","#39049A","#900EA3","#44039E","#360499","#6600A7","#C33D80","#D14E72","#7501A8","#370499","#2B0594","#5102A3","#C7427C","#7B02A8","#6F00A8"],"fillOpacity":0.2},null,null,["Balaka Water Office<br>Avg Water Level: 2.86<br>Avg Conductivity: 893.3","Chidoole Primary School<br>Avg Water Level: 16.07<br>Avg Conductivity: 225.4","Chikwawa Post Office<br>Avg Water Level: 34.17<br>Avg Conductivity: 5686.2","Chilayeni Primary School<br>Avg Water Level: 9<br>Avg Conductivity: 338.7","Chilomoni Police Station<br>Avg Water Level: 44.03<br>Avg Conductivity: 459.3","Kawiya Ccap<br>Avg Water Level: 6.2<br>Avg Conductivity: 302.5","Khwalala Primary School<br>Avg Water Level: 15.23<br>Avg Conductivity: 1365.1","Malaka Primary School<br>Avg Water Level: 7.21<br>Avg Conductivity: 760.6","Mikalati Primary School<br>Avg Water Level: 5.89<br>Avg Conductivity: 330.3","Mmanga Cdss<br>Avg Water Level: 10.68<br>Avg Conductivity: 916.6","Mokhoto Primary School<br>Avg Water Level: 22<br>Avg Conductivity: 1204.1","Mpatseabwire<br>Avg Water Level: 24.48<br>Avg Conductivity: 912.1","Mulanje Water Office<br>Avg Water Level: 12.17<br>Avg Conductivity: 121.9","Mwanza Prison<br>Avg Water Level: 5.99<br>Avg Conductivity: 332.1","Nansomba Lea<br>Avg Water Level: 4.91<br>Avg Conductivity: 939.8","Ngabu Water Office<br>Avg Water Level: 8.45<br>Avg Conductivity: 2144","Nsambangombe<br>Avg Water Level: 22.64<br>Avg Conductivity: 349.3","Nsanje Water Office<br>Avg Water Level: 12.84<br>Avg Conductivity: 420.6","Ntaja Water Office<br>Avg Water Level: 11.52<br>Avg Conductivity: 159.3"],null,null,{"interactive":false,"permanent":false,"direction":"auto","opacity":1,"offset":[0,0],"textsize":"10px","textOnly":false,"className":"","sticky":true},null]},{"method":"addLegend","args":[{"colors":["#0D0887 , #2C0594 5.19498421325033%, #6001A6 17.3411621089675%, #8E0CA4 29.4873400046848%, #B52F8C 41.633517900402%, #D45270 53.7796957961192%, #EB7655 65.9258736918364%, #FB9F3A 78.0720515875536%, #FCCE25 90.2182294832708%, #F0F921 "],"labels":["5","10","15","20","25","30","35","40"],"na_color":null,"na_label":"NA","opacity":0.5,"position":"bottomright","type":"numeric","title":"Avg Water Level (m)","extra":{"p_1":0.05194984213250334,"p_n":0.9021822948327082},"layerId":null,"className":"info legend","group":null}]}],"limits":{"lat":[-16.92180746,-14.8676492],"lng":[34.4642941,35.60694735]}},"evals":[],"jsHooks":[]}</script>

## License

Data are available as
[CC-BY](https://github.com/openwashdata/%7B%7B%7Bpackagename%7D%7D%7D/blob/main/LICENSE.md).

## Citation

Please cite this package using:

``` r
citation("mwgroundwaterdata")
#> To cite package 'mwgroundwaterdata' in publications use:
#> 
#>   Mhango E (2026). _mwgroundwaterdata: Malawi Groundwater Monitoring
#>   Time-Series Dataset (2024–2025)_. R package version 0.0.0.9000,
#>   <https://github.com/openwashdata/mwgroundwaterdata>.
#> 
#> A BibTeX entry for LaTeX users is
#> 
#>   @Manual{,
#>     title = {mwgroundwaterdata: Malawi Groundwater Monitoring Time-Series Dataset (2024–2025)},
#>     author = {Emmanuel Mhango},
#>     year = {2026},
#>     note = {R package version 0.0.0.9000},
#>     url = {https://github.com/openwashdata/mwgroundwaterdata},
#>   }
```
