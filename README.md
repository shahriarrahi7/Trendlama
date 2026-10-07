# TrendLama 🛍️

A modern, full-stack e-commerce web application built with **Next.js 15 (App Router & Turbopack)**, **React 19**, **TypeScript**, and **Tailwind CSS v4**. TrendLama offers a fast, responsive shopping experience featuring product discovery, variant selection, persistent cart state with Zustand, and a multi-step checkout flow validated by Zod and React Hook Form.

---

## 🚀 Live Demo & Preview

- **Local Development URL:** `http://localhost:3000`
- **Turbopack Dev Server:** Instant updates with Next.js 15 Fast Refresh

---

## ✨ Features

- **⚡ Blazing Fast Architecture:** Powered by Next.js 15 App Router and React 19 Server & Client Components.
- **🎨 Modern & Responsive Design:** Sleek UI built with Tailwind CSS v4 and Lucide React icons.
- **🔍 Product Browsing & Filtering:**
  - Category-based filtering (All, Men, Women, Accessories, etc.).
  - Sort by price, newest arrivals, and featured collections.
  - Interactive search bar component.
- **👕 Dynamic Product Details (`/products/[id]`):**
  - Interactive color variant switcher with real-time image updates.
  - Size selection (`S`, `M`, `L`, `XL`, `XXL`).
  - Quantity counter with stock limits.
  - Toast feedback upon adding items to cart.
- **🛒 Persistent Shopping Cart (`/cart`):**
  - Global state management powered by **Zustand**.
  - LocalStorage persistence across page reloads and browser sessions.
  - Hydration-safe state handling for seamless Next.js SSR compatibility.
  - Item increment/decrement and item removal.
- **📦 Multi-Step Checkout Flow:**
  - **Step 1:** Review Cart Items & Order Summary.
  - **Step 2:** Shipping Address Form with schema validation.
  - **Step 3:** Payment Details Form with credit card formatting and expiration checks.
- **🛡️ Robust Form Validation:** Strict type-safe schema validation using **Zod** and **React Hook Form**.
- **🔔 Toast Notifications:** Real-time user feedback via **React Toastify**.

---

## 🛠️ Tech Stack

| Category | Technology | Description |
| :--- | :--- | :--- |
| **Framework** | [Next.js 15](https://nextjs.org/) | React Framework with App Router, Turbopack, and SSR/SSG |
| **Library** | [React 19](https://react.dev/) | Latest React version with Actions and modern hooks |
| **Language** | [TypeScript 5](https://www.typescriptlang.org/) | End-to-end static type safety |
| **Styling** | [Tailwind CSS v4](https://tailwindcss.com/) | Next-generation utility-first CSS framework |
| **State Management** | [Zustand v5](https://zustand-demo.pmnd.rs/) | Lightweight, hook-based global state with persistence |
| **Forms & Validation** | [React Hook Form](https://react-hook-form.com/) + [Zod](https://zod.dev/) | Performant forms with schema-driven validation |
| **Icons** | [Lucide React](https://lucide.dev/) | Clean, customizable modern SVG icon library |
| **Notifications** | [React Toastify](https://fkhadra.github.io/react-toastify/) | Toast notifications for user interactions |
| **Linting** | [ESLint 9](https://eslint.org/) | Code quality and Next.js recommended lint rules |

---

## 📂 Project Structure

```text
TrendLama-starter/
├── public/                 # Static assets (product images, banners, icons)
│   ├── products/           # Product variant imagery
│   └── featured.png        # Hero banner asset
├── src/
│   ├── app/                # Next.js 15 App Router directory
│   │   ├── cart/           # Multi-step Cart & Checkout page (/cart)
│   │   ├── products/       # Product catalog & dynamic details (/products/[id])
│   │   ├── globals.css     # Global styles & Tailwind CSS imports
│   │   ├── layout.tsx      # Root layout with Navbar and Footer wrappers
│   │   └── page.tsx        # Homepage with featured products & hero banner
│   ├── Components/         # Reusable UI components
│   │   ├── Categories.tsx  # Product category filter tabs
│   │   ├── Filter.tsx      # Sorting and filter dropdowns
│   │   ├── Footer.tsx      # Application footer
│   │   ├── Navbar.tsx      # Header navbar with search & cart badge
│   │   ├── PaymentForm.tsx # Checkout Step 3: Card payment form
│   │   ├── ProductCard.tsx # Product card with variant preview
│   │   ├── ProductInteraction.tsx # Size/color selector & add-to-cart
│   │   ├── ProductList.tsx # Product grid component
│   │   ├── SearchBar.tsx   # Search input bar
│   │   ├── ShippingForm.tsx# Checkout Step 2: Address form
│   │   └── ShoppingCartIcon.tsx # Live cart item badge counter
│   ├── stores/             # Zustand state management
│   │   └── cartStore.ts    # Cart store with persist & hydration logic
│   └── types.tsx           # TypeScript models and Zod validation schemas
├── next.config.ts          # Next.js configuration
├── package.json            # Dependencies and npm scripts
├── postcss.config.mjs      # PostCSS configuration for Tailwind CSS v4
├── tsconfig.json           # TypeScript configuration
└── README.md               # Project documentation
