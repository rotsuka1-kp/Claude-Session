# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a data analysis repository containing HR dataset files and generated visualizations. There is no build system, test suite, or application code at this time.

## Data Files

- `toy_hr_data.csv` — 55-row HR dataset with columns: `employee_id`, `department`, `tenure_years`, `salary`, `satisfaction_score`, `performance_rating`
- `salary_distribution.png` — Histogram of salary distribution with mean (red) and median (blue) vertical lines

## Python Environment

Dependencies are installed system-wide via pip. The analysis scripts use:

```bash
pip install pandas matplotlib
```

Run ad-hoc analysis with:

```bash
python3 -c "<script>"
```

or save to a `.py` file and run:

```bash
python3 script.py
```

## Plotting Convention

- Use `matplotlib.use('Agg')` before importing `pyplot` when generating plots in headless environments (no display).
- Save plots as PNG files via `plt.savefig('filename.png', dpi=150)`.
