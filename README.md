# [Resume Project Challenge - 12](https://codebasics.io/challenge/codebasics-resume-project-challenge)

### Provide Insights to an Automotive company on Electric vehicles launch in India



## Overview:
AtliQ Motors, a leading EV manufacturer from the USA with a 25% market share in North America, plans to expand into the Indian market where their share is currently below 2%. To support this expansion, the head of AtliQ Motors India, has tasked the data analytics team, with conducting an in-depth market analysis of the EV/Hybrid vehicle sector in India.

## Table of Contents:

- [Project Presentation](#project-presentation)
- [Live Dashboard](#live-dashboard)
- [Tools & Technique used](#tools--technique)
- [Problem Statement](#problem-statement)
- [Goal & Purpose](#goal--purpose)
- [Data Source](#data-source)
- [Data Modeling](#data-modeling)
- [Key Metrics](#key-metrics)
- [Dashboard Overview](#dashboard-overview)
- [Insights & Recommendations](#insights-and-recommendations)


## Project Presentation:

<p align="center">
<a href="https://youtu.be/PaqcTxLJ4WI" target="_blank">
  <img src="https://raw.githubusercontent.com/PuranjoyPatra/DA_Resume_Project_Challenge12/master/Image/RPC-video-thumbnail.png" alt="Presentation Preview" style="width: 70%; max-width: 360px;">
  
</a>
</p>

## Live Dashboard:

Checkout the live dashboard here 👉🏻 [Live Dashboard](https://app.powerbi.com/view?r=eyJrIjoiZWM1OGI0NTctNmNjNC00N2JiLTk0NzAtOTg5NGQ3ZTMxMjI3IiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9&pageName=745d12dc2a5d28f2ed93)


## Tools & Technique:
- Data Analysis
   - Microsoft Excel (v 2021)
   - Microsoft Power BI Desktop (v July2024)
   - Power BI Service
   - Power Query
   - Data Modeling
   - DAX (Data Analysis Expression)
   - ETL (Extract, Transformation & Load)

- Project Documentation
   - Git & Github
   - VS Code Editor

- Video Recording & Presentation
   - OBS Studio
   - Microsoft Clipchamp - Video Editor
   - Microsoft Power Point

## Problem Statement:
AtliQ Motors is an automotive giant from the USA specializing in electric vehicles 
(EV). In the last 5 years, their market share rose to 25% in electric and hybrid 
vehicles segment in North America. As a part of their expansion plans, they wanted 
to launch their bestselling models in India where their market share is less than 2%.

Bruce Haryali, the chief of AtliQ Motors India wanted to do a detailed market study 
of existing EV/Hybrid market in India before proceeding further. Bruce gave this task 
to the data analytics team of AtliQ motors and Peter Pandey is the data analyst 
working in this team.

## Goal & Purpose:
- To conduct a comprehensive market study on the existing EV/Hybrid vehicle landscape in India, enabling AtliQ Motors to make informed decisions regarding their market entry and expansion strategies. 

- This analysis will provide insights into consumer preferences, competitive positioning, and market growth opportunities to increase AtliQ Motors' market share in India beyond 2%.


## Data Source:

The datasets include sales by state, sales by maker, and a date dimension table are provided by Codebasics.

<p align="center"> Preview </p>


  <p align="center">
    <img src="https://raw.githubusercontent.com/PuranjoyPatra/DA_Resume_Project_Challenge12/master/Image/date_table_view.png" alt="Date Table View" >
  </p>

  <p align="center">
    <img src="https://raw.githubusercontent.com/PuranjoyPatra/DA_Resume_Project_Challenge12/master/Image/ev_sales_by_maker_table_view.png" alt="EV Sales by Maker Table View">
  </p>

  <p align="center">
    <img src="https://raw.githubusercontent.com/PuranjoyPatra/DA_Resume_Project_Challenge12/master/Image/ev_sales_by_state_table_view.png" alt="EV Sales by State Table View">
  </p>

<p align="center"> Meta Data details </p>

&rarr; dim_date

- date: The specific date for which the data is relevant. Format: DD-MMM-YY. (Data is recorded on a monthly basis)
- fiscal_year: The fiscal year to which the date belongs. This is useful for financial and business analysis.
- quarter: The fiscal quarter to which the date belongs. Fiscal quarters are typically divided as Q1, Q2, Q3, and Q4.

&rarr; electric_vehicle_sales_by_makers

- date: The date on which the sales data was recorded. Format: DD-MMM-YY. (Data is recorded on a monthly basis)
- vehicle_category: The category of the vehicle, specifying whether it is a 2-Wheeler or a 4-Wheeler.
- maker: The name of the manufacturer or brand of the electric vehicle.
- electric_vehicles_sold: The number of electric vehicles sold by the specified maker in the given category on the given date.

&rarr; electric_vehicle_sales_by_state

- date: The date on which the data was recorded. Format: DD-MMM-YY. (Data is recorded on a monthly basis)
- state: The name of the state where the sales data is recorded. This indicates the geographical location within India.
- vehicle_category: The category of the vehicle, specifying whether it is a 2-Wheeler or a 4-Wheeler.
- electric_vehicles_sold: The number of electric vehicles sold in the specified state and category on the given date.
- total_vehicles_sold: The total number of vehicles (including both electric and non-electric) sold in the specified state and category on the given date.

> [!NOTE]
> These dataset is taken from [Vahan Sewa](https://vahan.parivahan.gov.in/vahan4dashboard/vahan/view/reportview.xhtml)


Additionally, I have added "EV Charging Station" dataset which is extracted from [Press Information Bureau (PIB)](https://pib.gov.in/PressReleaseIframePage.aspx?PRID=2003003). 

For building relationship between tables, i have created _**dim_state**_ and _**category**_ from existing tables in Power BI using DAX.

<p align="center"> Preview </p>

  <p align="center">
    <img src="https://raw.githubusercontent.com/PuranjoyPatra/DA_Resume_Project_Challenge12/master/Image/ev_charging_station_table_view.png" alt="Charging Station Table View">
  </p>

  <p align="center">
    <img src="https://raw.githubusercontent.com/PuranjoyPatra/DA_Resume_Project_Challenge12/master/Image/dim_state_table_view.png" alt="State Table View">
  </p>

  <p align="center">
    <img src="https://raw.githubusercontent.com/PuranjoyPatra/DA_Resume_Project_Challenge12/master/Image/category_table_view.png" alt="Category Table View">
  </p>


> [!IMPORTANT]
> Data is available from Fiscal Year 2022 to 2024. Charging Station data is available as per Feb, 2024. 

## Data Modeling
Here you can check the Data Model which is used for this project. In center you can see there are _Fact_ tables which are connected with different _Dimension_ tables. 

This Data Model is built as **STAR** schema structure.

<p align="center">
<img src="https://raw.githubusercontent.com/PuranjoyPatra/DA_Resume_Project_Challenge12/master/Data%20Model/Data-Model.png" alt="Data Model Preview" >
</p>

## Key Metrics:

### 1. **Penetration Rate**  

The penetration rate in EV analysis refers to the percentage of EVs among the total number of vehicles in a specific market or population. It helps in assessing the adoption level of electric vehicles relative to the entire vehicle population.

**Formula**:  

<p align="center">
<img src="https://raw.githubusercontent.com/PuranjoyPatra/DA_Resume_Project_Challenge12/master/Image/pr-formula.png" alt="PR Forrmula" >
</p>

### 2. **Compound Annual Growth Rate (CAGR)**  

CAGR measures the rate of return required for an investment to grow from its beginning balance to its ending balance, assuming the profits were reinvested at the end of each period. In the EV context, it is often used to measure the growth rate of EV adoption, sales, or charging infrastructure over a specific period.

**Formula**: 

<p align="center">
<img src="https://raw.githubusercontent.com/PuranjoyPatra/DA_Resume_Project_Challenge12/master/Image/cagr-formula.png" alt="CAGR Formula" >
</p>

Where:
- **EVs at End Period** = The number of EVs at the end of the time period.
- **EVs at Start Period** = The number of EVs at the start of the time period.
- **n** = The number of years.


## Dashboard Overview:

<p align="center"> Home Page </p>
<p align="center">
  <img src="https://raw.githubusercontent.com/PuranjoyPatra/DA_Resume_Project_Challenge12/master/Dashboard/home-page.png" alt="Home Page">
</p>

<p align="center"> <strong>Maker Page </strong></p>
<p align="center"> An overview of yearly Electric Vehicle sales performance, segmented by 2-Wheeler and 4-Wheeler categories, helps stakeholders identify trends, compare top-performing brands, and analyze market presence across makers..
 </p>

<p align="center">
  <img src="https://raw.githubusercontent.com/PuranjoyPatra/DA_Resume_Project_Challenge12/master/Dashboard/makers-view-page.png" alt="Maker Page">
</p>

<p align="center"><strong> State Page </strong></p>
<p align="center"> Analyzes EV adoption across Indian states, highlighting monthly 2-wheeler and 4-wheeler sales trends relative to total vehicle sales, helping assess regional policy impacts and identify leading states.
 </p>

<p align="center">
  <img src="https://raw.githubusercontent.com/PuranjoyPatra/DA_Resume_Project_Challenge12/master/Dashboard/state-view-page.png" alt="Sales Page">
</p>

<p align="center"><strong> Performance & Revenue Page </strong></p>
<p align="center"> Analyzes EV makers and state-wise sales performance, with revenue growth projections and estimated 2030 EV sales, available Charging Station, aiding industry trend forecasts and strategic planning
 </p>

<p align="center">
  <img src="https://raw.githubusercontent.com/PuranjoyPatra/DA_Resume_Project_Challenge12/master/Dashboard/Performance-Revenue-maker-page.png">
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/PuranjoyPatra/DA_Resume_Project_Challenge12/master/Dashboard/Performance-Revenue-state-page.png">
</p>


## Insights and Recommendations: 

<p align="center"> Preliminary Question </p>

1. List the top 3 and bottom 3 makers for the fiscal years 2023 and 2024 in terms of the number of 2-wheelers sold.

<p align="center" >2023: Top & Bottom 3 </p>

<p align="center">
  <img src="https://raw.githubusercontent.com/PuranjoyPatra/DA_Resume_Project_Challenge12/master/Insights/PQ1_A.png">
</p>

<p align="center" >2024: Top & Bottom 3 </p>

<p align="center">
  <img src="https://raw.githubusercontent.com/PuranjoyPatra/DA_Resume_Project_Challenge12/master/Insights/PQ1_B.png">
</p>



2. Identify the top 5 states with the highest penetration rate in 2-wheeler and 4-wheeler EV sales in FY 2024.

<p align="center">
<img src="https://raw.githubusercontent.com/PuranjoyPatra/DA_Resume_Project_Challenge12/master/Insights/PQ2.png">
</P>

3. List the states with negative penetration (decline) in EV sales from 2022 to 2024?

<p align="center">
  <img src="https://raw.githubusercontent.com/PuranjoyPatra/DA_Resume_Project_Challenge12/master/Insights/PQ3.png">
</p>

4. What are the quarterly trends based on sales volume for the top 5 EV makers (4-wheelers) from 2022 to 2024?

<p align="center">
  <img src="https://raw.githubusercontent.com/PuranjoyPatra/DA_Resume_Project_Challenge12/master/Insights/PQ4.png">
</p>

5. How do the EV sales and penetration rates in Delhi compare to Karnataka for 2024?

<p align="center">
  <img src="https://raw.githubusercontent.com/PuranjoyPatra/DA_Resume_Project_Challenge12/master/Insights/PQ5.png">
</p>

6. List down the compounded annual growth rate (CAGR) in 4-wheeler units for the top 5 makers from 2022 to 2024.

<p align="center">
  <img src="https://raw.githubusercontent.com/PuranjoyPatra/DA_Resume_Project_Challenge12/master/Insights/PQ6.png">
</p>

7. List down the top 10 states that had the highest compounded annual growth rate (CAGR) from 2022 to 2024 in total vehicles sold.

<p align="center">
  <img src="https://raw.githubusercontent.com/PuranjoyPatra/DA_Resume_Project_Challenge12/master/Insights/PQ7.png">
</p>

8. What are the peak and low season months for EV sales based on the data from 2022 to 2024?

<p align="center" >Overall </p>

<p align="center">
  <img src="https://raw.githubusercontent.com/PuranjoyPatra/DA_Resume_Project_Challenge12/master/Insights/PQ8_A.png">
</p>

<p align="center" >Fiscal Year wise </p>

<p align="center">
  <img src="https://raw.githubusercontent.com/PuranjoyPatra/DA_Resume_Project_Challenge12/master/Insights/PQ8_B.png">
</p>

9. What is the projected number of EV sales (including 2-wheelers and 4-wheelers) for the top 10 states by penetration rate in 2030, based on the compounded annual growth rate (CAGR) from previous years?

<p align="center">
  <img src="https://raw.githubusercontent.com/PuranjoyPatra/DA_Resume_Project_Challenge12/master/Insights/PQ9.png">
</p>

10. Estimate the revenue growth rate of 4-wheeler and 2-wheelers EVs in India for 2022 vs 2024 and 2023 vs 2024

<p align="center">
  <img src="https://raw.githubusercontent.com/PuranjoyPatra/DA_Resume_Project_Challenge12/master/Insights/PQ10.png">
</p>

<p align="center"> Secondary Research Questions </p>

#### 1. What are the primary reasons for customers choosing 4-wheeler EVs in 2023 and 2024?

   - **Environmental Concerns**

      - _**Pollution in Urban Areas:**_ Major cities in India, such as Delhi, Mumbai, and Bengaluru, face severe air pollution problems. Consumers are becoming more aware of the impact of vehicular emissions on air quality and climate change. This has led to a rising preference for EVs, which contribute to cleaner air by reducing local pollutants.

      - _**Government Push for Clean Energy:**_ The Indian government’s focus on renewable energy sources, such as solar and wind, aligns with the push for EV adoption, as more people look to reduce their dependency on fossil fuels.

   - **Cost Savings**

      - _**Lower Running Costs:**_ Electricity in India is significantly cheaper than petrol or diesel, making EVs more economical for daily commuting. As fuel prices fluctuate and often remain high, the stable and lower cost of electricity is a big draw for Indian consumers.

      - _**Maintenance Advantages:**_ With fewer mechanical parts, the cost of maintaining EVs is lower in India compared to traditional internal combustion engine vehicles. This is particularly appealing in cities where traffic conditions can lead to more frequent vehicle repairs.

      - _**Savings from Subsidies:**_ The central and state governments offer various incentives like reduced GST rates, subsidies on EV purchases, and tax benefits, making EV ownership more affordable for the average consumer.

   - **Government Incentives**

      - _**FAME II Scheme (Faster Adoption and Manufacturing of Hybrid and Electric Vehicles):**_ The FAME II scheme offers subsidies to promote the adoption of electric vehicles in India. Under this initiative, customers receive financial incentives, making the upfront cost of EVs more competitive with traditional vehicles.

      - _**State-Level Incentives:**_ States like Delhi, Maharashtra, Gujarat, and Tamil Nadu have additional incentives, such as reduced road taxes, registration fee waivers, and direct purchase subsidies. These benefits make EVs a more attractive option in those regions.

      - _**Incentives for Charging Infrastructure:**_ Alongside vehicle incentives, the government is supporting the expansion of charging infrastructure, making it easier for Indian consumers to transition to EVs without range anxiety.

   - **Technological Advancements**

      - _**Affordable Battery Technology:**_ In India, the price of lithium-ion batteries has steadily decreased, which directly reduces the cost of EVs. This affordability is critical for attracting the price-sensitive Indian market.

      - _**Expanding Charging Network:**_ The Indian government and private companies are working together to increase the availability of EV charging stations, particularly in urban areas and along highways, making EV ownership more convenient.

      - _**Smart Features and Connectivity:**_ Indian consumers, especially in metropolitan areas, are drawn to the advanced features of EVs, such as internet connectivity, app-based vehicle control, and real-time vehicle monitoring. These features cater to the tech-savvy, younger demographic.

   - **Variety and Availability of EV Models**

      - _**Growing Model Options:**_ Indian consumers now have access to a wider range of EV models, including budget-friendly options like Tata Nexon EV, MG ZS EV, and Mahindra XUV400. As automakers introduce more models catering to different price segments, consumers are finding EVs that suit their needs and budgets.

      - _**Local Manufacturing and Assembly:**_ Many global and Indian automakers are investing in local production and assembly of EVs in India, reducing costs and boosting availability. Companies like Tata Motors and Mahindra are leading the charge, making EVs more accessible to the Indian market.

      - _**Partnerships and Collaborations:**_ Collaborations between automakers and tech firms are enhancing the variety of EVs available. These partnerships bring in new innovations, such as faster charging and better range, helping to cater to the specific demands of Indian consumers.


#### 2. How do government incentives and subsidies impact the adoption rates of 2-wheelers and 4-wheelers? Which states in India provided most subsidies?

&rarr; Government incentives and subsidies have significantly boosted the adoption of both 2-wheelers and 4-wheelers in India's EV market. The FAME II scheme offers substantial subsidies, covering up to 40% of 2-wheeler costs and up to ₹1.5 lakh for 4-wheelers, driving sales growth.

**2-Wheelers:** Affordable and with high subsidies, 2-wheeler EVs have gained quick traction, supported by reduced battery costs and rising range capabilities.

**4-Wheelers:** Adoption has been slower but is gaining momentum, particularly for fleet use, with doubling sales in 2023. Subsidies, while capped at ₹15 lakh vehicle price, still make a notable difference.


<p align="center">
  <img src="https://raw.githubusercontent.com/PuranjoyPatra/DA_Resume_Project_Challenge12/master/Insights/SQ1.png">
</p>


#### 3. How does the availability of charging stations infrastructure correlate with the EV sales and penetration rates in the top 5 states?

<p align="center">
  <img src="https://raw.githubusercontent.com/PuranjoyPatra/DA_Resume_Project_Challenge12/master/Insights/SQ2.png">
</p>

- Correltion Efficient:

   - EV Sales and Charging Station - ~0.90
   - PR% and Charging Station - ~0.52

According to value, clearly it is showing that availability of charging stations infrastructure is _**Positively**_ correlate with the EV sales and penetration rates.


#### 4. Who should be the brand ambassador if AtliQ Motors launches their EV/Hybrid vehicles in India and why?


<p align="center">
  <img src="https://raw.githubusercontent.com/PuranjoyPatra/DA_Resume_Project_Challenge12/master/Image/msd.png" width="30%">
</p>

> As my opinion, _**MS Dhoni**_ as a brand ambassador would be an excellent choice for AtliQ Motors' EV/Hybrid vehicles in India
   
   **Reason:**

   - **Wide Appeal and Popularity**:
   MS Dhoni is a revered and highly influential figure in India, known for his remarkable achievements in cricket. His widespread popularity and strong fan base span across diverse demographics, making him an ideal ambassador to engage a broad audience. By associating with Dhoni, the new EV company can leverage his popularity to build trust and attract potential customers from various segments of the market.

- **Alignment with EV Values**:
   Dhoni’s interest in vehicles, including electric ones, resonates with the core values of innovation and sustainability that are central to the EV industry. His genuine affinity for advanced automotive technology reinforces the company’s commitment to environmental responsibility and cutting-edge solutions. This alignment ensures that his endorsement feels authentic and credible to consumers who value these principles.

- **Positive Impact on Consumer Perception**:
   An endorsement from Dhoni can significantly enhance the brand’s credibility and appeal. His association with the company can reassure environmentally conscious consumers that AtliQ Motors' EVs and hybrids are a trustworthy and desirable choice. Dhoni’s reputation for integrity and success can positively influence consumer perceptions, encouraging them to consider the brand for their next vehicle purchase.

- **Significant Media Presence**:
   Dhoni’s extensive media coverage and massive social media following provide a powerful platform for generating buzz and increasing visibility for the new EV launch. His involvement can drive significant media attention and social media engagement, creating a ripple effect that elevates the brand’s profile and stimulates interest in its offerings. His ability to capture public attention can be a key asset in establishing the brand’s presence in a competitive market.


#### 5. Which state of India is ideal to start the manufacturing unit?

<p align="center">
  <img src="https://raw.githubusercontent.com/PuranjoyPatra/DA_Resume_Project_Challenge12/master/Image/maharashtra-landscape.png" width="50%">
</p>

> Based on below reason, I would like to say _**Maharashtra**_ would be a ideal state of India to start manufacturing unit.

Reason:

- **Stability:** 

   &rarr; Known for its political and economic stability, Maharashtra offers a conducive environment for large-scale industrial projects.

- **Ease of Doing Business:** 

   &rarr; Ranked among the top states for ease of doing business with robust infrastructure and strong industrial presence.

- **Subsidies & Incentives:**

   &rarr; Offers generous incentives for EV manufacturing under its EV policy, including capital subsidies, power tariff incentives, and land allotment assistance.

#### 6. My top 3 recommendations for AtliQ Motors

+ **Pioneer in the 2-Wheeler EV Segment**:

   Launching electric vehicles (EVs) specifically in the 2-wheeler segment can be a strategic move, given that this category captures approximately 91% of the total EV market share in India. Being a first mover in this segment can provide a competitive advantage and establish a strong market presence.

+ **Invest in R&D and Charging Infrastructure**:

   Focus on research and development to create innovative designs and features that differentiate your EVs from competitors. Simultaneously, invest in developing a robust charging station infrastructure to enhance the availability and convenience of charging options. This dual approach will not only attract customers but also support the growth of the EV market in both 2-wheeler and 4-wheeler segments.

+ **Targeted Manufacturing and Production**:

   Strategically focus on manufacturing and production in specific states with high demand and potential for growth. This targeted approach will optimize production efficiency and address regional market needs effectively, positioning the company for revenue growth and operational success.