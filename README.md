### Project coupons
### Overview
This data analysis focuses on answering the question “Will a customer accept the coupon?” 
The project uses visualizations and probability distributions to distinguish between customers who accepted a driving coupon versus those that did not, emphasizing coupons for bars and coffee houses.
### Data:
This data comes to us from the UCI Machine Learning repository and was collected via a survey on Amazon Mechanical Turk. The survey describes different driving scenarios, including the destination, current time, weather, passenger, etc., and then asks people whether they will accept the coupon if they are the driver. Answers given that the users will drive there “right away” or “later before the coupon expires” are labeled as “Y = 1”, and answers “no, I do not want the coupon” are labeled as “Y = 0”. There are five different types of coupons—less expensive restaurants (under $20), coffee houses, carry out and take away, bars, and more expensive restaurants ($20–$50).

### Summary of the Data Analysis on the coupons dataset
- [Data Cleaning and Transformations](#data-cleaning-and-transformations)
- [Exploring the dataset](#exploring-the-dataset)
- [Exploring Bar coupons acceptance](#exploring-bar-coupons-acceptance)
- [Exploring Coffee House acceptance](#exploring-coffee-house-acceptance)
- [Next Steps](#next-steps)

### Data Cleaning and Transformations
- First steps was to identify duplicates, 74 records were dups
- Next dropped the duplicates from the datafram keeping the latest
- Checked for missing data and plot this information
- Analyze the null values
- Dropped records with no driver or driving a scooter or a motocycle
- Finally, removed extra characters from age and converted it to numeric
  
### Exploring the dataset
- 57% of the drivers of the total of observations accepted the coupons
- The number of coupons from biggest to smallest was distributed to coffee house, restaurant < 20, carry out & take away, bar, and restaurant from 20 to 50
- Comparing acceptance and rejected restaurant < 20 has the highest acceptance with 70%, the second one was coffee house with 49% acceptance
- More coupons were distributed on temperatures of >80 degrees and also those had higher acceptance
- Time category presented interested data for the best timing for acceptance was at 7 am and 6 pm, before the dat starts and after work or school
- As expected younger people had a higher coupon acceptance at the ages of 21 and 25

### Exploring Bar coupons acceptance
- Bar coupons for highest to lowest acceptance 1~3 times a month, less than 1, never, 4~8 times, and more than 8. The data shows that regulars will be in the bar with coupons or without.
- 41% of the drivers accepted the bar coupons
- The acceptance rate is 4.4 times higher for those who visit the bar 3 or fewer times a month
- The acceptance rate between drivers who go to a bar more than once a month and are over the age of 25 to all others is: 1.174. So most of the drivers who accepted the coupons are over 25 years old and go more that once to a bar. Even though the acceptance on drivers who are 21 years old is high, the sum all others is higher as we can see on the age graph above
- The acceptance rate is high for drivers with no kids and no farmers, fishermen, and foresters (0.965). Makes sense since kids cannot enter a bar at least in the US. It will be good to compare the occupation distribution for have input on farmers and fishermen

### Exploring Coffee House acceptance 
- The proportion of coupons accepted for coffee house was 49.9%
- The drivers who went 3 or less times a month took 2.3 more coupons than the drivers who went 4 or more times a month
- Drivers with not urgent destination accepted more coupons that drivers with destination work
- Drivers with destination home or work accepted more coupons that drivers with no urgent destination

### Next Steps
- Include some visualization including the acceptance, coupons, and some categories. I.e. including acceptance for restaurants under 20 and income
- Include acceptance rate including age and income for bar and restaurant
- Add acceptance for “to go” coupons and destination adding passenger
- Use aggregations and groupby from coupons throughout all 1~3, less1, .. and the categories i.e age, income, education, etc
