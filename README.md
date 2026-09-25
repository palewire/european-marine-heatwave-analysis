# European Marine Heatwave Analysis

By [Ben Welsh](https://palewi.re/who-is-ben-welsh/)

This repository contains the notebook, boundary data, and
exported results for a Reuters analysis of European sea-surface temperatures in
summer 2026.

The analysis uses daily NOAA OISST data and monthly Copernicus/ECMWF ERA5 data
to calculate area-weighted temperatures across European marine regions. Marine
heatwaves follow the Hobday method, using a 1991-2020 baseline and the NOAA
dataset.

See [analysis.ipynb](analysis.ipynb) for the calculations, maps, findings, and
source links.

## Reproduce

```sh
uv sync --group dev
uv run jupyter nbconvert --to notebook --execute --inplace --ExecutePreprocessor.timeout=-1 analysis.ipynb
```

The raw NOAA and ERA5 source files are not included. The exported analysis
tables and supporting boundary files are included under `data/` and
`boundaries/`.
