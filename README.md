# Paws-and-Paradise-System-Design
System design and analysis for the Paws &amp; Paradise e-commerce platform, including new feature enhancements and workflow diagrams.

🐾 Project Overview

Paws & Paradise is an online marketplace for pet products and grooming services.
This repository contains system design documentation for several enhanced features that improve:

- Customer experience

- Inventory control

- Scheduling reliability

- Engagement for dedicated pet owners

The focus is on clear use cases, class diagrams, sequence diagrams, and UI mockups.

✨ Key Features Designed
1. Paw Points Loyalty Redemption at Checkout

Customers can redeem Paw Points during checkout to receive discounts on products and grooming services.

2. Real-Time Slot Locking for Appointments

When a customer selects a time slot, the system temporarily locks it so no one else can book it during completion.

3. Low-Stock Auto Alert System

Automatically notifies inventory staff when an item falls below its minimum stock level.

4. Breeding Recommendation Concept (Pet Matchmaking)

Allows pet owners to explore compatible breeding matches, monitored by staff.

🧩 Feature Details

1️⃣ Paw Points Loyalty Redemption

User Story

As a loyalty member, I want to redeem Paw Points during checkout so I can get discounts on pet products or grooming services.

Core Idea

- Customers earn Paw Points from purchases or grooming sessions.

- They can apply points to reduce their order total.

- The system:

   . Validates eligibility

   . Converts points into a discount

   . Applies the discount

   . Updates the loyalty balance

   . Shows updated total + remaining points

Key Design Elements
Classes: LoyaltyAccount, Order, CheckoutController, Payment, Receipt, Customer
Artifacts: Use case, class diagram, sequence diagram, mockups.

2️⃣ Real-Time Slot Locking for Appointments

User Story

As a pet owner, I want the system to temporarily lock my selected time slot so no one else can select it while I finish booking.

Core Idea

- User selects a service → selects date → selects time slot

- System locks slot for 2 minutes

    . If the user confirms → appointment created

    . If time expires → slot released

Artifacts:
Sequence diagram, class diagram, UI mockups.

3️⃣ Low-Stock Auto Alert System

User Story

As an inventory staff member, I want automatic low-stock alerts so I can restock items before they run out.

Core Idea

- System updates item quantity

- Compares quantity to minimum level

- Detects low stock

- Generates alert

- Notifies staff

Artifacts:
Use case, sequence diagram, class diagram.

4️⃣ Breeding Recommendation Concept

User Story

As a pet owner, I want help finding a compatible match for my pet to produce healthy offspring.

Core Idea

- Fascinating and engaging for customers

- Staff-controlled for safety

- Intended for pet owners looking for recommended matches

📎 Conclusion

This project demonstrates proficiency in:

- System analysis

- UML modeling

- Feature design

- Workflow documentation

- User-centered design

It serves as a system blueprint for future development of Paws & Paradise enhancements.
