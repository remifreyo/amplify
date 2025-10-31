# Blog Subdomain Setup Guide

This guide will help you set up a blog on a separate subdomain (blog.yourdomain.com) for Amplify Creative Studios.

## Overview

Your main website already links to `https://blog.yourdomain.com` in the navigation. Now you need to:
1. Choose a blogging platform
2. Configure DNS settings
3. Set up the blog
4. Match the branding

---

## Option 1: WordPress (Recommended for Full Control)

### Why WordPress?
- Full customization control
- SEO-friendly
- Thousands of themes and plugins
- Industry standard for blogs

### Setup Steps:

1. **Get Hosting** (if you don't have it already)
   - Recommended hosts: Bluehost, SiteGround, Kinsta, WP Engine
   - Many include WordPress pre-installed

2. **Configure DNS**
   - Log into your domain registrar (e.g., GoDaddy, Namecheap, Cloudflare)
   - Add a CNAME record:
     - Host: `blog`
     - Points to: Your hosting provider's server (e.g., `yourdomain.com` or hosting IP)
     - TTL: 3600 (or default)
   - Alternatively, add an A record pointing to your hosting IP

3. **Install WordPress**
   - Most hosts have one-click WordPress installation
   - Or install manually by downloading from wordpress.org

4. **Choose a Theme**
   - Look for dark, modern themes to match your main site
   - Recommended: Astra, GeneratePress, Neve (all have dark mode options)
   - Customize colors to match your brand:
     - Primary: `#7c3aed` (purple)
     - Secondary: `#22d3ee` (cyan)
     - Background: `#0b0c10`
     - Text: `#e5e7eb`

5. **Essential Plugins**
   - Yoast SEO or Rank Math (for SEO)
   - Akismet Anti-Spam
   - WP Super Cache or W3 Total Cache
   - Contact Form 7 (for contact forms)

6. **Create Initial Content**
   - Behind-the-scenes posts
   - Photography/videography tips
   - Client success stories
   - Equipment reviews
   - Industry news and trends

---

## Option 2: Ghost (Great for Modern Blogs)

### Why Ghost?
- Built specifically for blogging
- Fast and modern
- Clean, minimalist design
- Built-in SEO and newsletter features
- Professional publishing platform

### Setup Steps:

1. **Sign up at Ghost.org** (managed hosting)
   - Choose a plan (starts at $9/month for creators)
   - Or self-host on your own server (more technical)

2. **Configure Custom Domain**
   - In Ghost settings, go to "General" > "Site URL"
   - Add your custom domain: `blog.yourdomain.com`
   - Follow Ghost's DNS configuration instructions

3. **Update DNS Records**
   - Add CNAME record as provided by Ghost
   - Usually: `blog` → `proxy.ghost.io`

4. **Customize Design**
   - Choose a dark theme from Ghost marketplace
   - Or customize the default Casper theme
   - Match colors to your main site

5. **Create Content**
   - Use Ghost's beautiful editor
   - Set up newsletter integration
   - Configure member subscriptions if needed

---

## Option 3: Medium Custom Domain (Easiest Setup)

### Why Medium?
- Easiest to set up
- Built-in audience
- No technical maintenance
- Focus purely on content

### Setup Steps:

1. **Create Medium Publication**
   - Sign up at medium.com
   - Create a new publication for Amplify Creative Studios

2. **Upgrade to Custom Domain**
   - Requires Medium membership ($5/month)
   - Go to publication settings
   - Add custom domain: `blog.yourdomain.com`

3. **Configure DNS**
   - Add CNAME record: `blog` → `custom-domain.medium.com`
   - Medium will verify your domain

4. **Customize Branding**
   - Upload your logo
   - Write a compelling publication description
   - Set up navigation links

5. **Start Publishing**
   - Focus on quality content
   - Leverage Medium's built-in discovery

---

## Option 4: Webflow CMS (For Design-Focused Blogs)

### Why Webflow?
- Professional designer-friendly
- No code required
- Beautiful templates
- Fast and modern

### Setup Steps:

1. **Sign up at Webflow.com**
   - Choose a plan with CMS features

2. **Choose a Blog Template**
   - Browse Webflow templates
   - Look for dark, modern blog templates

3. **Connect Custom Domain**
   - In project settings, add `blog.yourdomain.com`
   - Follow Webflow's DNS instructions
   - Add CNAME record as instructed

4. **Customize Design**
   - Use Webflow Designer to match your branding
   - Match fonts, colors, and style to main site

5. **Add CMS Collections**
   - Set up blog posts collection
   - Add author profiles
   - Configure categories/tags

---

## Option 5: Substack (If Newsletter-First)

### Why Substack?
- Perfect if you want a newsletter-first approach
- Built-in email subscriptions
- Easy to monetize
- Simple, clean interface

### Setup Steps:

1. **Create Substack Publication**
   - Sign up at substack.com
   - Set up your publication

2. **Configure Custom Domain**
   - Go to Settings > Domain
   - Add `blog.yourdomain.com`

3. **Update DNS**
   - Add CNAME record as instructed by Substack
   - Wait for propagation (can take 24-48 hours)

4. **Customize Branding**
   - Add logo
   - Set colors
   - Write welcome email

5. **Start Publishing**
   - Create content that goes to both web and email
   - Build your subscriber list

---

## Quick Comparison

| Platform | Cost | Ease of Setup | Customization | Best For |
|----------|------|---------------|---------------|----------|
| WordPress | $5-50/mo | Medium | ⭐⭐⭐⭐⭐ | Full control, SEO |
| Ghost | $9-199/mo | Medium | ⭐⭐⭐⭐ | Modern publishing |
| Medium | $5/mo | Easy | ⭐⭐ | Quick setup, built-in audience |
| Webflow | $14-42/mo | Medium | ⭐⭐⭐⭐⭐ | Design-focused |
| Substack | Free-$50/mo | Easy | ⭐⭐ | Newsletter-first |

---

## Recommended Content Topics for Amplify Blog

1. **Behind the Scenes**
   - Day in the life of a shoot
   - Studio setup and equipment
   - Post-production workflow

2. **Tips & Tutorials**
   - Photography lighting techniques
   - Video editing tips
   - Podcast recording best practices
   - Social media content strategies

3. **Client Success Stories**
   - Case studies
   - Before/after transformations
   - Testimonials and interviews

4. **Industry Insights**
   - Latest camera gear reviews
   - Video production trends
   - Music production tips
   - Web design trends

5. **Business Advice**
   - How to prepare for a photoshoot
   - What to expect when booking a studio
   - Choosing the right services
   - Maximizing your content RO
