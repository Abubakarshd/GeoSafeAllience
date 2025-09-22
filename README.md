# GeoSafeAllience
# Smart Tourist Safety MVP

## How to Run the MVP Prototype

### 1. Clone & Branch
```bash
# Clone the repository
git clone https://github.com/Abubakarshd/GeoSafeAllience.git

# Navigate to project directory
cd GeoSafeAllience

# Switch to MVP branch
git checkout mvp
```

### 2. Server Setup
```bash
# Navigate to server directory and install dependencies
cd server && npm install

# Create environment file
cp .env.example server/.env
# Edit .env and set these variables:
# SUPABASE_URL=your_supabase_project_url
# SUPABASE_SERVICE_ROLE_KEY=your_service_role_key
# PORT=8000 (or your preferred port)

# Start the server
npm run dev  # uses nodemon for development
# or
node index.js  # for production
```

### 3. Dashboard Setup
```bash
# Navigate to dashboard directory and install dependencies
cd dashboard && npm install

# Start development server
npm run dev

# Open browser at http://localhost:3000
```

### 4. Mobile App Setup
```bash
# Navigate to mobile app directory and install dependencies
cd mobile-app && npm install

# Start Expo development server
npx expo start

# Scan the QR code with Expo Go app on your phone
# Or press 'a' for Android emulator / 'i' for iOS simulator
```

### 5. Demo Flow
1. **Tourist Registration**
   - Open mobile app
   - Register as new tourist
   - Note your userId for verification

2. **Test Emergency Alert**
   - Navigate to map screen
   - Press the Panic button
   - Alert will be generated with your current location

3. **Monitor Dashboard**
   - Log into admin dashboard
   - View real-time map
   - Verify alert appears with tourist location
   - Check alert details match tourist information

Goal:
- Build a cross-platform **React Native (Expo)** app for tourists
- Build a **React web dashboard** for police/tourism authorities
- Create a **Node.js + Express API** with a database (Supabase/Firebase/PostgreSQL)
- Core features:
  1. Tourist registration/login with name, ID number, trip dates.
  2. Live map (Mapbox or Leaflet) showing current GPS location.
  3. Geofencing: trigger alert when user enters a predefined danger zone.
  4. Big red "Panic" button → POST to /alerts with userID + coordinates.
  5. Admin dashboard shows a real-time map of all tourists and active alerts.

Tech stack:
- Frontend Mobile: React Native + Expo + Mapbox
- Frontend Web: React + Mapbox
- Backend: Node.js + Express + Supabase (realtime)
- Authentication: Supabase Auth
- Deployment: Vercel for dashboard, Expo for mobile preview

Tasks:
1. Create a new Supabase project with tables: users, locations, alerts.
2. Build API routes: POST /register, POST /location, POST /alert, GET /alerts.
3. Implement a React Native screen flow: Login → Map with Panic button.
4. Implement React Web dashboard: secure login, map showing tourists & alerts in realtime.
5. Optional: hash each alert ID to a testnet blockchain (Polygon) for “blockchain-based Digital ID” demo.

Generate starter code for each part with clean folder structure and comments.
