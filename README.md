# Store Social Platform

A social media + marketplace platform for store owners, built with **Laravel** (backend) and **Vue.js** (frontend).

---

## 🚀 Features

### 1. User Registration & Authentication
- Store owner name
- Store name
- Email
- Password + Confirm Password
- Store cover image
- Store logo
- Account type: Public / Private
- Redirect to profile after registration
- Laravel Sanctum authentication

### 2. Home Feed
- Display posts from users
- Every 5 posts → display a sponsored product
- After 1 minute of browsing → show an alert asking to sign up
- Like & comment system

### 3. Profile Page
- Display user details
- Show posts & products of the user
- Edit profile info and images

### 4. Posts
- Create post with text + optional image
- Choose visibility: Public / Friends
- Edit & delete posts

### 5. Friends / Followers System
- Send friend requests
- Follow/unfollow accounts
- Friend suggestions

### 6. Products
- Store owners can add products
- Products must be approved by admin before appearing
- Sponsored products appear in the Home feed
- Product categories & images

### 7. Notifications
- **For users**: likes, comments, friend requests, product approvals
- **For admin**: new products pending approval

### 8. Admin Dashboard
- View all users & their content
- Ban/unban users
- Approve/reject products
- View site statistics (optional future feature)

---

## 🛠 Tech Stack
- **Backend**: Laravel 11 + MySQL
- **Frontend**: Vue.js 3 + Pinia + Vue Router
- **Auth**: Laravel Sanctum
- **Storage**: Laravel Storage (Local/S3)

---

## 📂 Project Structure
store-social-platform/
│── backend/ (Laravel)
│ ├── app/
│ ├── routes/
│ ├── database/
│ ├── public/storage/ (uploaded images)
│
│── frontend/ (Vue.js)
│ ├── src/
│ ├── public/
│ ├── components/

yaml
Copy
Edit

---

## ⚡ Installation

### Backend (Laravel)
```bash
composer create-project laravel/laravel store-social-platform
cd store-social-platform
composer require laravel/sanctum
php artisan vendor:publish --provider="Laravel\Sanctum\SanctumServiceProvider"
php artisan migrate
php artisan serve
Frontend (Vue.js)
bash
Copy
Edit
cd ..
npm create vue@latest frontend
cd frontend
npm install
npm install axios vue-router pinia
npm run dev