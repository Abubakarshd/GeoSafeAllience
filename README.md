# GeoSafeAllience
# Smart Tourist Safety MVP

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
