# Paws-and-Paradise-System-Design
System design and analysis for the Paws &amp; Paradise e-commerce platform, including new feature enhancements and workflow diagrams.
🐾 Project Overview

Paws & Paradise is an online marketplace for pet products and services such as grooming and appointments.
This repository contains system design documentation for several enhanced features that improve:

1. Customer experience

2. Inventory control

3. Scheduling reliability

4. Engagement for dedicated pet owners

The focus is on clear use cases, class diagrams, sequence diagrams, and UI mockups for key features.

✨ Key Features Designed

1. Paw Points Loyalty Redemption at Checkout
Customers can redeem their Paw Points during checkout to receive instant discounts on products and grooming services.

2. Real-Time Slot Locking for Appointments
When a customer selects a time slot, the system temporarily locks it so no one else can book it at the same time while they complete their booking.

3. Low-Stock Auto Alert System for Inventory Staff
When an item’s quantity drops below a defined minimum level, the system automatically notifies inventory staff so they can restock before it runs out.

4. Breeding Recommendation Concept (Pet Matchmaking)
A conceptual feature where pet owners can explore suitable matches for their pets for breeding, supported and controlled by staff.

🧩 Feature Details
1️⃣ Paw Points Loyalty Redemption

User Story

As a Paws & Paradise loyalty member, I want to redeem Paw Points during checkout so that I can get discounts on pet products or grooming services.

Core Idea

Customers earn Paw Points from past purchases or grooming sessions.

At checkout, they can apply Paw Points to reduce their order total.

The system:

Validates eligibility

Converts points into a discount

Applies the discount

Deducts points and updates the loyalty balance

Shows the updated total and remaining points

Key Design Elements

Classes: LoyaltyAccount, Order, CheckoutController, Payment, Receipt, Customer

Artifacts:

Use case specification: Redeem Paw Points for Purchase Discount

Class diagram

Object-level sequence diagram

Mockups:

Checkout before redemption

Redeem Paw Points modal

Checkout after applying Paw Points

2️⃣ Real-Time Slot Locking for Appointments

User Story

As a pet owner, I want the system to temporarily lock my selected time slot during booking so that no one else can select the same time and I can complete my appointment without conflicts.

Core Idea

When a user selects a time slot, it is locked for a short period (e.g., 2 minutes).

During that time, other users cannot book that slot.

If the user confirms, the system creates the appointment and releases the lock.

If the time expires or the user cancels, the slot is released back to availability.

Key Design Elements

Use case: Create Customer Appointment

Preconditions: logged-in customer, available services, staff availability configured

Flow:

Select service category

Select specific service

Choose date

Choose time slot

System locks slot

User confirms → appointment created

Diagrams:

Sequence diagram for slot locking

Class diagram for appointment, slot, lock, and customer

3️⃣ Low-Stock Auto Alert System

User Story

As an inventory staff member, I want the system to automatically notify me when an item’s stock falls below a minimum level so that I can restock items before they run out.

Core Idea

Each inventory item has a minimum stock level.

Whenever stock is updated (sales, usage, etc.), the system compares the current quantity with the minimum.

If the quantity falls below the threshold, an alert is generated and the staff is notified (e.g., by email).

Key Design Elements

Actor: Inventory Staff

Feature name: Low-Stock Auto Alert System

Main Flow:

System updates item quantity

Compares with minimum stock level

Detects low stock

Generates alert

Notifies staff

Alternate flows:

Notification fails → system logs error

Item discontinued → stop monitoring

Artifacts:

Use case description

Sequence diagram

Class diagram (e.g., InventoryItem, Alert, NotificationService, InventoryStaff)

4️⃣ Breeding Recommendation Concept

User Story (Conceptual)

As a pet owner, I am worried about finding the perfect match for my pet to mate and produce high-quality offspring. There should be a system that lets me get information about other pets suitable for my pet to mate with.

Core Idea

A feature that allows pet owners to browse or request compatible breeding matches.

Controlled and verified by staff for safety and quality.

Justification Highlights

Fascinates and engages customers

Makes owners feel more considered and supported

Used primarily by pet owners, but controlled by staff
