# LifeStream Blood Donation App

LifeStream is a full-stack blood donation platform that connects donors with recipients, manages blood requests, and keeps user profile and donation history in one place.

## Project Structure

This repository contains two apps:

### [LifeStream-Backend](./LifeStream-Backend/)

Node.js and Express API server with MongoDB integration.

- JWT-based user authentication
- Donor, recipient, and admin roles
- Blood request creation, listing, fulfillment, and cancellation
- Donation and request history endpoints
- Request logging middleware

### [LifeStream-Frontend](./LifeStream-Frontend/)

React Native and Expo mobile application.

- Login, registration, and logout flows
- Profile and edit-profile screens
- Blood request creation and browsing
- Donation and request history screens
- Donor search and custom drawer navigation

## Quick Start

Run the backend first, then start the frontend.

1. Install and start the backend:

   ```sh
   cd LifeStream-Backend
   npm install
   npm start
   ```

2. Install and start the frontend in a second terminal:

   ```sh
   cd LifeStream-Frontend
   npm install
   npm start
   ```

See the app-specific READMEs for environment setup:

- [LifeStream-Backend/README.md](./LifeStream-Backend/README.md)
- [LifeStream-Frontend/README.md](./LifeStream-Frontend/README.md)

By default, the backend runs on `http://localhost:5000`. If you test the mobile app on a physical phone, set the frontend API URL to your computer's local network IP address instead of `localhost`.

## Technology Stack

Backend:

- Node.js
- Express.js
- MongoDB with Mongoose
- JSON Web Tokens
- bcrypt

Frontend:

- React Native
- Expo
- Expo Router
- TypeScript
- Axios
- AsyncStorage

## Environment Variables

The backend requires a `.env` file with MongoDB and JWT configuration:

```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
```

The frontend uses `EXPO_PUBLIC_API_BASE_URL` to connect to the backend API. When testing on a physical phone, use your computer's local network IP instead of `localhost`.

```env
EXPO_PUBLIC_API_BASE_URL=http://127.0.0.1:5000
```

If this value is missing, the frontend shows a clear configuration error instead of failing with an undefined API URL.

Note: If your MongoDB password or other values include special characters (for example `@`, `:`, or `/`), URL-encode those characters when placing the connection string in `MONGO_URI` so the host and credentials parse correctly.

## Known Limitations

- Donor search currently uses demo data.
- Notifications currently use demo data.
- Automated frontend and backend test suites are not configured yet.

## Contributors

- [Mohammad Rayan](https://github.com/Mohammad-Rayan) - Full-stack Development, Project Lead
- [Abdul Wahab Subhani](https://github.com/Abdul-Wahab-Subhani) - Frontend Development

## Contributing

1. Fork the repository.
2. Create a feature branch.
3. Make your changes.
4. Test the backend and frontend.
5. Submit a pull request.

---

Made for the blood donation community.
