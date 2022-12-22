# Model Reserves

Parameters risks are encompassed under correlation and recovery ratios reserves.  Correlation reserves are computed at 0.15 for first to default baskets and 0.20 for other transactions that are not subject to EITF 02-03.  Recovery ratios are randomly simulated for each obligor with a beta distribution and reserves are set to a 25-percentile loss on a portfolio.

Data input risks are captured where difference between traders’ price and independent source used for valuation reserves.

The liquidation risk within bid-ask credit curve spreads is computed as close-out reserves (ref. https://finpricing.com/lib/IrInflationCurve.html)

The marked-to-market  (MTM) value of a CDO or FTD baskets can be represented as a function of the market spreads, market liquidity and underlying pricing model (which itself is dependent on the correlation engine and estimated correlation parameters).  Thus, the change in MTM can result from the change in either for the above-mentioned variables.

 

Risk factors:	Market risk	 Market liquidity risk	         Model Risk	           Parameter Risk

Measures:	Daily P&L	Individual credit curves     Model Reserves     Correlation Reserves	
				close-out reserves

mkt cs : market credit spreads
liq : market liquidity (proxied by bid-ask individual credit spreads from mid)
 engine: correlation model
 : correlation parameter

From the above mathematical representation, the GCP reserves are subject to one main source of model risk – choice of default correlation model. The current reserves amounts are model dependent but the conservative approach to the computation of these reserves will partially encompass model risk.  In order to compute model risk reserves, an alternative generally used model (referred to as the alternative model in this policy) must be available for comparison. The following methodology and process will be used for computing GCP model risk reserves.   

I.  Identification of alternative model and market data source

1.	Identify an alternative model for valuation comparison.  The alternative model should possess the following characteristics, whenever possible.  

•	Sufficiently simple to implement and maintain.
•	Relatively well recognised and commonly used in the industry.
•	Have similar data inputs to the in-house model so that external data requirement is kept to minimum.
•	Able to generate quantifiable valuation and interpretative measurement of valuation differences due to model choice.

The selection of alternative model is dependent on market maturity and industry practice.  

2.	Identify the data sources for parameter calibration. 

•	Determine whether there exist market-traded instruments that mimic the characteristics of the actual structured portfolio and strategies going forward.
•	The market for these instruments should be relatively liquid. 

Appropriate market data, if available, should be used.  


II. Calibration of asset correlations

3.	Calibrate the asset correlations for every CDO portfolio and FTD basket.
•	The asset correlations will be calibrated with industry-accepted methodology.  GCP currently uses the KMV engine.

III. Computation of model reserves

4.	To compute the model reserves, two valuations must to be performed for every CDO portfolio and FTD basket.

i.	MTMGCP in-house Model (calibrated correlations)
ii.	MTMAlternative Model(calibrated correlations)

•	The difference of (i) and (ii) represents the model divergence (or bias). Overvaluation of the financial structure using GCP in-house model relative to the alternative model will be set as reserves against model risk.
 
IV. Computation of correlation reserves

5.	To compute the parameter reserves, a range of plausible correlations is used compute the corresponding range of MTMs of each tranche given a model choice.    One of the three alternative methods to derive parameter reserves can be used.

i.	Correlations close-out reserves – The correlation bid/ask spreads represent the market uncertainty on correlation parameters and the correlation close-out reserves will capture the parameter risk,  or
ii.	Shocked parameter reserves – The use of a plausible range of correlations to compute the model sensitivity to parameter and reserves held for the range will capture parameter risk, or
iii.	EITF 02-03 requirement - The EITF 02-03 adjustment made to account for unobservable market model inputs such that zero MTM is attained at inception will encompass parameter risks.

V. Individual name credit spreads close-out reserves

6.	The bid-ask from market individual name credit curve spread data is used for the computation of close-out reserves.  Although the computation of close-out reserves will be subjected to model bias, the bias is already captured in the Model Reserves.  

