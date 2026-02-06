# NordLion Auto - Full Enterprise Project Code

## 🏗️ Project Structure

```
nordlion-auto/
├── prisma/
│   ├── schema.prisma
│   └── seed.js
├── src/
│   ├── app/
│   │   ├── (auth)/
│   │   │   ├── login/
│   │   │   │   └── page.tsx
│   │   │   └── register/
│   │   │       └── page.tsx
│   │   ├── (admin)/
│   │   │   ├── admin/
│   │   │   │   ├── dashboard/
│   │   │   │   │   └── page.tsx
│   │   │   │   ├── vehicles/
│   │   │   │   │   ├── page.tsx
│   │   │   │   │   ├── new/
│   │   │   │   │   │   └── page.tsx
│   │   │   │   │   └── [id]/
│   │   │   │   │       └── edit/
│   │   │   │   │           └── page.tsx
│   │   │   │   ├── users/
│   │   │   │   │   └── page.tsx
│   │   │   │   ├── inquiries/
│   │   │   │   │   └── page.tsx
│   │   │   │   └── layout.tsx
│   │   ├── api/
│   │   │   ├── auth/
│   │   │   │   └── [...nextauth]/
│   │   │   │       └── route.ts
│   │   │   ├── vehicles/
│   │   │   │   ├── route.ts
│   │   │   │   └── [id]/
│   │   │   │       └── route.ts
│   │   │   ├── users/
│   │   │   │   └── route.ts
│   │   │   └── inquiries/
│   │   │       └── route.ts
│   │   ├── vehicles/
│   │   │   ├── page.tsx
│   │   │   └── [id]/
│   │   │       └── page.tsx
│   │   ├── contact/
│   │   │   └── page.tsx
│   │   ├── about/
│   │   │   └── page.tsx
│   │   ├── layout.tsx
│   │   ├── page.tsx
│   │   └── globals.css
│   ├── components/
│   │   ├── ui/
│   │   │   ├── Button.tsx
│   │   │   ├── Input.tsx
│   │   │   ├── Card.tsx
│   │   │   └── Modal.tsx
│   │   ├── admin/
│   │   │   ├── AdminNav.tsx
│   │   │   ├── VehicleForm.tsx
│   │   │   ├── StatsCard.tsx
│   │   │   └── DataTable.tsx
│   │   ├── Navbar.tsx
│   │   ├── Footer.tsx
│   │   ├── VehicleCard.tsx
│   │   ├── HeroSection.tsx
│   │   └── ContactForm.tsx
│   ├── lib/
│   │   ├── prisma.ts
│   │   ├── auth.ts
│   │   ├── utils.ts
│   │   └── validations.ts
│   └── types/
│       └── index.ts
├── public/
│   ├── images/
│   └── favicon.ico
├── .env.example
├── .env.local
├── .gitignore
├── next.config.js
├── tailwind.config.js
├── postcss.config.js
├── tsconfig.json
├── package.json
└── README.md
```

---

## 📋 Complete File Contents

### See individual files being created below for full implementation.

---

## 🚀 Setup Instructions

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
   Update `.env.local` with your credentials.

4. **Set up database**
   ```bash
   npm run db:push
   npm run db:seed
   ```

5. **Run development server**
   ```bash
   npm run dev
   ```

6. **Access the application**
   - Frontend: `http://localhost:3000`
   - Admin: `http://localhost:3000/admin`
   - Default admin: `admin@nordlion.com` / `Admin123!`

---

## 🔑 Key Features

- ✅ Full authentication with NextAuth.js
- ✅ Role-based access control (Admin/User)
- ✅ Complete CRUD for vehicles
- ✅ User management system
- ✅ Inquiry/Contact form with email notifications
- ✅ Image upload to AWS S3
- ✅ Responsive design (mobile-first)
- ✅ Dark mode inspired by ELITA
- ✅ PostgreSQL database with Prisma ORM
- ✅ TypeScript for type safety
- ✅ Tailwind CSS for styling
- ✅ Framer Motion animations
- ✅ Admin dashboard with analytics
- ✅ SEO optimized
- ✅ Production-ready

---

## 📁 Files to Create

Due to GitHub file size limitations, create each file individually using the code below.
