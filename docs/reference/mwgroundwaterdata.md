# mwgroundwaterdata: Malawi Groundwater Monitoring Time-Series Dataset (2024–2025)

This dataset contains groundwater monitoring data collected from
monitoring wells across 10 districts in Malawi between 2024 and 2025.
The data were captured using automated data loggers installed in
monitoring wells and were collected and managed by BASEflow. The dataset
provides time-series measurements of key groundwater parameters,
enabling detailed analysis of aquifer behavior across multiple
geographic locations.

## Usage

``` r
mwgroundwaterdata
```

## Format

A tibble with 1415 rows and 9 variables

- date:

  Date when data was captured

- waterpoint_name:

  The name of the water point

- district:

  Administrative district the water point is located

- latitude:

  GPS latitude coordinate

- longitude:

  GPS longitude coordinate

- source:

  The device that captured the information

- water_level:

  Water level of the water

- temperature:

  Temperature of the data

- conductivity:

  Electical conductivity of the water
