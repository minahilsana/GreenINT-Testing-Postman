# Postman API Collection

# GreenINT-Testing-Postman

## Introduction
This repository contains a Postman collection for testing various API endpoints related to social media and user information of GreenINT. The collection includes requests for Reddit, Facebook, Instagram, Username, Phone, and Email endpoints, along with associated test scripts to validate the responses.

## Prerequisites
- Postman installed on your machine
- Access to the GreenINT running locally or remotely

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/minahilsana/GreenINT-Testing-Postman.git
   ```
2. Open Postman and import the `collection.json` file from the cloned repository.

## Usage
1. Open Postman and import the `collection.json` file.
2. Ensure that GreenINT is running locally or remotely.
3. Select the desired request from the collection and click "Send" to execute the request.
4. The test scripts associated with each request will automatically run and validate the responses.

## Endpoints

### Reddit
- **Method**: POST
- **URL**: `http://localhost:5000/scrap/reddit`
- **Request Body**:
  ```json
  {
      "Username": "asharbinkhalil"
  }
  ```
- **Expected Response**:
  ```json
  {
      "Data": {
          "subredditAboutInfo": {
              "t5_9k181e": {
                  "acceptFollowers": true
              }
          }
      }
  }
  ```

### Facebook
- **Method**: POST
- **URL**: `http://localhost:5000/scrap/facebook`
- **Request Body**:
  ```json
  {
      "Username": "asharbinkhalil"
  }
  ```
- **Expected Response**:
  ```json
  {
      "Data": {
          "home_town": "hometown, Pakistan",
          "name": "Ashar Khalil"
      }
  }
  ```

### Instagram
- **Method**: POST
- **URL**: `http://localhost:5000/scrap/instagram`
- **Request Body**:
  ```json
  {
      "Username": "nemrah_ahmad"
  }
  ```
- **Expected Response**:
  ```json
  {
      "Data": {
          "full_name": "Nemrah Ahmed"
      }
  }
  ```

### Username
- **Method**: POST
- **URL**: `http://localhost:5000/username/search`
- **Request Body**:
  ```json
  {
      "Username": "asharbinkhalil"
  }
  ```
- **Expected Response**:
  ```json
  {
      "Data": {
          "Reddit": {
              "id": "leqs10yz"
          },
          "GitHub": {
              "created_at": "2020-07-24T17:23:05Z"
          }
      }
  }
  ```

### Phone
- **Method**: POST
- **URL**: `http://localhost:5000/phone/search`
- **Request Body**:
  ```json
  {
      "Phone": "3*********"
  }
  ```
- **Expected Response**:
  ```json
  {
      "Data": {
          "CNIC": ["*************"]
      }
  }
  ```

### Email
- **Method**: POST
- **URL**: `http://localhost:5000/email/search`
- **Request Body**:
  ```json
  {
      "Email": "testemail@test.com",
      "SelectedModules": []
  }
  ```
- **Expected Response**:
  ```json
  {
      "Data": {
          "email_to_beatstar": {
              "username": "test"
          }
      }
  }
  ```
