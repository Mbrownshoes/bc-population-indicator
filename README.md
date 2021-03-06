<div id="devex-badge"><a rel="Delivery" href="https://github.com/BCDevExchange/assets/blob/master/README.md"><img alt="In production, but maybe in Alpha or Beta. Intended to persist and be supported." style="border-width:0" src="https://assets.bcdevexchange.org/images/badges/delivery.svg" title="In production, but maybe in Alpha or Beta. Intended to persist and be supported." /></a></div>


# Trends in B.C.'s Population Size & Distribution 

A set of R scripts to populate an indicator on trends in B.C.'s population size and distribution (2015). These scripts reproduce the analysis published on [Environmental Reporting BC](http://www.env.gov.bc.ca/soe/indicators/sustainability/bc-population.html) in May 2016.

## Usage

### Data
The data for the indicator is publically available from [BC Stats](http://bcstats.gov.bc.ca/Home.aspx), the central statistical agency of the Province of British Columbia.

 - 'Population Estimates for B.C. for 1867 to 2015' can be downloaded directly from [BC Stats](http://www.bcstats.gov.bc.ca/StatisticsBySubject/Demography/PopulationEstimates.aspx) (licence: [B.C. Crown Copyright](http://www2.gov.bc.ca/gov/content?id=1AAACC9C65754E4D89A118B875E0FBDA)). The downloaded MS Excel file must be converted to a machine-reabable CSV file.

- 'Population Estimates by B.C. Regional District for 1986-2015' can be downloaded from [BC Stats](http://www.bcstats.gov.bc.ca/StatisticsBySubject/Demography/PopulationEstimates.aspx) via the search tool under Population by Age and Sex (licence: [B.C. Crown Copyright](http://www2.gov.bc.ca/gov/content?id=1AAACC9C65754E4D89A118B875E0FBDA)). The downloaded MS Excel file must be converted to a machine-reabable CSV file, with the first cell renamed to SGC.

### Code
There are two core scripts that are required for the analysis, they need to be run in order:

- `01_clean.R` - cleans and prepares data for analysis
- `02_output.R` - creates maps and graphs and saves outputs

The `run_all.R` script can be `source`ed to run it all at once.

Most packages used in the analysis can be installed from CRAN using `install.packages()`, but you will need to install [envreportutils](https://github.com/bcgov/envreportutils) using devtools:

```r
install.packages("devtools") # If you don't already have it installed

library(devtools)
install_github("bcgov/envreportutils")
```

## Getting Help or Reporting an Issue

To report bugs/issues/feature requests, please file an [issue](https://github.com/bcgov/bc_population_indicator/issues/).

## How to Contribute

If you would like to contribute, please see our [CONTRIBUTING](CONTRIBUTING.md) guidelines.

Please note that this project is released with a [Contributor Code of Conduct](CODE_OF_CONDUCT.md). By participating in this project you agree to abide by its terms.

## License

    Copyright 2016 Province of British Columbia

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at 

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
    
This repository is maintained by [Environmental Reporting BC](http://www2.gov.bc.ca/gov/content?id=FF80E0B985F245CEA62808414D78C41B). Click [here](https://github.com/bcgov/EnvReportBC-RepoList) for a complete list of our repositories on GitHub.
