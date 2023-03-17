# Traders-Classification-Algorithm
This algorithm is a broad analysis of the behaviour of a sample of traders which leads to a classification between 3 categories

Introduction :

Today’s financial markets are trading at a phenomenal rate. Their globalization connects the whole planet, and it is not uncommon to be able to make juicy deals. For several years now, some people have tended to accelerate the phenomenon even further by using super-powerful calculation algorithms, which allow them to carry out several transactions per second, known as HFT’s (High Frequency Traders).

Inaccessible to traditional human and bank analysis, and operating through fiber, these methods consist of scheduling times to sell and buy one or more shares, depending on their price. The idea is to buy when the price is slow, and sell when the price is high. HFT’s, thanks to the power of computers, therefore gain a competitive advantage over « classic » traders. This can be broken down into 3 steps : 

●	Checking the order book : the order book can be seen as a history of purchases and sales made with the corresponding price for the chosen shares, this stage consists into making the algorithm « learn » this history  
●	Scalping : This is the step where the algorithm will define the price where it should buy, and the one where it should sell, as well as find all the trade of opportunities 
●	Defining a trend for the order book 

But then, the power of HFT lies in their scarcity, a bit like a sportsman who dopes to perform better than his opponents, but if they all did the same thing, then being doped would no longer bring any advantage, and you would be back to the beginning. 

The main participants are therefore the big companies which keep the biggest part of the cake and almost half of them are groups specializing in trading, such as NASDAQ or DirectEdge. This exclusivity is due to the fact that we need a monumental computing power to compete (we are talking about few orders made in a few microseconds), a good starting capital in order to be able to buy, and very high entry and opportunity costs, especially at the beginning, which are a hindrance for many small companies, or even individuals.

For the algorithms used, we find Monte Carlo experiments, especially for the simulation of the behavior of data from a small observed sample, the idea being that the algorithm réponds to predefined trade signals. These signals give an indication to either buy or sell, and cannot be detected quickly when doing « manual trading ». The profits per trade are often minimal (in the order of a few cents), but it is the repetition, and the very large volume of trades that can allow a seasoned trader to get very rich. 

One of the most widely used signals is the one that will detect  “Bid Ask Spreads” (the possibility of arbitrage due to a selling price asked by other users that is higher than the price at which one buys a share). These spreads never last very long, and can therefore only be exploited by HFTs, who will be able to detect them before they disappear. 

Background :
The first manipulations that could be assimilated to HFT took place in 1930, when buy and sell orders were transmitted by telegraphs. Of course, the émergence and development of computers made it possible to develop all this more quickly, and in 2005, a law in the regulatory system which stipulated that shares had to be sold at the best price on the stock exchange allowed the number of HFTs to increase exponentially, because the best price is often the one resulting from the algorithms.	
Between 2009 and 2010, at their peak, HFT’s accounted for more than 60% of transactions on the US market, but the subprime crisis put a slight damper on the phenomenon. Today, this figure has dropped to 50%. 
  
But so, why are we interested in high frequency trading ? 
Advantages and disadvantages :
HFT has several disadvantages on a macro-economic scale : it increases the liquidity of the markets, with money circulating faster and faster thanks to numerous transactions, and it helps to find the equilibrium price of a share more quickly, reduces spreads and decreases tradeoff opportunities (this is linked to the fact that the more HFT traders there are, the more difficult it is to make profit when you are one of them because you have more competitors fighting on equal terms with you, and therefore you have no way to take advantage of your position).  

Despite this, there is also a significant list of disadvantages, which are increasingly being questioned by market regulators these days : 

This makes the market unfair for small businesses, or individuals who want to invest in the stock market, the biggest companies have « carte blanche », and in a way a monopoly on the most profitable shares. You need capital, software and location to compete. It is very difficult to become powerful with this, you have to be powerful beforehand, to take advantage of it. Some researchers alert on the phenomenon, like Peter Gombert, a researcher for the Goethe University in Frankfurt in an article published in January 2011 for the SSRN Electronic journal, where it wrote that it “creates an uneven and unfair playing field among market participants”, and that “since market abuse is not limited to a particular subset of traders, all market participants should be investigated when applying such strategies (HFT algorithms)”, going as far as calling those methods of “illegal strategies”.
More recently, there are a lot of articles in this direction that were published. We can quote De Gruyter Oldenbourg in 2020 for the journal Review of economics, where he talks about the “widespread failures of HFT”, or again Ricky Cooper in September 2017 on his internet page.

On a more macro scale, the market becomes very volatile, which can lead to mini-crashes in case of sudden massive selling, the most famous one, took place in 2010, when the Dow Jones lost and then regained hundreds of points in barely half an hour, causing panic among the distincts market players. It is very rare to make changes into an algorithm, usually we do it only after a big crash (by then it is too late and the algorithm has already become obsolete). 

In addition to all this, the large number of repeated buying actions often give the impression of a strong demand for a certain type of stock, whereas this is not the case, and in these cases we are dealing with an illusion. 
Regulation:
For all these reasons, the financial market authority now wants to intervene in order to limit and regulate this type of operation, to keep HFT’s under control and not find itself in a situation where this type of trader makes his law on the market. Measures have already been taken : 
  
Among the most discussed ones, there is the requirement that an order must remain on the market for a certain amount of time before it can be canceled, linked to the obligation to pay taxes for companies after a certain number of canceled orders, because HFT’s order at will and then end up canceling orders that will not bring them enough profit. 
	
In theory, the FSA now obliges firms selling shares to put in place pre-trade and post-trade controls to detect abuse. The same applies to buying firms, which must ensure that the data they use does not manipulate the market. 
Proposal :
However, the difficulty in applying the measures lies in the fact that it is sometimes difficult to accurately identify one HFT trader from another who is not. Martin Wheatley, Director of the Financial Conduct Authority in England, says that even experts cannot agree on an exact definition of HFT. The criterion on the number of transactions is not enough because a large non-HFT group will do more than a smaller HFT group, so the analysis must go further. 
	
This is where we would like to intervene, in the identification of HFT traders : our goal will be to propose a model that will allow, according to common characteristics, to define whether a person is HFT or not. Once we have done this, we will be able to transmit the result to the market regulator, which will allow it to apply the regulations and restrictions that it has previously defined. 

This approach is part of a profit objective for us, linked to a desire for fairness and respect for the rules in place. In order to achieve our objectives we will use a database from the ENS on the classification of traders. 

We will present this database in more detail later, but to give you an idea, it would be a database with 40 variables corresponding to trading characteristics, one that identifies whether a trader is HFT or not. So it would be a supervised classification model, which, if we can get a satisfactory accuracy rate, could be extended to something bigger, and be used by regulators to identify HFT’s. 

To do so, we will conduct a complete econometric analysis in 3 phases : in the first time, we will present to you in detail the raw database, with the explanation for each variable, few descriptive statistics on it, how we will clean and format it, and the way we are going to choose the appropriate methods for the classification. After this, there will be an explanatory analysis of the use database, and the presentation of our results for the selection of methods, and the deepening analysis of the results for the method that we will choose as the best one. The last part will be the conclusion with the principal results that we found, the axes of improvement, and the idea on how to put our classifier to the use of the Financial Authority of the market.
