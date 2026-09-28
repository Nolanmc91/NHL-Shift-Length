# Optimal Shift Length in the NHL: Evidence from the 2023-24 Regular Season

Statistical analysis of optimal shift length in the NHL, showing that peak
Corsi differential per 60 seconds depends on score state.

**Author:** Nolan Cahill, Roxbury Latin School

## Paper
See `nhl_shift_length_writeup_v3.pdf` for the full writeup.

## Reproducing the analysis
1. Install R 4.6+ and RStudio.
2. Install packages: `install.packages(c("dplyr", "tidyr", "ggplot2", "mgcv", "lme4", "MASS", "data.table", "remotes"))`
3. Install hockeyR: `remotes::install_github("danmorse314/hockeyR")`
4. Run scripts in order:
   - `scripts/build_shifts.R` (pulls data, constructs shift dataset)
   - `scripts/explore.R` (diagnostic plots)
   - `scripts/model.R` (fits Model A and Model B)
   - `scripts/robustness.R` (score state split)
   - `scripts/final_analysis.R` (posterior CIs and effect sizes)

## Data
Data is pulled directly from the hockeyR package covering the 2023-24 NHL
regular season. No data files are included in this repository. The
`build_shifts.R` script produces `data/shifts_2024.rds` with 848,889
5v5 shifts.

## License
MIT License. See LICENSE file.
