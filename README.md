# Amazon-like E-Shopping MERN Application

A complete e-commerce web application built with the MERN stack (MongoDB, Express.js, React.js, Node.js) featuring Amazon-like UI and functionality.

## Features

### Frontend (React.js + TypeScript)
- Modern, responsive Amazon-style UI
- Home page with product grid layout
- User authentication (Login/Register)
- Product details page
- Admin dashboard (protected route)
- Live search functionality with regex
- Responsive design for desktop and mobile

### Backend (Node.js + Express.js)
- RESTful API design
- JWT authentication
- Password hashing with bcrypt
- Role-based access control (Admin/User)
- Image upload with multer
- MongoDB integration with Mongoose

### Database (MongoDB)
- User management (name, email, password, role)
- Product management (name, description, price, category, image)
- Regex-based search functionality

## Project Structure

```
mern-project-us-amazon/
├── backend/
│   ├── models/
│   │   ├── User.js
│   │   └── Product.js
│   ├── routes/
│   │   ├── auth.js
│   │   └── products.js
│   ├── middleware/
│   │   └── auth.js
│   ├── uploads/
│   └── server.js
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   │   ├── Header.tsx
│   │   │   ├── ProductCard.tsx
│   │   │   └── ProtectedRoute.tsx
│   │   ├── pages/
│   │   │   ├── Home.tsx
│   │   │   ├── Login.tsx
│   │   │   ├── Register.tsx
│   │   │   ├── ProductDetails.tsx
│   │   │   └── AdminDashboard.tsx
│   │   ├── context/
│   │   │   └── AuthContext.tsx
│   │   ├── services/
│   │   │   └── api.ts
│   │   ├── App.tsx
│   │   └── App.css
│   └── package.json
├── .env
├── package.json
└── README.md
```

## Installation & Setup

### Prerequisites
- Node.js (v14 or higher)
- MongoDB (local or cloud)
- npm or yarn

### 1. Clone and Install Dependencies

```bash
# Install backend dependencies
npm run install-server

# Install frontend dependencies
npm run install-client

# Or install all at once
npm run install-all
```

### 2. Environment Configuration

Update the `.env` file in the root directory:

```env
MONGODB_URI=your_mongodb_connection_string_here
JWT_SECRET=your_jwt_secret_key_here
PORT=5000
NODE_ENV=development
```

### 3. Run the Application

```bash
# Run both frontend and backend concurrently
npm run dev

# Or run separately:
# Backend only
npm run server

# Frontend only (in another terminal)
npm run client
```

## API Endpoints

### Authentication
- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login

### Products
- `GET /api/products` - Get all products (with optional search)
- `GET /api/products/:id` - Get single product
- `POST /api/products` - Create product (Admin only)
- `PUT /api/products/:id` - Update product (Admin only)
- `DELETE /api/products/:id` - Delete product (Admin only)

## Usage

### For Users:
1. Register/Login to access the platform
2. Browse products on the home page
3. Use the search bar to find specific products
4. Click on products to view detailed information

### For Admins:
1. Register with role "admin" or login with admin credentials
2. Access the Admin Dashboard
3. Add new products with images
4. Edit or delete existing products
5. Manage the product catalog

## Key Features Implemented

### Authentication & Authorization
- JWT-based authentication
- Password hashing with bcrypt
- Role-based access control
- Protected routes for admin functionality

### Search Functionality
- Live search with regex pattern matching
- Search by product name and category
- Real-time filtering as user types

### Image Upload
- Multer integration for file uploads
- Image preview in admin dashboard
- Secure file handling and storage

### Responsive Design
- Mobile-first approach
- Amazon-like UI components
- Grid layout for products
- Responsive navigation and forms

## Technologies Used

### Frontend
- React.js with TypeScript
- React Router for navigation
- Axios for API calls
- Context API for state management

### Backend
- Node.js with Express.js
- MongoDB with Mongoose
- JWT for authentication
- Multer for file uploads
- bcrypt for password hashing

### Development Tools
- Concurrently for running both servers
- Nodemon for backend development
- Create React App for frontend setup

## Security Features

- Password hashing
- JWT token authentication
- Protected API routes
- Role-based access control
- Input validation and sanitization
- Secure file upload handling

## Future Enhancements

- Shopping cart functionality
- Order management system
- Payment integration
- Product reviews and ratings
- Email notifications
- Advanced filtering options
- Wishlist functionality

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## License

This project is licensed under the MIT License.