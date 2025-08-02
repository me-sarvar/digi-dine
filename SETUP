
# ⚙️ DigiDine - Setup Instructions

This guide explains how to set up both the **backend** (FastAPI) and **frontend** (Flutter Web) for the DigiDine project.

---

## 🛠️ Backend Setup (FastAPI)

### 1. Prerequisites

- Python 3.12.5  
- `pipenv` installed  
- PostgreSQL running locally or remotely  

---

### 2. Installation

```bash
cd backend
pipenv install
```

---

### 3. Environment Variables

Create a `.env` file inside the `backend` folder:

```ini
DATABASE_URL=postgresql+psycopg2://user:password@localhost/digidine_db
SECRET_KEY=your_secret_key
ACCESS_TOKEN_EXPIRE_MINUTES=30
```

---

### 4. Database Setup

```bash
pipenv shell
alembic upgrade head
```

---

### 5. Run Backend Server

```bash
pipenv shell
uvicorn app.main:app --reload
```

API available at: [http://127.0.0.1:8000](http://127.0.0.1:8000)  
Docs at: [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)  

---

## 💻 Frontend Setup (Flutter Web)

### 1. Prerequisites

- Flutter SDK (latest stable version)  
- Dart SDK (bundled with Flutter)  

---

### 2. Installation

```bash
cd frontend
flutter pub get
```

---

### 3. Run Web App

```bash
flutter run -d chrome
```

The app will open in your default browser.  

---

### 4. Build for Production

```bash
flutter build web
```

Generated files will be located in `frontend/build/web`. Deploy these to your web server.  

---

## ✅ Additional Notes

- Ensure the backend API URL is correctly set in frontend `lib/config.dart` or equivalent  
- For production, both backend and frontend should run on secure (HTTPS) infrastructure  
- Database, secret keys, and environment-specific configs should never be committed to Git  

---

## 📂 License

This project is proprietary and strictly for use by the DigiDine project team only.  
See the [LICENSE.md](LICENSE.md) file for full terms and restrictions.


---
