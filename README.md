Design and implement a Food Ordering System in Python using stacks, queues, and object-oriented programming (OOP). The system will record customer orders, keep track of their status, and support a simple order-processing workflow. 
Use a queue to process pending orders in the order they were placed and a stack to support undoing the most recently placed pending order.

Objectives
===============================
Understand Data Structures: Use a queue for first-in, first-out order processing and a stack for last-in, first-out undo history.
Learn Object-Oriented Principles: Apply encapsulation and other OOP principles to organize orders and the system that manages them.
Develop Problem-Solving Skills: Apply data structures to a practical ordering workflow and handle changes in order status consistently.

Requirements
===============================
Class Design:
Create an Order class representing one customer order. Include attributes such as order_id, customer_name, items, total, and status (for example, pending, completed, or cancelled).
Create a FoodOrderingSystem class that manages orders using:
A queue of orders waiting to be prepared. Process pending orders in first-in, first-out order.
A stack of recently placed orders. Use it to find the most recently placed order when undoing an order.
A collection of orders that allows the system to look up and display orders by ID.

Functionality:
Implement these methods in FoodOrderingSystem:
place_order(order): Add a new order to the order records, the pending queue, and the recent-order stack.
view_orders(): Display the orders and their current statuses.
process_next_order(): Complete the next pending order in the queue. Skip orders that have already been cancelled.
cancel_order(order_id): Cancel an order that is still pending. Report when the ID is unknown or the order can no longer be cancelled.
undo_last_order(): Cancel the most recently placed order that is still pending, using the stack. Skip orders that are already completed or cancelled.
Keep the status consistent when an order is processed, cancelled, or undone.

User Interface:
Implement a simple command-line interface for placing orders, viewing orders, processing the next order, cancelling an order by ID, undoing the most recent pending order, and exiting.
Prompt for the information needed to create an order, such as the customer name, food items, and total price.

Testing:
Test the FoodOrderingSystem methods with cases such as an empty queue, an unknown order ID, cancelling an order, undoing the latest pending order, and processing after a cancellation.
