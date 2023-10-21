# Hotel_Reservations

Dataset Description
Booking_ID: unique identifier of each booking
No of adults: Number of adults
No of children: Number of Children
noofweekend_nights: Number of weekend nights (Saturday or Sunday) the guest stayed or booked to stay at the hotel
noofweek_nights: Number of week nights (Monday to Friday) the guest stayed or booked to stay at the hotel
typeofmeal_plan: Type of meal plan booked by the customer
requiredcarparking_space: Does the customer require a car parking space? (0 - No, 1- Yes).
roomtypereserved: Type of room reserved by the customer. The values are ciphered (encoded) by INN Hotels.
lead_time: Number of days between the date of booking and the arrival date
arrival_year: Year of arrival date
arrival_month: Month of arrival date
arrival_date: Date of the month
Market segment type: Market segment designation.(0- Offline, 1- Online, 2- Corporate, 3- Aviation, 5- Complementary )
repeated_guest: Is the customer a repeated guest? (0 - No, 1- Yes)
noofprevious_cancellations: Number of previous bookings that were canceled by the customer prior to the current booking
noofpreviousbookingsnot_canceled: Number of previous bookings not canceled by the customer prior to the current booking
avgpriceper_room: Average price per day of the reservation; prices of the rooms are dynamic. (in euros)
noofspecial_requests: Total number of special requests made by the customer (e.g. high floor, view from the room, etc)
booking_status: Flag indicating if the booking was canceled or not.





For this project, I utilized the Reservation Cancellation Prediction dataset from Kaggle, available at https://www.kaggle.com/datasets/gauravduttakiit/reservation-cancellation-prediction/. The dataset contains various variables, and the goal was to predict reservation cancellations.
To achieve this prediction, I employed three machine learning models. The evaluation of these models was based on the confusion matrix, with a specific focus on minimizing false negatives. The model selection was determined by choosing the one with the lowest false negative rate.
In terms of data preprocessing, the dataset was initially clean, with no null values. However, to enhance the analysis, I combined the columns for year, month, and day into a single "arrival date" column. Additionally, I created a new column named "booking created" to consolidate relevant information.
The overall approach involved leveraging machine learning algorithms, specifically tailored to predict reservation cancellations, and fine-tuning the model selection based on the performance metrics provided by the confusion matrix.

Exploration of the Distribution of Variables Representing Booking Characteristics

To gain a comprehensive understanding of the characteristics of most client reservations, it is evident that the majority are made for two adults with no children, typically for a two-night stay during the week. Additionally, most bookings show no specific requests for a meal plan, room type, parking, or other special accommodations. This pattern suggests that the hotel may cater to stopover guests or those traveling for business purposes.

Distribution of Previous Bookings

Examining past reservations reveals that the majority of customers are first-time bookers, and the number of repeat customers is relatively low. Among repeat customers, some have a history of previous cancellations. However, it's noteworthy that repeated customers are less inclined to cancel their bookings.

Distribution of Arrivals

The data indicates that a significant portion of bookings occurred in the year 2018, with a concentration in October for both 2017 and 2018. It's crucial to acknowledge that data for 2017 is available only from July onwards. Additionally, bookings for 2018 predominantly focus on arrivals during the first half of the month.

Time Lag Between Booking Creation and Arrival Date

A notable observation is that a substantial proportion of bookings are either created on the day of arrival or within the same month as the arrival date.

Average Room Price

The distribution of average room prices reveals that most bookings fall within the same price range, approximately €100.

Distribution of Show vs. No Show

There is no significant difference in the number of adults and children between canceled bookings and completed ones; the majority involve reservations for 2 adults with no children. Similarly, when considering the number of weekend nights and weeknights in the reservation, there is no clear pattern indicating that cancellations are influenced by these factors. Most bookings have 0 days during the weekend and are for one or two weeknights only.

Examining special requests, room type, meal plans, and parking requirements doesn't provide insights that explain cancellations through these variables.

However, a noteworthy observation is related to the "lead time" variable. It appears that most no-shows occur when reservations are made well in advance. In contrast, completed bookings often occur either on the arrival date or with a maximum lead time of three months.

The majority of bookings originate from online market segments, followed by offline market segments. Nevertheless, there are no significant insights related to cancellations based on market segments.

Furthermore, the room price does not seem to be a strong factor explaining cancellations, as most bookings are concentrated around 100€.

In summary, while certain variables like lead time show a potential correlation with cancellations, others such as the number of adults, children, and room price do not provide substantial insights into predicting cancellations.
