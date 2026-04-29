# Sterling Law Firm Website

A modern, professionally-designed law firm website built with **Astro** and integrated with WordPress backend via GraphQL. This project showcases a complete web presence for a law firm with responsive design, dynamic content integration, and SEO optimization.

[![Astro](https://img.shields.io/badge/Astro-6.1.10-purple?logo=astro)](https://astro.build)
[![Node.js](https://img.shields.io/badge/Node.js-22.12.0+-green?logo=nodedotjs)](https://nodejs.org/)
[![License](https://img.shields.io/badge/License-MIT-blue)](LICENSE)

## ✨ Features

- **🎨 Modern, Professional Design** - Elegant interface with premium color scheme (dark navy and gold accents)
- **📱 Fully Responsive** - Optimized for mobile, tablet, and desktop devices
- **🔗 WordPress Integration** - Live blog posts pulled via GraphQL from WordPress backend
- **⚡ Fast Performance** - Static generation with Astro for blazing-fast load times
- **🔍 SEO Optimized** - Proper meta tags, semantic HTML, and structured data
- **📄 Multiple Pages** - Home, Services, Blog, and Contact pages with professional layouts
- **♿ Accessible** - WCAG compliant components and semantic markup
- **🎯 Call-to-Action Focused** - Strategic CTAs throughout the site for client engagement

## 🏗️ Project Structure

```
src/
├── pages/
│   ├── index.astro              # Homepage with hero, services, team, testimonials
│   ├── services.astro           # Detailed services page with practice areas
│   ├── blog.astro               # Blog page with WordPress GraphQL integration
│   ├── contact.astro            # Contact form and office information
│   └── blog/
│       └── [slug].astro         # Dynamic blog post pages
├── components/
│   ├── HeroSection.astro        # Full-width hero banner
│   ├── ServicesSection.astro    # Services grid with practice areas
│   ├── TeamSection.astro        # Team members showcase
│   ├── TestimonialsSection.astro # Client testimonials with ratings
│   ├── CTASection.astro         # Call-to-action sections
│   └── Header.astro             # Navigation and branding
├── layouts/
│   └── Layout.astro             # Main layout wrapper with header and footer
├── graphql/
│   └── wordPressQuery.ts        # WordPress GraphQL query utilities
└── assets/
    └── [brand assets]           # Images and brand materials
```

## 🎨 Design System

### Color Palette
- **Primary**: `#1a3a52` - Dark Navy Blue
- **Secondary**: `#2d5f7f` - Steel Blue  
- **Accent**: `#d4af37` - Premium Gold
- **Background**: `#f8f9fa` - Light Gray

### Typography
- **Headings**: Playfair Display (serif) - Elegant and professional
- **Body Text**: Open Sans (sans-serif) - Clean and readable

## 📄 Pages

### Home (`/`)
- Eye-catching hero section with primary CTA
- Featured services overview
- Team introduction with member profiles
- Client testimonials and ratings
- Consultation call-to-action

### Services (`/services`)
- Comprehensive service descriptions
- 6 practice areas:
  - Corporate Law
  - Litigation
  - Real Estate Law
  - Family Law
  - Employment Law
  - Intellectual Property
- Benefits and details for each service
- Contact CTA

### Blog (`/blog`)
- Live blog posts from WordPress backend
- Professional blog card layout
- Author attribution and publication dates
- Category filtering
- Newsletter subscription section
- Fallback content if WordPress unavailable

### Contact (`/contact`)
- Complete contact information
- Office location and business hours
- Contact form for inquiries
- Map integration placeholder
- Practice areas reference
- Call-to-action buttons

## 🚀 Getting Started

### Prerequisites
- Node.js 22.12.0 or higher
- npm or yarn package manager

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/sterling-law-firm.git
   cd sterling-law-firm
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start the development server**
   ```bash
   npm run dev
   ```
   The site will be available at `http://localhost:4321`

4. **Build for production**
   ```bash
   npm run build
   ```

5. **Preview the production build**
   ```bash
   npm run preview
   ```

## 📋 Available Commands

| Command | Description |
|---------|-------------|
| `npm run dev` | Start local development server |
| `npm run build` | Build optimized production site to `./dist/` |
| `npm run preview` | Preview production build locally |
| `npm run astro add` | Add new Astro integrations |
| `npm run astro -- --help` | View Astro CLI documentation |

## 🔌 WordPress Integration

This project integrates with a WordPress backend to dynamically fetch blog posts. The integration is handled via GraphQL queries defined in `src/graphql/wordPressQuery.ts`.

### Configuration

Update the GraphQL endpoint in `src/graphql/wordPressQuery.ts`:

```typescript
const res = await fetch('YOUR_WORDPRESS_GRAPHQL_ENDPOINT', {
    // ...
});
```

### Features
- Automatic blog post fetching
- Fallback to sample posts if WordPress is unavailable
- Clean GraphQL query structure
- Type-safe queries

## 📦 Tech Stack

- **Framework**: [Astro](https://astro.build) - Modern static site builder
- **Styling**: CSS with semantic HTML
- **CMS Integration**: WordPress GraphQL
- **Runtime**: Node.js
- **Package Manager**: npm

## 🚀 Deployment

This project is built as a static site, making it easy to deploy anywhere. Popular options include:

- **Vercel** - Recommended for Astro
- **Netlify**
- **AWS S3 + CloudFront**
- **GitHub Pages**
- **Traditional web hosting**

### Deploy to Vercel (recommended)

1. Push your repository to GitHub
2. Connect your GitHub repository to Vercel
3. Vercel will automatically detect Astro and configure the build settings
4. Your site will deploy on every push to main branch

## 📝 Customization

### Update Firm Information
Edit the firm details in:
- `src/pages/contact.astro` - Contact information
- `src/pages/services.astro` - Service descriptions
- `src/components/TeamSection.astro` - Team member details

### Change Colors
Update the color palette in the component files or create a global CSS variables file for consistency.

### Add New Pages
Create new `.astro` files in `src/pages/` directory. Astro will automatically create routes based on file names.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🔗 Resources

- [Astro Documentation](https://docs.astro.build)
- [Astro Community Discord](https://astro.build/chat)
- [GraphQL Documentation](https://graphql.org)

## 📧 Contact & Support

For questions or support regarding this project, please open an issue on GitHub or contact the development team.

---

Built with ❤️ using Astro