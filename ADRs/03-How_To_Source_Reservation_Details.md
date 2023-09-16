## Question: How to source reservation details?

Reservation details can be updated in the system in majorly 2 ways:
1. Manually: The user can manually add, update and delete their reservations in the system.
2. Auto updation: The system smartly fetches any reservation changes and updates in the system within 5 minutes of the actual update happeing in the primary system. To facilitate this,
   our system uses two components: Poller and scheduler.
   We have used four individual adaptors to faciliate the updations: Email scanner, Flight vendor adaptor, Hotel vendor adaptor, Car rental adaptor.
   Each of these adaptors have their individual poller which poll the latest data from their respective sources and make necessary updations in the management system and send out alerts
   to the users.
   All these pollers have a common scheduler which schedules the polling interval.

   The system further allows for passive updates. Some vendors actively send notifications for any changes on their end. For such vendors, updates in our system can be made more actively
   making them practically realtime. To faciliate this, we use vendor webHook service to listen for any update alerts from the vendor and update them in our system.

   All these variety of mechanisms help us keep our systems updated at the earliest.
