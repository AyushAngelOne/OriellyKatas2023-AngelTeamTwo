## Recording and Visualising User Backend Events

- For every upserts in our `Trip` database, we'll publish Kafka events.
- These events will be consumed by our `Events Aggregator Consumer Group` which saves/updates the data in our Analytics Database.
- Using this we'll create various visualisation dashboards which can be used to get several insights on user's reservations.
