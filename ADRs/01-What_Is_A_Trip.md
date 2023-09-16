## Question: What is a trip?

A trip is a user-defined time box which defined time box with a label. For example, a user might say "I will be in Europe from 1st to 28th September" or "I will be on a road trip to Ladakh from 1st to 28th September".

Statements like these give us 3 common points:

- Start Time
- End Time
- A label - for example: "Europe Trip", "Road Trip to Ladakh"

This is what out core `Trip` schema will model as:

```
CREATE TABLE Trip (
   Trip_ID INT PRIMARY KEY,
   User_ID INT NOT NULL,
   Parent_Trip_ID INT REFERENCES Trip(Trip_ID),
   Trip_Name VARCHAR(255) NOT NULL,
   Start_Datetime DATETIME NOT NULL,
   End_Datetime DATETIME NOT NULL,
   Status VARCHAR(20) NOT NULL,
   FOREIGN KEY (User_ID) REFERENCES User(User_ID),
   FOREIGN KEY (Parent_Trip_ID) REFERENCES Trip(Trip_ID)
);
```
