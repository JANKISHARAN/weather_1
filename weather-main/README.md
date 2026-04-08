# Weather App - Run Locally

## Backend

1. Open a terminal and go to the backend folder:

```bash
cd /Users/jankisharan/Desktop/weather-main/backend
```

2. Install Python dependencies:

```bash
python3 -m pip install -r requirements.txt
```

3. Start the backend server:

```bash
python3 -m uvicorn server:app --reload --host 0.0.0.0 --port 8000
```

4. If you need environment variables, create a `.env` file in `backend/` or copy the example file:

```bash
cd /Users/jankisharan/Desktop/weather-main/backend
cp .env.example .env
```

Then edit `.env` and set a valid Weather API key:

```bash
MONGO_URL=mongodb://localhost:27017
DB_NAME=weather
WEATHER_API_KEY=your_api_key_here
```

If you do not set `WEATHER_API_KEY`, the backend will still start, but weather data requests will return `Weather API key is not configured`.

## Frontend

1. Open a terminal and go to the frontend folder:

```bash
cd /Users/jankisharan/Desktop/weather-main/frontend
```

2. Install Node dependencies:

```bash
export PATH=/usr/local/bin:$PATH
npm install --legacy-peer-deps
```

3. Start the frontend app:

```bash
export PATH=/usr/local/bin:$PATH
npm run start
```

4. If port `3000` is already in use, start on a different port:

```bash
export PATH=/usr/local/bin:$PATH
PORT=3001 npm run start
```

## Notes

- Backend runs on `http://localhost:8000` by default.
- Frontend runs on `http://localhost:3000` by default.
- Ensure MongoDB is running locally or update `MONGO_URL` to point to your database.
- If the frontend has a dependency conflict, use `--legacy-peer-deps` when installing.
