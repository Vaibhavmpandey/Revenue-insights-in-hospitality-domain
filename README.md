# Revenue-insights-in-hospitality-domain

## Prolem Statement
### A hotel chain company noticed a loss in their market share and revenue over a few months. To understand the cause of this loss, they needed a way to analyze this.

## Solution
Three months of data is taken for creating a dashboard in Power BI to visualize the performance of the hotels overall, filtered by city and individual hotels as well.
![image](https://user-images.githubusercontent.com/117555175/232653718-6c0f1860-c6de-4bd2-8d2c-4d07d55fcc72.png)
![image](https://user-images.githubusercontent.com/117555175/232656921-e55f285d-b5cd-4e3d-9fab-c62aebb6397e.png)
![image](https://user-images.githubusercontent.com/117555175/232657020-fb5c310d-5d6d-4589-b039-d08053b415e5.png)
![image](https://user-images.githubusercontent.com/117555175/232657183-40f0050e-c84e-4c24-a1f3-361be5488d46.png)
![image](https://user-images.githubusercontent.com/117555175/232657361-799c7171-838f-4a89-9c67-6eaf6d35f5b2.png)
![image](https://user-images.githubusercontent.com/117555175/232657468-34a56f3c-4c90-4be4-a367-22b6d5820271.png)
![image](https://user-images.githubusercontent.com/117555175/232657592-d7f83b3b-4230-4b95-9b51-daa2bc7decca.png)




## Steps involved
1- Data cleaning in SQL  
2- Data transformation in Power BI  
3- Creating Measures  
4- Dashboarding  

### Note
For Hospitality industry weekend is considered on Friday and Saturday  

## Important observations
1- From this dashboard we can come to a conclusion that this hotel chain is not using dynamic pricing so to increase its revenue we can have dynamic pricing based on weekday/weekend.  
2- To incease the booking from Hotels own website they can provide some discount coupons.  
3- For the hotels whoose occupancy is very low we can see that the average rating for them is also very low, so in that case they have to look for the feedbacks by customers and then analyze it further to increase the services so as to increase its rating.   

## Column details  
This file contains all the meta information regarding the columns described in the CSV files.  
1. dim_date  
2. dim_hotels  
3. dim_rooms  
4. fact_aggregated_bookings  
5. fact_bookings  


### Column Description for dim_date:  
1. date: This column represents the dates present in May, June and July.  
2. mmm yy: This column represents the date in the format of mmm yy (monthname year).  
3. week no: This column represents the unique week number for that particular date.  
4. day_type: This column represents whether the given day is Weekend or Weekeday.  



### Column Description for dim_hotels:  
1. property_id: This column represents the Unique ID for each of the hotels.  
2. property_name: This column represents the name of each hotel.  
3. category: This column determines which class[Luxury, Business] a particular hotel/property belongs to.   
4. city: This column represents where the particular hotel/property resides in.  



### Column Description for dim_rooms:  
1. room_id: This column represents the type of room[RT1, RT2, RT3, RT4] in a hotel.  
2. room_class: This column represents to which class[Standard, Elite, Premium, Presidential] particular room type belongs.  


### Column Description for fact_aggregated_bookings:  
1. property_id: This column represents the Unique ID for each of the hotels.  
2. check_in_date: This column represents all the check_in_dates of the customers.  
3. room_category: This column represents the type of room[RT1, RT2, RT3, RT4] in a hotel.  
4. successful_bookings: This column represents all the successful room bookings that happen for a particular room type in that hotel on that particular date.  
5. capacity: This column represents the maximum count of rooms available for a particular room type in that hotel on that particular date.  



### Column Description for fact_bookings:  
1. booking_id: This column represents the Unique Booking ID for each customer when they booked their rooms.  
2. property_id: This column represents the Unique ID for each of the hotels  
3. booking_date: This column represents the date on which the customer booked their rooms.  
4. check_in_date: This column represents the date on which the customer check-in(entered) at the hotel.  
5. check_out_date: This column represents the date on which the customer check-out(left) of the hotel.  
6. no_guests: This column represents the number of guests who stayed in a particular room in that hotel.  
7. room_category: This column represents the type of room[RT1, RT2, RT3, RT4] in a hotel.  
8. booking_platform: This column represents in which way the customer booked his room.  
9. ratings_given: This column represents the ratings given by the customer for hotel services.  
10. booking_status: This column represents whether the customer cancelled his booking[Cancelled], successfully stayed in the hotel[Checked Out] or booked his room but not stayed in the hotel[No show].  
11. revenue_generated: This column represents the amount of money generated by the hotel from a particular customer.  
12. revenue_realized: This column represents the final amount of money that goes to the hotel based on booking status. If the booking status is cancelled, then 40% of the revenue generated is deducted and the remaining is refunded to the customer. If the booking status is Checked Out/No show, then full revenue generated will goes to hotels.  

  
