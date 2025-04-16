Practical No. 7
Title: Modeling Sequence Diagrams for Pharmacy Management System
________________________________________
Aim:
To model and understand the working of a sequence diagram for a Pharmacy Management System by representing the interactions between different system objects through message passing with respect to time.
________________________________________
Objective:
•	To learn the concept and structure of sequence diagrams.
•	To identify and represent system objects and their life-lines.
•	To model message passing between objects in a Pharmacy Management System scenario.
•	To visualize the dynamic behavior of the system for medicine purchasing and billing operations.
________________________________________
Introduction:
A sequence diagram is a type of interaction diagram that shows how processes operate with one another and in what order. It represents the objects involved in the scenario and the sequence of messages exchanged between them.
In a Pharmacy Management System, different components such as Customer, Pharmacist, Inventory System, and Billing System interact to perform tasks like medicine inquiry, stock verification, purchase processing, and bill generation. By using sequence diagrams, developers can visually capture these interactions for better system analysis and design.
________________________________________
Theory:
Sequence Diagram
A sequence diagram illustrates the behavior of a system by showing the interaction between different system objects through message passing, arranged in a time sequence. It is especially useful for understanding complex processes in software systems.
Elements in Sequence Diagram
A sequence diagram typically contains:
•	Objects: The system components or actors that interact.
•	Life-line bars: Vertical lines extending from object boxes, representing the object's existence over time.
•	Messages: Arrows indicating the communication between objects.
Object
An object is an instance of a class shown in a rectangle box. It may contain the object name, class name, or both, underlined within the rectangle.
Example:
customer : Customer
Life-line Bar
A vertical line extending downward from the object box, showing the existence of the object over time. An activation bar (a small rectangle on the life-line) indicates when the object is active.
Messages
Messages represent the communication between two objects:
•	Synchronous messages: Sender waits for the receiver to process and return control.
•	Asynchronous messages: Sender proceeds without waiting for the receiver’s response.
•	Return messages: Represent the return of data from one object to another.
•	Response messages (self-messages): An object interacting with itself.
________________________________________
Case Study: Pharmacy Management System
Scenario Description:
In a Pharmacy Management System, a customer visits the pharmacy to purchase medicines. The pharmacist verifies medicine availability through the inventory system, proceeds to generate the bill, and hands over the medicines to the customer. This sequence of operations can be modeled effectively using a sequence diagram.
Objects involved:
•	customer : Customer
•	pharmacist : Pharmacist
•	inventory : InventorySystem
•	billing : BillingSystem
Sequence of Events (Messages):
1.	Customer requests to purchase medicine.
2.	Pharmacist sends a searchMedicine() message to the Inventory System (Synchronous).
3.	Inventory System responds with medicine availability.
4.	If available, Pharmacist sends createBill() message to Billing System (Synchronous).
5.	Billing System calculates total, applies discounts if applicable (self-message), and generates a bill.
6.	Pharmacist delivers medicines and bill to the Customer.
7.	If medicine stock is low, Inventory System asynchronously sends notifyLowStock() message to Pharmacist.
Diagram Overview (Textual):

 

Conclusion:
The sequence diagram of a Pharmacy Management System clearly represents object interactions and message sequences over time. It simplifies understanding of system behavior, making it easier for developers to design, communicate, and implement the system efficiently.

