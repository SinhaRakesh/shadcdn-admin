# 🧱 Project Stack & Architecture

This project is a **SaaS-ready Admin Panel** built with a scalable and modern frontend architecture using **Next.js**, **shadcn/ui**, **Zustand**, **React Query**, and more. It integrates custom JWT-based authentication with ACL, multi-tenant support, and internationalization.

---

## 🔧 Core Stack

| Concern                  | Tool / Library                                                                 | Description                                                  |
|--------------------------|----------------------------------------------------------------------------------|--------------------------------------------------------------|
| **Framework**            | [Next.js](https://nextjs.org)                                                  | React-based frontend framework with routing & SSR support    |
| **UI Framework**         | [shadcn/ui](https://ui.shadcn.com) + [Tailwind CSS](https://tailwindcss.com)  | Accessible, customizable components                          |
| **State Management**     | [Zustand](https://github.com/pmndrs/zustand) + `persist` middleware             | Lightweight global store with optional localStorage sync     |
| **Data Fetching**        | [React Query](https://tanstack.com/query/latest)                               | Efficient API caching, pagination, mutation handling         |
| **Authentication**       | Custom JWT + Google OAuth                                                      | Tokens issued from backend (Spring Boot)                     |
| **Access Control (ACL)** | Custom `useACL()` Hook                                                         | Role- and permission-based UI control                        |
| **Internationalization** | [next-i18next](https://github.com/i18next/next-i18next)                         | i18n with JSON translations and SSR compatibility            |
| **HTTP Client**          | [Axios](https://axios-http.com)                                                | API requests with auth token handling via interceptors       |
| **Form Handling**        | [React Hook Form](https://react-hook-form.com) + [Zod](https://zod.dev)        | Schema-based validation for scalable form UX                 |

---

## 🧩 Additional Features

- 🔐 Route protection via `<AuthGuard />` and role-check HOCs  
- 🌍 Language support for multiple locales (e.g., English, Hindi, Marathi)  
- 🧠 Multi-tenant support via scoped user context (JWT or API-based)  
- 🌓 Dark/light theme ready (optional with `next-themes`)  
- 🔥 SaaS-ready architecture supporting expansion and subscription logic  
- 📦 Modular file/folder structure for maintainability  

---

## 📁 Project Structure

<pre>
src/
├── components/        # UI components, guards, wrappers
├── pages/             # Next.js routes
├── stores/            # Zustand stores (e.g. auth)
├── hooks/             # Custom hooks (auth, acl, etc.)
├── api/               # React Query API hooks
├── lib/               # Utilities (axios, jwt, etc.)
├── styles/            # Global styles (Tailwind, variables)
├── public/locales/    # i18n JSON files
└── middleware.ts      # Optional SSR middleware
</pre>

---

This setup is designed to be **clean, modular, and extensible** — ideal for production-grade SaaS applications that need fine-grained access control, responsive UI, and global language support.
