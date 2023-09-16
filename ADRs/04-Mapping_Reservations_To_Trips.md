## Question: Mapping reservations to trips?

We have implemented a separate table to store all the reservations. Here reservation includes but is not limited to bookings of flight, car rental, hotel, tourist places and so on.
Each of this reservation entry is linked to the userId and the tripId for that user. This helps in minimizing the redundancy and present this data on the dashboard in a tree like
manner.
Each reservation entry has details like reservationId, reservation type, vendor reservation id, vendor name and so on. This allows for swiftly updating the data in case of any changes on the vendor's end.
