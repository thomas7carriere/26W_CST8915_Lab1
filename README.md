# CST8915 Lab 1: Algonquin Pet Store on Azure VM

**Student Name**: Thomas de Haan Carriere
**Student ID**: 41276876
**Course**: CST8915 Full-stack Cloud-native Development
**Semester**: Winter 2026

---

## Demo Video

🎥 [Watch Demo Video](https://youtu.be/gJij8g5vp9Q)

---

## Technical Explanations

### Order Service (Node.js)

Purpose: The Order Service handles customer orders by receiving them from the store front and placing them into RabbitMQ, allowing orders to be processed asynchronously.
Technology Stack: Uses Node.js, which is a Javascript runtime environment for running Javascript code outside of a web browser.
Architecture Role: The order service is a standalone backend service that can be accessed by the store front via its REST endpoint.
Inter-Service Communication: Interacts syncronously with the store front via HTTP(REST), and asyncronously with RabbitMQ by publishing messages to a queue to be processed.

### Product Service (Rust)

Purpose: Handles everything to do with products for the application (product details, inventory). Provides a REST endpoint for product resources.
Technology Stack: The product service is written in Rust, as it is a fast, memory-safe language ideal for high-performance APIs (lab handout)
Architecture Role: The product service is a standalone backend service that can be accessed by the store front via its REST endpoint.
Inter-Service Communication: The product service is running on the Azure Virtual Machine open on PORT 3030. Exposes a REST endpoint for communication.

### Store Front (Vue.js)

Purpose: The store front in the user facing (frontend) portion of the application, where users can interact with the application by placing orders and checking inventory.
Technology Stack: The framework used is Vue.js, which is a javascript framework used for building web user interfaces.
Architecture Role: The store front is on the presentation layer, allowing for user iteractions and accesses information via the back-end services.
Inter-Service Communication: Open on port 8080, the store front accesses information from the product and order REST apis using HTTP.


---

## Challenges and Learnings (Optional)

[Share any interesting challenges you faced during setup, how you solved them,
and what you learned from this lab experience]

---

## Acknowledgments

Lab Instructions
