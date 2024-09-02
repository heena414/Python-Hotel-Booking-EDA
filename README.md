# Hotel Booking Analysis
<br /> 
<div align="center" style="margin-bottom: 20px;">
    <img src="/assets/hotel.png" height="500px" width="auto" style="display:block; margin-bottom: 20px;" />
</div>
<br /> 

## Business Problem

In recent years, both city hotels and resort hotels have experienced high cancellation rates, leading to significant challenges such as reduced revenue and suboptimal room occupancy. This situation demands urgent attention, as reducing cancellation rates is crucial for improving revenue generation. Our goal is to offer comprehensive business advice to tackle this issue effectively.

## Objective

The primary objective of this analysis is to perform exploratory data analysis (EDA) on the given hotel booking dataset. By uncovering general trends and interactions between factors governing hotel bookings, we aim to determine the best strategies for maximizing bookings and minimizing cancellations. Ultimately, this will help identify the optimal time for booking and improve overall hotel efficiency.

## Data Overview

The dataset contains detailed information on various aspects of hotel bookings, including:

- **hotel**: Name of the hotel (City or Resort)
- **is_canceled**: Whether the booking was canceled (0 for not canceled, 1 for canceled)
- **lead_time**: Time (in days) between the booking transaction and actual arrival
- **arrival_date_year**: Year of arrival
- **arrival_date_month**: Month of arrival
- **arrival_date_week_number**: Week number of the arrival date
- **arrival_date_day_of_month**: Day of the month of arrival
- **stays_in_weekend_nights**: Number of weekend nights spent in the hotel
- **stays_in_week_nights**: Number of weeknights spent in the hotel
- **adults**: Number of adults in a single booking record
- **children**: Number of children in a single booking record
- **babies**: Number of babies in a single booking record
- **meal**: Type of meal chosen
- **country**: Country of origin of customers
- **market_segment**: Segment via which the booking was made and its purpose
- **distribution_channel**: Medium through which the booking was made
- **is_repeated_guest**: Whether the customer has made any bookings before (0 for No, 1 for Yes)
- **previous_cancellations**: Number of previous canceled bookings
- **previous_bookings_not_canceled**: Number of previous non-canceled bookings
- **reserved_room_type**: Room type reserved by the customer
- **assigned_room_type**: Room type assigned to the customer
- **booking_changes**: Number of booking changes made by the customer
- **deposit_type**: Type of deposit at the time of booking (No deposit/Refundable/No refund)
- **agent**: ID of the booking agent
- **company**: ID of the company making the booking
- **days_in_waiting_list**: Number of days on the waiting list
- **customer_type**: Type of customer (Transient, Group, etc.)
- **adr**: Average Daily Rate
- **required_car_parking_spaces**: Number of car parking spaces requested in the booking
- **total_of_special_requests**: Total number of special requests
- **reservation_status**: Whether the customer has checked out, canceled, or did not show up
- **reservation_status_date**: Date of the reservation status

## Data Preparation and Cleaning

Before conducting the analysis, the data underwent several cleaning and preprocessing steps:

1. **Handling Missing Values**:
   - The `company` column had 112,593 missing values, which were replaced with 0.
   - The `agent` column had 16,340 missing values, which were also replaced with 0.
   - The `country` column contained missing values that could not be set to 0 due to their significance. Instead, the missing values were replaced with the mode (most frequent) value of the column.
   - The `children` column's missing values were replaced with the mean value.

2. **Dropping Irrelevant Rows**:
   - Rows containing no adults, children, or babies were removed, as they did not provide meaningful information.

3. **Data Type Conversion**:
   - The data types of relevant columns were checked and converted to appropriate formats (e.g., converting data types to `int64`).

## Exploratory Data Analysis (EDA)

### Key Questions Explored:

1. **Which type of hotel books more (City Hotel or Resort Hotel)?**
   - Analysis revealed that city hotels are more frequently booked compared to resort hotels.

2. **How many bookings were canceled?**
   - A significant proportion of bookings, around one-fourth of the total, were canceled.

3. **In which week number are stays more common?**
   - Stays were found to peak during specific weeks, particularly around holiday seasons.

4. **Which month has the highest number of rooms booked?**
   - The months of July and August saw the highest number of room bookings.

5. **How many guests are repeated guests?**
   - A notable number of bookings came from repeat guests, particularly from the corporate sector.

6. **Market segment-wise booking?**
   - Most bookings were made through the corporate segment, indicating a strong relationship between hotels and businesses.

7. **From which country do people book more rooms?**
   - The majority of bookings were made by guests from Portugal and Great Britain.

## Additional Analysis on Hotel Booking Insights

### Insight 1: Understanding Data Distributions for Better Decision-Making

- **Key Observation**: Analyzing histograms reveals no immediate threats to growth, but it highlights the importance of understanding data distributions. By identifying outliers, especially in pricing, hotels can avoid setting unrealistic rates that might deter potential customers.
- **Business Implication**: Recognizing pricing outliers can prevent negative customer reactions and optimize pricing strategies to enhance bookings.

### Insight 2: Impact of Reservation Cancellations

- **Key Observation**: The bar graph shows a significant cancellation rate, with 37% of reservations being canceled. This poses a considerable challenge to the hotel’s revenue generation.
- **Business Implication**: The high cancellation rate directly impacts earnings, emphasizing the need for strategies to reduce cancellations, such as flexible pricing, better customer engagement, or cancellation policies.

### Insight 3: City Hotels vs. Resort Hotels Bookings

- **Key Observation**: City hotels have a higher booking rate compared to resort hotels, likely due to the higher costs associated with resort stays.
- **Business Implication**: Resort hotels may need to re-evaluate their pricing structures or offer special promotions to increase their competitiveness against city hotels.

### Insight 4: Average Daily Rate (ADR) Trends

- **Key Observation**: The line graph shows that ADR for city hotels is generally lower than resort hotels, but this gap widens on weekends and holidays, indicating price surges in resort hotels during these periods.
- **Business Implication**: Resort hotels might explore dynamic pricing models or off-peak discounts to maintain a steady flow of bookings throughout the week.

### Insight 5: Monthly Reservation Patterns

- **Key Observation**: The grouped bar graph highlights that August has the highest number of both confirmed and canceled reservations, while January sees the most cancellations.
- **Business Implication**: Hotels could focus marketing efforts and special promotions in August to maximize confirmed bookings, while addressing the factors leading to high cancellations in January through targeted campaigns.

### Insight 6: Price Sensitivity and Cancellations

- **Key Observation**: The bar graph reveals that cancellations are most frequent when prices are highest and least common when prices are lowest.
- **Business Implication**: This reinforces the need for pricing strategies that balance profitability with affordability, potentially reducing cancellations during peak pricing periods.

### Insight 7: Weekday vs. Weekend Bookings

- **Key Observation**: The violin chart shows lower customer rates during certain weeks.
- **Business Implication**: Hotels could implement more advertising and offer discounts during these periods to attract more customers and optimize occupancy.

### Insight 8: Performance of Booking Agents

- **Key Observation**: Analysis of top-performing agents can help hotels incentivize these agents to drive further bookings. Conversely, identifying underperforming agents could prompt strategic decisions regarding partnerships.
- **Business Implication**: Hotels should focus on strengthening relationships with top agents while considering improvements or alternatives for less effective agents.

### Insight 9: Country-Specific Cancellations

- **Key Observation**: Portugal (PRT) has the highest number of cancellations.
- **Business Implication**: Hotels should investigate the reasons behind this trend and consider tailored strategies to reduce cancellations from customers in Portugal, such as improving service quality or offering location-specific incentives.

### Insight 10: Customer Booking Channels

- **Key Observation**: Around 46% of clients book through travel agencies, 27% through groups, and only 4% book directly.
- **Business Implication**: Direct bookings are minimal, suggesting an opportunity to boost direct sales through enhanced online presence, customer loyalty programs, and exclusive offers.

### Insight 11: Meal Offerings and Repeat Orders

- **Key Observation**: Enhancing the quality and variety of meal offerings could encourage repeat orders and attract new customers.
- **Business Implication**: Improving culinary services could lead to higher customer satisfaction, potentially reducing cancellations and boosting repeat business.

## Conclusion

1. **Repeated Guests**:
   - The majority of repeated guests come from the corporate sector, highlighting the importance of maintaining strong business relationships.

2. **City Hotels**:
   - City hotels are more popular among travelers and generate more revenue compared to resort hotels. They also have a higher retention rate for guests.

3. **Stay Duration**:
   - Most guests tend to stay for 3-4 days, indicating that hotels should focus on optimizing services for this duration.

4. **Peak Booking Months**:
   - July and August are the peak months for bookings. Hotels should prepare for high demand during these months to maximize revenue.

5. **Preferred Room Type**:
   - Room Type A is the most popular choice among guests, suggesting that hotels should prioritize the availability of this room type.

## Recommendations

1. **Developing a cancellation strategy**:
   - With a 37% cancellation rate, hotels should implement strategies such as flexible pricing, better customer engagement, and cancellation policies to minimize cancellations.

2. **Targeting the Right Audience**:
   - Hotels should focus marketing efforts on countries with the highest booking rates and address the needs of repeated guests from the corporate sector.

3. **Optimizing Room Availability**:
   - Prioritize the availability of Room Type A to meet guest preferences and ensure higher booking rates.

4. **Preparing for Peak Months**:
   - Hotels should be fully prepared for the high demand in July and August, with strategies to maximize revenue during these months.

By implementing these strategies and focusing on data-driven decision-making, hotels can enhance their performance and achieve better outcomes in the highly competitive hospitality industry.
