# Live Resume Template

A modern, AI-customizable resume and portfolio website built with Next.js 16, React 19, and Tailwind CSS 4.

## ✨ Features

- **Professional Design** — Clean, modern layout suitable for any industry
- **Fully Responsive** — Mobile-first design that looks great on all devices
- **Dark Mode** — Built-in dark/light mode support
- **Portfolio Section** — Showcase projects with filtering by category
- **Print / PDF Export** — Print-optimized view at `/print`
- **Contact Form** — Ready-to-integrate contact form with validation
- **Side Navigation** — Desktop sidebar for quick section jumping
- **Smooth Animations** — Framer Motion powered transitions
- **SEO Ready** — Metadata and structured layout for search engines

## 🚀 Quick Start

```bash
# Install dependencies
bun install

# Start development server
bun dev
```

Open [http://localhost:3000](http://localhost:3000) to view your resume.

## 🎨 Customization

All content and configuration lives in two places:

### Content — `src/data/`

| File | What to edit |
|------|-------------|
| [`src/data/profile.ts`](src/data/profile.ts) | Name, title, email, location, summary |
| [`src/data/experience.ts`](src/data/experience.ts) | Work history and achievements |
| [`src/data/skills.ts`](src/data/skills.ts) | Skills, levels, and categories |
| [`src/data/education.ts`](src/data/education.ts) | Degrees, certifications, awards |
| [`src/data/projects.ts`](src/data/projects.ts) | Portfolio projects |

### Configuration — `src/config/site.config.ts`

```typescript
export const siteConfig = {
  theme: {
    primaryColor: '220 92% 50%', // HSL — change to any color
  },
  features: {
    portfolio: true,       // Show/hide portfolio section
    certifications: true,  // Show/hide certifications
    languages: true,       // Show/hide languages
    skillBars: true,       // Show/hide skill progress bars
    sideNav: true,         // Show/hide desktop side navigation
    contactForm: true,     // Show/hide contact form
  },
}
```

### Theme Color Presets

| Color | HSL Value |
|-------|-----------|
| Blue (default) | `220 92% 50%` |
| Purple | `280 70% 50%` |
| Green | `150 70% 45%` |
| Orange | `25 95% 53%` |
| Red | `0 72% 51%` |

### Profile Photo

Place your photo at `public/images/profile.jpg`.

## 📁 Project Structure

```
src/
├── app/                    # Next.js App Router pages
│   ├── page.tsx            # Main resume page
│   ├── portfolio/          # Portfolio pages
│   ├── print/page.tsx      # Print-optimized view
│   └── api/                # API routes (contact, PDF export)
├── components/
│   ├── layout/             # Header, Footer, Navigation
│   ├── resume/             # Resume section components
│   ├── portfolio/          # Portfolio components
│   ├── contact/            # Contact form components
│   └── ui/                 # Reusable UI primitives
├── config/
│   └── site.config.ts      # All site settings & theme
├── data/                   # All user content (edit these!)
└── lib/                    # Utility functions
```

## 🛠️ Commands

| Command | Description |
|---------|-------------|
| `bun dev` | Start development server |
| `bun build` | Build for production |
| `bun lint` | Run ESLint |
| `bun typecheck` | Run TypeScript type checking |

## 📄 Pages & Routes

| Route | Description |
|-------|-------------|
| `/` | Main resume page |
| `/portfolio` | Portfolio project grid |
| `/portfolio/[slug]` | Individual project detail |
| `/print` | Print-optimized resume view |
| `/api/contact` | Contact form handler |
| `/api/pdf/text` | Plain text resume export |
| `/api/pdf/json` | JSON resume export |

## 🧰 Tech Stack

- **[Next.js 16](https://nextjs.org/)** — React framework with App Router
- **[React 19](https://react.dev/)** — UI library
- **[TypeScript 5](https://www.typescriptlang.org/)** — Type-safe JavaScript
- **[Tailwind CSS 4](https://tailwindcss.com/)** — Utility-first CSS
- **[Framer Motion](https://www.framer.com/motion/)** — Animations
- **[Lucide React](https://lucide.dev/)** — Icon library
- **[React Hook Form](https://react-hook-form.com/)** + **[Zod](https://zod.dev/)** — Form handling & validation

## 📬 Contact Form Setup

The contact form at `/api/contact` is ready to connect to any email service. Edit [`src/app/api/contact/route.ts`](src/app/api/contact/route.ts) to integrate with:

- [Resend](https://resend.com/)
- [SendGrid](https://sendgrid.com/)
- [Nodemailer](https://nodemailer.com/)
- Any other email provider

## 🖨️ PDF Export

Visit `/print` for a print-optimized view. Use your browser's print dialog (`Ctrl+P` / `Cmd+P`) to save as PDF.

## 📝 License

MIT — free to use for personal and commercial projects.
