# Giant oil and gas field discoveries
## An extended version of Horn’s giant oil and gas field discoveries dataset for economic analysis

### James Cust, David Mihalyi and Alexis Rivera-Ballesteros

<br />
<br />
<br />


[Home](#giant-oil-and-gas-field-discoveries) | 
[Codebook](#variables) | 
[NPV calculation](#npv-calculation) | 
[Summary](#summary) | 
[Bibliography](#bibliography)


![image](https://i.imgur.com/BDCqADC.gif)

# Download data here: [giant_fields_2018.csv](https://github.com/alexis-ribal/giant-oil-and-gas-field-discoveries/blob/master/giant_fields_2018.csv)

<br />
<br />

## SCOPE

*Years included*: the dataset contains giant fields that where discovered between 1868 and 2018, however, the net present value for all giant field discoveries is available only after 1950 and their share to GDP only after 1960.  It is expected that more giant fields will be discovered during the publication of this dataset, therefore observations after 2018 will be added in future updated versions of the dataset.

*Discovery size*: Giant oil and gas field discoveries are defined as those with estimated ultimate recovery (EUR) reserves greater or equal than 500 MMBOE.  At the same time, all giant field discoveries are split into three sub-categories:
	Giant – EUR are between 500 and 4,999 MMBOE
	Supergiant – EUR are between 5,000 and 49,999 MMBOE
	Megagiant – EUR are more than 50,000 MMBOE

## UPDATES

We have updated the year of the discovery for 22 observations in the dataset published originally by Horn (2014).   For these 22 observations we could not find a public source supporting that the giant field was discovered during the recorded year, but found public sources indicating a different year.  We updated the year of the discovery according to the public source and inserted the link to the website containing this information in the [DISCO_SOURCE1] field.  These 22 observations can be identified with the legend “Horn updated” in the [DISCO_SOURCE2] field.

This dataset contains giant field discoveries from 1868 to 2018, however, more observations after 2018 could be added in future updates.  This current version includes 3 giant oil and gas field discovered in 2019.

## SOURCING AND DISCLAIMER

All the data verted in this dataset comes from public datasets, oil and gas company websites, press release news, news articles, industry magazines, specialized blogs and research papers.  All the sources used to build this dataset are inserted as web links below the DISCO_SOURCE1, DISCO_SOURCE2, DISCO_SOURCE3 and DISCO_SOURCE4 columns.  Since all these web links are hosted by third parties, we are not responsible for their content, availability, free access or performance.  Some of these websites might be already deleted, moved, updated or reported as unsafe.  If this is the case, we suggest looking for alternative sources of data using a standard internet browser and the same giant field discovery data as keywords.

## VARIABLES

**FIELD_ID**

A field ID with no specific sorting method used.


**FLD_NAME**

The name that is commonly used to refer to this field and that frequently appears in different sources used.  This field name could have changed over time or it could vary from one source to another.


**FLD_NAME2**

The block name where the field was discovered or a second name also used to refer to this field but differ from the recorded under [FLD_NAME].


**REG_NAME and REG_CODE**

Region name and region code used in Horn (2014).  The region names and their one-letter codes are: North America-A, Central and South America-B, Western Europe-C, Eastern Europe and former USSR-D, Middle East-E, Africa-F, Asia and Oceania-G. Source: Horn (2014).

**WB_REGION**

World Bank country groups by geographical region identified with their 3-letter codes.  The regions definition and their codes are: EAP – East Asia & the Pacific, ECA – East Europe & Central Asia, LAC – Latin America & the Caribbean, MNA – Middle East & North Africa, SAR – South Asia and SSA – Sub-Saharan Africa.  Source: World Bank: https://datahelpdesk.worldbank.org/knowledgebase/articles/906519-world-bank-country-and-lending-groups


**COUNTRY**

Country common name.  Joint discoveries made by two or more countries have the names of the countries involved.  The dataset has in total 78 countries with at least one giant oil or gas field discovered.


**CountrynameWEO - weo_code**

Country name and 3-digit code defined in the World Economic Outlook (WEO) report.  Missing values correspond to joint discoveries between two or more countries.  Source: IMF: https://www.imf.org/external/pubs/ft/weo/2019/02/weodata/index.aspx 


**ISO**

ISO-3 letter country code.  Missing values correspond to joint discoveries. Source: UN: https://unstats.un.org/unsd/tradekb/Knowledgebase/Country-Code 


**STATE**

Name of the state where the field was discovered.  For USA, Canada and Mexico only, when available.


**LAT_DD and LON_DD**

Latitude and longitude in decimal degrees of the location where the field was discovered.  Location coordinates are approximated, and the location accuracy may vary across fields and could be greater than one degree.


**ON_OFF_LOC**

Field location.  Indicates whether the field is located onshore or offshore.


**year**

Year of the discovery. Year recorded from Horn (2014) or from other sources as indicated in the DISCO_SOURCE1 – DISCO_SOURCE4 columns.


**FIELD_TYPE**

Principal type of hydrocarbon discovered in the field that reaches the threshold of giant field discovery.  Most of giant discoveries where oil fields (58.2%), followed by gas (41.6%) and 2 discoveries where both giant oil and gas resources were combined (0.2%).  


**SIZE_CLASS**

Classification according to the size of the discovery in million barrels of oil equivalent (MMBOE): Giant (greater than 500 MMBOE but lower than 5,000 MMBOE), Supergiant (greater than 5,000 MMBOE but lower than 50,000 MMBOE) and Megagiant (greater than 50,000 MMBOE).  These values where recorded from the sources listed in the DISCO_SOURCE1 – DISCO_SOURCE4 columns.


**SIZE_CLASS_CODE**

One-digit code indicating whether the observation corresponds to a Giant (1), Supergiant (2) or Megagiant (3) field discovery.


**EUR_MMBOE**

Estimated ultimate recovery (EUR) measured in million barrels of oil equivalent (MMBOE).  The estimated ultimate recovery is defined as the sum of proven reserves at a specific period of time and the cumulative production up to that time (Morehouse, 2017).  We use the EUR reported from the sources listed in DISCO_SOURCE1 – DISCO_SOURCE4 columns.  Most sources report the amount of oil discovered in barrels of oil equivalent, no further calculations were used to report EUR for giant oil field discoveries.  However, if the amount of oil discovered were reported in metric tons, we used the conversion ratio of 7.33 MMBOE to 1 million metric tons.  Gas field EUR discoveries are typically reported in trillion cubic feet of natural gas (TCF) and these where converted to MMBOE using the conversion ratio of 200 MMBOE to 1 TCF, based on four oil and gas companies’ reports and conversion tables, rounded to the nearest hundred .  The lowest EUR value for all these discoveries is 500 MMBOE and the highest is 176,060 MMBOE corresponding to a field discovered in 1971 in Qatar.


**oil_price**

Crude oil prices in dollars per barrel from 1950 to 2018.  These prices are calculated as the average of the three oil reference prices equally weighted in nominal US dollars.  Years of data availability and sources are indicated in parenthesis:
1.	Brent crude oil (1979-2018, World Bank)
2.	Arabian light (1950-1959, Quandl) and Dubai Fateh crude oil (1960-2018, World Bank)
3.	WTI spot crude oil (1950-1981, Federal Reserve Bank of St Louis) and WTI crude oil (1982-2018, World Bank)


**gas_price**

Gas prices in nominal US dollars per barrel of oil equivalent from 1950 to 2018. These prices were calculated as the average of US and Europe’s natural gas prices from the US Energy Information Administration (EIA) and World Bank’s Commodity Markets portal measured in dollars per million British thermal units (US$/mmbtu).  These values were converted to dollars per barrel (US$/bbl) using the conversion ratio of 0.17 barrels of oil to 1 million British thermal units, based on four oil and gas companies’ reports and conversion tables, rounded to the two decimal places . Years of data availability and sources are indicated in the parenthesis.
1.	US natural gas price (1950-1959, EIA; and 1959-2018, World Bank)
2.	European Union’s natural gas price (1960-2018,   World Bank)

For the Europe’s natural gas price, please consider that the calculations of prices have changed for some years: from April 2015 it uses the Netherlands Title Transfer Facility (TTF); from April 2010 to March 2015 it is calculated with the average import border price and a spot price component, including UK; and during June 2000 - March 2010 prices excludes UK.  


**firstdiscoyear**

Year when the first oil or gas giant field was discovered in a country since 1868.


**disco_cumu**

Cumulative count of giant oil or gas fields discovered in a country since 1868 at the time of each giant oil or gas field discovery.


**disco_count**

Total count of giant fields discovered in a country between 1868 and 2018.  If the country had giant discoveries in 2019, these were also considered.


**EUR_cumu**

Cumulative estimated ultimate recovery (EUR) resources in million barrels of oil equivalent (MMBOE) from giant oil and gas fields discovered by country since 1868.

**NPV_USD_n**
Net present value in nominal million US dollars calculated as the product of multiplying the net present value of the estimated ultimate recovery (EUR) measured in million barrels of oil equivalent (MMBOE) by oil or gas prices, depending on the field type.  The net present value or NPV is defined as today’s value of future cashflows over a period of time and using a certain discount rate.  


**defl_uscpi**

Deflator used to convert nominal net present value to real net present value, corresponding to the US price level of household consumption deflator in 2011 dollars from 1950 to 2017 from the Penn World Table version 9.1. Source: https://www.rug.nl/ggdc/productivity/pwt/


**NPV_USD_r**

Net present value in real million 2011 US dollars calculated by dividing the nominal net present value [NPV_USD] by the deflator [defl_uscpi].


**gdp_curr**

Current gross domestic product in million US dollars. Source: World Bank, https://data.worldbank.org/indicator/NY.GDP.MKTP.CD 


**gdp_const**

Gross domestic product in million constant 2010 US dollars. Source: World Bank, https://data.worldbank.org/indicator/NY.GDP.MKTP.KD 


**NPV_GDP_n**

Field discovery nominal net present value share of current GDP at the year of the oil or gas field discovery, calculated as [NPV_USD_n]/[gdp_curr] x 100.  Values are available from 1960 to 2017.


**NPV_GDP_r**

Field discovery real net present value (2011 US dollars) share of constant GDP (2010 US dollars) at the year of the discovery, calculated as [NPV_USD_r]/[gdp_const] x 100   Values are available from 1960 to 2017.


**DISCO_SOURCE1, DISCO_SOURCE2, DISCO_SOURCE3, DISCO_SOURCE4**

Website link to the article, press release, blog or any other public access website with relevant information related to the giant field discovery and used to complete the discovered field data.  The website links provide data on year of the discovery, size of the field, EUR discovered, location of the field and type of resource.  All sources used were included up to a total of four sources.  Disclaimer: since all these websites are hosted by third parties, we are not responsible for their content, availability, free access or performance.  Some of these websites might be already deleted, moved, updated or reported as unsafe.  If this is the case, we suggest looking for alternative sources of data using a standard internet browser and the same giant field discovery data as keywords.


## NPV CALCULATION

To compute the net present value [NPV_USD_n] of giant oil and gas field discoveries we follow Arezki et al (2016) method that uses the estimated ultimate recovery reserves [EUR_MMBOE] at the time of the discovery and a production profile that stops when the remaining reserves (RRR) drop to <1.  Since production startup dates are unknown in the dataset, we follow Arezki’s et al (2016) estimation of four-to-six delay from the year of the discovery to the startup date.  Continuing with Arezki’s et al (2016) calculation, we use an approximation of the production profile of a giant discovery and derive it using a field size dependent plateau production level q_p that is field size dependent and a maximum depletion rate of remaining reserves d_m.  

The depletion rate of remaining reserves at time t is defined as:

d(t)=q(t)/RRR(t) ,

where q(t) is annual production rate and RRR(t) = EUR_MMBOE - Q(t), where RRR(t) are remaining reserves and Q(t) cumulative production.

We use the parameter estimates for plateau production (α, β) and maximum depletion rate (γ, δ) approximation functions for all pooled giant fields, where α= 0.57, β= 0.65, γ= 0.64 and δ= -0.31 (Arezki et al 2017).

The relationship between field size and plateau production q_pis defined as
q_p=  α  〖[EUR_MMBOE]〗^β

and the relationship between field size and the depletion rate d_m as:

d_m= γ 〖[EUR_MMBOE]〗^δ

The duration of the production plateau will be defined by:

N =([EUR_MMBOE])/q_p   –1/d_m 

Therefore, the duration of the plateau production will depend on the size of the discovery indicated by the [EUR_MMBOE] variable.

Then, we calculate the net present value of the field's production measured in barrels assuming a discount rate of 10% and time determined by the size of the field discovered until remaining reserves are lower than 1 in the exhaustion year:

〖NPV〗_(i,t)= ∑_(t=1)^n▒q(t)/(1+r)^t ,
as long as RRR < 1.

Finally, we multiply the net present value measured in million barrels by nominal oil or gas prices, depending on the type of the field to calculate nominal net present values in million US dollars [NPV_USD_n].  Then, we divide these nominal net present values by the deflator [defla_uscpi] from the Penn World Table version 9.1 to obtain real net present values in million 2011 US dollars [NPV_USD_r]. 


## SUMMARY

Giant oil and gas discoveries have an important impact on the economy. As highlighted by Arezki et al (2017), Smith (2015), Cust and Mihalyi (2017), Harding et al (2016), Mansoorian (1991), Toews and Vezina (2016) and Van der Ploeg (2011) research these discoveries impact on economic growth, investment, debt, exchange rate, etc. These giant discoveries are also unanticipated, as such they provide ideal testing ground to economic researchers to empirically test for causal relationship between change in natural resource wealth and economic outcomes.

In order to support the growing research in this area, we have updated and extended the dataset on giant oil discoveries previously published by Horn (2014) under the auspice of the American Association of Petroleum Geologists (AAPG) that contains discoveries from 1868 to 2010 .

This updated version of the dataset has a multifold contribution for economic analysis: it incorporates recent discoveries from 2010 and up to 2018, updates the year of the discovery for 22 observations in Horn’s dataset based on public sources, adds 7 giant oil and gas field discoveries not included in Horn (2014), provides the net present value (NPV) in million US dollars for all discoveries between 1950 and 2017 and the corresponding share of the country’s gross domestic product (GDP) where the giant field was discovered.  

All the new data poured into this dataset comes from public sources and each observation comes with one link or more to the source supporting or amplifying the information for each one of them.  Discovered fields’ sizes are determined by their estimated ultimate recovery (EUR) resources measured in million barrels of oil equivalent (MMBOE). Net present value (NPV) are calculated as the product of multiplying the EUR by oil and gas prices in US dollars per barrel and then divided by the country’s GDP to get its share to the total economy, both in nominal and real terms.  

The dataset comprises a total of 1,060 giant oil and gas field discoveries in 78 countries across seven different regions.  Europe & Central Asia (ECA) and the Middle East & North Africa (MNA) have the highest count of giant oil and gas field discoveries.  These regions are followed by the US and Canada (NAC), East Asia & the Pacific (EAP), Latin America & the Caribbean (LAC), Sub-Saharan Africa (SSA) and South East Asia (SAR).

|_Region_|_Giant discoveries_|_% of total_|
|--------|-------------------|------------|
| ECA	 | 285               |	26.89     |
| MNA	 | 285               |	26.89     |
| NAC    |	142          |	13.4      |
| EAP    |	119          |	11.23     |
| LAC    |	118	     |  11.13     |
| SSA	 |  95	             |   8.96     |
| SAR	 |16                 |	 1.51     |
##### Figure 1. Number of giant oil and gas discoveries by region and share of total. Source: Cust et al (2019)

Map 1 shows the concentration of giant oil and gas field discoveries.  In the Middle East & North Africa region, Libya and countries around the Persian Gulf had discovered more giant oil and gas fields than any other countries in that region.  In Sub-Saharan Africa, Nigeria concentrates the largest number of giant oil and gas field discoveries of that region, while in Latin America, no other country had discovered more giant oil and gas fields than Venezuela, Brazil and Mexico.  The countries that have discovered more than 100 giant oil and gas fields are Russia with 158 and the US with 116.  After them, the countries with more giant oil and gas field discoveries are Iran (70), Saudi Arabia (59) and China (38).  Countries in white represent those that haven’t found any giant oil and gas field, countries that are typically landlocked.

![image](https://i.imgur.com/NJX7xsO.png)
##### Map 1. Count of giant discoveries by country.

In terms of the cumulative estimated ultimate recovery (EUR) resources measured in million barrels of oil equivalent (MMBOE) from all giant oil and gas field discoveries by country, Russia leads the list with more than 460 billion barrels of oil equivalent since 1868.  The US (159 billions), which is the country with the second highest count of giant oil and gas field discoveries, drops to the sixth place since its giant discoveries were relatively smaller.  The countries that lead the list after Russia are Saudi Arabia (372 billions), Iran (352 billions), Qatar (204 billions) and Iraq (167 billions).  Map 2 shows the distribution of these resources measured in EUR in all the world. The five countries mentioned above plus the US account for more than 60% of all the EUR from oil and gas fields discovered between 1868 and 2019.

![image](https://i.imgur.com/oYRhyCZ.png)
##### Map 2. Cumulative EUR from giant oil and gas field discoveries by country (1868-2019)

In this dataset there are 101 giant oil and gas field discoveries that exceed the 50 billion barrels of oil equivalent, also known as supergiant discoveries (MMBOE > 5,000) or megagiant discoveries (MMBOE > 50,000).  Almost half of them were discovered in the Middle East & North Africa, while one fourth of them were discovered in Europe & Central Asia and the other fourth in the rest of the world.  The first giant oil and gas fields that exceeded the 5 billion barrels of oil equivalent were discovered in Venezuela (Lagunillas) and in Oklahoma, United States (Hugoton), both in 1926.  All megagiant oil and gas fields (exceeding 50 billion barrels of oil equivalent, above the red line on figure 2) were discovered in the Middle East & North Africa plus one more in Russia.  In the past few decades, the number of giant oil and gas fields in Middle Eastern and North African countries has been less frequent (see Figure 5).

![image](https://i.imgur.com/766V7d4.png)
##### Map 3. Cumulative real NPV from giant oil and gas field discoveries by country in million US$ (1868-2019)

Almost half of the super and megagiant oil and gas fields were discovered between 1960 and 1980.  Since the 1990s, the number of super and megagiant discoveries have been fewer, especially in the last decade when there were only four giant oil and gas discoveries.

![image](https://i.imgur.com/V1ibUit.png)
##### Figure 2. Super and megagiant oil and gas field discoveries. The red line indicates the threshold for megagiant oil and gas field discoveries (above 50 billion barrels of oil equivalent).  Source: Cust et al (2019).

In this dataset, there are 617 giant oil field discoveries, 441 giant gas field discoveries and 2 discoveries where both giant oil and gas resources were combined.  The regions with the largest number of discoveries where the Middle East & North Africa and Europe & Central Asia.  The region with the lowest number of discoveries is South East Asia.  On the other hand, East Asia & Pacific and Europe & Central Asia had more gas than oil giant field discoveries, but there were more oil giant field discoveries in the rest of the regions (see Figure 3). 

![image](https://i.imgur.com/UUG6RC6.png)
##### Figure 3. Cumulative oil and gas giant field discoveries by region.  Calculated as the count of giant field discoveries by type and by region.  Source: Cust et al (2019).

There were some cases when the real NPV from the giant oil and gas discoveries exceeded the country’s constant GDP of that year.  This happened in Sub-Saharan African and Middle Eastern countries.  However, the most recent Guyanan giant discovery represented a real NPV greater than the country’s GDP.  For many Middle Eastern and Sub-Saharan African countries, real NPV from giant oil and gas field discoveries are an important share of their GDP, however, for the US and Canada, these giant discoveries are a much smaller proportion.  In these two countries giant oil and gas field discoveries mean less than 1% of their GDP (see Figure 4).

![image](https://i.imgur.com/fiyhp7i.png)
##### Figure 4. Real NPV as percent of constant 2010 GDP vs constant 2010 GDP in billion US dollars, between 1960 and 2017, when GDP data and deflator data are available.  Source: Cust et al (2019).

The NPV of these giant discoveries has changed over the time.  Each region experienced a boom in different periods.  While Middle East & North Africa had a giant oil and gas boom during the 1960s and the 1970s, Latin America & the Caribbean had its giant oil and gas field discoveries boom during the 2000s, due to the supergiant oil discoveries in Brazil and Trinidad and Tobago.  Also, during the last two decades, Sub-Saharan Africa had an important increase of the real NPV from giant oil and gas field discoveries, just behind Latin America (see Figure 5).

![image](https://i.imgur.com/aA9xmbo.png)
##### Figure 5. Cumulative real NPV from giant oil and gas discoveries by decade and region in billion US dollars.  Calculated as the sum of real NPV of all countries in a region for a period of 10 years. Source: Cust et al (2019)

If we take the real NPV as percent of constant 2010 GDP average by country, we see that these giant oil and gas discoveries have different meanings to the countries.  While the NPV from giant oil and gas discoveries means a very small portion of the US and Canada GDP, it claims more importance for Sub-Saharan African countries, especially during the 1980s and 2000s when the real NPV from them represented in average 50% of Sub-Saharan African countries’ GDP.  Latin America & the Caribbean’s NPV from giant oil and gas discoveries show a larger share of GDP due to the most recent giant discoveries in Trinidad and Tobago and Guyana.  The importance of these giant oil discoveries or the frequency of them has been declining in other regions.  For instance, Middle Eastern countries’ real NPV average from these discoveries has declined to less than 1% in this decade (see Figure 6).


![image](https://i.imgur.com/PbiIW0E.png)
##### Figure 6. Average real NPV as percent of constant 2010 GDP, calculated as the decade average for all countries in each region, converted to log values. Source: Cust et al (2019)



## Bibliography

Arezki, R., V. A. Ramey, and L. Sheng (2016). News shocks in open economies: Evidence from giant oil discoveries. The Quarterly Journal of Economics, qjw030.

Cust, J. and D. Mihalyi (2017).  Evidence for a presource curse? Oil discoveries, elevated expectations, and growth disappointments. Policy Research Working Paper, 8140.

Harding, T., R. R. Stefanski, and G. Toews (2016). Boom goes the price: Giant resource discoveries and real exchange rate appreciation.

Horn, M.K. (2014). Giant oil and gas fields of the world. American Association of Petroleum Geologists. Tulsa, Oklahoma.
http://www.datapages.com/AssociatedWebsites/GISOpenFiles/HornGiantFields.aspx 

Mansoorian, A. (1991). Resource discoveries and excessive external borrowing. The Economic Journal 101 (409), 1497–1509.

Morehouse, David F. (July 1997). The Intricate Puzzle of Oil & Gas "Reserve Growth". Natural Gas Monthly. Energy Information Administration.

Smith, B. (2015). The resource curse exorcised: Evidence from a panel of countries. Journal of Development Economics 116, 57–73.

Toews, G., P.-L. Vezina, et al. (2016). Resource discoveries and fdi bonanzas. Technical report, Oxford Centre for the Analysis of Resource Rich Economies, University of Oxford.

Van der Ploeg, F. (2011). Natural resources: Curse or blessing? Journal of Economic Literature 49 (2), 366–420.







