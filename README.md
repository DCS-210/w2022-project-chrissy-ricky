Covid-19 & Making Predictions
================
Chrissy Aman & Ricky Sun

## Summary

#### \[Motivation & current literature\]

Up until April 11, there are over 497,057,239 infections and 6,179,104
deaths since the beginning of the pandemic. Covid-19, or corona virus,
has been impacting the world for over two years from all dimensions.
Researchers have also appoached Covid-19 from all angles, and many of
them seek to use currently available data to predict future trends.

Current research has already explored a wide variety of predictors for
Covid-19 severity, infections, and deaths. Those research also evaluated
potential impacts of the pandemic (such as economy and job market).
Social media (such as Google search, Twitter twits), weather data (such
as temperature, humidity), economic related data (such as GDP, interest
rate), general health information (such as share of people aged over 70,
share of smokers) are all factors that have been studied in current
literature.

#### \[Our research question and data\]

In our research, we used data from “Our World in Data” Covid-19 public
dataset, which includes data ranging from Covid-19 infections, gdp per
capital, to vaccinations. Our project focus mainly on vaccintaions and
death rate of Covid-19, but we also included many other variables and
explored using multiple statistical tools.

#### \[Methods\]

We first did some preliminary analyses, such as maps, heat maps of
correlations, scatter plots using death rate of Covid-19, vaccination
rate and some other variables of our interest, such as Human Development
Index (HDI), share of smokers, and so on.

We then move on to some regression analyses, starting from linear
models. We first only include vaccination rate as x and death rate as y,
and used data at more recent date at “2022-2-20”, which was the time
that Omicron is the major variant virus in the world. Then, we include
more variables in our model. We also included the same model but using a
date during which Delta was the dominant variant (“2021-09-30”).

Because of the nature of panel data, the simple linear regressions
selecting a specific day, the models may not be sufficient in making
predictions. Also, when considering the time span from 2020 to 2022, the
virus has mutated from alpha, Delta, to currently Omicron, and
vaccinations have also been developed from first, second to booster
doses. The simple linear regression may not be able to compromise those
factors. Thus, we continued our analyses with more advanced
manipulations.

Thus, We included regression discontinuity design and fixed effect model
to further study the relationship between vaccination rate and death
rate of Covid-19. We included ARiMA model and KNN machine learning model
to predict total cases and death rates.

#### \[Results\]

According to our models, we found that: 1. Linear model: vaccination can
negatively predict Covid-19 death 2. Linear model: stringency index (how
strict a country’s policy is on Covid-19) can negatively predict
Covid-19 death rate at a before Omicron date, but is positively
predicting Covid-19 death rate at a Omicron date 3. Fixed effect: there
is a clear negative correlation between vaccination rate and
hospitalizations 4. RDD: the slope for regression of vaccination rate
and Covid-19 death rate is positive until reaching the threshold of 50%
and the slope turns negative after the 50% threshold 5. ARiMA: our ARiMA
model gives a good forecast of future new cases 6. KNN: our KNN machine
learning model categorize country into good and bad of coping with
Covid-19 death rate with around 71% accuracy

There are many smaller findings, which are included in the presentation
and rmd file.

#### \[Limitations\]

1.  Since we are using the global level by country data, the predictions
    and model accuracy may not be high if we want to predict local level
    Covid-19 cases or deaths
2.  We did not take policies into considerations, which is an important
    factor
3.  We have touched on Covid-19 variants, but our data does not actually
    distinguish between different infections
4.  Some of the data might need to be normalized or taken natural log to
    better deal with the screwness of the data

#### \[Potential future studies\]

1.  Use of county level data or more detailed datasets of certain
    country or region
2.  Compare effectiveness of different vaccines (Pfizer, Moderna,
    Sinovax, and so on)
3.  US and China can be a good natural experiment pair to compare with
    in terms of policies and Covid-19 data
4.  Use of social media data through machine learning models to make
    predictions

## Presentation

Our presentation can be found [here](presentation/presentation.html).

## Data

Our dataset is coming from “Our World in Data” Covid-19 public data,
together with data from JHU, WHO, CDC and World Bank. The data covers a
wide range:

