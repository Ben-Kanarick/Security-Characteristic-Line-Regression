# Security-Characteristic-Line-Regression
For this assignment, each team will write a Python program that will determine a public company's equity beta, provide some statistical information, and then interpret the results.  This is an important function that is often done at investment banks, asset management firms, consulting firms, and valuation firms.

The program will query the user for a particular stock (for now, just US stocks) and a date range (through June 30, 2022 or other specified range if you have the data).  If you are ambitious, you can ask the user what kind of data frequency (daily, weekly, monthly) to use.  By default, we will assume monthly.  You may use the data file (to the extent you can) in Canvas: Files: Models & Spreadsheets: CAPM and SCL.  If you want more data, you can access it from WRDS (more on this during class).  Otherwise, you will have to have force the user to only use date ranges and frequency as included in the file.  That file includes information on the "market" risk premium (Rm-rf) and the risk free rate (one month treasury bill).  You will need to have the program download the appropriate data for your stock and then merge this data together.  There are a number of public libraries/routines available (e.g., yfinance) in Python that allow you to download stock data for certain ranges.  You'll need to manipulate the data to get it into a consistent data frame (with the appropriate dates). 
Yahoo doesn't allow you to download index information.  As a result, if you are going to use your own market index or query the user for which market index to use, make sure it is an ETF.

Once you have all your data (date, market risk premium, individual stock risk premium), you are ready to run your SCL time series regression.  The market risk premium is your independent variable and the individual stock risk premium is the dependent variable.  We are interested in collecting the following information:

Summary statistics
number of data points
correlation
R2
Standard Error
ANOVA
Full Analysis of Variance Table
Coefficient Analysis
For both alpha and beta
the estimates
the standard errors of each
the t-statistic
the p-value
You should report the alpha and beta values and then run hypothesis tests to determine and report whether:
the alpha is statistically significant (different from zero), and at what level (e.g., 95%)
the beta is statistically significant (different from one), and at what level (e.g., 95%).
Remember that many standard packages will use a null hypothesis of zero, so if you are "testing" against a different value (like one), then you need to compute the t-statistic yourself.
Draw the scatter plot (X,Y) and the regression (SCL) line.  There are Python packages like Seaborn which can be useful for this, but use whatever package/library you like.
As a last step, query the user whether they would like you to compute an expected return for the stock for the next year (we will assume that we can use the monthly beta for an annual estimate, though this is not strictly right).  If they do, then query the user for an expected rate of return on the market E(Rm) over the next year.  Determine the current risk-free rate by using WRDS, Yahoo, or any other source to get the current one-year risk free rate (1 year Treasury bill yield on the day you run this program).  Then, using the SML equation, compute the Expected Rate of Return for your security.  Report this number.  You should also give a range of estimated Expected Returns based on the prediction interval (not confidence interval) of the beta.

Finally, write up a professional memo that provides a narrative of the work that you performed.  This is mostly about methods and procedures as opposed to the specific user query; however, you can use excerpts of output as your exhibits to explain what you are doing.  As part of the "Results" section below, explain how the ANOVA table can be used to provide information on the following statistics (you can use a sample "run" as an example):

Systematic Risk  
Idiosyncratic Risk 
Correlation
R2
Beta
Standard Error
Make sure you provide an explanation/brief description of each of these terms.
Note:  the section below is the same as last week, but incorporated here as a reminder:
