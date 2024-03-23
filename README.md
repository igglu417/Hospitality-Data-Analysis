# Hospitality-Data-Analysis
![image](https://github.com/igglu417/Hospitality-Data-Analysis/assets/54131004/2063667d-acf7-4797-9130-6f1baf50acb7)

## DATA MODEL:
![image](https://github.com/igglu417/Hospitality-Data-Analysis/assets/54131004/1b9eb1d1-acb9-4b25-bb17-2ac9e0766198)

## STEPS AND ANALYSIS
1. Install Power Bi from web browser
2. Upload the the folder consisting of data folders(csv files)
3. Perform EDA:
	1. Make first row as head in every table
	2. Remove 'mmm yy' from dim_datefor visual clarity
	3. Used Filled up to add dummy data to ratings_given column in fact_booking
	4. Change data type of revenue holding column to currency
4. Data Analysis & Visualization
	1. Create measure for total realized revenue using DAX and placed on  card
			Total Realized Revenue = SUM(fact_bookings[revenue_realized])
	2. Create measure for total bookings and placed on  card
		Total Bookings = DISTINCTCOUNT(fact_bookings[booking_id])
	3. 	Create measure for average rating and placed on  card
		Average Rating = AVERAGE(fact_bookings[ratings_given])
	4. Create measure for Total capacity and placed on  card
		Total Capacity = SUM(fact_aggregated_bookings[capacity])
	
	5. Create measure for total successful bookings and placed on card
		
	6. 
	
	7. Create measure for occupancy percentage and placed on card
		Occupancy % = CALCULATE(([Total Bookings]/[Total Capacity])*100)
	8. Create measure to check how many 5 ratings are received by differernt hotels
		Top Rated Hotels = CALCULATE(COUNTROWS(fact_bookings),fact_bookings[ratings_given] = 5)
		
## Major Insights:
- Total 70.15% of bookings status are checked out, 24.83% are cancelled and remaiming are no show
- Elite-class room has the highest share of booking with 36.78% and standard room with 28.75%
- Top Rated hotel is GDS Blu with 9.8K 5 rating
- Mumbai is major contributor to revenue i.e, 0.67 Billion
- Highest revenue was generated in the month of May
- 'Other' as the booking platform contributed most with 55K bookings
- Luxury category had more booking than business category which is 85K
- Weekday had more bookings than weekend with 84K bookings but weekend had more occupancy.

## Recommendations		
- Focus more on Elite and standard calss rooms. Discount and complementary breakfast can be given to attract more successful bookings
- Promote GDS Blu and GDS Exotica more
- Enhance the the quality of GDS seasons and GDS Grand to increase rating
- Focus on 'Other', 'makeyourtrip' and 'logtrip' platforms to get more bookings
- Emphasize efforts on promoting and selling luxury category	
- To increase bookings provide more discounts on weekends and weekdays		
		
		
		
		
		
		
		
