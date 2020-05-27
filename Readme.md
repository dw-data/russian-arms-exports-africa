# Russian arms exported to African States

Idea, data analysis, research, writing: [Tatiana Kondratenko](https://twitter.com/takondratenko)

You can read the [story here]()


## Source and Definitions

### Source 

Data for this analysis was extracted from [SIPRI's Arms Transfers Database](https://www.sipri.org/databases/armstransfers). 

### Definitions

* **SIPRI's Trend Indicator Values (TIV)** If not otherwise stated, all figures used in this analysis refer to SIPRI's TIV expressed in millions. The TIV does not reflect the financial value of weapons traded. Instead it is a military capability index based on weapons purchased by countries. A more detailed definition can be found [here](https://www.sipri.org/sites/default/files/files/FS/SIPRIFS1212.pdf). Furthermore SIPRI states that figures may not add up due to the conventions of rounding. A '0' indicates that the value of deliveries is less than 0.5m. More details can be found [here](http://www.sipri.org/databases/armstransfers/sources-and-methods/).

* **Classification of regions**: In this analysis we chose to classify countries differently from how SIPRI clusters countries into regions. According to [SIPRI's classification of countries](https://www.sipri.org/databases/regional-coverage), Egypt is not assigned to the Middle East region. In our analyis we assigned it to Africa. This is why our figures for overall exports from Russia to African countries are higher than those cited in SIPRI's reports on this topic.


## Data and Analysis

All data used for this analysis was extracted from the SIPRI Arms Transfers Database on April 6, 2020. 

You can find the raw data this analysis is based on in the [data folder](/data). It contains three files corresponding to the three charts that are part of the article.

### Russian exports to African states over time, compared to China, USA and France

[File](/data/ExportVolume-to-AfricanCountries.csv)

**Timeframe:** TIV of arms exports from Russia to African countries, 2000-2019

**Dataset Structure**

Column | Content | Type
---------------|----------| ---------|
year | year of delivery | numerical
country | exporting country | categorical
ExportsToAfricanStates_million_TIV | total export volume from exporting country to all African states, in million TIV | numerical

### Most-ordered weapons by African states from Russian suppliers

[File](/data/RussianArmsImportedByAfricanCountries.csv)

**Timeframe:** Arms exports from Russia, 2000-2019


### Russian exports to African states: geographical distribution of recipients

[File](/data/WeaponsTypesExportedFromRussiaToAfrica.csv)

**Timeframe:** TIV of arms exports from Russia, 2015 and 2019







