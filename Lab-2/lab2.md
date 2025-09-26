# CST8915 FullStack Cloud Native Development

## Name: Aryan Rudani
## Student ID: 041171391
## Lab-2

<br>
<br>
<br>
<

# Reflection Questions

1. What changes did you make to the order-service and product-service to comply with the Configurations and Backing Services factors of the 12-Factor App methodology?

* For both services, I removed the hard-coded values and moved those values to environment variables. In the order-service, I used the dotenv package in Node.js so it can fetch  things like the RabbitMQ connection string and port from a .env file. For the product-service, I added the dotenv file in Rust and updated main.rs so the port comes from the environment instead of being fixed in the code. By doing this, both services can connect to RabbitMQ and run on different machines without  changing any source code.

2. Why is it important to use environment variables instead of hard-coding configurations in your application?

* Hard coding configuration makes  apps inflexible and  risky. If any passwords, ports, or IPs are hardcoded into the actual code, The code would have to be edited the every time something changes, which is not a best practice and unsafe.

3. Why is it important to have separate repositories for each microservice? How does this help maintain independence and scalability of each service?

* Splitting them into their own repos keeps everything  independent. Each service has its own code, dependencies, and setup, so if any updates or fixes aer applied there is no risk of breaking the other services. Additionally it could be  scaled or deploy one service without touching the rest.

# Link to Repositories

### Store-front : https://github.com/ruda0008/store-front 
### Order-service : https://github.com/ruda0008/order-service
### Product-Service : https://github.com/ruda0008/product-service

# Youtube Link : 
https://youtu.be/KNgRQMlVgto