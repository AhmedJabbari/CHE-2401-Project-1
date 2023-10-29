CHE-2410-Analsysis of Corrosion Rate % in Gas Pipelines Considering the operating Parameters (Gas Flowrate and Water Cut %)

Background and Analysis Motivation:
Corrosion is one of the greatest challenges in the oil and gas industry. There are multiples methods which are used in industry to control corrosion inside carbon steel pipes such as chemical injection (corrosion inhibitor). However, most of these methods are expensive and they consume up to 20% of the operating cost. My role as an operation engineer at one of the oil and gas companies is to develop an economical mechanism to control corrosion rates and operate with more efficiency. 
Therefore, I decided to analyze the historical data of operating parameters (gas flowrate and water cut %) of number of carbon steel pipelines that are used to transport a natural gas and try to capture the most contributing factor to the corrosion in terms of operation parameters. Then, develop a controlling method to minimize/eliminate the corrosion inside gas pipelines. 
In fact, there are several factors which can cause corrosion. These factors are not limited to the operation parameters, but they could involve other factors such as pipelines configuration (geometries). In my analysis, I am neglecting other corrosion factors since there is no enough information about them and they are not measurable.  In addition to that I am assuming that all these pipelines have the same diameter and length. 
The collected data is related to 110 pipelines with their average gas flowrate for two years in MMSCFD, water cut % from the total flowrate and the measured corrosion rate % (The percentage of metal loss) inside the pipes using an instrument in-line scraper which is being utilized to measure the metal loss inside the pipelines. 
Analysis Summary: 
Initially, I plotted the corrosion rate % verse the water cut % to find out if there is a linear relationship between the two: 
  

 
By just looking at the graph I can see that there is a linear relationship between the water cut % and the corrosion rate % and to confirm that I used Python’s OLS linear regression model package, I found that the Corrosion Rate %=0.1429* Water Cut% -0.4131 and the p-value for water cut % is less than 0.05, which indicates that there is a statistical significant positive linear relationship between the water cut % and the corrosion rate %, meaning that as the water % increase, the corrosion rate tends to increase. In fact, this observation is expected because as the amount of water increase there will more water accumulated inside the pipe, which will react with iron and cause internal corrosion in the pipe.   

Then, I plotted gas flowrate verse the corrosion rate % and I applied the Python’s OLS linear regression model package, I found that the Corrosion Rate %=-0.5* Gas-Flowrate +0.4131 and the p-value for gas flowrate is less than 0.05, which indicates that there is a statistical significant negative linear relationship between the gas flowrate and the corrosion rate %, meaning that as the gas flowrate increase, the corrosion rate will increase. This observation is expected as the flowrate increase the fluid velocity will increase and minimize the water accumulation at the bottom of the pipe. 

 

 

Linear models considering multiple factors:

To figure out which parameter has more effect on corrosion rate %, I used linear models considering two factors. The result shows that Corrosion Rate % = -0.366 * Gas-Flowrate + 0.1298 * Water Cut % + 1.43 and the p-values less than 0.05 indicates that the relationships between these variables and the corrosion rate are statistically significant. So, based on this model, it appears that water percentage has a stronger positive effect on corrosion rate than flowrate has a negative effect.

 
Linear models considering multiple factors with interactions:
At the final stage of my analysis, I utilized linear models considering two factors with interactions to find if there is an interaction between the operating parameters, I got that the Corrosion Rate% = -0.0234* Gas-Flowrate+0.244* Water Cut %-0.0263*Gas-Flowrate*Water Cut % - 0.151. The p-value is less than 0.05 of flowrate*water% which suggests that there is an interaction between flowrate and water cut % and this interaction is highly significant in predicting corrosion rate %.

 
Conclusion:
As a conclusion of my detail analysis, there is a positive linear relationship between corrosion rate percentage and water cut percentage and there is a negative linear relationship between corrosion rate percentage and gas flowrate. However, the water percentage has a stronger positive effect on corrosion rate than flowrate negative effect. Furthermore, there is an interaction between flowrate and water cut percentage in predicting corrosion rate percentage.
