# covid-death-stats

A command-line tool for comparing and charting Covid-19 death statistics with overall death statistics and total population sizes.

Data granularity:

- All United States or individual states
- Years or Months from 2020-01 to current
- Age Ranges:
  - All Ages
  - Under 1 year
  - 0-17 years
  - 1-4 years
  - 5-14 years
  - 15-24 years
  - 18-29 years
  - 25-34 years
  - 30-39 years
  - 35-44 years
  - 40-49 years
  - 45-54 years
  - 50-64 years
  - 55-64 years
  - 65-74 years
  - 75-84 years
  - 85 years and over

> Note: You may notice some "nulls" in the output. This data is missing in the CDC source data. Interestingly, you may find that sometimes the data is missing in the detailed counts, like for a specific state or age-range, but it is present in the aggregate counts (e.g. aggregate counts are sometimes clearly more than the sum of the non-null separated out counts).

# Usage

```bash
> covid-death-stats numbers
```

For help on the many options:

```bash
> covid-death-stats numbers --help
```

# Examples

#### Number of Total Deaths vs Covid-19 Deaths by Age
Run:
```bash
> covid-death-stats numbers --chart
```
Output:
```
  610700.00 ┼                                               ╭───
  580166.45 ┤                                               │
  549632.90 ┤                                               │
  519099.35 ┤                                           ╭───╯
  488565.80 ┤                                           │
  458032.25 ┤                                       ╭───╯
  427498.70 ┤                                       │
  396965.15 ┤                                       │
  366431.60 ┤                                       │
  335898.05 ┤                                       │
  305364.50 ┤                                   ╭───╯
  274830.95 ┤                                   │
  244297.40 ┤                                   │
  213763.85 ┤                                   │
  183230.30 ┤                                   │
  152696.75 ┤                                   │
  122163.20 ┤                               ╭───╯
   91629.65 ┤                           ╭───╯
   61096.10 ┤               ╭───────────╯           ╭───────────
   30562.55 ┤           ╭───╯               ╭───────╯
      29.00 ┼───────────╯───────────────────╯
x-axis: age
y-axis: covid19Deaths, totalDeaths
state:  All United States
data:
  "Under 1 year":      population: 3783052,  totalDeaths: 12099,  covid19Deaths: 53
  "1-4 years":         population: 15793631, totalDeaths: 2342,   covid19Deaths: 29
  "5-14 years":        population: 40994163, totalDeaths: 3730,   covid19Deaths: 77
  "15-24 years":       population: 42250205, totalDeaths: 24322,  covid19Deaths: 683
  "25-34 years":       population: 45482275, totalDeaths: 51331,  covid19Deaths: 3139
  "30-39 years":       population: 43827888, totalDeaths: 63506,  covid19Deaths: 4953
  "35-44 years":       population: 41430182, totalDeaths: 75923,  covid19Deaths: 7645
  "40-49 years":       population: 40194520, totalDeaths: 94174,  covid19Deaths: 12183
  "45-54 years":       population: 40816619, totalDeaths: 132519, covid19Deaths: 19136
  "55-64 years":       population: 42444212, totalDeaths: 297864, covid19Deaths: 42296
  "65-74 years":       population: 31483433, totalDeaths: 456950, covid19Deaths: 65319
  "75-84 years":       population: 15969872, totalDeaths: 530132, covid19Deaths: 70562
  "85 years and over": population: 6604958,  totalDeaths: 610700, covid19Deaths: 64567
  ```
