# Unautomated Home Page

## Changelog & Section Details

This changelog summarizes the major updates and the structure of the landing page, with details for each section:

### Hero Section
- Eye-catching headline with gradient text and a call-to-action.
- Subheadline explains the value proposition.
- Buttons for "Analyze My Career Free" and "See How It Works".
- Features quick overview (Instant Analysis, Future Strategies, Expert Insights) with icons.

### Benefits Section
- Three-column layout highlighting:
  - Privacy First (shield icon): All analysis is local, no resume stored.
  - Resume Intelligence (brain icon): AI-powered resume scanning.
  - Structured Report (document icon): Output includes risk, reasoning, and references.
- Updated to use SVG icons for a modern look.

### How It Works Section
- Three-step process in card layout:
  - Step 1: Upload Resume (upload icon)
  - Step 2: AI Analyzes It (search icon, "Free" badge)
  - Step 3: Receive Risk Report (document icon, "Paid" badge)
- Responsive, visually engaging, and clear.

### Feature Showcase
- Two-column layout:
  - Left: List of four features (chevron icons, bolded titles, descriptions)
  - Right: Card with brain icon, "Powerful AI Engine" heading, description, and stat boxes (90% skill extraction, 85% risk assessment)
- Emphasizes AI credibility and privacy.

### User Testimonial Section
- Headline and subheadline centered.
- Three testimonial cards with colored initials, italicized quotes, bold names, and roles.
- Summary line: "50+ resumes analyzed so far".
- Modern card style with shadow and rounded corners.

### FAQ Section
- Centered heading and subheading.
- Interactive accordion for questions/answers (only one open at a time).
- Clean, minimal design with dividers.
- JavaScript for accordion functionality.

### Snackbar / Toast Notification
- Bottom-center notification to create urgency (e.g., "A user from <city> just analyzed a resume").
- Light green color, small size, auto-hides after a few seconds, cycles through random cities.
- JavaScript for randomization and timing.

### SEO & Accessibility
- Meta tags for SEO, Open Graph, Twitter Card.
- Sitemap.xml and robots.txt present and referenced.
- Semantic HTML and accessibility best practices.

### Removed Sections
- Pricing Plans section removed for simplicity.
- User Showcase / Community Gallery section removed.

---

This is the landing page for Unautomated, hosted at unautomated.xyz.

## Overview

A simple, SEO-optimized landing page built with HTML and Tailwind CSS. The page is designed to be hosted on GitHub Pages.

## Features

- SEO optimized with proper meta tags (title, description, Open Graph, Twitter Card)
- Responsive design using Tailwind CSS
- Fast loading with minimal dependencies
- Proper sitemap.xml and robots.txt configuration
- CNAME file for custom domain
- **LLMO/ChatGPT Plugin integration** (see below)

## SEO & LLMO Integration

### SEO Features
- **Sitemap**: `sitemap.xml` includes the main landing page URL with lastmod, changefreq, and priority.
- **Robots.txt**: Allows all crawlers and references the sitemap.
- **Meta Tags**: All key meta tags (title, description, canonical, Open Graph, Twitter Card) are present in `index.html`.
- **Structured Data**: (Optional) Add `structured-data.js` for JSON-LD schema if needed for enhanced search appearance.
- **Accessibility**: All images have `alt` attributes, semantic HTML is used, and color contrast is considered.

### LLMO/AI Integration
- **API Endpoint**: `/api/projects.json` returns a list of public projects in JSON format.
- **OpenAPI Spec**: `openapi.json` describes the API for LLM/ChatGPT plugin use.
- **Plugin Manifest**: `ai-plugin.json` provides metadata for ChatGPT plugin discovery.
- **No authentication required** for public endpoints.

#### Example: `/api/projects.json`
```json
[
  {
    "id": "career-risk-analyzer",
    "title": "Career Risk Analyzer",
    "description": "AI-powered tool to analyze your career's automation risk and provide future-proofing strategies."
  },
  {
    "id": "resume-tips",
    "title": "Resume Tips",
    "description": "Guidance and best practices for writing a modern, AI-friendly resume."
  }
]
```

#### OpenAPI Spec: `openapi.json`
- Describes the `/api/projects.json` endpoint and its response schema.

#### Plugin Manifest: `ai-plugin.json`
- Enables ChatGPT and other LLMs to discover and use the public API.

#### Usage (for ChatGPT Plugin Users)
- Add the plugin using the manifest URL: `https://unautomated.xyz/ai-plugin.json`
- Query for public project data using the `/api/projects.json` endpoint.

## Validation Checklist
- [x] Main URL is in `sitemap.xml`
- [x] `robots.txt` references the sitemap
- [x] Meta tags are present and correct in `index.html`
- [ ] Structured data (JSON-LD) present if needed
- [x] Accessibility best practices followed
- [x] CNAME file for custom domain
- [x] README documents SEO and LLMO features
- [x] `/api/projects.json` endpoint present
- [x] `openapi.json` present
- [x] `ai-plugin.json` present

## Deployment

The site is configured to be deployed to GitHub Pages. To deploy:

1. Push your changes to the main branch
2. GitHub Pages will automatically build and deploy the site
3. The site will be available at unautomated.xyz

## Local Development

To run the site locally:

1. Install a local server (e.g., using Python):
```bash
python -m http.server 8000
```

2. Open http://localhost:8000 in your browser

## SEO Configuration

The site includes:
- Meta tags for search engines
- Open Graph tags for social media
- Twitter Card support
- Proper heading hierarchy
- Semantic HTML structure
- Sitemap.xml
- Robots.txt
- CNAME for custom domain 