# PHEIC Causal Project

WEBPAGE LINK: https://abhishekangadi.github.io/WHO-Pandemic-Emergency-Document-Economic-Impact-Cuasal-Inference-Study/

![200417125229-01-coronavirus-cdc-image-super-tease](https://user-images.githubusercontent.com/44275206/82979238-8efb8780-9fb4-11ea-8553-0440ac0040c7.jpg)


# Project Description
According to Wikipedia, a Public Health Emergency of International Concern (PHEIC) is a formal declaration by the 
World Health Organization (WHO) of "an extraordinary event which is determined to constitute a public health 
risk to other States through the international spread of disease and to potentially require a coordinated international 
response".

Recently, WHO just issued its 6th PHEIC in history to China’s recent outbreak of novel coronavirus. While some argue 
that PHEIC could help curb the epidemic situation as countries become more alarmed of the situation and thus take 
necessary steps to prevent it from spreading further, others argue that it could cause the economic outlook of infected 
countries to deteriorate further.

Thus our project aims to discover whether there is any causality between PHEIC and the economic outlook of infected 
countries and regions.

# Experiment Design
As the issuance of PHEIC is in the middle of the spreading epidemic, it could be
difficult to isolate the effect of PHEIC on economic outlook from the effect of the
epidemic and other factors that potentially influence the economy in the long run.
Therefore, we decided to focus on events that happen fast and during a short period
of time before and after the issuance of the document to minimize the long-term
effect that the epidemic has on it.

One thing that always acts fast according to current events is stock price. It
represents people’s prospects on the economic outlook to a certain extent.
Therefore, we will use this as the key variable in our model to quantify the infected
country’s economic outlook. To understand how PHEIC impacts infected countries,
the specific causal question we will ask here is how is the issuance of PHEIC affecting
the stock price of companies that have a large percentage of revenue from the
infected country?

Therefore, we would use a difference-in-differences model. We will select the companies 3 days before and
after the issuance on PHEIC for Covid-19 - the date for issuance of PHEIC is January
30.

# Study Design & Methodology
As China was the most severely infected country when WHO issued the PHEIC on Jan
30th, 2020, our analysis focuses on assessing the impact of PHEIC on China.

The ideal experiment to answer our problem statement is to observe the stock prices
of selected companies when PHEIC is issued compared to the same companies when
PHEIC is not issued. However, such an experiment is not possible since the event of
the issuance of PHEIC has already happened.

Moreover, such events (issuance of PHEIC) are rare so it is difficult to find other
similar events having other variables ceteris paribus. Therefore we would use a
difference-in-differences model. We will select the companies 3 days before and
after the issuance on PHEIC for Covid-19. The date for issuance of PHEIC is January
30 and that time COVID-19 was in China. Instead of dividing data into two separate
groups - one having significant revenue from China and other not having not
significant revenue from China - we have considered our treatment variable i.e.
revenue from China as a continuous variable. By adopting this methodology, we did
not have to choose the cut-off baseline for revenue to decide on the treatment and
control groups. Further, we would also repeat our difference-in-difference analysis
for specific industries such as food and healthcare separately to study the effects in
particular industries.

# Data Collection, Munging & Description
According to our study design, there are two primary data points we require - stock
prices and the companies’ percentage of revenue from China. We have collected
data for 95 companies using the following sources:

- We used NASDAQ’s official website for collecting the stock prices of
companies. These websites have historical day-to-day stock price data for
companies listed on stock exchanges.

- We estimated the companies’ percentage of revenue from China based on its
past financial reports and articles. For example, as per the financial report
released by Apple on 28th Jan 2020, Apple's reported revenue in Greater
China is 13 billion which accounts for 14.8% of Apple's total revenue ($91.9
billion).

# Final Model
We used a difference-in-differences (DID) model for our final analysis. DID relies on
an assumption that in the absence of treatment, the unobserved differences
between treatment and control groups are the same overtime. Hence, we tested for
parallel trends between the treated and control groups before the treatment. Since
percentage revenue is a continuous treatment variable, we chose a threshold of 40
percent revenue from China to divide the data into treatment and control groups
only for the parallel trend analysis. In figure 1, a clear parallel trend can be noticed in
between the two groups before the treatment.

![Capture](https://user-images.githubusercontent.com/44275206/82992044-9595f900-9fcc-11ea-9e73-4383c8ba9cfc.JPG)

The data we have can be categorized as panel data which is essentially
multi-dimensional data involving measurements over time . To help us better control
the heterogeneity of cross-section units (different companies for example), we chose
to use a Panel OLS to estimate the fixed effects regression. The companies and the
actual dates are treated as fixed variables in the panel OLS regression.
We have treated Stock Price as the dependent variable while companies and the
actual dates as the Entity variables. We have included an interaction between the
percentage revenue (the continuous treatment variable) and the Pre-Post PHEIC
declaration dummy.


# Conclusion
The results from this difference-in-difference model show that there is no significant
effect of the issuance of PHEIC on stock prices of the 95 companies. Therefore, it
implies that PHEIC has no impact on downgrading the economic outlook when we
look at all industries together. The fact that the model considers all companies from
different industries is not useful to explain the causal effect of the issuance of PHEIC.
But when looking at the specific industries, we did find that the issuance of PHEIC
impacts the stock prices implying that it impacts the economic outlook for specific
industries. The healthcare industry benefited from the PHEIC issuance while other
industries such as the food industry were negatively impacted. However, we are
aware that there is a limitation to our study and we need to include a larger sample
size in each industry. Moreover, there could be many other factors that might not
have been factored in our analysis. For example, the stock prices of companies may
already have factored the effect of the pandemic and therefore the issuance of
PHEIC did not make any significant effect on stock prices.
