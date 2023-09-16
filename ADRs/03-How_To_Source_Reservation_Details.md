## How to source reservation details?

- For sourcing reservation details, we'll need to onboard users into our system. This can be done by signing into our app.
- For adding reservation details there are following options -
    - Manual - The user can manually add, update and delete their reservations in the system.
    - Automated - 
        - Once the user is onboarded, we'll ask access for reading their emails.
        - We'll scan through their emails and identify the reservations.
        - We'll group them by trips.

- Every reservation detail will be saved in the `Trip` database and the CRUD operations will be handled by the `Trip Manager Service`.
