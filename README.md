# European Marine Heatwave Analysis

By [Ben Welsh](https://palewi.re/who-is-ben-welsh/)

This repository contains data and code supporting a Reuters analysis of European sea-surface temperatures in summer 2026.

Published September 26, 2026: ["Europe's seas are breaking heat records. Its fisheries are paying the price."]()

The key findings of the data analysis are:

1.  “European waters notched their hottest summer months since satellite sensors began providing reliable data in 1982, according to a Reuters analysis of temperatures recorded at the seas’ surface.”

2.  “Records fell from the English Channel to the Mediterranean Sea.”

3.  "Taken together, European seas averaged 21.6 C (70.9 F) between June and August, the highest in 45 years of available data."

4.  “Few areas strayed further from the norm this summer than the Bay of Biscay, off the Atlantic-facing coast of France and Spain.”

5.  "The bay's traditionally cool waters averaged 21.4 C (70.5 F) between June and August, more than 2.4 degrees (4.4 degrees) above the 1991-2020 average. Readings from the U.S. National Oceanic and Atmospheric Administration peaked on August 13 at 23.2 C (74 F), the highest of the satellite era."

6.  "In the 1980s, the Bay of Biscay averaged a handful of heatwave days per year. By the end of August, it had logged 186 this year, more than three out of every four days."

7.  "Since 2022, the English Channel has been under heatwave conditions for around six months out of the year on average, logging more than 900 days in all."

The analysis is based on data compiled by the [U.S. National Oceanic and Atmospheric Administration](https://www.ncei.noaa.gov/products/optimum-interpolation-sst) and the [European Union's Copernicus Climate Change Service](https://cds.climate.copernicus.eu/datasets/reanalysis-era5-single-levels?tab=overview). The two organizations publish average temperatures across a global grid with a resolution of 0.25 degrees of latitude and longitude per cell, based on readings gathered by buoys, ships, satellite sensors and other sources.

The data was downloaded from the public data portals maintained by each agency and stored in a local directory that is excluded from this repository. The NOAA data is drawn from the [Optimum Interpolation Sea Surface Temperature (OISST) dataset](https://www.ncei.noaa.gov/products/optimum-interpolation-sst) archive at [www.ncei.noaa.gov](https://www.ncei.noaa.gov/data/sea-surface-temperature-optimum-interpolation/v2.1/access/avhrr). The Copernicus data is drawn from the [ERA5 reanalysis dataset](https://cds.climate.copernicus.eu/datasets/reanalysis-era5-single-levels?tab=overview) archive at [cds.climate.copernicus.eu](https://cds.climate.copernicus.eu/api/catalogue/v1/collections/reanalysis-era5-single-levels/).

Reuters defined European waters as a combination of six marine regions [identified by the European Environment Agency](https://www.eea.europa.eu/en/analysis/maps-and-charts/marine-regions-and-subregions), which do not include Arctic areas or Macaronesia. Boundaries for the Bay of Biscay, the English Channel and other seas were taken from the [International Hydrographic Organization](https://iho.int/uploads/user/pubs/standards/s-23/S-23_Ed3_1953_EN.pdf).

This notebook calculates the average temperatures across those areas in June, July and August for each year since 1982, when satellite-based observations began providing reliable data. Values are area-weighted to account for the varying size of grid cells at different latitudes. While results varied slightly, the summer of 2026 had the highest European averages in both datasets.

Marine heatwaves were defined using [the Hobday method](https://www.sciencedirect.com/science/article/abs/pii/S0079661116000057) adopted by most scientists and major climate research organizations. Each daily reading was compared against a 1991-2020 baseline and judged to be in a heatwave when it surpassed the 90th percentile for five-or-more consecutive days. This portion of the analysis was done exclusively with the NOAA dataset.
