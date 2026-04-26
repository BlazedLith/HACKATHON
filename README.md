# Curie Engine

### **[CLICK HERE FOR THE LIVE DEMO](https://curie-engine.vercel.app/)**

**Note to Judges:** Because this application relies on a serverless Pinecone Vector Database for its Semantic Learning Loop, live AWS Bedrock integration, and Tavily internet scraping, **we highly recommend evaluating the platform via the Live Demo link above.** The live environment is fully provisioned and ready for testing. (final branch has the working code. It is also the default branch.)

---

## Local Setup Guide

If you wish to run the project locally from the provided `.zip` file, follow the instructions below.

### Prerequisites

- Node.js (v18+)
- Python 3.9+
- AWS Account with Bedrock Claude 3 access
- Pinecone Account
- Tavily Account

### 1. Backend Setup

1. Navigate to the `backend/` directory (or wherever the Python files reside).
2. Ensure you have the required dependencies. You can install them using the provided `requirements.txt`:
    ```bash
    pip install -r requirements.txt
    ```
    **Note on dependencies:** The `requirements.txt` should include `fastapi`, `uvicorn`, `pydantic`, `boto3`, `requests`, `python-dotenv`, and `pinecone-client` (or `pinecone` as specified).
3. Rename the `.env.example` file to `.env` and fill in your actual API keys.
4. Start the FastAPI server:
    ```bash
    uvicorn main:app --reload
    ```
    The backend will start running on `http://localhost:8000`.

### 2. Frontend Setup

1. Navigate to the `frontend/` directory (where the React code resides).
2. Install the necessary packages:
    ```bash
    npm install
    ```
3. Create a `.env` file in the root of the frontend directory (if needed) or just run the development server. The frontend is configured to default to `http://localhost:8000` for API calls during local development.
4. Start the frontend development server:
    ```bash
    npm run dev
    ```
5. Open your browser and navigate to the localhost URL provided by Vite (usually `http://localhost:5173`).
