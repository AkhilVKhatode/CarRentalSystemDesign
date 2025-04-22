# CarRentalSystemDesign

Designing a Car Rental System

## Functional Requirements:
1. The Car Rental System is designed to enable users to explore and book vehicles for specific timeframes.
2. Each vehicle entry includes attributes like make, model, manufacturing year, license plate, daily rental rate, and current availability.
3. Users should be able to filter cars based on factors such as vehicle category, price range, and open rental dates.
4. The platform will manage the full reservation lifecycle, including creation, updates, and cancellations.
5. Availability is dynamically maintained and updated in real time based on booking activity.
6. Customer details—such as full name, contact information, and driver's license—are stored securely.
7. Payment functionality is integrated to support reservation transactions.
8. The system supports simultaneous booking operations and guarantees data consistency across threads.

## Key Classes, Interfaces, and Enums:
1. Car: Captures vehicle attributes like make, model, year, license number, price per day, and availability.
2. Customer: Stores customer-related data including name, contact info, and driver's license number.
3. Reservation: Holds booking data including reservation ID, associated customer and car, rental period (start and end date), and total cost.
4. PaymentProcessor (Interface): Defines the structure for processing payments. -> CreditCardPaymentProcessor and PayPalPaymentProcessor provide concrete implementations of payment handling.
5. RentalSystem: Implements the Singleton pattern to manage the rental operations and ensure centralized control. Utilizes thread-safe structures (like ConcurrentHashMap) to maintain integrity of car and reservation data under concurrent access. Provides methods to manage cars, perform availability searches, book or cancel rentals, and process payments.
6. CarRentalSystem: Acts as the application's main class, showcasing typical usage and interactions within the rental system.
