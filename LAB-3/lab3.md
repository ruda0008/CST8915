# Refelection Questions
## What challenges did you encounter when configuring environment variables in the GitHub Actions workflow?

* There were 2 challenges for me while doing this lab one was with orderservice the code was somehow deployed on azure but did not work. While investigating my friend showed me that we can view runtime logs thus with the help of logs i was able to identify that the dotenv dependency was missing and because of that the code was broken.

* Another challenge was with the env variables in the yml file in storefront everything was working perfectly fine the env was also placed properly. To test i just simply added /orders and /products after the link to the server address and it worked i was able to figureout for the product service as it was rewritten by my in python but couldn't know for order service.

## How does deploying microservices on Azure Web App Service differ from running them locally?

* Deploying microservice on Azure could provide instant scalability which could not be acheived by deploying it locally as it is limited to the same resource. Additionaly continous development and continous deployment could also be acheived which is more convinient and safe and standard way to update or  deploy new service.


## Why is it important to use environment variables for configurations in a cloud environment?

* By using environment varaibles in cloud we can make changes without changing the whole code for example in this lab i added rabbitmq connection string consisting of the username, password and the rabbitmq IP if the server ip or the password is changede all we have to do is just change the variable value mkaing it safe without changing the code.

# Youtube Link : https://youtu.be/XM2mDo_A4rk