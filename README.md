# 🦁 NordLion Auto - Enterprise Luxury Vehicle Brokerage Platform

> A full-stack, production-ready luxury vehicle brokerage platform inspired by ELITA.net, built with Next.js 14, TypeScript, Prisma, PostgreSQL, and NextAuth.

[![Next.js](https://img.shields.io/badge/Next.js-14.2-black)](https://nextjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.5-blue)](https://www.typescriptlang.org/)
[![Prisma](https://img.shields.io/badge/Prisma-5.19-2D3748)](https://www.prisma.io/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-15-316192)](https://www.postgresql.org/)

## 🎯 Overview

NordLion Auto is a **7-figure enterprise-grade** web application for luxury vehicle brokerage. It features:

- ✅ **Full Authentication System** with NextAuth.js
- ✅ **Role-Based Access Control** (Admin/User)
- ✅ **Complete Vehicle CRUD** with image uploads
- ✅ **User Management Dashboard**
- ✅ **Inquiry System** with email notifications
- ✅ **Responsive Dark Design** inspired by ELITA
- ✅ **PostgreSQL Database** with Prisma ORM
- ✅ **TypeScript** for complete type safety
- ✅ **Admin Analytics Dashboard**
- ✅ **AWS S3 Integration** for image storage
- ✅ **Production-Ready** with security best practices

---

## 📦 Tech Stack

### Frontend
- **Next.js 14** (App Router)
- **React 18**
- **TypeScript**
- **Tailwind CSS**
- **Framer Motion** (animations)
- **Lucide React** (icons)
- **React Hook Form** + **Zod** (forms & validation)

### Backend
- **Next.js API Routes**
- **Prisma ORM**
- **PostgreSQL**
- **NextAuth.js** (authentication)
- **bcryptjs** (password hashing)
- **Nodemailer** (emails)
- **AWS SDK** (S3 storage)

### DevOps & Tools
- **ESLint** + **Prettier**
- **Vercel** deployment ready
- **Docker** support

---

## 🚀 Quick Start

### Prerequisites

- Node.js 18.17.0 or higher
- PostgreSQL database
- AWS S3 bucket (for image uploads)
- SMTP email service

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/lucdemierre/PossibleWebsite.git
   cd PossibleWebsite
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   ```bash
   cp .env.example .env.local
   ```

   Update `.env.local` with your credentials:
   ```env
   # Database
   DATABASE_URL="postgresql://user:password@localhost:5432/nordlion"

   # NextAuth
   NEXTAUTH_URL="http://localhost:3000"
   NEXTAUTH_SECRET="your-super-secret-key-min-32-chars"

   # AWS S3
   AWS_REGION="us-east-1"
   AWS_ACCESS_KEY_ID="your-access-key"
   AWS_SECRET_ACCESS_KEY="your-secret-key"
   AWS_S3_BUCKET="nordlion-vehicles"

   # Email (SMTP)
   EMAIL_SERVER="smtp://username:password@smtp.gmail.com:587"
   EMAIL_FROM="desk@nordlion.com"
   ```

4. **Set up the database**
   ```bash
   npm run db:push
   npm run db:seed
   ```

5. **Run the development server**
   ```bash
   npm run dev
   ```

6. **Open your browser**
   - Frontend: [http://localhost:3000](http://localhost:3000)
   - Admin Dashboard: [http://localhost:3000/admin](http://localhost:3000/admin)

### Default Admin Credentials

```
Email: admin@nordlion.com
Password: Admin123!
```

---

## 📚 Project Structure

```
nordlion-auto/
├── prisma/
│   ├── schema.prisma          # Database schema
│   └── seed.js                # Seed data
├── src/
│   ├── app/
│   │   ├── (auth)/              # Authentication routes
│   │   │   ├── login/
│   │   │   └── register/
│   │   ├── (admin)/             # Protected admin routes
│   │   │   └── admin/
│   │   │       ├── dashboard/
│   │   │       ├── vehicles/
│   │   │       ├── users/
│   │   │       └── inquiries/
│   │   ├── api/                 # API routes
│   │   │   ├── auth/
│   │   │   ├── vehicles/
│   │   │   ├── users/
│   │   │   └── inquiries/
│   │   ├── vehicles/            # Public vehicle pages
│   │   ├── contact/
│   │   ├── about/
│   │   ├── layout.tsx
│   │   ├── page.tsx
│   │   └── globals.css
│   ├── components/
│   │   ├── ui/                  # Reusable UI components
│   │   ├── admin/               # Admin-specific components
│   │   ├── Navbar.tsx
│   │   ├── Footer.tsx
│   │   └── ...
│   ├── lib/
│   │   ├── prisma.ts            # Prisma client
│   │   ├── auth.ts              # Auth configuration
│   │   ├── utils.ts             # Utility functions
│   │   └── validations.ts       # Zod schemas
│   └── types/
│       └── index.ts             # TypeScript types
├── public/
│   └── images/
├── .env.example
├── .gitignore
├── next.config.js
├── tailwind.config.js
├── tsconfig.json
├── package.json
└── README.md
```

---

## 🔑 Key Features

### 1. Authentication & Authorization
- Secure login/register with NextAuth.js
- JWT-based session management
- Password hashing with bcrypt
- Role-based access (Admin/User)
- Protected routes with middleware

### 2. Admin Dashboard
- **Vehicle Management**: Full CRUD operations
- **User Management**: View, edit, delete users
- **Inquiry Management**: View and respond to inquiries
- **Analytics**: Real-time statistics and charts
- **Image Upload**: AWS S3 integration

### 3. Public-Facing Pages
- **Homepage**: Hero section with featured vehicles
- **Vehicle Catalog**: Browse all available vehicles
- **Vehicle Details**: Individual vehicle pages
- **Contact Form**: Inquiry submission with email notifications
- **About Page**: Company information

### 4. Database Schema
- **Users**: Authentication and profile data
- **Vehicles**: Complete vehicle information
- **Inquiries**: Contact form submissions
- **Sessions**: NextAuth session management

---

## 💻 Development

### Available Scripts

```bash
npm run dev          # Start development server
npm run build        # Build for production
npm run start        # Start production server
npm run lint         # Run ESLint
npm run db:generate  # Generate Prisma client
npm run db:push      # Push schema to database
npm run db:studio    # Open Prisma Studio
npm run db:seed      # Seed database with sample data
```

### Environment Variables

See `.env.example` for all required environment variables.

---

## 🚀 Deployment

### Vercel (Recommended)

1. Push your code to GitHub
2. Import repository in Vercel
3. Add environment variables
4. Deploy!

### Docker

```bash
docker build -t nordlion-auto .
docker run -p 3000:3000 nordlion-auto
```

---

## 🔐 Security Features

- ✅ Password hashing with bcrypt
- ✅ CSRF protection
- ✅ SQL injection prevention (Prisma)
- ✅ XSS protection
- ✅ Environment variable security
- ✅ Secure session management
- ✅ Rate limiting (recommended: add Upstash)

---

## 📚 Database Schema

### User
```prisma
model User {
  id            String    @id @default(cuid())
  email         String    @unique
  name          String?
  password      String
  role          Role      @default(USER)
  image         String?
  createdAt     DateTime  @default(now())
  updatedAt     DateTime  @updatedAt
}
```

### Vehicle
```prisma
model Vehicle {
  id            String    @id @default(cuid())
  make          String
  model         String
  year          Int
  price         Float
  mileage       Int
  description   String
  status        Status    @default(AVAILABLE)
  images        String[]
  createdAt     DateTime  @default(now())
  updatedAt     DateTime  @updatedAt
}
```

See `prisma/schema.prisma` for complete schema.

---

## 👥 Contributing

This is a private enterprise project. For access or collaboration inquiries, contact the repository owner.

---

## 📧 Support

For issues, questions, or feature requests:
- Email: desk@nordlion.com
- GitHub Issues: [Create an issue](https://github.com/lucdemierre/PossibleWebsite/issues)

---

## 📝 License

Proprietary - All Rights Reserved

---

## 📌 Complete File Listing

**For the complete source code of all files, see the `FULL_PROJECT_CODE.md` file in this repository.**

The file contains:
- All configuration files (Next.js, TypeScript, Tailwind, Prisma)
- Complete database schema and seed file
- All API routes with full implementations
- All page components (public and admin)
- All reusable UI components
- All utility functions and types
- Production deployment configurations

---

**Built with ❤️ for NordLion Auto**
