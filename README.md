# Ecommerce API .NET

Full stack ecommerce web application built with Node.js, Express, HTML, CSS, and JavaScript.

This project demonstrates a simple ecommerce architecture with a frontend product catalog, shopping cart functionality, and backend payment integration structure using MercadoPago SDK.

---

# Features

* Product catalog interface
* Responsive ecommerce landing page
* Shopping cart system
* Product cards with pricing
* Product selection functionality
* Backend API with Express.js
* REST endpoint for payment preference creation
* Static asset serving
* Automatic browser launch on server startup
* ES Modules architecture

---

# Current Project Status

The frontend ecommerce interface and shopping cart functionality are fully operational.

The MercadoPago integration was implemented at the backend/API level for learning purposes, including payment preference generation and SDK configuration.

However, the payment checkout flow is currently in development and is not fully connected to a production payment process.

Current working features:

* Product catalog
* Shopping cart interaction
* Product selection
* Frontend UI
* Express backend server
* MercadoPago SDK integration structure

---

# Technologies Used

## Frontend

* HTML5
* CSS3
* JavaScript
* Responsive Web Design
* CSS Grid
* DOM Manipulation

## Backend

* Node.js
* Express.js
* REST API
* CORS Middleware

## Payment Integration

* MercadoPago SDK
* Backend payment preference generation

## Tools

* npm
* Git & GitHub

---

# Project Architecture

The project follows a client-server architecture.

```text
ecommerce-api-dotnet
│
├── client/
│   ├── index.html
│   ├── script.js
│   └── style.css
│
├── server/
│   ├── index.js
│   ├── package.json
│   └── package-lock.json
│
├── public/
│   └── images/
│
└── README.md
```

---

# Frontend

The frontend was developed using vanilla HTML, CSS, and JavaScript.

Main features include:

* Product cards
* Product descriptions
* Shopping cart interaction
* Responsive layout
* Promotional landing section

---

# Backend Server

The backend server was developed using Express.js and Node.js.

The server:

* Serves static frontend files
* Handles MercadoPago payment requests
* Creates payment preferences dynamically
* Exposes REST endpoints

## Express Server Example

```javascript
app.post("/create_preference", async (req,res)=>{
    try{

        const body = {
            items: [{
                title: req.body.title,
                quantity: Number(req.body.quantity),
                unit_price: Number(req.body.price),
                currency_id: "MXN"
            }]
        };

        const preference = new Preference(client);
        const result = await preference.create({ body });

        res.json({
            id: result.id
        });

    }catch(error){
        console.log(error);
    }
});
```

---

# MercadoPago Integration

The application integrates MercadoPago using the official SDK for Node.js.

Implemented features:

* SDK configuration
* Backend payment preference generation
* Dynamic product pricing
* MXN currency configuration

---

# npm Configuration

The project uses npm and ES Modules.

## package.json

```json
{
  "name": "server",
  "version": "1.0.0",
  "type": "module",
  "main": "index.js"
}
```

---

# Backend Dependencies

| Package     | Purpose                       |
| ----------- | ----------------------------- |
| express     | Backend server framework      |
| cors        | Cross-origin request handling |
| mercadopago | Payment gateway SDK           |
| open        | Automatically opens browser   |

Install dependencies using:

```bash
npm install
```

---

# Application Preview

## Main Ecommerce Interface

<img src="./images/1.jpg" width="800">

---

## Product Catalog Section

<img src="./images/2.jpg" width="800">

---

# Running the Project

## 1. Clone the repository

```bash
git clone https://github.com/AdrielHa/ecommerce-api-dotnet.git
```

---

## 2. Navigate to the server folder

```bash
cd server
```

---

## 3. Install dependencies

```bash
npm install
```

---

## 4. Start the server

```bash
npm start
```

The application will open automatically at:

```text
http://localhost:3000
```

---

# Learning Objectives

This project was built to practice:

* Full stack web development
* Node.js backend architecture
* Express.js APIs
* Ecommerce frontend design
* JavaScript DOM manipulation
* REST API development
* Client-server architecture
* npm dependency management
* Backend payment integration concepts

---

# Author

Adriel Yulissa Hernández Albarrán

Background in Physics with experience in:

* Scientific computing
* Backend development
* Full stack web development
* Numerical modeling
* Data analysis
* Software architecture

