# PHEIC Causal Project
This is a repository on the causal analysis of the impact PHEIC having on China's economic outlook

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

