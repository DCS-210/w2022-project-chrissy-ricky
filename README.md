Covid-19 & Data Science
================
Chrissy & Ricky

## Summary

COVID-19, also known as Coronavirus disease 2019 is a contagious disease
caused by a virus, the severe acute respiratory syndrome coronavirus 2
(SARS-CoV-2). Up until April 11, there are over 497,057,239 infections
and 6,179,104 deaths since the beginning of the pandemic. Although no
one could have predicted a pandemic like Covid-19, with the help of
data, we might be able to use current data to, for example, evaluate
risks and predict future trends, so that the virus and mutations can be
better managed or even contained in earlier stages.

Current research has already explored a wide variety of predictors for
Covid-19 severity and infections, and evaluated potential impacts of the
pandemic. Social media, weather data, economic related data, general
health information are all factors that have been studied in current
literature.

In our research, we are trying to use Covid-19 related data, together
with other relevant data to take a brief look of the global Covid-19
situation, explore potential predictors and models for Covid-19 cases,
deaths, and evaluate the effects of vaccines. Factors like population of
elder people, stringency index (how strict the policy is around the
Covid-19), population density, and so on, which is, to some degree, a
summary of previous research, with some new elements.

According to the summary statistics, we found that those more developed
countries, such as Norway, France, United States, have more Covid-19
infections but lower death rate. This could be due to the following
reasons: 1. more developed countries have better testing and recording
methods. Many developing countries have encountered similar surge of
cases in earlier stages, but they may not be able to reflect that
through data, because of their testing constraint. 2. People from more
developed countries embrace more of the “free will”, so many people may
not be willing to wear masks and implement those protocols recommended
by CDC or WHO. Ther bette medical resources and technologies also make
people think of Covid-19 just another “flu” during earlier stages. 3.
With considerations of economies, developed countries may not be willing
to lockdown the whole country for an extended period of time.

Of course, more developed countries also have much higher rate of
vaccination rate, which is the potential reason for lower death rate.

We also included multiple maps to better visualize the global
discrepancies in Covid-19 cases, death, HDI, and so on.

According to the heat map, it is interesting to see that, smoking is
correlated with Covid-19 deaths, but it is a little bit
counter-intuitive that population density is negatively correlated with
Covid-19 cases.

The simple linear regressions also show that the the vaccination rate
can negatively predict the Covid-19 deaths.

Because of the nature of panel data, the simple linear regressions
selecting a specific day, the models may not be sufficient in making
predictions. Also, when considering the time span from 2020 to 2022, the
virus has mutated from alpha, Delta, to currently Omicron, and
vaccinations have also been developed from first, second to booster
doses. The simple linear regression may not be able to compromise those
factors. Thus, we continued our analyses with more advanced
manipulations.

The fixed effect regression model uses a fixed effect to control for
differences in-country to isolate the effect of vaccination rate on
covid hospitalizations. The beta1 coefficient, the coefficient for
vaccination rate was -0.39604 meaning a one-unit change in the number of
fully vaccinated people per hundred would result in .26733 fewer
hospitalizations per week per million. The t statistic is statistically
significant at -5.138. The graph below and the regression were performed
on a limited data set of countries that used similar vaccines and
limited for purposes of r-studio not crashing every time the regression
runs. This visualization shows the effect of vaccination on
hospitalization when controlled for differences between countries. The
red line signifies the average. There is a clear negative correlation
between vaccination rate and hospitalizations which makes sense.

The two maps show covid cases by country early in the pandemic. The
first graph shows cases on a day in March when the pandemic was just
beginning and then two months later in May when the pandemic was
spreading more. A country that sticks out is the United States which
took a more reserved approach to the lockdowns compared to other
countries, especially when compared to China which started out as a
country with a lot of cases relatively but in the two months, time was
able to lower their cases significantly especially compared to the which
started out with fewer cases than china but went up significantly in the
two months.

Beyond those models mentioned above, time series analyses and machine
learning models could also be useful. If time permits, we will also
include those analyses in our project.

Finally, the limitations of our project and potential future studies
will be discussed in the presentation.

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