#### Number of Total Deaths vs Covid-19 Deaths by Month
Run:
```bash
> covid-death-stats numbers --chart --age All
```
Out:
```
  372934.00 ┼                                           ╭───────╮
  354287.55 ┤                                           │       │
  335641.10 ┤                                           │       │
  316994.65 ┤           ╭───╮                           │       │
  298348.20 ┤           │   │                       ╭───╯       │
  279701.75 ┤           │   ╰───╮   ╭───────╮   ╭───╯           ╰───╮
  261055.30 ┼───╮   ╭───╯       │   │       ╰───╯                   ╰───────╮           ╭───╮
  242408.85 ┤   ╰───╯           ╰───╯                                       ╰───────────╯   │
  223762.40 ┤                                                                               │
  205115.95 ┤                                                                               │
  186469.50 ┤                                                                               │
  167823.05 ┤                                                                               │
  149176.60 ┤                                                                               │
  130530.15 ┤                                                                               │
  111883.70 ┤                                               ╭───╮                           │
   93237.25 ┤                                           ╭───╯   │                           │
   74590.80 ┤           ╭───╮                           │       │                           │
   55944.35 ┤           │   │                       ╭───╯       ╰───╮                       │
   37297.90 ┤           │   ╰───╮   ╭───────╮       │               │                   ╭───╰───
   18651.45 ┤           │       ╰───╯       ╰───────╯               ╰───────────╮   ╭───╯   │
       5.00 ┼───────────╯                                                       ╰───╯       ╰───
x-axis: months
y-axis: covid19Deaths, totalDeaths
age:    All Ages
state:  All United States
data:
  2020-01: population: 327052602, totalDeaths: 264676, covid19Deaths: 5
  2020-02: population: 327052602, totalDeaths: 244950, covid19Deaths: 19
  2020-03: population: 327052602, totalDeaths: 269807, covid19Deaths: 7158
  2020-04: population: 327052602, totalDeaths: 322417, covid19Deaths: 65476
  2020-05: population: 327052602, totalDeaths: 280562, covid19Deaths: 38298
  2020-06: population: 327052602, totalDeaths: 250441, covid19Deaths: 18004
  2020-07: population: 327052602, totalDeaths: 279008, covid19Deaths: 31111
  2020-08: population: 327052602, totalDeaths: 277288, covid19Deaths: 29881
  2020-09: population: 327052602, totalDeaths: 257191, covid19Deaths: 19138
  2020-10: population: 327052602, totalDeaths: 273909, covid19Deaths: 24903
  2020-11: population: 327052602, totalDeaths: 302583, covid19Deaths: 53205
  2020-12: population: 327052602, totalDeaths: 367151, covid19Deaths: 98050
  2021-01: population: 327052602, totalDeaths: 372934, covid19Deaths: 105116
  2021-02: population: 327052602, totalDeaths: 281961, covid19Deaths: 48263
  2021-03: population: 327052602, totalDeaths: 270107, covid19Deaths: 23057
  2021-04: population: 327052602, totalDeaths: 252066, covid19Deaths: 18521
  2021-05: population: 327052602, totalDeaths: 250501, covid19Deaths: 14684
  2021-06: population: 327052602, totalDeaths: 236349, covid19Deaths: 7802
  2021-07: population: 327052602, totalDeaths: 244389, covid19Deaths: 10654
  2021-08: population: 327052602, totalDeaths: 254148, covid19Deaths: 38965
  2021-09: population: 327052602, totalDeaths: 35457,  covid19Deaths: 6444
```

####

```bash
covid-death-stats numbers --covidDeathOdds --time 2020 --state cali
```
Out:
```
time:  2020
state: California
data:
  "All Ages":          population: 39356141, totalDeaths: 320718, covid19Deaths: 33457, covidDeathOdds: 1:1,176
  "Under 1 year":      population: 462589,   totalDeaths: 1667,   covid19Deaths: null,  covidDeathOdds: null
  "0-17 years":        population: 8894449,  totalDeaths: 3047,   covid19Deaths: 18,    covidDeathOdds: 1:494,136
  "1-4 years":         population: 1921127,  totalDeaths: 318,    covid19Deaths: null,  covidDeathOdds: null
  "5-14 years":        population: 5007987,  totalDeaths: 538,    covid19Deaths: null,  covidDeathOdds: null
  "15-24 years":       population: 5113402,  totalDeaths: 3848,   covid19Deaths: 94,    covidDeathOdds: 1:54,398
  "18-29 years":       population: 6670575,  totalDeaths: 6749,   covid19Deaths: 203,   covidDeathOdds: 1:32,860
  "25-34 years":       population: 5993606,  totalDeaths: 7573,   covid19Deaths: 363,   covidDeathOdds: 1:16,511
  "30-39 years":       population: 5697826,  totalDeaths: 8872,   covid19Deaths: 609,   covidDeathOdds: 1:9,356
  "35-44 years":       population: 5257626,  totalDeaths: 10309,  covid19Deaths: 922,   covidDeathOdds: 1:5,702
  "40-49 years":       population: 5005537,  totalDeaths: 13128,  covid19Deaths: 1505,  covidDeathOdds: 1:3,326
  "45-54 years":       population: 4975333,  totalDeaths: 19009,  covid19Deaths: 2349,  covidDeathOdds: 1:2,118
  "50-64 years":       population: 7249639,  totalDeaths: 52859,  covid19Deaths: 6355,  covidDeathOdds: 1:1,141
  "55-64 years":       population: 4786356,  totalDeaths: 41393,  covid19Deaths: 4951,  covidDeathOdds: 1:967
  "65-74 years":       population: 3386670,  totalDeaths: 60641,  covid19Deaths: 7260,  covidDeathOdds: 1:466
  "75-84 years":       population: 1701599,  totalDeaths: 73565,  covid19Deaths: 8205,  covidDeathOdds: 1:207
  "85 years and over": population: 749846,   totalDeaths: 101857, covid19Deaths: 9302,  covidDeathOdds: 1:81
  ```

  # Source Data

- Population data: https://www.census.gov/data/tables/time-series/demo/popest/2010s-state-detail.html
- Covid Deaths data: https://data.cdc.gov/NCHS/Provisional-COVID-19-Deaths-by-Sex-and-Age/9bhg-hcku
- Non-Covid Death Data (2019): https://wonder.cdc.gov/controller/datarequest/D77