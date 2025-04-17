
# 💳 Web Payment Link + QR App

This full-stack web app allows you to generate pre-filled payment links and QR codes for clients. Clients can pay via UPI, wallets, or bank transfer using Razorpay, and their payments go directly to your bank account.

---

## ✨ Features

- Enter client name, amount, and optional note
- Generate unique Razorpay payment link and QR code
- Client can pay via UPI (Google Pay, Paytm, etc.), bank, or wallet
- Store payment metadata in MongoDB
- Webhook updates payment status upon success
- Ready for deployment (Vercel + Render)

---

## 📁 Folder Structure

```
payment-app/
├── client/         # React frontend
├── server/         # Node.js backend with Razorpay & MongoDB
└── deploy/         # Optional deployment configs (vercel/render)
```

---

## ⚙️ Setup Instructions

### 1. Clone & Install

```bash
git clone https://github.com/your-username/payment-app.git
cd payment-app
npm install
cd client && npm install
cd ../server && npm install
```

### 2. Environment Variables

Create a `.env` file inside `/server` with the following:

```
RAZORPAY_KEY_ID=your_key_id
RAZORPAY_SECRET=your_key_secret
RAZORPAY_WEBHOOK_SECRET=your_webhook_secret
MONGO_URI=your_mongodb_connection_string
```

### 3. Local Development

```bash
npm install concurrently
npm run dev  # concurrently starts both client and server
```

---

## 🛰️ Webhook Setup

Set this in Razorpay Dashboard:
```
https://your-backend-url/api/webhook
```

---

## 🌐 Deployment

- **Frontend**: [Vercel](https://vercel.com) or [Netlify](https://www.netlify.com)
- **Backend**: [Render](https://render.com), [Railway](https://railway.app), or [Heroku](https://www.heroku.com)

---

## 📬 Optional Features

- Send payment confirmations using **Twilio** (SMS) or **SendGrid** (Email)
- Add authentication, input validation, or admin dashboard

---

## 🛠 Tech Stack

- **Frontend**: React + Tailwind CSS (optionally)
- **Backend**: Express + Razorpay SDK + MongoDB
- **Tools**: QRCode, dotenv, concurrently

---

## 👩‍💻 Author

Built with ❤️ by [Your Name]
