# Car Rental Service
Car Rental System where customer can login, explore cars options and can make booking.

# Table of Contents
* Technologies used 
* Project Overview
* Project Architecture

# Technologies used
* Java
* Spring Boot
* Spring Security
* API Gateway
* Netflix Eureka


![CarRentalDemoVideo2](https://user-images.githubusercontent.com/59741887/200380142-9c93459f-58f1-40d5-b1bb-1d404c576a50.gif)

# Project Architecture
<img src="https://user-images.githubusercontent.com/59741887/200380408-9a9fa591-3765-41b7-a86c-9e9615662382.PNG" width="600" height="450"/>


###  Customer Service
Performs customer registration, authentication and stores bookings information of customers. 
Method	| Path	| Description	| Role |
------------- | ------------------------- | ------------- | ---------
POST | /customer/register | Register Customer | USER |
POST | /customer/login | Login into account | USER |
GET	| /customer/{custId}	| Get Customer Details | USER | 
GET	| /customer/bookings	| Get all bookings of customer | USER | 
GET	| /product/booking/{bookingId}	| Get booking by bookingId	| USER | 
GET | /logout | Logout of account | USER/ADMIN | 
 
### Booking Service
Used for booking cars and cancellation, maintaining records of cars in stock and its history. 

Method	| Path	| Description	| ROLE
------------- | ------------------------- | ------------- | ------------
GET | /explore/cars | Get all cars records | USER
GET | /explore/car/{carId} | Get car record by id | USER
POST	| /book	| Book a car | USER
GET	| /logs/cars/{carId}	| Get Car history	 | ADMIN
GET	| /logs/customer/{customer}	| Get Customer booking history	| ADMIN

### API Gateway


### Discovery Server

Service Discovery allows automatic detection of the network locations for all registered services. These service might have dynamically assigned addresses. 
In this project, <b>Netflix Eureka</b> is used. It uses client-service discovery pattern, where clients fetch the registry from discovery server for determining the location available services and load balancing between them. 

Eureka Dashboard provides information of running services and no. of instance: `http://localhost:8761`




