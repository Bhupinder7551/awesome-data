---
title: Coronavirus Data and Resources
description: A collection of the most important, relevant datasets on Coronavirus (COVID-19) outbreak.
keywords: coronavirus, covid-19, health, epidemic
date: 2020-03-25
modified: 2020-03-25
image: climate-change.png
---

Coronavirus disease 2019 (COVID-19) time series listing confirmed cases, reported deaths and reported recoveries. Data is disaggregated by by country (and sometimes subregion). Coronavirus disease (COVID-19) is caused by the [Severe acute respiratory syndrome Coronavirus 2 (SARS-CoV-2)][sars2] and has had a worldwide effect. On March 11 2020, the World Health Organization (WHO) declared it a pandemic, pointing to the over 118,000 cases of the coronavirus illness in over 110 countries and territories around the world at the time.

[covid]: https://en.wikipedia.org/wiki/Coronavirus_disease_2019
[sars2]: https://en.wikipedia.org/wiki/Severe_acute_respiratory_syndrome_coronavirus_2

[[toc]]

## Cases, Deaths and Recoveries

Primary Dataset: https://datahub.io/core/covid-19

This dataset includes time series data tracking the number of people affected by COVID-19 worldwide, including:

* confirmed tested cases of Coronavirus infection
* how many have reportedly died while sick with Coronavirus
* the number of people who have reportedly recovered from it

Data is in CSV format and updated daily. It is sourced from [this upstream repository](https://github.com/CSSEGISandData/COVID-19) maintained by the amazing team at [Johns Hopkins University Center for Systems Science and Engineering](https://systems.jhu.edu/) (CSSE) who have been doing a great public service from an early point by collating data from around the world.

Data is cleaned and normalized, for example tidying dates and consolidating several files into normalized time series. There is also metadata such as column descriptions.

### Sources

The upstream dataset currently lists the following upstream datasources:

- World Health Organization (WHO): https://www.who.int/
- DXY.cn. Pneumonia. 2020. http://3g.dxy.cn/newh5/view/pneumonia.
- BNO News: https://bnonews.com/index.php/2020/02/the-latest-coronavirus-cases/
- National Health Commission of the People’s Republic of China (NHC):
- http://www.nhc.gov.cn/xcs/yqtb/list_gzbd.shtml
- China CDC (CCDC): http://weekly.chinacdc.cn/news/TrackingtheEpidemic.htm
- Hong Kong Department of Health: https://www.chp.gov.hk/en/features/102465.html
- Macau Government: https://www.ssm.gov.mo/portal/
- Taiwan CDC: https://sites.google.com/cdc.gov.tw/2019ncov/taiwan?authuser=0
- US CDC: https://www.cdc.gov/coronavirus/2019-ncov/index.html
- Government of Canada: https://www.canada.ca/en/public-health/services/diseases/coronavirus.html
- Australia Government Department of Health: https://www.health.gov.au/news/coronavirus-update-at-a-glance
- European Centre for Disease Prevention and Control (ECDC): https://www.ecdc.europa.eu/en/geographical-distribution-2019-ncov-cases
- Ministry of Health Singapore (MOH): https://www.moh.gov.sg/covid-19
- Italy Ministry of Health: http://www.salute.gov.it/nuovocoronavirus

Additional background is available in the [CSSE blog](https://systems.jhu.edu/research/public-health/ncov/), and in the [Lancet paper](https://www.thelancet.com/journals/laninf/article/PIIS1473-3099(20)30120-1/fulltext) ([DOI](https://doi.org/10.1016/S1473-3099(20)30120-1)), which includes this figure:

![](https://i.imgur.com/X32lUEU.png)

## Cases By Country

For now see https://datahub.io/core/covid-19 as that includes aggregate figures by country.

Coming soon ...

### US

### Italy

### United Kingdom

### France


## Models
There are various types of models in epidemiology, which are used for prediction of prevalence (total number of infected) or the duration of an epidemic spreading processes. One of the most commonly used types is compartmental models, where population is divided into compartments of people with the same properties, e.g. people who are susceptible to virus, who are recovered etc.
There are three main types of compartmental models in epidemiology: 
    Susceptible-Infected (SI), where each person can be just in two states, either susceptible (S) or infected (I); 
     Susceptible-Infected-Recovered (SIS), where each person can be in one of two states, susceptible (S) or infected (I), but then can become susceptible again;
     Susceptible-Infected-Recovered (SIR), where each person can be  in one of three states, susceptible (S), infected (I) or recovered (R).
     
In SIR model we study the number of people in each of the compartments, denoted by variable S, I and R correspondingly. SIR system can be  expressed by the set of ordinary differential equations proposed by [O. Kermack and Anderson Gray McKendrick](https://en.wikipedia.org/wiki/Compartmental_models_in_epidemiology). 
The simulations of SIR model are shown in the python script [here](https://github.com/Liyubov/heterogeneous-dynamics-on-networks/blob/master/code_network_heterogen_models/spreading_SIR.py).

The main take-away message from the SIR model simulations is that we observe so-called peak of epidemic, when the number of infected people reaches its maximum. This moment of when size of epidemic outbreak is maximal depends on SIR model parameters: probability of epidemic transmission and recovery from the disease. 
