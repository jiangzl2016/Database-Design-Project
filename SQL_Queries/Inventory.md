### Query 5 Inventory Time Series Analysis

The purpose of Query 5 is to create an approach for the Cal Student Store to track  the historical inventory level of merchandise items. Being well aware of the merchandise inventory information, the business owner can make more strategic decisions in purchasing inventory by controlling the frequency of restocking. In addition, seasonal time series models allow the store manager to observe the trends and seasonal patterns more precisely, and adjust inventory in the future. In the future, the program can be extended into an alert system API, which interfaces with store’s database and prompts store owner to refill inventory when its level is low.  


Queries:
	FROM Transaction t, Transaction_Product tp 
	WHERE t.Date IS BETWEEN
	GROUP BY SKU 
	ORDER BY sales DESC
	tp.SKU AS SKU, SUM(t.Quantity) AS purchase
	GROUP BY t.Date, tp.SKU ;

	GROUP BY date, SKU ;


	s.shipment AS shipment, x.current_inventory AS current_inventory
	AS Date, t.purchase, 47 AS current_inventory
	ON strftime('%Y-%m-%d', d.Date) = strftime('%Y-%m-%d', t.Date)) x
	ON strftime('%Y-%m-%d', x.Date) = strftime('%Y-%m-%d', s.Date)

Algorithms:


Time series Analysis:


![](../SQL_Queries/graphs/51.png)

Then we expand our vision to full time series. We build a seasonal decomposition model to break down the time series into trend (T), cyclical (C), seasonal (S) and irregular noise (I). The formula and the visualization created is the following: 

**y(t) = T(t) +C(t) + S(t) + I(t)**

![](../SQL_Queries/graphs/52.png)
Besides visualizing the trend component and cyclic component, we also used ARIMA to make predictions of future inventories to capture autocorrelation existing between data.  The formula of ARIMA is the following:
**(1−ϕ1B−⋯−ϕpBp)(1−B)dyt=c+(1+θ1B+⋯+θqBq)et**

![](../SQL_Queries/graphs/53.png)

Code snippet:
![](../SQL_Queries/graphs/54.png)
![](../SQL_Queries/graphs/55.png)
![](../SQL_Queries/graphs/56.png)

