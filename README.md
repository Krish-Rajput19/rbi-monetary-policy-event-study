# RBI Policy Tone and Bank Stock Reactions

**Overview**  
Using an Indian context, this project tests the hypothesis that the words contained in RBI policy statements have an impact on Indian banking stocks regardless of the news effect of the interest rate decision.

**Methodology**  
Over the past decade, I constructed a sample of 15 RBI Monetary Policy Committee meetings, with the official policy summaries scored on the "tone" of the statement (hawkish or dovish). I built an event-study system in Python (pandas, statsmodels, yfinance) that computed the return performance of select banking stocks relative to NIFTY 50 during the -5 to +6 day window around each meeting. I ran an OLS regression with HC1 robust standard errors to isolate the differential effects of tone, separate from rate hikes/cuts.

**Findings**  
Banking stock performance based on hawkish language was also significant at 5%. With the inclusion of the actual rate decision in the regressors, a hawkish prevailing tone is a significant predictor of a lower banking sector abnormal return, pointing to Really the market seems to be responding to the forward-looking liquidity messages sent by the RBI even after taking the magnitude of the repo rate decision into account.

**Main Limitation**  
The number of 15 meetings is relatively small owing to in reality the RBI MPC was only created in 2016. It is not possible to compare with previous sets of data because of this, decreasing the statistical power of the model.
