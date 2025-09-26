# LAB-1
![alt text](app-architecture.png)
# Order-Service
The order-service is built using node.js with express framework. It is designed to handle incoming customer orders from the fron webapp. For instance when a customer makes an order on Store-front side the service makes a POST in JSON format. Once the data is received it connects to RabbitMQ and publishes the order to order_queue. In simple words this service acts as a bridge between the front-end which is Store-front and the backend system that is rabbitMQ

# Product-Service
The product service is built in RUST langauge the sole purpose of this service is to provide an HTTP API at /products which returns data in JSON format. I also noticed that this script uses CORS which helps vue.js to call it driectly from any domain or port. To Simplify, this service just provides hardcoded list of products which is then fetched by store-front and displayed to the user.

# Store-Front
 Store Front is a single-page Vue.js application to mimic pet store user interface. It retrieves a list of products by calling Rust Product Serviceand displays products to be selected. Users can select a product, enter quantity, and display calculated total price on client-side. When order is submitted, frontend calls a POST request with order information to Node.js Order Service that then forwards it to RabbitMQ. Essentially, the Vue.js app ties everything together by keeping users busy with the system but offloading product information and order processing to backend services.



# Youtube Link To Lab Video
https://youtu.be/bl_eSk-dlFY 