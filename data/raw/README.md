# CPS input data

Place your IPUMS CPS extract in this folder:

- `cps_00001.dat.gz`: fixed-width microdata.
- `cps_00001.xml`: the matching DDI data dictionary.

To obtain the files, sign in to [IPUMS CPS](https://cps.ipums.org/cps/). Select the January Basic Monthly samples for 2020–2026, not ASEC. Include YEAR, MONTH, AGE, EDUC, EMPSTAT, and WTFINL. Download the data and matching XML dictionary.

If your extract has different file names, update the two input paths in `code/analysis.R`. Run the analysis from the repository folder with `source("code/analysis.R")`.

The input files are kept locally and ignored by Git. Each reader should obtain their own extract under the IPUMS terms. See the repository README for the full method and replication instructions.

The same extract supports all three figures. Keep people outside the labor force in the download: the script includes them in the status chart and excludes them only when calculating unemployment rates. No extra variables or new extract are needed for this revision.
