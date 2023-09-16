## Question: What is a subtrip?

A substrip is collection of high level trips which the user wants to do as a part of the trip. This collection can include items like cities to visit under a trip. All these items will be linear with respect to the time. Asumming that a planner can be at one place at one particular time the subtrip items have unqiue date and time and togther constitute the complete duration of the "trip". The subtrips can further include their own reservations of flights, cab, tourist places, and so on.

For instance:
We have a trip say Europe trip from 1st Sept to 20th Sept.
This trip is a collection of the following subtrips:
1. Spain = 1st Sept to 4th Sept
2. Greece = 5th Sept to 10th Sept
3. Italy = 11th Sept to 13th Sept
4. Gremany = 14th Sept to 18th Sept
5. Portugal = 19th Sept to 20th Sept

Each of these subtrips can further be granulated to n level distribution. What it means is that we can be as particular in defining a trip as we want.
For instance, Greece trip can further be a collection of subtrips where each subtrip is a trip of a partiular city in Greece.
1. Athens = 5th Sept to 6th Sept
2. Santorini = 7th Sept to 8th Sept
3. Mykonos = 9th Sept to 10th Sept

This provides the planner to make a trip as particular as he wants.

Since this is an N-level hierarchy, the root trip will have it's `Parent_Trip_ID` set as `NULL` and all subtrips of any parent trip will have their `Parent_Trip_ID` set as the trip ID of the parent trip.