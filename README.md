# Lottery Number Analysis: Patterns or Randomness?

This project explores historical winning numbers from **Mega Millions, Powerball, and New York Pick 10**. It asks whether frequently drawn numbers, changes over time, or apparent clusters offer a useful pattern. The analysis was prepared for a general audience as part of Bellevue University's DSC 640 Data Presentation and Visualization course.

**Main takeaway:** Some numbers appeared more often than others in the historical records, but the visualizations did not show a stable pattern that could be used to predict future draws. The project is an exploration of past results, **not a lottery-number prediction tool**.

## What the presentation shows

- **Number frequency:** Bar charts compare the most frequently observed numbers in Mega Millions and Powerball, with Pick 10 shown separately.
- **Changes over time:** A line chart and yearly views examine whether apparent frequency patterns persist.
- **Distribution and clustering:** Distribution charts and a bubble chart provide other views of how drawn numbers are spread across each game.
- **Interpretation:** Differences in counts must be considered in light of the games' different structures and periods of available data. Pick 10 draws 20 numbers at a time, so its raw counts should not be compared directly with those of the other games.

The presentation's data overview lists Mega Millions (2002–2024), Powerball (2010–2024), and Pick 10 (1987–2024). The charts describe the records included in this project; they are not a formal test of lottery fairness or proof that every number has appeared equally often. Game rules and partial-year coverage can affect comparisons.

## Repository contents

| Location | Contents |
| --- | --- |
| [`analysis/LotteryNumbersAnalysis.twbx`](analysis/LotteryNumbersAnalysis.twbx) | Tableau packaged workbook containing the interactive analysis |
| [`data/`](data/) | Four prepared, long-format CSV files for the three games; Mega Millions is split into two periods |
| [`images/`](images/) | Exported charts and working images |
| [`presentation/LotteryNumbersAnalysis.pdf`](presentation/LotteryNumbersAnalysis.pdf) | Presentation of the question, visual findings, design choices, ethics, and conclusion |

The accompanying written report, *Lottery Number Analysis – Patterns or Randomness?* (Teresa Ferrill, May 10, 2026), describes the audience, preparation steps, visualization choices, and interpretation. It is not currently included in this repository.

## Data and preparation

The analysis uses publicly available historical lottery results from [New York State Open Data](https://data.ny.gov/), as described in the project report and presentation. The repository contains the **prepared** CSV files rather than the original downloads.

The report describes the preparation as checking for duplicate or incomplete records; standardizing dates; separating number strings into individual numeric values; adding year, game, and ball-type fields; and reshaping the records so each selected number has its own row. The CSVs include fields such as `Date`, `Number`, `Multiplier`, `Year`, `Game_Type`, and `Ball_Type`. The game and ball-type fields help distinguish main numbers and special balls where applicable.

The repository does **not** contain a script or notebook that recreates these cleaned CSVs from the original source datasets. Treat the included CSVs as the starting point for reproducing the Tableau views.

## Explore the analysis

1. Download [the Tableau packaged workbook](analysis/LotteryNumbersAnalysis.twbx).
2. Open it in a compatible version of Tableau Desktop or Tableau Reader. A packaged workbook normally includes the data used by its views.
3. Review the dashboards and worksheets alongside [the presentation PDF](presentation/LotteryNumbersAnalysis.pdf), which explains their intended interpretation.

The exported charts in [`images/`](images/) can be viewed without Tableau. Some are working or alternate versions; the presentation and workbook are the best starting points for the final story.

## Responsible interpretation

A number's historical frequency does not give it an advantage in a future independent draw. The project also avoids direct raw-count comparisons with Pick 10 because it selects more numbers per draw. Visual choices, differing game rules, and incomplete years can otherwise make ordinary variation look more meaningful than it is. This analysis should be used to understand the historical data, not to select bets or claim a predictive edge.

## Source and credit

- New York State Open Data, historical winning-number datasets for Mega Millions, Powerball, and Pick 10: https://data.ny.gov/
- Teresa Ferrill, *Lottery Number Analysis – Patterns or Randomness?*, Bellevue University, DSC 640, May 10, 2026.
