# ParkEngine – Scalable Parking Allocation System

ParkEngine is a Java-based parking management system designed to manage
vehicles, parking floors, parking spots, tickets, pricing, payments, and
vehicle entry/exit operations.

The project demonstrates Object-Oriented Programming (OOP) and commonly used
Design Patterns to create a modular and maintainable parking system.

---

## 🚀 Features

- Manage multiple parking floors
- Support multiple vehicle types:
  - Bike
  - Car
  - Truck
- Different parking spots for different vehicle types
- Automatic parking spot allocation
- Parking ticket generation
- Vehicle search using vehicle number
- Vehicle exit and ticket processing
- Parking fee calculation
- Multiple payment options:
  - Cash
  - UPI
  - Card
- Parking display boards
- Active ticket management
- Multiple parking and pricing strategies
- Console-based user interface

---

## 🧠 Design Patterns Used

### 1. Singleton Pattern

Used in `ParkingLot` to maintain a single parking lot instance.

### 2. Factory Pattern

`VehicleFactory` is used to create vehicle objects based on vehicle type.

### 3. Strategy Pattern

Used for flexible:

- Parking spot allocation
- Pricing calculation
- Payment processing

### 4. Observer Pattern

Used by parking display boards to receive updates from parking floors.

---

## 🏗️ System Structure

```text
                         ParkEngine
                             |
                      ParkingLot
                             |
          -------------------------------------
          |                 |                 |
      ParkingFloor      ParkingTicket      Gates
          |                                   |
    ParkingSpot                         Entry / Exit
          |
   ----------------
   |      |       |
 Bike    Car    Truck


ParkingLot
    |
    ├── ParkingStrategy
    ├── PricingStrategy
    ├── PaymentStrategy
    └── VehicleFactory