-   Basic Covid-19 data (cases, deaths)
-   Hospital & ICU (ICU beds, ICU patients)
-   Policy responses (stringency_index)
-   Reproduction rate
-   Tests & positivity
-   Vaccinations
-   Others (populations, life_expectancy, GDP per catpita and so on)

Hannah Ritchie, Edouard Mathieu, Lucas Rodés-Guirao, Cameron Appel,
Charlie Giattino, Esteban Ortiz-Ospina, Joe Hasell, Bobbie Macdonald,
Diana Beltekian and Max Roser (2020) - “Coronavirus Pandemic
(COVID-19)”. Published online at OurWorldInData.org. viewed 25 February
2022, Retrieved from: ‘<https://ourworldindata.org/coronavirus>’
\[Online Resource\]

@article{owidcoronavirus, author = {Hannah Ritchie, Edouard Mathieu,
Lucas Rodés-Guirao, Cameron Appel, Charlie Giattino, Esteban
Ortiz-Ospina, Joe Hasell, Bobbie Macdonald, Diana Beltekian and Max
Roser}, title = {Coronavirus Pandemic (COVID-19)}, journal = {Our World
in Data}, year = {2020}, note =
{<https://ourworldindata.org/coronavirus>} }

## References

\[1\] Aboubakri, O., Ballester, J., Shoraka, H. R., Karamoozian, A., &
Golchini, E. (2022). Ambient temperature and covid-19 transmission: An
evidence from a region of Iran based on weather station and satellite
data. Environmental Research, 209, 112887.
<https://doi.org/10.1016/j.envres.2022.112887>

\[2\]Azuma, K., Kagi, N., Kim, H., & Hayashi, M. (2020). Impact of
climate and ambient air pollution on the epidemic growth during COVID-19
outbreak in Japan. Environmental Research, 190, 110042.
<https://doi.org/10.1016/j.envres.2020.110042>

\[3\] Chew, A. W., Pan, Y., Wang, Y., & Zhang, L. (2021). Hybrid deep
learning of social media big data for predicting the evolution of
COVID-19 transmission. Knowledge-Based Systems, 233, 107417.
<https://doi.org/10.1016/j.knosys.2021.107417>

\[4\] Chiodini, I., Gatti, D., Soranna, D., Merlotti, D., Mingiano, C.,
Fassio, A., Adami, G., Falchetti, A., Eller-Vainicher, C., Rossini, M.,
Persani, L., Zambon, A., & Gennari, L. (2021). Vitamin D status and
SARS-COV-2 infection and COVID-19 clinical outcomes. Frontiers in Public
Health, 9. <https://doi.org/10.3389/fpubh.2021.736665>

\[5\] Fernández-González, R., Pérez-Pérez, M., Hervés-Estévez, J., &
Garza-Gil, M. D. (2022). Socio-economic impact of covid-19 on the
fishing sector: A case study of a region highly dependent on fishing in
Spain. Ocean & Coastal Management, 221, 106131.
<https://doi.org/10.1016/j.ocecoaman.2022.106131>

\[6\] Fritz, C., Dorigatti, E., & Rügamer, D. (2022). Combining graph
neural networks and spatio-temporal disease models to improve the
prediction of weekly COVID-19 cases in Germany. Scientific
reports, 12(1), 3930. <https://doi.org/10.1038/s41598-022-07757-5>

\[7\] Hannah Ritchie, Edouard Mathieu, Lucas Rodés-Guirao, Cameron
Appel, Charlie Giattino, Esteban Ortiz-Ospina, Joe Hasell, Bobbie
Macdonald, Diana Beltekian and Max Roser (2020) - “Coronavirus Pandemic
(COVID-19)”. Published online at OurWorldInData.org. viewed 25 February
2022, Retrieved from: ‘<https://ourworldindata.org/coronavirus>’
\[Online Resource\]

\[8\] Hou, Z., Du, F., Jiang, H., Zhou, X., & Lin, L. (2020). Assessment
of public attention, risk perception, emotional and behavioural
responses to the COVID-19 outbreak: Social media surveillance in China.
<https://doi.org/10.1101/2020.03.14.20035956>

\[9\] Khan, A. R., Abedin, S., & Khan, S. (2022). Interaction of
temperature and relative humidity for growth of COVID-19 cases and death
rates. Environmental Research Letters, 17(3), 034048.
<https://doi.org/10.1088/1748-9326/ac4cf2>

\[10\] Izcovich, A., Ragusa, M. A., Tortosa, F., Lavena Marzio, M. A.,
Agnoletti, C., Bengolea, A., Ceirano, A., Espinosa, F., Saavedra, E.,
Sanguine, V., Tassara, A., Cid, C., Catalano, H. N., Agarwal, A.,
Foroutan, F., & Rada, G. (2020). Prognostic factors for severity and
mortality in patients infected with COVID-19: A systematic review. PloS
one, 15(11), e0241955. <https://doi.org/10.1371/journal.pone.0241955>

\[11\] Lee, C.-K., Jung, E.-K., Kang, S.-E., Petrick, J. F., & Park,
Y.-N. (2022). Impact of perception of covid-19 on NPI, job satisfaction,
and customer orientation: Highlighting three types of npis for the
airline industry. Journal of Air Transport Management, 100, 102191.
<https://doi.org/10.1016/j.jairtraman.2022.102191>

\[12\] Li, J., He, X., Yuan Yuan, Zhang, W., Li, X., Zhang, Y., Li, S.,
Guan, C., Gao, Z., & Dong, G. (2021). Meta-analysis investigating the
relationship between clinical features, outcomes, and severity of severe
acute respiratory syndrome coronavirus 2 (SARS-CoV-2)
pneumonia. American journal of infection control, 49(1), 82–89.
<https://doi.org/10.1016/j.ajic.2020.06.008>

\[13\] Mudatsir, M., Fajar, J. K., Wulandari, L., Soegiarto, G.,
Ilmawan, M., Purnamasari, Y., Mahdi, B. A., Jayanto, G. D., Suhendra,
S., Setianingsih, Y. A., Hamdani, R., Suseno, D. A., Agustina, K., Naim,
H. Y., Muchlas, M., Alluza, H. H., Rosida, N. A., Mayasari, M., Mustofa,
M., … Harapan, H. (2021). Predictors of COVID-19 severity: A systematic
review and meta-analysis. F1000Research, 9, 1107.
<https://doi.org/10.12688/f1000research.26186.2>

\[14\] Muhammad, L.J., Algehyne, E.A., Usman, S.S. et al. Supervised
Machine Learning Models for Prediction of COVID-19 Infection using
Epidemiology Dataset. SN COMPUT. SCI. 2, 11 (2021).
<https://doi.org/10.1007/s42979-020-00394-7>

\[15\] Qin, Lei, Qiang Sun, Yidan Wang, Ke-Fei Wu, Mingchih Chen,
Ben-Chang Shia, and Szu-Yuan Wu. 2020. “Prediction of Number of Cases of
2019 Novel Coronavirus (COVID-19) Using Social Media Search
Index” International Journal of Environmental Research and Public
Health 17, no. 7: 2365. <https://doi.org/10.3390/ijerph17072365>

\[16\] Ray, R. L., Singh, V. P., Singh, S. K., Acharya, B. S., & He, Y.
(2022). What is the impact of COVID-19 pandemic on global carbon
emissions? Science of The Total Environment, 816, 151503.
<https://doi.org/10.1016/j.scitotenv.2021.151503>

\[17\] Xu, L., Magar, R., & Barati Farimani, A. (2022). Forecasting
covid-19 new cases using Deep Learning Methods. Computers in Biology and
Medicine, 144, 105342.
<https://doi.org/10.1016/j.compbiomed.2022.105342>

\[18\] Yousefinaghani, S., Dara, R., Mubareka, S., & Sharif, S. (2021).
Prediction of covid-19 waves using social media and google search: A
case study of the US and Canada. Frontiers in Public Health, 9.
<https://doi.org/10.3389/fpubh.2021.656635>

\[19\] Zoabi, Y., Deri-Rozov, S. & Shomron, N. Machine learning-based
prediction of COVID-19 diagnosis based on symptoms. npj Digit. Med. 4, 3
(2021). <https://doi.org/10.1038/s41746-020-00372-6>
