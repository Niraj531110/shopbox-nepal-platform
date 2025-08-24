# Shop-in-a-Box Nepal – API Endpoints

## Auth & User
- POST `/api/auth/register` – Sign up (phone/email/google)
- POST `/api/auth/login` – Log in
- POST `/api/auth/google` – Google OAuth
- GET `/api/user/me` – Profile info

## Seller Registration
- POST `/api/seller/register` – Upload docs, business info
- GET `/api/seller/status` – Registration progress

## Store Creation
- POST `/api/store/create` – Create store, select type/theme
- PUT `/api/store/customize` – Update colors, logo, banner
- GET `/api/store/:id` – Get store info

## Payment Integration
- POST `/api/payment/connect` – Add payment method (Esewa, Khalti, etc.)
- GET `/api/payment/balance` – Seller balance
- POST `/api/payment/withdraw` – Withdraw to bank

## Product Upload
- POST `/api/product/upload` – Add product (photos, AI title/desc/price)
- POST `/api/product/import` – Import from FB/Instagram
- GET `/api/product/list` – List store products

## Delivery Setup
- POST `/api/delivery/create` – Generate shipping label, request pickup
- GET `/api/delivery/track/:id` – Track delivery status

## Order Management
- POST `/api/order/create` – New order
- GET `/api/order/list` – Seller’s orders
- PUT `/api/order/update/:id` – Update status

## Dashboard & Analytics
- GET `/api/dashboard/overview` – Sales, orders, revenue
- GET `/api/dashboard/analytics` – Best products, top customers

## Chat & Grievance
- POST `/api/support/chat` – Start/chat with customer
- POST `/api/support/grievance` – Log complaint

## Monetization/Subscription
- GET `/api/subscription/plans` – List plans
- POST `/api/subscription/subscribe` – Change plan

---
## Sample Payloads

### Register
```json
{
  "fullName": "Niraj Shrestha",
  "email": "niraj@email.com",
  "phone": "9800000000",
  "password": "secure"
}
```

### Upload Product
```json
{
  "storeId": "abc123",
  "title": "AI generated title",
  "description": "AI generated description",
  "images": ["img1.jpg", "img2.jpg"],
  "price": 500,
  "stock": 10,
  "category": "Electronics"
}
```

### Create Delivery
```json
{
  "orderId": "xyz789",
  "partner": "pathao",
  "address": "Kathmandu, Nepal"
}
```