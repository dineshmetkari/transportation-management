# **Transportation Management** #
By
### Asif Hossain, Ferdous Haque ###


# Introduction #
With a largely growing transportation need transportation companies are emerging day by day. This companies use paper based system to manage their bookings, maintaining schedule, drivers and coaches working hour tracings.

Our system will provide solutions to this service providers. By using our solution they can handle bookings, cancellations, record all of the information coming in from the drivers and keep track of their working hours easily. It will also keep track of every coaches show them in map. If  any unexpected event occurs then it will notify service providers and helps them to take necessary steps.

# Scope #
Targeted users of our system are transportation service providers and the people who want to hire any coach from them.

# Users and their role #

  1. Admin/Owner
    * Create/Update Area Controller
    * Watch Monthly Report
  1. Area Controller
    * Create New Agents
    * Create New Coach
    * Watch Monthly Area Report
    * Track coaches
    * Approve Drivers Payment
  1. Agents
    * Check available coaches
    * Confirm Booking
    * Cancel booking and Refund
    * Track Coach
    * Request for backup
  1. Driver
    * Post departure, arrival time.
    * Post if any repair needed for a certain coach
    * Inform agents if coach damaged or not working
  1. System
    * Cancel reservation after a certain time if not confirmed
    * Suggest for nearest coach service for both user and agents
  1. Registered User
    * Search coach for a specific destination
    * Reserve coach
    * Confirm payment
  1. Anonymous User
    * Search coach for a specific destination

# Use Cases of The System #

## Make Order ##
  1. Brief Description: Through this use case a client can make an order for a coach.
  1. Preconditions: The client must be registered to the system.
  1. Actors Involved: Client and Server
  1. Business Trigger: Client wishes to make an order.
  1. Basic Flow:
    1. Registration
    1. Input Travel information
  1. Post Condition: A new order with an order ID has been created and Server is notified to take necessary steps.

## Check Availability ##
  1. Brief Description: System first checks the confirmed order list and then the unconfirmed order list
  1. Preconditions: Client must place an order for a coach.
  1. Actors Involved: System
  1. Business Trigger: Order from a client for a coach.
  1. Basic Flow:
    1. Make order
  1. Post Condition: A new unconfirmed order has been created in the database with an order ID.
## Payment confirmation ##
  1. Brief Description: In this use case client notify server about the payment of the order by giving the bank receipt scroll number.
  1. Preconditions: Client must have booked a coach pay the bill and log in to the system to give the scroll number.
  1. Actors Involved: Client
  1. Business Trigger: Bill payment in the bank.
  1. Basic Flow:
    1. make order
    1. order receipt receive
  1. Post Condition: If payment is successful the coach is reserved and if not the client is notified about the unsuccessful payment.
## Reserve Coach ##
  1. Brief Description: In this use case server finally confirm an order and reserve a coach for that
  1. Preconditions: The client must pay the full payment for that order.
  1. Actors Involved: Server
  1. Business Trigger: If client pays the full payment in the due time.
  1. Basic Flow:
    1. Payment Confirmation
    1. Payment status checking
  1. Post Condition: The order is confirmed and the confirmed order is updated in the database.
## Update Location data ##
  1. Brief Description: In this use case GPS interacts with the server.
  1. Preconditions: The GPS device must be setup in the coach going to a trip.
  1. Actors Involved: GPS based agent and Server
  1. Business Trigger: If a coach going for a trip.
  1. Basic Flow:
    1. Coach Reservation
    1. Coach Status Update
  1. Post Condition: By updating the location of the coach to the server by GPS, the server can keep track on the coach. And by this it can calculate distance travelled and driver’s working hour.

# Technology #
  * Thymeleaf
  * Spring
  * JPA
  * JTA
  * Hibernate
  * Android
# Version Control #
  * Git
# Build Tools #
  * Gradle
# Web Server #
  * Apache Tomcat
# Database #
  * MySQL