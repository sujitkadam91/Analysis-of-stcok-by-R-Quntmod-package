# Analysis-of-stcok-by-R-Quntmod-package
How to Analyze any stock Alibaba Google HDFC Kotak in share market  by R quantmod Package
###########################################################################################################################
#########Subscribe this YouTube Channel Data/Fun  ####################################################
###########################################################################################################################
install.packages(quantmod)
library(quantmod)
loadSymbols(c("AMZN","GOOG","BABA"))

head(AMZN)
head(BABA)
tail(BABA)
############## Subscribe this YouTube Channel Data/Fun  ####################################################
chartSeries(BABA)
addMACD() # adds moving average convergence divergence signals
addBBands() # Adds Bollinger bands to the stock price.
addCCI() # Add Commodity channel index.
addADX() #Add Directional Movement Indicator
addCMF() #Add Money Flow chart

############## Subscribe this YouTube Channel Data/Fun  ####################################################

seriesHi(BABA) # To check the highest point of price.
seriesLo(BABA) # To check the lowest point of price.


only_2015_values<-BABA ['2015'] #Subset shares values all BABA in 2015 
head(only_2015_values);tail(only_2015_values)
dadafrom2017onwards<-BABA ['2017::'] # BABA data, from 2017 onward
head(dadafrom2017onwards);tail(dadafrom2017onwards)

############## Subscribe this YouTube Channel Data/Fun  ####################################################

## ANALYSIS OF RETURNS
Returns_by_day<-dailyReturn(BABA) # Returns by day
head(Returns_by_day);tail(Returns_by_day)
############## Subscribe this YouTube Channel Data/Fun  ####################################################

Returns_by_week<-weeklyReturn(BABA) # Returns by week
head(Returns_by_week)
head(Returns_by_week);tail(Returns_by_week)

Returns_by_Month<-monthlyReturn(BABA) # month, indexed by yearmon  daily,weekly,monthly,quarterly, and yearly
head(Returns_by_Month);tail(Returns_by_Month)

Returns_by_yaer<-yearlyReturn(BABA)
head(Returns_by_yaer);tail(Returns_by_yaer)##https://www.netcials.com/stock-returns-nyse/BABA-Alibaba-Group-Holding-Limited/
############## Subscribe this YouTube Channel Data/Fun  ####################################################

baba_ALLReturns<-allReturns(BABA) #https://www.netcials.com/stock-returns-nyse/BABA-Alibaba-Group-Holding-Limited/
head(baba_ALLReturns);tail(baba_ALLReturns)

###########################################################################################################################
############## Subscribe this YouTube Channel Data/Fun  ####################################################
###########################################################################################################################

##ANALYSIS OF KOTAK BANK

getSymbols("KOTAKBANK.BO", src="yahoo")
chartSeries(KOTAKBANK.BO)

addMACD() # adds moving average convergence divergence signals
addBBands() # Adds Bollinger bands to the stock price.
addCCI() # Add Commodity channel index.
addADX() #Add Directional Movement Indicator
addCMF() #Add Money Flow chart

Returns_by_yaer_KOTAKBANK.BO<-yearlyReturn(KOTAKBANK.BO)
head(Returns_by_yaer_KOTAKBANK.BO);tail(Returns_by_yaer_KOTAKBANK.BO)

##########################################################################################################################
############## Subscribe this YouTube Channel Data/Fun  ####################################################
###########################################################################################################################

### ANANLYSIS OF HDFC BANK

getSymbols("HDFCBANK.BO", src="yahoo")
chartSeries(HDFCBANK.BO)
chartSeries(BABA,multi.col = T,theme = "white",subset = "2015-1::2018-11")

addMACD() # adds moving average convergence divergence signals
addBBands() # Adds Bollinger bands to the stock price.
addCCI() # Add Commodity channel index.
addADX() #Add Directional Movement Indicator
addCMF() #Add Money Flow chart

## Yearly Returns

Returns_by_yaer_HDFCBANK.BO<-yearlyReturn(HDFCBANK.BO)
head(Returns_by_yaer_HDFCBANK.BO);tail(Returns_by_yaer_HDFCBANK.BO)
###########################################################################################################################
############## Subscribe this YouTube Channel Data/Fun  ####################################################
###########################################################################################################################


