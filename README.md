# Delayed Correlation: Vaccination and SARS-CoV-2 in Argentina. 
![Uploading Presentación Proyecto Investigación Geométrico Profesional Azul Verde (1).png…]()



####  Correlation analysis, regression analysis & time serie analysis

## Introduction:
Over the past two decades, the world has witnessed various outbreaks of infectious diseases. The Ebola virus, Influenza A (H1N1), SARS, MERS, and the Zika virus have had a significant global impact in terms of economic disruption and public health on both local and global scales.
By late 2019, the outbreak of the novel coronavirus 2019 (SARS-CoV-2) emerged. This virus, a member of the Coronaviridae family, was first discovered and isolated in the city of Wuhan, China. SARS-CoV-2 possesses a viral envelope and is classified as a single-stranded positive-sense RNA virus.

SARS-CoV-2 was initially identified from patient samples on December 31, 2019. In March 2020, the World Health Organization (WHO) named the disease caused by this virus COVID-19. Due to its global implications, COVID-19 was declared a pandemic.

As of August 2023, approximately 769 million cases of coronavirus have been recorded worldwide, with an estimated 7 million deaths on a global scale.
As highlighted in the research published in the Vaccine journal in 2021, “Previous studies have shown that vaccine, as a powerful weapon to control an infectious disease, can notably allay or defeat diseases caused by pathogens”. There are numerous examples that support this statement, such as Smallpox, Polio, Measles, among others.

## Hypothesis
In consideration of the previously established theoretical framework, a primary hypothesis is formulated as follows:
Primary Hypothesis: "Vaccination results in a reduction of COVID-19 cases in Argentina."
Expanding upon this primary hypothesis, three additional hypotheses are proposed:

  •	Hypothesis 1: "There exists a significant and negative correlation between the vaccination rate and the number of COVID-19 cases."
  
  
  •	Hypothesis 2: "There exists a significant and negative correlation between the proportion of immunized individuals and the number of COVID-19 cases."
  
  
  •	Hypothesis 3: "Both relationships are characterized by a specific delay during which a maximum negative correlation is observed. 
  
  
This delay represents the time it takes for individual and collective immunization to have a noticeable impact at the population level."

## Methodology
The data were obtained from the vaccination dataset provided by Our World in Data [18], which utilizes the most recent official figures from government health ministries worldwide.
Correlation analyses were conducted among the selected variables, and regression models were proposed.
Finally, a time series analysis was performed, and two SARIMAX (Seasonal Autoregressive Integrated Moving Average with Exogenous Variable) models were estimated—one with an exogenous variable and another without an exogenous variable.

## Results and Discussion
In the notebook.
### SARIMAX models comparisson:
Both SARIMAX models demonstrated remarkable ability to capture the observed seasonal pattern in the original data and replicate it in subsequent predictions. This capacity to accurately reproduce seasonal fluctuations is crucial for effective forecasting. 

A significant difference was observed in the trends identified by the two SARIMAX models. The SARIMAX model without exogenous variables exhibited a more pronounced negative trend compared to the model that incorporated the considered exogenous variable.

Quantitative evaluation of the models was based on key metrics, including the Mean Squared Error (MSE) and the Akaike Information Criterion (AIC). It was observed that the SARIMAX model incorporating the exogenous variable exhibited lower values in terms of MSE and AIC compared to the model that did not include this variable. These results indicate a better fit and greater explanatory power of the SARIMAX model with the analyzed exogenous variable.

Finally, both models share similar characteristics in terms of autocorrelation in the residuals and skewness in the distribution. However, the model with the exogenous variable appears to have a better normality of the residuals (though not perfect) and less evidence of heteroscedasticity compared to the model without the exogenous variable.

The SARIMAX model incorporating an exogenous variable, demonstrates a remarkable ability to discern and quantify the impact of this variable on the dynamics of cases. This capacity parallels previous observations made through a linear regression analysis. In particular, it is evident that an increase in the rate of growth of the exogenous variable (i.e., the number of individuals fully immunized per 100 inhabitants) positively correlates with an increase in the observed negative trend in the time series of COVID-19 cases,as illustrated in the following image.

![Presentación Proyecto Investigación Geométrico Profesional Azul Verde](https://github.com/JulianDietrich97/COVID19-ARG/assets/117474938/d036f3dc-9eae-4cbc-a134-db876757c1eb)

## Conclusion
According to the analysis conducted, evidence has been obtained that supports the hypothesis posited, which asserts that the implementation of vaccination programs is associated with a significant reduction in COVID-19 cases in the Argentine population. Additionally, it has been concluded that there is a negative and statistically significant correlation between vaccination coverage in the population, measured in terms of the proportion of immunized individuals per 100 persons, and the incidence of COVID-19 cases in the country. This correlation has been assessed considering a one-year lag in the analyzed data.

Both SARIMAX models exhibited similar evaluation metrics, although the model with the exogenous variable appeared to perform slightly better. While both models successfully captured and replicated the observed seasonality in the original data, I would recommend ongoing real-time assessment to observe how each model responds. This is done to determine which one performs better in forecasting.

## Applications of the Model:
Time series models are highly valuable in various applications and can be beneficial across a range of sectors. To mention some ideas for potential applications and potential target markets:

  -*Government and Public Health:* Sale or collaboration with the Ministry of Health in Argentina to enhance case predictions and plan more effective responses. Assisting in decision-making regarding restrictions and social distancing measures.
  
  -*Pharmaceutical Industry:* Collaboration with pharmaceutical companies that can utilize the predictions for pharmaceutical and vaccine production planning.
  
  -*Insurance Companies:* Sales to insurance companies to aid in risk assessment and estimation of medical service demand.
  -Universities and Research Institutions: Sale or collaboration with academic institutions to enhance research on disease spread and public response.
  
  -*Media Outlets:* Collaboration with media outlets to provide updated forecasts and analysis on the COVID-19 situation in Argentina.
  
## Bibliography:
Boopathi S, Poma AB, Kolandaivel P. Novel 2019 coronavirus structure, mechanism of action, antiviral drug promises and rule out against its treatment. J Biomol Struct Dyn. 2021 Jun;39(9):3409-3418. doi: 10.1080/07391102.2020.1758788. Epub 2020 Apr 30. PMID: 32306836; PMCID: PMC7196923.

Caldas, L.A., Carneiro, F.A., Higa, L.M. et al. Ultrastructural analysis of SARS-CoV-2 interactions with the host cell via high resolution scanning electron microscopy. Sci Rep 10, 16099 (2020). https://doi.org/10.1038/s41598-020-73162-5 Caldas, L.A., 

Li Z, Liu X, Liu M, Wu Z, Liu Y, Li W, Liu M, Wang X, Gao B, Luo Y, et al. The Effect of the COVID-19 Vaccine on Daily Cases and Deaths Based on Global Vaccine Data. Vaccines. 2021; 9(11):1328. https://doi.org/10.3390/vaccines9111328

Yamin, M. (2020). Counting the cost of COVID‐19. International Journal of Information Technology, 12(2), 311–317. 10.1007/s41870-020-00466-0 [PMC free article] [PubMed] [CrossRef] [Google Scholar]

Estadísticas de COVID19: https://www.statista.com/statistics/
DATA: https://github.com/owid/covid-19-data/tree/master/public/data


