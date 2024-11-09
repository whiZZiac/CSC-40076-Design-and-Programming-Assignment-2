# CSC-40076-Design-and-Programming-Assignment-2

# Library Notification System - Assessment 2 (CSC-40076)

This project simulates an extensible library notification system for managing book loans, reservations, and member notifications using CSV and JSON for permanent data storage. This repository contains the code for each functional component of the library system.

## Project Overview

The aim is to create a library system that can handle notifications without user input, enabling easy integration of new notification types. The system performs tasks such as converting CSV files to JSON, updating loan records, issuing and reissuing membership cards, and reserving books. Notifications for events like book availability and overdue returns are implemented as per design patterns to ensure flexibility for future requirements.

## Tasks

The project consists of the following core tasks:

### Task 1: CSV to JSON Conversion and Book/Membership Scanning
- **Objective**: Convert `books_2024.csv`, `bookloans_2024.csv`, and `members_2024.csv` into JSON format for in-memory processing and updates.
- **Features**:
  - Implement a `scan()` method for both `Book` and `Member` classes, simulating barcode scanning.
  - Update the JSON file when a book is borrowed by a member.
  - **Example Output**: JSON files reflect real-time borrowing updates.

### Task 2: Book Return System
- **Objective**: Update JSON records when a book is returned.
- **Features**:
  - Update JSON files upon book return, ensuring book availability status changes.
  - If the book was reserved, notify that it is available (see Task 5).
  - **Example Output**: Updated JSON showing book availability post-return.

### Task 3: Membership Application and Card Issuance
- **Objective**: Provide a system to manage membership applications and unique card issuance.
- **Features**:
  - Membership cards have a unique format combining member ID and issue count.
  - Reissue cards with incremented counts, resetting after 99 issues.
  - **Example Output**: Membership JSON updated with card issuance transactions.

### Task 4: Book Reservation System
- **Objective**: Allow members to reserve books.
- **Features**:
  - Create `reserved.json` to store reserved books.
  - Notify users if a book is reserved or currently available.
  - **Example Output**: Reservation system with notifications for reserved books.

### Task 5: Notification System for Reserved and Overdue Books
- **Objective**: Notify users about the availability of reserved books and overdue fines.
- **Features**:
  - Notify members when a reserved book becomes available.
  - Issue overdue notifications with fines for late returns.
  - **Example Output**: Notifications displayed in the console for overdue and reserved book events.

### Extensibility and Future Requirements
The system is designed with flexibility to handle future notification needs. By isolating notification functions, new types can be easily integrated, ensuring the library system can grow as requirements evolve.

## Setup and Usage

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/username/repository-name.git
