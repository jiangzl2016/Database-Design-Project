### Query 4 Customer Behavior Prediction

The purpose of query 4 is to find out the category of products that are mostly likely to be purchased by different customers, during both special and non-special event periods. After finding out the product category, the Cal Student Store can implement targeted marketing strategy regarding different customers, thus achieving higher sales. 
    

	SELECT TC.TID, TC.Is_group, TC.Group_Name, 
	TC.Sport, TC.College_Name, TC.Club_Name, 
	
In order to achieve higher prediction accuracy, we used three different machine learning algorithms so that we could compare and contrast and select the best model. The three algorithms that we used are K-Nearest-Neighbor (KNN) Classification, Logistic Regression, and Classification Tree. 

To see how this model predicts the product category for a particular customer segment, the following plot shows an example of the purchase probability for Club Phoenix during normal time period:

![](../SQL_Queries/graphs/41.png)
As we can see from the graph, students that are part of Club Phoenix are most likely to purchase office items, followed by a bag or decoration. Hence the promotional email that the student store sends to these students should include information (pictures, promotional events) related to the office items and bags.

The last model is Classification Tree. The model also helped us extract different customer feature importance during different time period:  
![](../SQL_Queries/graphs/42.png) 