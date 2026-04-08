# 🎬 CineRec AI: Advanced Recommendation Engine

CineRec AI is a high-performance movie recommendation backend powered by **FastAPI** and **Scikit-Learn**. It implements a content-based filtering system using TF-IDF vectorization and cosine similarity to provide hyper-relevant movie suggestions.

## 🚀 Key Features
- **FastAPI Core**: Asynchronous, high-concurrency API performance.
- **AI Recommendations**: Multi-layer recommendation logic (TF-IDF Similarity + TMDB Genre Discover).
- **Global Movie Data**: Full integration with The Movie Database (TMDB) for posters, backdrops, and metadata.
- **Docker Ready**: Pre-configured for seamless deployment on Render, AWS, or DigitalOcean.

## 🛠️ Tech Stack
- **Framework**: FastAPI
- **Data Science**: Pandas, NumPy, Scikit-Learn
- **Async Communication**: HTTPX
- **Deployment**: Docker, Uvicorn

## 🚦 API Endpoints
| Method | Endpoint | Description |
| :--- | :--- | :--- |
| `GET` | `/health` | System health check |
| `GET` | `/home` | Fetch trending, popular, or upcoming movies |
| `GET` | `/movie/search` | Full bundle: Details + TF-IDF Recs + Genre Recs |
| `GET` | `/tmdb/search` | Search TMDB by keyword (for suggestions) |
| `GET` | `/recommend/tfidf` | Raw TF-IDF recommendations by title |

## 📦 Installation & Setup

1. **Clone the repository**:
   ```bash
   git clone https://github.com/YOUR_USERNAME/CineRec-AI-Backend.git
   cd CineRec-AI-Backend
   ```

2. **Create a virtual environment**:
   ```bash
   python -m venv .venv
   source .venv/bin/activate  # Linux/macOS
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Set Environment Variables**:
   Create a `.env` file and add your TMDB API Key:
   ```env
   TMDB_API_KEY=your_tmdb_api_key_here
   ```

5. **Run Locally**:
   ```bash
   uvicorn main:app --reload --port 8000
   ```

## ☁️ Deployment on Render

1. Create a **New Web Service** on Render.
2. Link your `CineRec-AI-Backend` repository.
3. Use the **Docker** runtime (it will automatically use the `Dockerfile`).
4. Add `TMDB_API_KEY` to the **Environment Variables** section on Render.

---
*Created with ❤️ by the CineRec Team*
