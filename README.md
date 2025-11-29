✈️ Airport Ticket Reservation System (MEVN Stack)
📌 Overview

This project is a full-stack MEVN (MongoDB, Express, Vue.js, Node.js) application for managing airport ticket reservations.
The system allows users to search for flights, book seats, manage their reservations, and interact with a user-friendly interface built using Vue.js.

The backend provides a RESTful API developed with Node.js and Express, while MongoDB is used to store all flight, user and reservation data.

🚀 Features
User Features

Search for available flights

View flight details (airline, date, time, price, destination)

Ticket booking and seat reservation

Cancel or update reservations

User login & registration

Admin Features

Add, edit, or delete flights

View all reservations

Manage users

Ensure data integrity

🛠️ Technologies Used
Frontend

Vue.js

HTML5 / CSS3 / Bootstrap

Axios for API requests

Backend

Node.js

Express.js

MongoDB & Mongoose

Other

RESTful API architecture

JSON-based communication

📂 Project Structure
root/
│── backend/
│   ├── app.js
│   ├── models/
│   ├── routes/
│   ├── package.json
│
│── frontend/
│   ├── src/
│   ├── public/
│   ├── package.json
│
│── docs/
│   └── report.pdf   (optional – full documentation)
│
└── README.md

🔧 Installation & Setup
1️⃣ Clone the repository
git clone https://github.com/your-username/your-repo.git
cd your-repo

2️⃣ Backend Setup
cd backend
npm install
npm start


Server starts at:

http://localhost:3000

3️⃣ Frontend Setup
cd frontend
npm install
npm run serve


App runs at:

http://localhost:8080

📡 API Endpoints (Examples)
Flights
Method	Endpoint	Description
GET	/flights	Get all flights
POST	/flights	Add new flight
GET	/flights/:id	Get specific flight
PUT	/flights/:id	Update flight
DELETE	/flights/:id	Delete flight
Reservations
Method	Endpoint	Description
POST	/reservations	Create reservation
GET	/reservations/user/:id	Get reservations by user
DELETE	/reservations/:id	Cancel reservation
🖼️ Screenshots (optional)

Add images such as:

Homepage

Flight list

Booking page

Admin panel

Example:

/assets/screenshots/home.png

👤 Author

Panagiotis Leftheriotis
