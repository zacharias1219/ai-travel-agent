# **AI Travel Assistant**

**AI Travel Assistant** is an intelligent, full-stack web application that predicts flight prices and provides optimized travel recommendations. Leveraging AI models, this platform uses historical data to forecast prices and suggest the best travel options, combining state-of-the-art tools and frameworks.

---

## **Features**

- **Flight Price Prediction**:
  - Utilizes historical data to forecast flight prices between selected destinations.
  - Supports input for departure and destination airports, non-stop preferences, and more.

- **AI Recommendation Engine**:
  - Powered by **OpenAI** and **MindsDB** to analyze forecast data and provide optimized travel recommendations.

- **Database Integration**:
  - Data stored and managed with **MariaDB** (self-hosted and Dockerized for scalability).
  - Connection with **MindsDB** for AI-powered SQL queries.

- **Frontend User Interface**:
  - Built with **Next.js** and styled using **TailwindCSS** for a modern and responsive design.
  - User-friendly components for airport selection and filtering.

- **Backend Integration**:
  - Developed using **FastAPI**, a Python web framework, for handling data processing and API endpoints.

- **Synthetic Data Generation**:
  - Utilizes **Gretel AI** for creating synthetic datasets to simulate real-world scenarios.

---

## **Tech Stack**

- **Frontend**: Next.js, TailwindCSS
- **Backend**: FastAPI, Jupyter Notebooks
- **Database**: MariaDB (Dockerized), SQLAlchemy
- **AI Models**: MindsDB, Gretel AI, OpenAI
- **Deployment**: AWS EC2 with Docker

---

## **Directory Structure**

```bash
├── app
│   ├── components
│   ├── pages
│   ├── styles
│   ├── services
│   └── utils
├── database
│   ├── schemas
│   ├── migrations
│   └── docker-compose.yml
├── notebooks
│   ├── data-preparation.ipynb
│   └── analysis.ipynb
├── public
│   └── assets
├── README.md
└── package.json
```

---

## **Setup and Installation**

### **Prerequisites**

1. **Node.js**: Version 16 or above.
2. **Python**: Version 3.10 or above.
3. **Docker**: Installed and configured for local development.
4. **MariaDB**: Deployed via Docker.
5. **API Keys**: Obtain credentials for OpenAI, Gretel AI, and MindsDB.

### **Steps**

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/ai-travel-assistant.git
   cd ai-travel-assistant
   ```

2. Install dependencies:

   ```bash
   npm install
   pip install -r requirements.txt
   ```

3. Set up environment variables:
   - Create a `.env.local` file for the frontend:

     ```env
     NEXT_PUBLIC_API_URL=http://localhost:8000
     ```

   - Create a `.env` file for the backend:

     ```env
     MARIADB_URL=mysql://username:password@localhost:3306/travel_db
     MINDSDB_API_KEY=your_mindsdb_api_key
     ```

4. Start the database:

   ```bash
   docker-compose up
   ```

5. Start the backend:

   ```bash
   uvicorn app.main:app --reload
   ```

6. Start the frontend:

   ```bash
   npm run dev
   ```

7. Access the app at `http://localhost:3000`.

---

## **How It Works**

1. **Data Ingestion**:
   - Historical flight price data is loaded into MariaDB using Python and Jupyter Notebooks.

2. **AI Integration**:
   - MindsDB connects to MariaDB for querying and predictive analysis.
   - OpenAI enhances recommendation accuracy.

3. **Frontend Functionality**:
   - Users input travel details like departure, destination, and travel preferences.
   - Results are displayed in a user-friendly UI with real-time filtering.

4. **Backend Processing**:
   - FastAPI handles requests and interacts with AI models for predictions.

---

## **Deployment**

1. **Build for Production**:

   ```bash
   npm run build
   ```

2. **Deploy on AWS EC2**:
   - Provision an EC2 instance.
   - Install Docker and deploy MariaDB using the provided Docker Compose file.
   - Deploy the frontend and backend.

---

## **Future Enhancements**

- Expand to support additional travel data, such as hotels and car rentals.
- Include support for multi-city trips and flexible dates.
- Enhance AI models with user feedback.

---

## **Contributing**

Contributions are welcome! Fork the repository, create a feature branch, and submit a pull request.

---

## **License**

This project is licensed under the MIT License. See the `LICENSE` file for more details.

---
