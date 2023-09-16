## Sourcing Reservation Updates

Based on different vendors, we'll use the following mechanisms for sourcing the reservation updates -

1. Webhook
    - Some vendors actively send notifications for any changes on their end and expose APIs for integration. For such vendors, we'll expose a webhook endpoint where the vendor can directly send us any updates regarding the reservation.
    - This will be helpful in making the updates near realtime.

2. Poller
    - For those vendors where direct integration isn't possible, we'll be using poller to poll the data every 5mins.
    - We'll use individual adaptors to faciliate the updations of Email scanner, Flight, Hotels and Car rental updates.
    - Each of these adaptors have their individual poller which poll the latest data from their respective sources.
    - All these pollers have a common scheduler which schedules as per the polling interval.


All these variety of mechanisms help us keep our systems updated at the earliest.