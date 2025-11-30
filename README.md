# 🛠️ Sanosco

**Sanosco** is a RESTful API backend application developed for the **Sanosco company**, a leader in trading various building tools and construction materials. This platform provides comprehensive APIs for managing inventory, orders, and user interactions, allowing customers to browse, order, and manage products effortlessly.

## 📝 Description

Sanosco provides a robust backend API that supports:

- **Product Management**: Complete CRUD operations for items, categories, brands, collections, and advertisements
- **Order Processing**: Full order lifecycle management with order tracking and status updates
- **User Management**: Dual-role system supporting both regular users and managers with role-based access control
- **Shopping Cart**: Cart management with item addition, modification, and checkout functionality
- **Notifications**: Real-time push notifications via Firebase Cloud Messaging
- **Ratings & Reviews**: Product rating and review system
- **File Uploads**: Image upload support for products, brands, categories, and advertisements
- **Analytics**: Chart and reporting endpoints for business insights

## 🏷️ Badges

![Build Status](https://img.shields.io/badge/build-passing-brightgreen)
![License](https://img.shields.io/badge/license-ISC-blue)
![Version](https://img.shields.io/badge/version-1.0.0-yellow)
![Node.js](https://img.shields.io/badge/node.js-v18+-green)
![Express](https://img.shields.io/badge/express-v4.18+-green)

## 🚀 Getting Started

### Prerequisites

- Node.js (v14 or higher)
- MySQL (v5.7 or higher)
- npm or yarn package manager

### Installation

1. **Clone the repository:**

   ```sh
   git clone https://github.com/haydarB11/Sanosco.git
   cd Sanosco
```

2. **Install dependencies:**

```sh
npm install
```

3. **Configure environment variables:**

Create a `.env` file in the root directory with the following variables:

```env
PORT=3070
USER_NAME=your_db_username
PASSWORD=your_db_password
DB_NAME=sanosco_db
DBHOST=127.0.0.1
JWT_SECRET=your_jwt_secret_key
FIREBASE_ADMIN_SDK_PATH=./sansco-b9f2b-firebase-adminsdk-9zchg-5ced75b282.json
TWILIO_ACCOUNT_SID=your_twilio_account_sid
TWILIO_AUTH_TOKEN=your_twilio_auth_token
```

4. **Set up the database:**

Create a MySQL database and update the connection details in your `.env` file. The application uses Sequelize ORM for database management.

5. **Run database migrations:**

```sh
npx sequelize-cli db:migrate
```

6. **Start the server:**

```sh
npm start
```

The server will start on `http://localhost:3070` (or the port specified in your `.env` file).

## 📦 Features

- **RESTful API Architecture**: Clean, well-structured API endpoints following REST principles
- **Role-Based Access Control**: Separate endpoints for managers and users with JWT authentication
- **File Upload System**: Multer-based image upload for products, brands, categories, and advertisements
- **Push Notifications**: Firebase Cloud Messaging integration for real-time notifications
- **SMS Integration**: Twilio integration for OTP verification and notifications
- **Excel Export**: ExcelJS integration for data export functionality
- **Scheduled Tasks**: Node-cron integration for automated background jobs
- **Comprehensive Error Handling**: Structured error responses with appropriate HTTP status codes
- **CORS Support**: Cross-origin resource sharing enabled for frontend integration

## 🛠️ Technologies Used

- **Backend Framework**: Node.js with Express.js
- **Database**: MySQL with Sequelize ORM
- **Authentication**: JSON Web Tokens (JWT)
- **File Upload**: Multer
- **Push Notifications**: Firebase Admin SDK
- **SMS/WhatsApp**: Twilio API
- **Excel Processing**: ExcelJS
- **Task Scheduling**: Node-cron
- **HTTP Client**: Axios
- **Additional Libraries**: Moment.js, Crypto, OpenCage API

## 📁 Project Structure

```
Sanosco/
├── app.js                 # Application entry point
├── config/                # Configuration files
├── controllers/           # Request handlers (Manager & User)
├── models/                # Sequelize database models
├── routes/                # API route definitions
├── services/              # Business logic layer
├── utils/                 # Utility functions (auth, upload, notifications)
├── public/                 # Static file storage
└── statics/               # Static JSON data
```

## 🔌 API Endpoints

### Manager Endpoints
- `/sansco/manager/charts` - Analytics and reporting
- `/sansco/manager/advertisements` - Advertisement management
- `/sansco/manager/offers` - Offer management
- `/sansco/manager/categories` - Category management
- `/sansco/manager/brands` - Brand management
- `/sansco/manager/collections` - Collection management
- `/sansco/manager/items` - Product/item management
- `/sansco/manager/orders` - Order management
- `/sansco/manager/static-contents` - Static content management
- `/sansco/manager` - Manager authentication and profile

### User Endpoints
- `/sansco/user/static-contents` - Static content retrieval
- `/sansco/user/notifications` - User notifications
- `/sansco/user/categories` - Browse categories
- `/sansco/user/favorites` - Favorite items management
- `/sansco/user/brands` - Browse brands
- `/sansco/user/collections` - Browse collections
- `/sansco/user/items` - Browse and search items
- `/sansco/user/advertisements` - View advertisements
- `/sansco/user/carts` - Shopping cart management
- `/sansco/user/orders` - Order placement and tracking
- `/sansco/user/ratings` - Product ratings and reviews
- `/sansco/user` - User authentication and profile

## 🧑‍💻 Contributing

We welcome contributions from the community! To contribute:

1. Fork the repository
2. Create a new branch (`git checkout -b feature-branch`)
3. Commit your changes (`git commit -m 'Add some feature'`)
4. Push to the branch (`git push origin feature-branch`)
5. Open a pull request

## 📝 License

This project is licensed under the ISC License.

## 📞 Contact

    If you have any questions or feedback, feel free to reach out:

- **Name**: Haydar Baddour
- **Email**: haydar.baddour.11@gmail.com
- **GitHub**: [haydarB11](https://github.com/haydarB11)

## 🙏 Acknowledgements

Special thanks to the following technologies and resources that made this project possible:

- Express.js
- Sequelize
- MySQL
- Firebase
- Twilio
- Node.js Community
