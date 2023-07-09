# RentARide
Rent a Ride
As a customer to Rent a Ride you book a cab. We charge you as per the
distance covered. We charge 8rs/km.
The moment you click the button to RIDE, we search for the nearby
drivers who will accept your ride.
Suppose there are 15 drivers near your location, then we send the request
to the first driver who is closest to you, then the second, and so on.
There are few conditions though, on the basis of which we can not send the
request to the nearby driver.
Condition 1:
If the driver rating is lower than 4. (out of 5)
Condition 2:
If you selected a specific car, and that car driver is not the closest one.
In case there is no driver present as per your request for the car, we will
ask you to select some other car.
Let’s see an example
Driver Car Model Rating DistanceFromCustomer
A Sedan 4 500m
B HatchBack 4.3 1km
C 5 Seater 4.8 200m
D Sedan 4.1 700m
E HatchBack 4.7 430m
The customer booked a cab asking for a sedan. The total distance that will
occur is 43km.
The driver with the closest distance is C but it is not a Sedan, therefore we
will look for Sedan. Driver A(500) and Driver D(700). Both have rating
greater than 4.
Driver A gets the request first because he is the closest driver.
Driver A accepts the request. There is not mechanism now a driver can
cancel the request. Unless he/she doesn’t fit in the criteria.
Sample Input: 1
Customer Ride Distance: 43km
Car Requested: Sedan
List of Drivers with Details:
Driver Car Model Rating DistanceFromCustomer
A Sedan 4 500m
B HatchBack 4.3 1km
C 5 Seater 4.8 200m
D Sedan 4.1 700m
E HatchBack 4.7 430m
Sample Output: Driver A will get you to the destination.
Your charge will be Rs 344 (43*8).
Sample Input: 2
Customer Ride Distance: 20.5 km
Car Requested: HatchBack
List of Drivers with Details:
Driver Car Model Rating DistanceFromCustomer
A HatchBack 3 500m
B HatchBack 4.3 1km
C 5 Seater 4.8 200m
D Sedan 4.1 700m
E HatchBack 4.7 430m
Sample Output: Driver E will get you to the destination.
Your charge will be Rs164 (20.5*8)
Extension:-
The driver can Cancel the request if the ride is not their preferred
destination.
Sample Input:-
Customer Ride Distance: 60km
Car Requested: 5 seater
Destination: Delhi
List of with Details:
Driver Car Model Rating DFC PReffDestination
A 5 Seater 4 500m Gurgaon, Noida, Delhi
B HatchBack 4.3 1km Gurgaon
C 5 Seater 4.8 200m Noida
D Sedan 4.1 700m Noida
E 5 Seater 4.7 430m Delhi
Sample Output:
Driver E will take you to the destination
Your charge will be Rs 480 (60*8)
Explanation:-
The request goes to Driver C first. As he is the closest and rating is good.
But he cancels the request, so the next request goes the Driver E.
