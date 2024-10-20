# Geolocation Flask App

## Overview

This project is a simple web application built with Flask that allows users to retrieve geolocation information based on an IP address. Utilizing the [IP Geolocation API](https://ipgeolocation.io/), users can input an IP address to get details about its location.

## Features

- Fetch geolocation data for a provided IP address.
- Automatically retrieves the geolocation of the server's IP if none is provided.
- User-friendly interface for easy IP input and results display.
- Error handling for invalid IP addresses.

### Prerequisites

- Python 3.x
- Flask
- Requests
- An API key from [IP Geolocation API](https://ipgeolocation.io/)

### Installation

1. *Clone the repository:*
```
   git clone https://github.com/Shivani-glitch18/geolocation-flaskapp
   cd geolocation-flaskapp
```   

2. *Set up your environment variables:*

   Creating a .env file in the root directory and adding the API key:

```   
   API_KEY=api_key_here
```

3. *Install dependencies:*
```
   pip install -r requirements.txt
```

### Usage

1. *Run the application:*
```
   python app.py
```  

   The application will be available at http://localhost:5000.
   
3. *Access the application:*
   - At the home page, information of users IP will be displayed.
     
   - Click on `search another IP` button to giving an IP address as input to fetch geolocation data.
   ![image](https://github.com/user-attachments/assets/934365bd-bd17-4756-aa41-744aba7cc2dd)

   
   - If the IP Address does not exist, the following error page is displayed.
   ![image](https://github.com/user-attachments/assets/cf9cfe57-9465-4414-92aa-bb154426da57)

   
   - Otherwise the Geolocation information of the IP given as input will be displayed.
     ![image](https://github.com/user-attachments/assets/6ca650d4-aba5-44a0-ba56-9dbedd3e58db)

   
   


### Using Docker

To run the application using Docker, following these steps:

1. *Build the Docker image:*
```
   docker build -t geoloc .
```   

2. *Run the Docker container:*
```
   docker run --name geo-cont -p 5000:5000 --env-file .env geoloc
```
OR use 
```
   docker run --name geo-count -p 5000:5000 --env API_KEY=<api_key> geoloc
```

*Link to Docker image:*

```  docker pull shivani1820/geoloc:latest ```
   
