# Russian arms exported to African states

Idea, data analysis, research, writing: [Tatiana Kondratenko](https://twitter.com/takondratenko)

You can read the [story here]()


## Source and definitions

### Source 

Data for this analysis was extracted from [SIPRI's Arms Transfers Database](https://www.sipri.org/databases/armstransfers). 

### Definitions

* **SIPRI's Trend Indicator Values (TIV)** If not otherwise stated, all figures used in this analysis refer to SIPRI's TIV expressed in millions. The TIV does not reflect the financial value of weapons traded. Instead it is a index based on value of weapons purchased by countries. A more detailed definition can be found [here](https://www.sipri.org/sites/default/files/files/FS/SIPRIFS1212.pdf). Furthermore SIPRI states that figures may not add up due to the conventions of rounding. A '0' indicates that the value of deliveries is less than 0.5m. More details can be found [here](http://www.sipri.org/databases/armstransfers/sources-and-methods/).

* **Classification of regions**: In this analysis we chose to classify countries differently from how SIPRI clusters countries into regions. According to [SIPRI's classification of countries](https://www.sipri.org/databases/regional-coverage), Egypt is assigned to the Middle East region. In our analyis we assigned it to Africa. This is why our figures for overall exports from Russia to African countries are higher than those cited in SIPRI's reports on this topic.


## Data and analysis

All data used for this analysis was extracted from the SIPRI Arms Transfers Database on April 6, 2020. 

You can find the raw data this analysis is based on in the [data folder](/data). It contains three files corresponding to the three charts that are part of the article.

### Russian exports to African states over time, compared to China, USA and France

[Data File](/data/ExportVolume-to-AfricanCountries.csv)

**Timeframe:** TIV of arms exports from Russia to African countries, 2000-2019

**Dataset structure**

Column title | content | data type
---------------|----------| ---------|
year | year of delivery | numerical
country | exporting country, filtered to only include Russia, China, USA, France | string, categorical
ExportsToAfricanStates_million_TIV | total export volume from exporting country to all African states, in million TIV | numerical

![](/charts/165_en_arms_countries_01.png)

### Russian exports to African states: geographical distribution of recipients

[Data File](/data/RussianArmsImportedByAfricanCountries.csv)

**Timeframe:** TIV of arms exports from Russia, 2015 and 2019

**Dataset structure**
Column title | content | data type
---------------|----------| ---------|
country | African country importing Russian arms | string, categorical
*year columns* | one column for each year between 2000 and 2019 | numerical
TIV_ArmsFromRussia_2000_2019 | sum, created by adding up all year columns | numerical
TIV_ArmsFromRussia_2015_2019 | sum, created by summing up the columns from 2015 to 2019 | numerical

The column `TIV_ArmsFromRussia_2015_2019` is the one that was used to create the map.

![](/charts/166_en_mapping_RussianWeapons_Africa-01.png)

### Most-ordered weapons by African states from Russian suppliers

[Data File](/data/WeaponsTypesExportedFromRussiaToAfrica.csv)

**Timeframe:** Arms exports from Russia, 2000-2019

**Dataset structure**
Column title | content | data type
---------------|----------| ---------|
Recipient | country, filtered to include African recipients only | string, categorical
Supplier | filtered to only reflect Russia as a supplier | string, categorical
No. ordered | number of ordered items | numerical
uncertain | assessment of `No. ordered` column| binary
Weapon designation| weapon types | string, unstructured
Weapon description| classification of weapons | string, categorical
Year of order | year or timespan of order| numerical
uncertain| assessment of `Year of order` column| binary
Year of delivery| year or timespan of delivery, dataset filtered to include orders delivered between 2000 and 2019 | numerical
No. delivered| number of delivered items | numerical 
uncertain| assessment of `No. delivered` column | binary
Comments | comments made by SIPRI researchers | string, unstructured


The chart is based on the number of orders for different weapon types, rather than the number of items ordered. Thus, the ranking was created by condensing the table with a pivot table on column `Weapon description` rather than on column `No. ordered`. With either approach, the picture does not change radically and about the same weapons rank among the top10, just in a slightly different order. 

Since less valuable items such as firearms can naturally be ordered in a much higher quantity than more expensive items like helicopters for example, we decided to settle on the number of orders for particular weapon systems instead, to reflect what items are often bought from Russian suppliers.

![](/charts/167_en_weaponsystems.png)




