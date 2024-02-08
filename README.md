# Saudi_Arabia_Used_Cars

#### **Context**

Saudi Arabia Used Car Market was valued at USD 4.91 billion in 2021 and is expected to surpass a net valuation of USD 8.69 billion by 2027 end, registering a solid CAGR (Compound Annual Growth Rate) growth of 7.36% over the forecast period.

The COVID-19 pandemic had a moderate impact on the market as initial lockdowns in 2020 resulted in a slowdown in demand, however with ease in restrictions in 2021 consumers were encouraged to prefer used cars over new cars in wake of the pandemic coupled with fewer vehicle production due to supply chain disruptions and shortage of some auto components.

Syarah.com is one of a platform for buying and selling used cars in Saudi Arabia. This website allows users to search, compare, and purchase used cars with a wide range of brands, models, and prices. It is similar to other used car buying and selling platforms available in various countries.

On Syarah.com, you can find comprehensive information about the used cars for sale, including pictures, descriptions, prices, and contact information for the sellers. It is a valuable resource for individuals looking for used cars in Saudi Arabia who want to compare various options before making a purchase decision.

#### **Problem Statement**

Purchasing and selling used cars can be quite challenging, especially for those with limited knowledge about the automotive industry. Often, they need to find a suitable and fair price for the car they want to sell or buy. Considering this, a platform like 'Syarah.com' that can provide accurate price estimates would be helpful. These estimates can serve as valuable guidance for car owners looking to sell their vehicles, making it easier for them to determine a competitive price. On the other hand, buyers will also feel more confident when evaluating a fair price for the car they desire.

Although this Syarah.com provides price estimates, it still allows sellers the flexibility to set their prices according to their personal policies. Some sellers may choose to sell at a higher price, while others may want to offer a more competitive price for a quick sale. Thus, Syarah.com will help create transparency in the used car market, making it more accessible and assisting all parties, both sellers and buyers, in making better decisions.

#### **Goals**

Based on the issue, Syarah.com requires a program to assist them in predicting prices so that sellers can offer the right price. Price variations can be provided based on features, distance, brand, origin, gear type, seller's region, and of course, a price that suits them.

With this program, Syarah.com can help provide sellers and buyers with suitable prices, thereby increasing the number of transactions that generate profits for Syarah.com from both sellers and buyers, known as booking charges

#### **Analytic Approach**

So, what we need to do is analyze the data to identify patterns within the existing features that differentiate each vehicle.

Next, we will build a regression model that will assist the company in providing a pricing prediction tool for used cars newly listed on Syarah.com. This tool will be useful for sellers in determining the listing rental price.

#### **Metric Evaluation**

In evaluating a regression model for predicting used car rental prices, three key metrics come into play: RMSE (Root Mean Square Error), MAE (Mean Absolute Error), and MAPE (Mean Absolute Percentage Error). RMSE measures the magnitude of prediction errors by averaging their square roots, while MAE calculates the average absolute error, offering a straightforward measure of accuracy. MAPE, on the other hand, provides a sense of error as a percentage of the actual values. Smaller values for these metrics indicate a more accurate model.

Additionally, if you're working with a linear model, R-squared (or adjusted R-squared) can be useful. It quantifies how well the model explains the overall data variance, with values closer to 1 signifying a better fit. However, remember that R-squared isn't suitable for non-linear models. Utilizing this combination of metrics allows for a comprehensive evaluation of your model's ability to predict rental prices, considering both the magnitude and percentage of prediction errors, and, when applicable, the model's explanatory power in relation to the data.

### **Data Understanding**
- The dataset contains 5624 records of used cars collected from syarah.com
- Each row represents a used car. Other information regarding each car is the brand name, model, manufacturing year, origin, options, engine capacity, transmission type, mileage that the car covered, region price, and negotiable.

#### **Features**
-	Type: Type of used car.
-	Region: The region in which the used car was offered for sale.
-	Make: The company name.
-	Gear_Type: Gear type size of used car.
-	Origin: Origin of used car.
-	Options: Options of used car.
-	Year: Manufacturing year.
-	Engine_Size: The engine size of used car.
-	Mileage: Mileage of used car in KM
-	Negotiable: True if the price is 0, that means it is negotiable.
-	Price: Used car price in SAR (Saudi Arabia Riyal)

### **Data Preprocessing**
At this stage, we will perform data cleaning, and the cleaned data will be used for the subsequent analysis processes. Some of the tasks involved are as follows:
- Dropping features that are not relevant to the current problem.
- Handling missing values, if any. This can be done by either dropping the feature if it's not needed or by imputing it with a logically reasonable value based on the specific case.

### **Conclusion**

The evaluation metrics used for the model are RMSE, MAE, and MAPE. Judging from the MAPE value generated by the model after hyperparameter tuning, which is approximately 16%, we can conclude that if this model is used to estimate the listing prices for used cars on Syarah.com within the trained value range, the price estimates on average will deviate by approximately 16% from the actual prices.

However, it is also possible for the predictions to deviate further, as the model's bias remains relatively high when considering the visualization of actual and predicted prices, especially for prices above 200,000 SAR and within the range of 25,000 to 57,000 SAR. The bias introduced by the model is primarily due to the limited dataset availability for used cars within the price range of 25,000 to 57,000 and above 200,000 SAR.

### **Recommendations**

1. This model can certainly be further improved to yield even better predictions. We can augment the dataset with used cars priced above 25,000-57,000 and above 200,000 SAR.

2. This model can be utilized for estimating the buying and selling prices of used cars, assisting sellers in determining the prices for their vehicles, and enabling buyers to adjust their budget plans for purchasing cars. 

3. This model will enhance transparency regarding car specifications that align with their respective prices, alleviating concerns for both sellers and buyers. Additionally, it can boost the turnover of Syarah.com as a platform for buying and selling used cars.
