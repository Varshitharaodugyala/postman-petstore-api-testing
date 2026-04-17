# Swagger Petstore API Testing using Postman

This repository contains API testing for the Swagger Petstore using Postman.
The collection includes requests, test scripts, environment variables, and execution screenshots for the assignment tasks.

---

## Project Overview

This project demonstrates API testing of the Swagger Petstore using Postman.
It includes request validation, dynamic test scripting, environment variables, and automated test execution to ensure API reliability and correctness.


##  Application Details
- Base URL: https://petstore.swagger.io/v2
- API Documentation: https://petstore.swagger.io/

 ##  Tools Used
- Postman
- REST APIs
- JavaScript (Postman Test Scripts)
- JSON

##  Environment Setup

This project uses Postman Environment variables for dynamic execution.

##  Environment Variable

| Key | Value |
|-----|------|
| url | https://petstore.swagger.io/v2 |


## How to Run
'''
Import Postman collection
Select environment: PetstoreEnv
Ensure variable:
url = https://petstore.swagger.io/v2
Run collection using Collection Runner

'''

# Assignment Tasks

## 1. Find Pets by Status

### Description

This API retrieves a list of pets filtered by their status.
For this test, the status parameter **available** was used to fetch all pets currently available in the store.


### Request Details

* Method: **GET**
* Endpoint: `/pet/findByStatus`
* Query Parameter: `status=available`

### Test Validation

The following test validations were performed:

* Verified the response status code is **200 OK**
* Confirmed the response body contains pet data
* Checked that the response is returned in JSON format

### Test Result

The API successfully returned a list of pets with status **available**.

### find pets by status test results

![Find Pets by Status](Screenshots/find-pets-by-status.png)


---

## 2. Create Pet

### Description

This API is used to create a new pet in the store by sending pet details in the request body.

### Request Details

* Method: **POST**
* Endpoint: `/pet`
* Request Body: JSON containing pet ID, name, and status.

### Test Validation

The following validations were performed:

* Verified response status code **200 OK**
* Confirmed the response contains the same pet details that were sent in the request
* Verified that the pet ID was created successfully
* Validated response data dynamically using request body

### Test Result

The pet was successfully created and returned in the response.

### Screenshot



![Create Pet](Screenshots/create-pet.png)
![Create Pet Test Results](Screenshots/create-pet-test-results.png)
---

## 3. Status Code Testing

### Description

This task verifies that the API returns appropriate status codes for different scenarios.

### Test Cases

* **Valid Request** → Expected Status Code **200**
* **Not Found Request** → Expected Status Code **404**
* **Invalid Request** → Expected Status Code **400**

### Test Validation

Each request was executed and validated using Postman test scripts to confirm the returned status code.

### Test Result

The API returned the correct status codes for each scenario.

### Screenshot

![Not Found Request](Screenshots/not-found-request.png)


---

## 4. Get Pet Using Environment Variable

### Description

This task demonstrates the use of **Postman environment variables** to dynamically pass values between requests.

### Implementation

* The pet ID returned from the **Create Pet API** was stored in an environment variable.
* The variable was then used in the **Get Pet by ID request**.

Example variable:

{{petId}}

### Test Validation

* Verified that the pet ID stored in the environment variable was used successfully.
* Confirmed the API returned the correct pet details.

### Test Result

The pet details were retrieved successfully using the stored environment variable.

### Screenshot

![Get Pet Using Environment Variable](Screenshots/get-pet-using-environment-variables.png)


![Environment Variable](Screenshots/petstore-environment.png)

## Key Features

- Dynamic test validation using request & response data
- Environment variable usage for reusable testing
- Automated status code verification
- Response time and content-type validation
- End-to-end API testing using Postman Collection Runner

## Test Results

![Test Results](Screenshots/test-results.png)

## Conclusion

All API endpoints were successfully tested with proper validations.  
The collection demonstrates reliable API behavior with dynamic testing and complete coverage of key scenarios.

