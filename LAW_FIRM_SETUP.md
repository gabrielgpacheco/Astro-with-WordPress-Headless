# Sterling Law Firm - Astro Website

A professional, fully-featured law firm website built with Astro and integrated with WordPress backend via GraphQL.

## 🎯 Project Overview

This is a complete law firm website featuring:
- **Professional Design**: Modern, elegant design with gold accents and professional color scheme
- **Responsive Layout**: Fully responsive on mobile, tablet, and desktop
- **WordPress Integration**: GraphQL integration for blog posts from WordPress backend
- **Multiple Pages**: Home, Services, Blog, and Contact pages
- **SEO Optimized**: Proper meta tags and semantic HTML

## 📁 Project Structure

```
src/
├── pages/
│   ├── index.astro           # Homepage with hero, services, team, testimonials
│   ├── services.astro        # Detailed services page with all practice areas
│   ├── blog.astro            # Blog page with WordPress integration
│   └── contact.astro         # Contact form and office information
├── layouts/
│   └── Layout.astro          # Main layout with header, footer, global styles
├── components/
│   ├── HeroSection.astro     # Hero banner component
│   ├── ServicesSection.astro # Services grid component
│   ├── TeamSection.astro     # Team members showcase
│   ├── TestimonialsSection.astro # Client testimonials
│   └── CTASection.astro      # Call-to-action section
└── graphql/
    └── wordPressQuery.ts     # WordPress GraphQL query utility
```

## 🎨 Design Features

### Color Scheme
- **Primary**: #1a3a52 (Dark Navy Blue)
- **Secondary**: #2d5f7f (Steel Blue)
- **Accent**: #d4af37 (Gold)
- **Background**: #f8f9fa (Light Gray)

### Typography
- **Headings**: Playfair Display (serif)
- **Body**: Open Sans (sans-serif)

### Components

1. **HeroSection** - Full-width hero banner with call-to-action button
2. **ServicesSection** - 6 practice areas displayed in a responsive grid
3. **TeamSection** - Team member cards with photos and specialties
4. **TestimonialsSection** - Client testimonials with ratings
5. **CTASection** - Call-to-action section for consultations
6. **Header/Footer** - Navigation and contact information in sticky header

## 📄 Pages

### Home (index.astro)
- Hero section with main CTA
- Featured services overview
- Team introduction
- Client testimonials
- Call-to-action for consultations

### Services (services.astro)
- Detailed descriptions of 6 practice areas:
  - Corporate Law
  - Litigation
  - Real Estate
  - Family Law
  - Employment Law
  - Intellectual Property
- Benefits listed for each service
- Consultation CTA

### Blog (blog.astro)
- WordPress GraphQL integration for live blog posts
- Fallback sample blog posts if WordPress unavailable
- Professional blog card layout with images, dates, categories
- Author attribution
- Newsletter subscription section

### Contact (contact.astro)
- Comprehensive contact information
- Office location, phone, email, hours
- Contact form for inquiries
- Map placeholder
- Practice areas reference

## 🔧 Technical Setup

### Dependencies
- Astro 6.1.10+
- Node.js 22.12.0+

### Running the Project

```bash
# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

## 📡 WordPress Integration

The blog page integrates with your WordPress backend via GraphQL:

- **Endpoint**: `https://astro.gabrielpacheco.com.br/graphql`
- **Queries**: Posts with title, excerpt, date, author, categories, featured images
- **Fallback**: Sample blog posts display if WordPress is unavailable

To customize the WordPress endpoint, edit `src/graphql/wordPressQuery.ts`:

```typescript
const res = await fetch('YOUR_WORDPRESS_GRAPHQL_URL', {
    // ... configuration
});
```

## 🎯 Content

### Sample Data
All content uses:
- **Text**: Lorem Ipsum and freely available professional legal descriptions
- **Images**: Unsplash stock images (free, high-quality photos)
- **Team Members**: Stock photography from Unsplash
- **Blog Posts**: Sample content with realistic legal topics

## 🚀 Customization

### Change Firm Name
Update "Sterling Law Firm" throughout:
1. `src/layouts/Layout.astro` - Header/footer
2. `src/pages/index.astro` - Page title
3. Contact information in contact form

### Change Colors
Edit CSS variables in `src/layouts/Layout.astro`:
```css
:root {
    --primary-color: #1a3a52;
    --secondary-color: #2d5f7f;
    --accent-color: #d4af37;
    --text-dark: #2c3e50;
    --text-light: #ecf0f1;
    --border-color: #bdc3c7;
    --background: #f8f9fa;
}
```

### Add Services
Edit the services array in `src/components/ServicesSection.astro` or create individual service pages.

### Update Team Members
Modify the team array in `src/components/TeamSection.astro` with real attorney information and photos.

### Replace Images
All images use Unsplash URLs. Replace with your own images or update the URLs.

## 📱 Responsive Design

The website is fully responsive with breakpoints at:
- **Mobile**: < 768px
- **Tablet**: 768px - 1024px
- **Desktop**: > 1024px

## ♿ Accessibility

- Semantic HTML structure
- Proper heading hierarchy
- Alt text for all images
- ARIA labels where appropriate
- Keyboard navigable

## 🔒 Best Practices

- Clean, maintainable code
- Professional styling and layout
- Fast performance (Astro static site generation)
- SEO-friendly structure
- Mobile-first responsive design

## 📞 Next Steps

1. Replace sample content with real firm information
2. Connect to your WordPress instance for live blog posts
3. Add real team photos and bios
4. Update contact information and office address
5. Customize colors to match your brand
6. Add more pages as needed (practice areas detail, about us, etc.)
7. Set up contact form submissions (email or webhook)
8. Add Google Analytics or other tracking
9. Deploy to your hosting platform

## 📝 License

This template is free to use and customize for your law firm website.

---

**Built with**: Astro, GraphQL, and professional web design principles.
