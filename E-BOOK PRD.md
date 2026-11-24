**#Product Requirements Document (PRD)**
**Project Name: E-Bookshop**
**Date: 21st November 2026**

 1. Problem Statement
The Problem: Whenever a new semester starts, the campus bookshop experiences severe overcrowding. Students spend hours in line without knowing if the required textbooks are in stock or how much they actually cost. Most people only realize the price of the textbook when they reach the counter , occasionally realizing they do not have sufficient funds, which causes embarrassment and wastes both student and cashiers time.
Impact:  Loses academic time for students, bad customer experience, high abandonment rates at the register, and immense stress on bookshop staff who act as both cashiers and inventory searchers.

 2. Research & User Insights
 2.1 How they cope today
Wasted Queuing: Students wait in the main checkout line for 30-45 minutes if the boosk shop is crowded just to ask the cashier if a book is available.
Syllabus Guesswork: Students brings the wrong amount of money based on what there seniors told them, and the prices could have increased.
Last-Minute Abandonment: Students leave books at the counter when the total price exceeds their budget, requiring staff to restock items manually.

 2.2 Why existing solutions fall short
The bookshop only relies on a POS system that is only accessible to the cashiers. There is no online catalog. Inventory checking and price checking both require verbal communication with a staff member, creating a massive bottleneck.

 2.3 Interview and Survey Findings
We conducted interviews with 4 students across different faculties.
Student A (1st Year, software engineer): "I waited in line for 40 minutes on the second day of classes. When I got to the front, they told me the accounting textbook was sold out. I missed the first half of my next lecture for nothing and when I got to class I was not allowed to enter for being late."
Student B (3rd Year, Engineering): "The worst feeling is getting to the counter, finding out the required materials cost double what you expected, and having to tell the cashier you can't afford it with a huge line behind you."
Student C (2nd Year, Accounting):  “  The bookshop experience is so bad, you can leave your hostel on a Sunday morning just to get there and see the textbook is not available.”
Student D (2nd Year, Computer Science): “ I decided not to buy the textbook the day it came out because I thought they brought enough for everyone, but by the time I came the next day they told me they were out of stock and I came back every single day for 2 weeks since I did not know when next the textbook will become available or be in stock.”

3. Proposed Solution
E-Book is a mobile-responsive web application that serves as a digital catalog for the campus bookshop. Students can search for books by Course Code, or Title to view real-time availability and exact pricing. 
Users can add available books to a digital cart to see their exact total befoe leaving their hostel, and place a reservation for a pickup window within 24 hours, ensuring the book is held for them and they arrive with the correct payment.

4. Minimum Viable Product (MVP) Scope
To ensure rapid development and testing, the MVP will focus purely on inventory visibility and reservation routing.

4.1 In Scope for MVP
1. User Authentication: Login using existing student martic number and password/staff university email.
2. Digital Catalog & Search: Search bar for Course Codes (e.g., bu cos-209) and Titles, displaying the exact price and stock status (In Stock / Low Stock / Out of Stock).
3. Cart & Price Calculator: A cart that calculates the exact total price of selected items so students know exactly how much money to bring.
4. Reserve & Pickup: Ability to reserve items and receive a digital ticket/order number for the express Pickup line withing a 24 hours window.
5. Staff Dashboard: A backend interface for staff to upload CSVs of inventory/prices, view incoming reservations, and mark reservations as fulfilled.

4.2 Out of Scope for MVP (Future Versions)
In-App Payment Processing: MVP will use "Pay at Pickup" to bypass complex financial compliance, security routing, and transaction fees in the first iteration. 
Used Book Marketplace: Peer-to-peer textbook selling will not be included yet.
Digital E-Book Delivery: The MVP will only handle physical inventory currently in the shop.

5. Functional Requirements
REQ-1: The system must allow users to search the database using only 2 parameters: Course Code and Book Title.
REQ-2: The cart must display the exact calculated total in the local currency, updating immediately when items are added or removed or if the price has changed.
REQ-3: The system must automatically deduct "1" from the available stock count temporarily when a reservation is placed, preventing double-booking of the last copy.
REQ-4: Reservations must automatically expire and return to the main inventory if not picked up within 24 hours.
REQ-5: Staff must be able to bulk-update inventory by uploading a standardized CSV file.
REQ-6: When a reservation expires the students money must be refunded as fast as possible.




6. Non-Functional Requirements

Scalability: The database must handle massive traffic spikes during "Syllabus Week" (the first 2 weeks of the semester), supporting up to 1,000 concurrent searches without crashing.
Data Accuracy: Stock levels must sync with reservations in near real-time (under 5 seconds) to prevent false positives on book availability.
Accessibility: The UI must be highly legible on mobile devices, as 90% of students will use the platform on their phones while on campus.

7. Success Metrics (KPIs for MVP)
Price Transparency: Reduces the number of books abandoned at the front of the register due to insufficient funds during the start of the semester.
Queue Time: Reduce the average wait time for users in the express Pickup line to under 5 minutes.
Staff Efficiency: reduces the workload on the staff since people will not be asking whether they have this or that textbook, and will not be asking the price of each item.
