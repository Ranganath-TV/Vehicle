<h1><center>Data Analysis for Electric Vehicle Population</center></h1>

![image](https://user-images.githubusercontent.com/43418706/236799646-043670a4-fa1a-4435-8494-4710e34b8d10.png)

### About Data

* **Data:** This dataset lists the Battery Electric Vehicles (BEVs) and Plug-in Hybrid Electric Vehicles (PHEVs) that are currently (April-2023) registered with the Department of Licencing (DOL) of Washington State (USA). 

* **You can get the data at:** https://catalog.data.gov/dataset/electric-vehicle-population-data

* **Task:** Using the provided dataset, we want to do exploratory data analysis (EDA). The EDA will serve as the foundation for the necessary Data Wrangling activities to be carried out for the purposes of data cleansing and normalization. During the coding process, we will document our observations. Eventually, we will produce a summary and draw conclusions from our findings.

### Objectives:
The main goal of this project is to thoroughly analyze the dataset in order to find important insights. The battery-electric and plug-in hybrid electric vehicles (BEVs and PHEVs) that are currently registered with the Washington State Department of Licencing (DOL) are displayed in this dataset. Our goal was to develop a justification for the population of plug-in hybrid electric vehicles (PHEVs) and battery electric vehicles (BEVs).

On the relevant dataset, we will apply **EDA** in an effort to observe and research the dynamics of churn transformation.

### Import Libraries:
We will use the follwoing libraries.
1. **Pandas:** Data manipulation and analysis library.
2. **Numpy:** Numerical computing library.
3. **Matplotlib:** Data visualization library.
4. **Seaborn:** Statistical data visualization library.
5. **Scipy:** To provide a comprehensive set of numerical algorithms and tools for scientific computing in Python.
6. **Shapely:** Shapely is a BSD-licensed Python package for manipulation and analysis of planar geometric objects.
7. **GeoPandas:** To make working with geospatial data in python easier.

### Glossary / Data Dictionary / Important Terms:
* **'VIN (1-10)':** The 1st 10 characters of each vehicle's Vehicle Identification Number (VIN).
* **'County':** The county in which the registered owner resides.
* **'City':** The city in which the registered owner resides
* **'State':** The state in which the registered owner resides
* **'Postal Code':** The 5 digit zip code in which the registered owner resides
* **'Model Year':** The model year of the vehicle, determined by decoding the Vehicle Identification Number (VIN)
* **'Make':** The manufacturer of the vehicle, determined by decoding the Vehicle Identification Number (VIN)
* **'Model':** The model of the vehicle, determined by decoding the Vehicle Identification Number (VIN).
* **'Electric Vehicle Type':** This distinguishes the vehicle as all electric or a plug-in hybrid.
* **'Clean Alternative Fuel Vehicle (CAFV) Eligibility':** This categorizes vehicle as Clean Alternative Fuel Vehicles (CAFVs) based on the fuel requirement and electric-only range requirement in House Bill 2042 as passed in the 2019 legislative session.

* **'Electric Range':** Describes how far a vehicle can travel purely on its electric charge.

* **'Base MSRP':** This is the lowest Manufacturer's Suggested Retail Price (MSRP) for any trim level of the model in question.
* **'Legislative District':** The specific section of Washington State that the vehicle's owner resides in, as represented in the state legislature.
* **'DOL Vehicle ID':** Unique number assigned to each vehicle by Department of Licensing for identification purposes.
* **'Vehicle Location':** The center of the ZIP Code for the registered vehicle.
* **'Electric Utility':** This is the electric power retail service territories serving the address of the registered vehicle. All ownership types for areas in Washington are included: federal, investor owned, municipal, political subdivision, and cooperative. If the address for the registered vehicle falls into an area with overlapping electric power retail service territories then a single pipe | delimits utilities of same TYPE and a double pipe || delimits utilities of different types. We combined vehicle address and Homeland Infrastructure Foundation Level Database (HIFLD) Retail_Service_Territories feature layer using a geographic information system to assign values for this field. Blanks occur for vehicles with addresses outside of Washington or for addresses falling into areas in Washington not containing a mapped electric power retail service territory in the source data.

* **'2020 Census Tract':** The census tract identifier is a combination of the state, county, and census tract codes as assigned by the United States Census Bureau in the 2020 census, also known as Geographic Identifier (GEOID)

## Exploratory Data Analysis and Visualization

![image](https://user-images.githubusercontent.com/43418706/236800592-801f7a6d-ab43-4965-a976-92eac5ea2e2b.png)

## Now exploring Numeric columns or attributes of the dataset mainly:
PostalCode, ModelYear, Electric_Range, Base_MSRP, DOL_Vehicle_ID

![image](https://user-images.githubusercontent.com/43418706/236800857-67568ca9-244d-4e7e-b327-1036265be335.png)

## Distribution of numerical variables
ModelYear, Electric_Range, Base_MSRP, DOL_Vehicle_ID

![image](https://user-images.githubusercontent.com/43418706/236801087-cdf42f2c-291d-4051-a6ab-e54eb397ebfa.png)

## Top 10 count of cars per county

![image](https://user-images.githubusercontent.com/43418706/236801436-1ad2edc4-6c2f-40ab-a2a1-293b4cdb58b7.png)

## Top 10 count of cars per city

![image](https://user-images.githubusercontent.com/43418706/236801631-121c6a28-b3a9-4bd2-b2b9-bf168266e78f.png)

## Top 10 count of cars per state

![image](https://user-images.githubusercontent.com/43418706/236801876-5fbf8074-b676-4637-ae48-cdedff3bbaf3.png)

## Top 10 count of cars per postal code

![image](https://user-images.githubusercontent.com/43418706/236802039-2c770011-7591-4bdd-9b41-9b4bfae14d27.png)

## Top 10 Make distribution count per top 10 County

![image](https://user-images.githubusercontent.com/43418706/236802178-ab802d5a-6f7a-4939-a204-5546110d2b80.png)

## Top 10 Make distribution count per top 10 City

![image](https://user-images.githubusercontent.com/43418706/236802426-9bbc780e-05e6-4304-9f08-5575cc6f8b7f.png)

## Top 10 Make distribution count per top 10 State

![image](https://user-images.githubusercontent.com/43418706/236802587-caa8b956-ef23-4b74-b675-5452e497481b.png)

## Electric Utility Distribution in top 10 cities with highest number of cars

![image](https://user-images.githubusercontent.com/43418706/236802794-fb000244-3b2c-4a60-ab10-3a83a5215e3c.png)

## Top 5 vs Bottom 5 Comparison

![image](https://user-images.githubusercontent.com/43418706/236803016-9cf32dc9-efa6-48a4-9118-92c8a3232d42.png)

## Distances Travel by vehicle make per electric charge

![image](https://user-images.githubusercontent.com/43418706/236803174-7523a53e-5b86-41b5-8b0d-f71349bf52ce.png)

## Year Wise Cars sales growth

![image](https://user-images.githubusercontent.com/43418706/236803357-8888a97b-a514-49f8-a758-b0df4645959b.png)

## Plotting the lat and lon

![image](https://user-images.githubusercontent.com/43418706/236803484-b22c712e-9588-4cb2-b33f-a414d7114657.png)


## Summary & Conclusion
The Electric Vehicle Population dataset contains information on Battery Electric Vehicles (BEVs) and Plug-in Hybrid Electric Vehicles (PHEVs) registered through the Washington State Department of Licensing (DOL). Through exploratory data analysis, the top 10 counts of cars per county, city, state, and postal code were determined. King County had the most cars registered, followed by Snohomish and Pierce counties. Seattle had the most cars registered by city, followed by Bellevue and Redmond. Washington had the most cars registered by state, followed by California and Virginia.

The dataset also provided insight into the top 10 consumed car makers by county, city, and state, with Tesla being the most popular make overall. There appears to be an opportunity for car vendors like Audi and BMW to market their vehicles in other states. The top 10 postal codes were also identified, providing further insight for marketing and upselling opportunities.

![image](https://user-images.githubusercontent.com/43418706/236803558-ec970653-049a-4e08-b1ec-90690db23b45.png)

  To Conclude:

* King County has the highest number of electric cars registered with 65,268 cars, followed by Snohomish and Pierce County.
* Seattle is the city with the highest number of electric cars with 22,009 cars, followed by Bellevue and Redmond.
* Washington state has the highest number of electric cars with 1,24,419 cars, followed by California, Virginia, and Maryland.
* The top 10 postal codes with the highest number of electric cars are in the Seattle metro area, with 98052 having the most with 3,247 cars.
* Tesla is the most popular electric car maker in Washington state, followed by Nissan, Chevrolet, and Toyota.
* Tesla is also the most popular maker in Seattle, followed by Nissan, Chevrolet, and BMW.
* Washington state has the highest number of Audi, BMW, and Chevrolet electric cars registered among all states.
* There is a big marketing opportunity for car vendors like Audi, BMW, and Chevrolet in other states, such as Arizona, Florida, and Colorado.
