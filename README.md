# Bus Reservation System

The Bus Reservation System is a C-based console application that facilitates bus ticket reservations, cancellations, and passenger information display. It uses a linked list data structure to manage reservations and a queue for handling waiting lists.

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Code Structure](#code-structure)
- [Contributing](#contributing)
- [License](#license)

## Introduction
This Bus Reservation System allows users to book and cancel bus tickets, while maintaining a waiting list for full bookings. It is a simple, text-based interface suitable for learning and small-scale applications.

## Features
- **Seat Booking**: Book a bus seat, providing details like name, age, travel date, origin, and destination.
- **Reservation Cancellation**: Cancel an existing reservation by registration number.
- **Passenger Details Display**: View all current reservations.
- **Waiting List Management**: Automatically manages a waiting list when reservations are full.

## Installation
1. **Clone the repository**:
   ```bash
   git clone https://github.com/RexO77/Bus-reservation.git
   ```
2. **Navigate to the project directory**:
   ```bash
   cd Bus-reservation
   ```
3. **Compile the source code**:
   ```bash
   gcc -o BusReservation BusReservation.c
   ```
4. **Run the application**:
   ```bash
   ./BusReservation
   ```

## Usage
After running the application, a menu will prompt you to choose an action:
1. **Reserve a ticket**: Enter passenger details to book a seat.
2. **Cancel Booking**: Provide the registration number to cancel a reservation.
3. **Display Passenger Details**: View details of all reserved passengers.
4. **Exit**: Close the application.

## Code Structure
The code is organized into several key functions, each responsible for different parts of the system:

- **create()**: Initializes the first reservation if no reservations exist.
- **reserve()**: Handles new reservations, including managing the waiting list if the bus is full.
- **cancel(int reg)**: Cancels a reservation by registration number and manages the waiting list.
- **enq(node* new_node)**: Adds a new reservation to the waiting list.
- **deq(int reg)**: Moves a waiting list reservation to the active list when a seat is canceled.
- **display()**: Prints all current reservations.

### Analysis
The system uses a linked list to store active reservations and a queue to manage the waiting list. The main data structure (`node`) holds passenger information and pointers to the next node. The `reserve` function handles both immediate reservations and waiting list additions. The `cancel` function updates the list and fills vacancies from the waiting list. The overall design ensures modularity and efficient management of reservations and cancellations.

## Contributing
Contributions are welcome! Please fork the repository, create a new branch for your changes, and submit a pull request. Ensure your code follows the existing style and is well-documented.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---
