## Propagating Reservation Updates

- To propagate the reservation updates into our system, we need to have an adapter to convert vendors' data to a common structure which can be consumed by our system.
- Once the webhook/poller receives any updates, they'll forward it to the `Reservation Adapter` interface which maps the incoming data to a common interface that can be used by our system.
- We'll push this data to Kafka which will be consumed by the `Reservation Consumer Group`.
- The consumers update the respective reservations in the `Trip` database.
