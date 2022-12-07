# Linear Regression Model 👁‍🗨💥

## This project is an academic use of case to model the sales of a tech company, and study his performance against the other variables (independent ones).

### We have the following Dataset to analyze:

![Captura 1](https://user-images.githubusercontent.com/116805861/206144526-0cbe4078-aa97-457d-8d7f-1549f7696b1c.PNG)

#### Our data goes from 02/01/2022 to 19/06/2022 


#### First step we should take is to create our correlation matrix, where we will see our variables relations and will prevent multicollinearity issues. 

![Captura 2](https://user-images.githubusercontent.com/116805861/206144981-d48f4215-410f-4186-8359-be0c7fc92e9b.PNG)

#### We can notice that there are some high-related features (the ones with higher green colour). To avoid multicollinearity we have to choose which features to include in our model, in order to get the best model with the least number of features. 
#### Our first pick will be: ‘TV grps 20seg AD55’, ‘radio grps 20seg AD15’, ‘FB impresiones’, ‘TV grps 20seg Competidores’ and ‘paro’.

##### *The feature ‘TV grps 20seg Competidores’ have been created from the sum of the three competitor’s data. 


#### Now we have released our model and these are the outcomes:  

![Captura 3](https://user-images.githubusercontent.com/116805861/206145959-7f5c2424-9091-40e0-9c04-7a5f22920769.PNG)

#### Everything seems to be fine except our feature ‘paro’, which should be negative (have no sense that an increase of ‘paro’ please our sales), and also his P-value is too high. 


#### So our next step is to create a new model without ‘paro’, here's what it looks like:

![Captura 4](https://user-images.githubusercontent.com/116805861/206146371-fed34e4f-2fc8-4afc-a9eb-1a5da56b71d4.PNG)

#### Now all the coefficients make sense and also the P-value results are quite good. 
#### Despite the fact that our adjusted R^2 has decreased by 26%, the new performance is approximately 70% explainability, which we find to be a quite acceptable level to move forward.


#### Then, we calculate our model fit and plot it.

#### - Final Data used in the model:

![Captura 5](https://user-images.githubusercontent.com/116805861/206146945-80acc583-5522-43e1-90fc-d7cdb5a53e52.PNG)

#### - ‘Ventas’ vs ‘Ajuste’ plot:

![Captura 6](https://user-images.githubusercontent.com/116805861/206147164-957bb881-b1dc-4462-b86f-f134aff4c6d3.PNG)

#### As we can see in the plot, our model fits quite closely to what is happening in reality.


#### To conclude the project, we will extract the total contributions per feature, and also, the % of each competitor feature (remember we had 3 initially) for ‘TV grps 20seg Competidores’.

![Captura 7](https://user-images.githubusercontent.com/116805861/206147526-683bdf36-e5fa-4331-90b6-ce53c52e37bb.PNG)

#### From our 1878 sales, 1177 are coming from radio campaigns. Furthermore, we are losing -611 sales due to our competitors.

![Captura 8](https://user-images.githubusercontent.com/116805861/206147873-c436077a-fdc3-4a8a-8a8f-bd67ea56258d.PNG)

#### Among our 3 competitors, competitor 1 holds 61% of the total.  


### Endpoints of the Project 💣:

### ✅ The advertising channel that is giving us by far the highest performance is radio.
### ✅ Competitors have a substantial impact on our business, particulary competitor 1, so we should develop solutions to minimize this harmful impact.


## *To achieve the best model we iterate more than the 2 times that have been showed up, actually we iterate with 5 or 6 models before getting the optimal one. 



