# Easiway - College Bus Tracking System

## Overview

Easiway is a real-time college bus tracking system designed to help students track their assigned buses, estimate arrival times, and receive live location updates. The system uses GPS data from the driver's mobile device and displays the bus location on a web application.

The project aims to improve student convenience and reduce waiting time by providing accurate and real-time bus information.

---

## Features

- Real-time bus location tracking
- Student login authentication
- Live bus movement updates
- Interactive map integration
- Multiple bus support
- GPS tracking using driver's mobile phone
- Firebase Realtime Database integration
- ETA (Estimated Time of Arrival) calculation
- Bus route and stop information
- Responsive web interface
- Notification support (future enhancement)

---

## System Architecture

```

Driver Mobile App (Traccar Client)
|
v
Traccar Server
|
v
Python Flask Middleware
|
v
Firebase Realtime Database
|
v
Student Web Application
|
v
Live Bus Tracking Interface

```

---

## Tech Stack

| Technology | Purpose |
|-----------|-----------|
| Python | Middleware development |
| Flask | API handling |
| Firebase Realtime Database | Live data storage |
| HTML | Frontend |
| CSS | UI styling |
| JavaScript | Frontend logic |
| Leaflet.js | Interactive maps |
| OpenStreetMap | Map tiles |
| Traccar | GPS tracking |
| Git & GitHub | Version control |

---

## Project Workflow

1. Driver opens the Traccar Client application.
2. Driver's GPS coordinates are sent to the Traccar Server.
3. The Flask middleware receives location updates.
4. Middleware processes and stores data in Firebase.
5. Student web application listens for Firebase updates.
6. Bus location is displayed on the map in real time.

---

## Folder Structure

```

Easiway/
│
├── backend/
│   ├── app.py
│   ├── requirements.txt
│   └── firebase\_config.json
│
├── frontend/
│   ├── index.html
│   ├── style.css
│   └── script.js
│
├── assets/
│   └── images
│
├── README.md
└── LICENSE

```

---

## Installation

### Clone the Repository

```bash
git clone https://github.com/yourusername/easiway.git

cd easiway
```

---

## Backend Setup

### Create Virtual Environment

```bash
python -m venv venv
```

Activate the virtual environment:

Linux:

```bash
source venv/bin/activate
```

Windows:

```bash
venv\Scripts\activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

Run Flask Server:

```bash
python app.py
```

---

## Firebase Setup

1. Create a Firebase project.
2. Enable Realtime Database.
3. Download the Firebase Admin SDK JSON file.
4. Add the JSON file inside the backend folder.
5. Configure Firebase credentials in the Flask application.

Example Database Structure:

```json
{
  "buses": {
    "bus14": {
      "location": {
        "latitude": 16.845,
        "longitude": 81.070,
        "speed": 45,
        "timestamp": "2026-07-21T10:30"
      }
    }
  }
}
```

---

## Frontend Setup

Simply open:

```bash
index.html
```

Or use a local server:

```bash
python -m http.server 5500
```

---

## Map Integration

The project uses:

- Leaflet.js
- OpenStreetMap Tiles

Features include:

- Live marker updates
- Bus routes
- Stop markers
- Zoom and navigation controls

---

## Authentication

Students can log in using:

```
Roll Number
Password
```

Each student is assigned to a specific bus in Firebase.

Example:

```json
students:
{
   "22IT001":
   {
      "busId":"bus14"
   }
}
```

---

## Future Enhancements

- Push notifications
- ETA prediction using speed and distance
- Driver calling feature
- Bus schedule management
- Mobile application
- Admin dashboard
- Geofencing
- SMS alerts
- Attendance integration
- Multi-college support

---

## Screenshots

Add screenshots of:

- Login Page
- Dashboard
- Live Bus Tracking
- Firebase Database
- Traccar Client
- Map View

---

## Advantages

- Saves student waiting time.
- Provides accurate bus locations.
- Easy to deploy.
- Cost-effective solution.
- Supports multiple buses.
- Scalable architecture.

---

## Challenges Faced

- Dynamic IP configuration.
- Real-time data synchronization.
- Firebase integration.
- GPS accuracy handling.
- Multiple device management.
- Port configuration issues.

---

## Learning Outcomes

Through this project, we learned:

- Real-time system design.
- GPS tracking implementation.
- Flask API development.
- Firebase Realtime Database.
- Interactive map integration.
- Client-server architecture.
- Middleware development.
- Version control using Git and GitHub.

---

## Authors

### Manoj Chinthala

- B.Tech Information Technology
- Sir C. R. Reddy College of Engineering

---

## License

This project is licensed under the MIT License.

---

## Project Status

```

Current Status: Working Prototype

✔ Real-time Tracking
✔ Firebase Integration
✔ Live Map Updates
✔ Multiple Bus Support
✔ Student Authentication
✔ Middleware Implementation

```

---

### Easiway

> Track. Travel. Arrive Smart.
