# flighttripdeals

flighttripdeals is a modern travel landing site built with React, Vite, and Tailwind CSS. It showcases flight deals, popular destinations, airline-specific pages, and a quote request flow that sends traveler information to EmailJS directly from the browser.

## Overview

This project is a front-end website for a flight booking brand. It includes:

- a homepage with a flight search experience
- destination pages for popular routes
- airline-specific landing pages
- trust-building sections such as testimonials, FAQs, and why-book content
- a quote request form that submits via EmailJS
- legal and support pages like privacy, terms, disclaimer, and cancellation policy

## Tech Stack

- React 19
- Vite
- React Router
- Tailwind CSS
- EmailJS for quote form email delivery

## Project Structure

```bash
flighttripdeals/
├── public/
├── src/
│   ├── assets/
│   ├── components/
│   ├── data/
│   ├── App.jsx
│   ├── main.jsx
│   ├── index.css
│   └── App.css
├── index.html
├── package.json
├── vite.config.js
├── vercel.json
├── README.md
└── .env
```

## Features

- Search-based flight quote experience
- Multi-page routing for destinations and airline brands
- Responsive landing page design
- CTA and call popup components for conversions
- Email-based quote submission through EmailJS
- SEO-friendly route pages and static informational content

## Prerequisites

Make sure you have the following installed:

- Node.js 18 or newer
- npm

## Getting Started

1. Clone the repository
2. Install dependencies:

```bash
npm install
```

3. Start the local development server:

```bash
npm run dev
```

4. Open the local URL shown in the terminal, usually:

```bash
http://localhost:5173
```

## Build for Production

```bash
npm run build
```

To preview the production build locally:

```bash
npm run preview
```

## EmailJS Configuration

The quote form sends requests directly from the browser using EmailJS. You need to create an EmailJS account and configure a service and email template before the form can work.

Create a `.env` file in the project root with the following variables:

```bash
VITE_EMAILJS_SERVICE_ID=your_service_id
VITE_EMAILJS_TEMPLATE_ID=your_template_id
VITE_EMAILJS_PUBLIC_KEY=your_public_key
```

The recipient email in the app is currently set to:

```bash
support@flighttripdeals.com
```

The form sends these template parameters:

- `to_email`
- `customer_name`
- `customer_email`
- `customer_phone`
- `trip_type`
- `from_airport`
- `to_airport`
- `departure_date`
- `return_date`
- `travelers`
- `cabin_class`

## Scripts

```bash
npm run dev     # run Vite dev server
npm run build   # create production build
npm run preview # preview production build
npm run lint    # run project linter
```

## Deployment

This project is ready to be deployed to Vercel or any static hosting provider that supports Vite applications. A `vercel.json` file is already included.

## Notes

- This is a front-end-only project; there is no backend or database.
- The quote workflow depends on EmailJS being configured correctly.
- If your site is being used in production, update the company email, phone number, and legal copy as needed.
