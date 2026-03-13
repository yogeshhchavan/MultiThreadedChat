🚀 TomatoApp – Food Delivery System (C++)

![Language](https://img.shields.io/badge/Language-C++-blue)

A C++ console-based food delivery system inspired by platforms like Zomato / Swiggy.
This project demonstrates clean architecture and object-oriented design patterns including Factory, Strategy, Singleton, and Facade.

The system simulates the complete food ordering workflow from restaurant discovery to payment processing and order notification.

✨ Features
👤 User Management

Create and manage user profiles

Maintain individual user carts

🍽 Restaurant Search

Search restaurants by location

Browse restaurant menus

🛒 Cart System

Add menu items to cart

View cart contents

Calculate order totals

📦 Order Types

Immediate Orders

Scheduled Orders

💳 Payment Strategies

Supports multiple payment methods:

UPI

Credit Card

Implemented using the Strategy Pattern.

🔔 Notifications

Users receive notifications after successful order placement.

🚚 Delivery Options

Supports both:

Delivery Orders

Pickup Orders

🏗 System Architecture

The application follows layered architecture with design patterns.

User
  │
  ▼
TomatoApp (Facade)
  │
  ├── Managers
  │     ├── RestaurantManager
  │     └── OrderManager
  │
  ├── Factories
  │     ├── NowOrderFactory
  │     └── ScheduledOrderFactory
  │
  ├── Strategies
  │     ├── UpiPaymentStrategy
  │     └── CreditCardPaymentStrategy
  │
  └── Services
        └── NotificationService

This architecture improves:

Extensibility
Separation of concerns
Maintainability

📂 Project Structure

TOMATO/
│
├── factories/            # Factory pattern for order creation
│   ├── NowOrderFactory.h
│   ├── OrderFactory.h
│   └── ScheduledOrderFactory.h
│
├── managers/             # Singleton managers
│   ├── OrderManager.h
│   └── RestaurantManager.h
│
├── models/               # Core domain models
│   ├── Cart.h
│   ├── DeliveryOrder.h
│   ├── MenuItem.h
│   ├── Order.h
│   ├── PickupOrder.h
│   ├── Restaurant.h
│   └── User.h
│
├── services/             # External services
│   └── NotificationService.h
│
├── strategies/           # Strategy pattern for payment
│   ├── CreditCardPaymentStrategy.h
│   ├── PaymentStrategy.h
│   └── UpiPaymentStrategy.h
│
└── utils/
    └── TimeUtils.h


⚙️ Installation & Setup
Prerequisites

C++ Compiler (g++ or Visual Studio)

Standard C++ libraries

🛠 Build Instructions
Clone Repository

git clone https://github.com/YOUR_USERNAME/TomatoApp.git
cd TomatoApp

Compile Project
g++ main.cpp -o tomatoapp

▶ Running the Application
./tomatoapp

The program simulates a food ordering workflow for a user.

🧪 Example Output
User: Adityais active. 
Found Restaurant : 
 - Binker
Selected Restauarant : Binker
Item in cart : 
---------------------------------------------
P1 : Chole Bhature : $120
P2 : Samosa : $15
---------------------------------------------
Grand total : $135
Paid $135 using UPI: (1234567890)

Notification : New Deliveryorder places!
________________________________________________________
Order ID: 1
Customer: Aditya
Restaurant: Binker
Items Ordered:
 - Chole Bhature ($120)
 - Samosa ($15)
Total : $135
Scheduled For: Sat Mar 14 00:03:11 2026
Payment Done...!
________________________________________________________

🧠 Design Patterns Used
Pattern	Purpose
Facade Pattern	TomatoApp provides a simplified interface
Factory Pattern	Handles order creation
Strategy Pattern	Payment method selection
Singleton Pattern	Managers ensure single instance

These patterns improve:

scalability

maintainability

modular architecture

🚀 Future Enhancements

Possible improvements:

Add user authentication

Implement database persistence

Add GUI interface

Real-time order tracking

Restaurant ratings & reviews

Microservice architecture version

Separation of concerns

Maintainability
