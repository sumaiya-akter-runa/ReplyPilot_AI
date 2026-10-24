<div align="center">

# ReplyPilot AI

**An AI assistant that helps Facebook sellers reply faster, track orders and never lose a customer.**

![Flutter](https://img.shields.io/badge/Flutter-02569B?logo=flutter&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)
![Platform](https://img.shields.io/badge/Platform-Android-3DDC84?logo=android&logoColor=white)

[**Download APK**](https://github.com/sumaiya-akter-runa/ReplyPilot_AI/releases/latest) · [Backend Repository](https://github.com/sumaiya-akter-runa/ReplyPilot_Backend)

</div>

---

## The Problem

Thousands of small businesses in Bangladesh sell through Facebook pages. Their owners answer the same questions all day: *"What is the price?"*, *"Is size M available?"*, *"How much is delivery?"*

- Replies are slow at night or when the seller is busy, and customers leave
- It is hard to remember who wanted what and who needs a follow-up

## The Solution

ReplyPilot turns the seller's own product data into ready-to-send replies, and keeps customers, orders and follow-ups in one place.

> **Prices and stock come from the database. The AI only writes the language.**
> Replies containing numbers that do not match the data are flagged. Nothing is ever sent automatically.

## How It Works

```mermaid
flowchart LR
    A[Customer messages<br/>on Messenger] --> B[Seller copies<br/>the message]
    B --> C[Reply Studio<br/>in the app]
    C --> D[Backend reads<br/>price and stock]
    D --> E[AI writes<br/>the reply]
    E --> F[Seller reviews,<br/>edits and sends]
```

1. Copy the customer's message from Messenger
2. Paste it into **Reply Studio**
3. The app checks your products and writes a reply in Bangla, Banglish or English
4. Review, edit, copy and send it yourself

## Features

| Module | What it does |
|---|---|
| **Reply Studio** | AI replies using real prices and stock, with refine and tone options |
| **Customers** | Track status: new, interested, follow-up, ordered, lost |
| **Orders** | Create from a message; stock decreases automatically, cancel restores it |
| **Follow-up** | Reminders for who to message today, with AI-drafted messages |
| **Products** | Size variants, stock levels, low-stock alerts, FAQs |
| **AI Usage** | Monthly limit enforced on the server |

## Screenshots

| Home | Reply Studio | Customers |
|:---:|:---:|:---:|
| ![Home](screenshots/home.png) | ![Reply Studio](screenshots/reply.png) | ![Customers](screenshots/customers.png) |

| Orders | Follow-up | Products |
|:---:|:---:|:---:|
| ![Orders](screenshots/orders.png) | ![Follow-up](screenshots/followup.png) | ![Products](screenshots/products.png) |

## Installation

1. Open the [latest release](https://github.com/sumaiya-akter-runa/ReplyPilot_AI/releases/latest) and download `app-release.apk`
2. Open it on an Android phone (allow *Install from unknown sources* if asked)
3. Register, add your products and start replying

> The server may take up to a minute to respond on the first request after being idle.

## Tech Stack

| Layer | Technology |
|---|---|
| Mobile app | Flutter, Riverpod |
| Backend | FastAPI, SQLAlchemy |
| Database | PostgreSQL (Neon) |
| AI | Grok API |
| Deployment | Docker on Render |
| Security | JWT authentication, Argon2 password hashing |

## Known Limitations

- Messenger is not connected yet, so messages are pasted manually
- No push notifications
- Android only

## Future Work

- Messenger webhook so customer messages arrive automatically (requires Meta App Review for real customers)
- Push notifications for follow-up reminders
- Share-to-app from Messenger

## Author

**Sumaiya Akter Runa**
