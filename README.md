# Energyease
Smart Energy Optimization MVP
# Smart Energy Optimization MVP

## Project Overview
This is a basic full-stack web application designed for small businesses in India to monitor their energy use and get simple AI-powered tips to save costs. It has a dark-themed dashboard showing energy consumption in a chart and a panel with cost-saving suggestions. The app is built as a Minimum Viable Product (MVP) with:

- **Frontend**: React with Tailwind CSS for a simple, dark-themed UI.
- **Backend**: Flask with SQLite for user data and energy readings.
- **AI Model**: A basic prediction model using Scikit-learn and rule-based recommendations.

This project was built using GitHub Codespaces, making it easy to set up and test.

## Setup & Execution Steps
You can run this app locally or in Codespaces. Here’s how:

### Using GitHub Codespaces
1. Open the repo on GitHub: `github.com/your-username/smart-energy-optimization`.
2. Click the "Code" button → "Open with Codespaces" → "New Codespace".
3. Wait for the environment to load.

### Running the Backend
1. In the terminal:
2. 2. The backend runs on `http://localhost:5000`.

### Running the Frontend
1. Open a new terminal (click “+” in Codespaces):
2. 2. Click “Open in Browser” when Codespaces prompts you. The app runs on `http://localhost:3000`.

### Local Setup (Optional)
- Install Node.js (from nodejs.org) and Python (from python.org).
- Follow the same steps as above in your local terminal.

## API Endpoints
The backend provides these simple APIs:
- **POST /api/signup**: Creates a new user.
- Request: `{ "email": "user@example.com", "password": "pass123" }`
- Response: `{ "message": "User created" }`
- **POST /api/login**: Logs in a user and returns a token.
- Request: `{ "email": "user@example.com", "password": "pass123" }`
- Response: `{ "token": "jwt-token-here" }`
- **GET /api/energy-data**: Returns dummy energy readings (time and kWh).
- Response: `[{ "time": "12:00", "value": 15.3 }, ...]`
- **GET /api/recommendations**: Returns AI-generated cost-saving tips.
- Response: `["Reduce power usage between 2-4 PM to save costs", ...]`

## Dependencies
### Frontend
- React (`npm install react`)
- Tailwind CSS (`npm install -D tailwindcss`)
- react-chartjs-2 & chart.js (`npm install react-chartjs-2 chart.js`)
- react-router-dom (`npm install react-router-dom`)

### Backend
- Flask (`pip install flask`)
- Flask-SQLAlchemy (`pip install flask-sqlalchemy`)
- PyJWT (`pip install pyjwt`)
- Scikit-learn (`pip install scikit-learn`)

See `frontend/package.json` and `backend/requirements.txt` for full lists.

## How the AI Model Works
- **Prediction**: Uses a simple Linear Regression model from Scikit-learn to predict the next hour’s energy use based on dummy historical data (24 hours of random kWh values).
- **Recommendations**: A rule-based system checks if the predicted usage is 20% higher than the average. If yes, it suggests reducing power usage during peak hours (e.g., 2-4 PM). Otherwise, it says to maintain the current pattern.
- **Data**: For this MVP, dummy data is generated randomly instead of using real IoT sensors.

## Live Demo (Optional)
- Frontend: [Deployed on Netlify/Vercel - add link if you deploy]
- Backend: [Deployed on Render/Heroku - add link if you deploy]

## Notes
- This is a prototype with basic features and dummy data.
- Authentication is simple (no password hashing yet).
- Built for easy scaling to add real IoT data later.

---
Built by Team EnergyEase for the AI- Gati Hackathon  
