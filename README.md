# Forever Full Stack Project

## Project Overview
This project is a full-stack e-commerce application with a React frontend and an Express backend. The backend provides RESTful API endpoints for user authentication, product management, cart operations, and order processing including payment integrations with Stripe and Razorpay.

---

## Backend API Endpoints

### User Routes (`/api/user`)
- `POST /register` - Register a new user
- `POST /login` - User login
- `POST /admin` - Admin login

### Product Routes (`/api/product`)
- `POST /add` - Add a new product (Requires admin authentication and supports file uploads)
- `POST /remove` - Remove a product (Requires admin authentication)
- `POST /single` - Get details of a single product
- `GET /list` - List all products

### Cart Routes (`/api/cart`)
- `POST /get` - Get the current user's cart (Requires user authentication)
- `POST /add` - Add an item to the cart (Requires user authentication)
- `POST /update` - Update the cart (Requires user authentication)

### Order Routes (`/api/order`)
- `POST /list` - List all orders (Admin only)
- `POST /status` - Update order status (Admin only)
- `POST /place` - Place a new order (Requires user authentication)
- `POST /stripe` - Place order with Stripe payment (Requires user authentication)
- `POST /razorpay` - Place order with Razorpay payment (Requires user authentication)
- `POST /userorders` - Get orders for the current user (Requires user authentication)
- `POST /verifyStripe` - Verify Stripe payment (Requires user authentication)
- `POST /verifyRazorpay` - Verify Razorpay payment (Requires user authentication)

---

## Environment Variables

### Backend
- `JWT_SECRET` - Secret key for JWT token signing
- `ADMIN_EMAIL` - Admin email for authentication
- `ADMIN_PASSWORD` - Admin password for authentication
- `STRIPE_SECRET_KEY` - Stripe API secret key
- `RAZORPAY_KEY_ID` - Razorpay API key ID
- `RAZORPAY_KEY_SECRET` - Razorpay API key secret
- `PORT` - Port number for backend server (default: 4000)
- `CLOUDINARY_NAME` - Cloudinary cloud name for image uploads
- `CLOUDINARY_API_KEY` - Cloudinary API key
- `CLOUDINARY_SECRET_KEY` - Cloudinary API secret key
- `MONGODB_URI` - MongoDB connection URI

### Frontend
- `VITE_RAZORPAY_KEY_ID` - Razorpay API key ID for frontend payment integration
- `VITE_BACKEND_URL` - Backend API base URL

---

## Setup Instructions

### Backend
1. Navigate to the `backend` directory:
   ```bash
   cd backend
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Create a `.env` file in the `backend` directory and set the required environment variables listed above.
4. Start the backend server:
   - For development with auto-reload:
     ```bash
     npm run server
     ```
   - For production:
     ```bash
     npm start
     ```

### Frontend
1. Navigate to the `frontend` directory:
   ```bash
   cd frontend
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Create a `.env` file in the `frontend` directory and set the required environment variables listed above.
4. Start the frontend development server:
   ```bash
   npm run dev
   ```

---

This README provides an overview of the API endpoints, environment variables, and setup instructions to get the project running locally.
