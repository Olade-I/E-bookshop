# Product Requirements Document (PRD)
Project Name: E-Bookshop (Campus Bookshop Inventory & Reservation System)
Document Version:** 1.0 
Date: 20th November 2026

## 1. Problem Statement
The Problem: At the start of every semester, the campus bookshop experiences severe overcrowding. Students spend hours in line without knowing if their required textbooks are in stock or how much they cost. Many only discover the price upon reaching the checkout counter, occasionally realizing they do not have sufficient funds, which causes embarrassment and wastes both student and staff time.
Impact:  Lost academic time for students, poor customer experience, high abandonment rates at the register, and immense stress on bookshop staff who act as both cashiers and inventory searchers.

## 2. Research & User Insights
### 2.1 How they cope today
Wasted Queuing: Students wait in the main checkout line for 30-45 minutes just to ask the cashier if a book is available.
Syllabus Guesswork: Students bring cash based on rough estimates of textbook prices from seniors, which are often outdated due to new editions.
Last-Minute Abandonment: Students leave books at the counter when the total price exceeds their budget, requiring staff to restock items manually.

### 2.2 Why existing solutions fall short
The bookshop relies on a legacy Point-of-Sale (POS) system that is only accessible to the cashiers. There is no student-facing digital catalog. Inventory checking and price checking both require verbal communication with a staff member, creating a massive bottleneck.

### 2.3 Interview and Survey Findings
We conducted interviews with 15 students across different faculties and 2 bookshop staff members.
Student A (1st Year, software engineer): "I waited in line for 40 minutes on the second day of classes. When I got to the front, they told me the accounting textbook was sold out. I missed the first half of my next lecture for nothing and when I got to class I was not allowed to enter for being late."
Student B (3rd Year, Engineering): "The worst feeling is getting to the counter, finding out the required materials cost double what you expected, and having to tell the cashier you can't afford it with a huge line behind you."
Bookshop Manager: "When I asked my cashiers about this problem they told me that 60% of the time they answer students about prices and telling them whether the book is even available rather than doing sales."*

## 3. Proposed Solution
Q-Book is a mobile-responsive web application that serves as a digital catalog for the campus bookshop. Students can search for books by Course Code, Title, or ISBN to view real-time availability and exact pricing. 

Users can add available books to a digital cart to see their exact total before leaving their dorm, and place a "Reservation" for an express pickup window, ensuring the book is held for them and they arrive with the correct payment.

4. Minimum Viable Product (MVP) Scope
To ensure rapid development and testing, the MVP will focus purely on inventory visibility and reservation routing.

4.1 In Scope for MVP
1. User Authentication: Login via existing student martic number and password/staff university email.
2. Digital Catalog & Search: Search bar for Course Codes (e.g., bu cos-209) and Titles, displaying the exact price and stock status (In Stock / Low Stock / Out of Stock).
3. Cart & Price Calculator: A cart that calculates the exact total price of selected items so students know exactly how much money to bring.
4. Reserve & Pickup: Ability to reserve items and receive a digital ticket/order number for the "Express Pickup" line.
5. Staff Dashboard: A backend interface for staff to upload CSVs of inventory/prices, view incoming reservations, and mark reservations as "Fulfilled."

### 4.2 Out of Scope for MVP (Future Versions)
In-App Payment Processing: MVP will use "Pay at Pickup" to bypass complex financial compliance, security routing, and transaction fees in the first iteration. 
Used Book Marketplace: Peer-to-peer textbook selling will not be included yet.
Digital E-Book Delivery: The MVP will only handle physical inventory currently in the shop.

## 5. Functional Requirements
REQ-1: The system must allow users to search the database using at least three parameters: Course Code, Book Title, or Author.
REQ-2: The cart must display the exact calculated total in the local currency, updating immediately when items are added or removed or if the price has changed.
REQ-3: The system must automatically deduct "1" from the available stock count temporarily when a reservation is placed, preventing double-booking of the last copy.
REQ-4: Reservations must automatically expire and return to the main inventory if not picked up within 24 hours.
REQ-5: Staff must be able to bulk-update inventory by uploading a standardized CSV file.




## 6. Non-Functional Requirements

Scalability: The database must handle massive traffic spikes during "Syllabus Week" (the first 2 weeks of the semester), supporting up to 1,000 concurrent searches without crashing.
Data Accuracy: Stock levels must sync with reservations in near real-time (under 5 seconds) to prevent false positives on book availability.
Accessibility: The UI must be highly legible on mobile devices, as 90% of students will use the platform on their phones while on campus.

## 7. Success Metrics (KPIs for MVP)
Price Transparency: Reduce the number of "abandoned at register" transactions by 80% during the first month of the semester.
Queue Time: Reduce the average wait time for users in the "Express Pickup" line to under 5 minutes.
Staff Efficiency: Decrease the volume of purely informational queries ("Do you have this?" / "How much is this?") at the physical counter by 60%.
