# Yoga Form

![mainscreen](https://github.com/Satyam298/Yogaclass-signup-form/assets/79797786/f48a2132-32d5-4577-bbf0-31bd1a586f42) 
![batch](https://github.com/Satyam298/Yogaclass-signup-form/assets/79797786/52761146-5e04-48dc-9ff0-4884ccd34d05)


Live App - https://satyam298.github.io/Yogaclass-signup-form/

## Overview

This project is a web application designed to manage yoga session registrations and payments. It utilizes a PostgreSQL database and a backend API made on Django hosted on Railway and incorporates frontend languages such as HTML, CSS, and JavaScript deployed on GitHub Pages.

## Project Structure

### Database Design

The application's database comprises four main tables:

- **User Table:** Stores basic user information and associated batch IDs.
- **Batch Table:** Contains details of the available yoga batches.
- **Payment Table:** Records payment details.
- **Admission Table:** Confirms user admissions based on successful payments.
If the payment is successful and the admission of the user is confirmed then user data is stored in the admission tables. 

**ER Diagram:** 

![er](https://github.com/Satyam298/Yogaclass-signup-form/assets/79797786/045b462e-89a0-4f50-9a94-2376538d1b73)


### Backend Implementation

- **Models:** Django models are used to define and validate the structure of the database tables.
- **API Creation:** The project includes APIs designed using Django's serializers and views. The `FormSerializer` manages complex data, converting it into JSON format and storing it in the database.
  
  Admission Table
  
  ![myapp_admission](https://github.com/Satyam298/Yogaclass-signup-form/assets/79797786/94ab47c5-4376-4304-b875-076a32cb0899)

  Payment Table
  
  ![myapp_payment](https://github.com/Satyam298/Yogaclass-signup-form/assets/79797786/d2c7978a-9ed1-42ff-8f19-0a9c6d0776ec)

  User Table
  
  ![myapp_user](https://github.com/Satyam298/Yogaclass-signup-form/assets/79797786/85325996-f203-4723-92fb-a0dcdb254645)

  Batch Table

  ![myapp_batch](https://github.com/Satyam298/Yogaclass-signup-form/assets/79797786/772a7ef9-cd13-400b-8620-652df9325f8d)


### Form Validation and Payment Process

Upon registration, user data is validated through the API. The `CompletePayment()` function is triggered, currently returning a constant 'true' to simulate a successful payment confirmation.

![payment_mainpage](https://github.com/Satyam298/Yogaclass-signup-form/assets/79797786/ff4b7ab9-8191-432b-945f-6b9768bfbd8e)

![registered](https://github.com/Satyam298/Yogaclass-signup-form/assets/79797786/4d3a706b-9661-4ac8-badb-ee75a8131c14)

![payment_code](https://github.com/Satyam298/Yogaclass-signup-form/assets/79797786/d72342ae-c5db-477d-8227-ff3be80cda82)


### Assumptions and Flow

- All registered users are admitted due to the stubbed `CompletePayment()` function.
- Users registering for subsequent months are re-registered for those months.
- Clicking the register button in the form generates an HTTP response of 'Payment Successful.'
