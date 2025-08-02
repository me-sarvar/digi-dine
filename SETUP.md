# ⚙️ DigiDine - Setup Instructions

This guide explains how to set up both the **backend** (NestJS) and **frontend** (Flutter Web) for the DigiDine project.

---

## 🛠️ Backend Setup (NestJS)

### 1. Prerequisites

- Node.js (v18 or above)  
- npm or yarn  
- PostgreSQL running locally or remotely  
- Docker (optional, for containerization)  

---

### 2. Installation

```bash
cd backend
npm install         # or yarn install
```

---

### 3. Environment Variables

Create a `.env` file inside the `backend` folder:

```ini
DATABASE_URL=postgresql://user:password@localhost:5432/digidine_db
JWT_SECRET=your_jwt_secret
JWT_EXPIRES_IN=3600s
```

---

### 4. Database Setup

If using **TypeORM**:

```bash
npm run typeorm migration:run
```

If using **Prisma**:

```bash
npx prisma generate
npx prisma migrate dev
```

---

### 5. Run Backend Server

```bash
npm run start:dev
```

API available at: [http://localhost:3000](http://localhost:3000)

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
- Database credentials, secret keys, and other sensitive environment variables should **not** be committed to version control  

---

## 📂 License

This project is proprietary and strictly for use by the DigiDine project team only.  
See the [LICENSE.md](LICENSE.md) file for full terms and restrictions.
