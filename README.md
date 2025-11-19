# ✨ SuiteSpot: Online Property Listing & Booking Platform

Welcome to SuiteSpot, the ultimate platform for discovering and booking unique accommodations! Whether you're a traveler seeking the perfect getaway or a host looking to share your space, SuiteSpot connects you with unforgettable experiences. Our intuitive platform makes listing, browsing, and booking a breeze, all powered by a robust and modern tech stack.

## 🚀 Features That Elevate Your Experience

*   **Seamless User Authentication**: Dive in with secure and easy registration, login, and logout, powered by Passport.js.
*   **Effortless Listing Management**: Hosts can effortlessly create, showcase, update, and manage their properties with a few clicks.
*   **Intelligent Booking System**: Find and reserve your dream stay with flexible date selections and real-time availability checks.
*   **Transparent Billing**: Automated bill generation for all confirmed bookings, keeping everything clear and organized.
*   **Dynamic Search & Filter**: Discover your ideal spot! Search by available dates, explore vibrant cities, or find listings near exciting festivals.
*   **Authentic Reviews**: Share your experiences and read genuine feedback from other travelers to make informed decisions.
*   **Smart Automation**: Pending bookings are automatically cancelled if not confirmed within 24 hours, ensuring fair availability for everyone.
*   **Stunning & Responsive Design**: Enjoy a beautiful and fluid user interface on any device, thanks to Bootstrap.

## 🛠️ Built with Cutting-Edge Technologies

SuiteSpot is crafted with a powerful combination of modern web technologies:

*   **Backend Powerhouse**: Node.js & Express.js for a fast, scalable, and efficient server-side.
*   **Reliable Database**: MongoDB, managed with the elegant Mongoose ODM, ensuring flexibility and scalability.
*   **Captivating Frontend**: EJS templating for dynamic content, styled beautifully with the versatility of Bootstrap.
*   **Fortified Security**: Passport.js for robust authentication, utilizing `passport-local-mongoose` for secure user management.
*   **Smooth Sessions**: `express-session` and `connect-mongo` for a seamless and persistent user journey.
*   **Cloud-Powered Media**: Cloudinary (integrated via `cloudConfig.js`) for efficient and scalable image storage.
*   **Automated Efficiency**: `node-cron` handles background tasks, keeping the platform running smoothly.
*   **Developer-Friendly Tools**: `dotenv` for environment variables, `method-override` for RESTful API support, and `ejs-mate` for layout management.

## ⚙️ Quick Start: Get SuiteSpot Running!

Ready to explore SuiteSpot? Follow these simple steps to set up your local development environment:

### 1. Clone the Treasure Trove

```bash
git clone <repository-url>
cd SuiteSpot
```

### 2. Install the Essentials

```bash
npm install
```

### 3. Database Magic: MongoDB Setup

SuiteSpot thrives on MongoDB. Let's get it connected:

*   **MongoDB Atlas**: Create a cluster on MongoDB Atlas or use a local MongoDB instance.
*   **Secure Your `.env`**: Create a `.env` file in the project root and fill in your credentials and API keys:

    ```
    ATLASDB_URL=your_mongodb_connection_string
    SECRET=your_session_secret
    MAP_TOKEN=your_mapbox_token
    CLOUD_NAME=your_cloudinary_cloud_name
    CLOUD_API_KEY=your_cloudinary_api_key
    CLOUD_API_SECRET=your_cloudinary_api_secret
    ```

### 4. Initialize Your Data (Optional, but Recommended!)

Bring your database to life with seed data:

```bash

# To create an admin user:
node init/seedAdmin.js
```

### 5. Ignite the Server!

```bash
npm start
```

Your SuiteSpot adventure begins! Open your browser and navigate to `http://localhost:8080`.

## 🗺️ Navigating SuiteSpot: A User's Guide

1.  **Join the Community**: Easily register or log in to your account.
2.  **Discover & Explore**: Browse a diverse range of properties on the homepage.
3.  **Become a Host**: List your own unique space and share it with the world.
4.  **Book Your Stay**: Select your perfect listing, choose dates, and confirm your booking.
5.  **Manage Your World**: Keep track of your bookings and associated bills with ease.
6.  **Smart Search**: Utilize powerful filters to pinpoint listings by dates, city, or festival.

## 🗄️ Behind the Scenes: Database Schema

Here's a glimpse into the organized structure of SuiteSpot's data (Mongoose Schemas):

*   **User Model**: The heart of our community.
    *   `User` references `Listing`, `Review`, `Booking`, `Bill`.
*   **Listing Model**: Your next favorite place to stay.
    *   `Listing` references `User` (owner).
    *   `Listing` references `Review` (reviews).
*   **Review Model**: Your voice, heard.
    *   `Review` references `User` (author).
    *   `Review` references `Listing`.
*   **Booking Model**: Your confirmed adventure.
    *   `Booking` references `User` (guest).
    *   `Booking` references `Listing`.
*   **Bill Model**: Keeping things clear.
    *   `Bill` references `Booking`.
    *   `Bill` references `User`.

## 📂 Project Structure

```
├── .env
├── .gitignore
├── README.md
├── app.js
├── cloudConfig.js
├── controllers\
│   ├── bookings.js
│   ├── listings.js
│   ├── reviews.js
│   └── users.js
├── database.js
├── init\
│   └── seedAdmin.js
├── middleware.js
├── models\
│   ├── bill.js
│   ├── booking.js
│   ├── listing.js
│   ├── review.js
│   └── user.js
├── package-lock.json
├── package.json
├── public\
├── routes\
│   ├── billing.js
│   ├── booking.js
│   ├── listing.js
│   ├── review.js
│   └── user.js
├── schema.js
├── utils\
└── views\
```

## 🤝 Contribute to SuiteSpot

We welcome your creativity and expertise! If you find a bug, have a brilliant idea, or want to enhance SuiteSpot, please don't hesitate to submit a pull request or open an issue. Let's build something amazing together!
