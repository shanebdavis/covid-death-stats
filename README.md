# Covid-19 Death Stats

### How to Make Evidence Based Decisions About Safety

Statistics and probability are hard to understand. Our biological hardware isn't good at assessing probabilities that didn't help us survive in the past. In order to understand Covid-19, we need math to translate the data into something meaningful to help us make important decisions.

- [Launch the Covid-19 Death Stats App](https://shanebdavis.github.io/covid-death-stats/)

# Source Data

> 2023 Note: Current only through September 2023 (see below)

- Covid Deaths data: https://data.cdc.gov/NCHS/Provisional-COVID-19-Deaths-by-Sex-and-Age/9bhg-hcku
- Population data: https://www.census.gov/data/tables/time-series/demo/popest/2010s-state-detail.html
- Non-Covid Death Data (2019): https://wonder.cdc.gov/mcd-icd10.html

> 2023 Note: The Provisional-COVID-19-Deaths-by-Sex-and-Age is no longer being updated as-of September 2023. There appears to be a provisional, all-causes data-set that is kept up to date here: [Provisional Mortality Statistics, 2018 through Last Week Request](https://wonder.cdc.gov/controller/datarequest/D176). I need to update the code to build from that data-set. Plus, this will give us up-to-date non-covid death data, rather than just the 2019 numbers.

### Collated Data

The data sources above were ingested and collated into a standardized format for this app to use:

- [Collated Data used in the Covid-19 Statistics App (json)](data/preparedData.json)

### Other Data of Note (not used in this app, though)

- https://www.cdc.gov/nchs/nvss/vsrr/covid19/index.htm
- [Lightning Victim Data](https://www.cdc.gov/disasters/lightning/victimdata.html)
- [How Are Covid-19 Deaths Counted - It's Complicated](https://www.aamc.org/news-insights/how-are-covid-19-deaths-counted-it-s-complicated)
- [Minnesota Suicide Mortality, Preliminary 2020 Report](https://www.health.state.mn.us/communities/suicide/documents/2020prelimsuicidedata.pdf)
- [Excess Deaths Associated with COVID-19, by Age and Race and Ethnicity — United States, January 26–October 3, 2020](https://www.cdc.gov/mmwr/volumes/69/wr/mm6942e2.htm) (i.e. trying to estimate Covid-19 deaths missed in the main, death-certificate-based data)
