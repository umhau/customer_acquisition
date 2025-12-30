# Setup Guide: Security Camera Lead Generation Site

This guide walks you through customizing and deploying your landing pages.

---

## Quick Start Checklist

- [ ] Replace `[YOUR TEAM NAME]` with your business name in all HTML files
- [ ] Replace `(XXX) XXX-XXXX` with your phone number
- [ ] Replace `contact@yourdomain.com` with your email
- [ ] Set up Cal.com and embed your calendar
- [ ] Deploy to Netlify or Vercel (free)
- [ ] Set up Facebook Pixel and Google Analytics
- [ ] Create your first ads

---

## Step 1: Customize Your Business Info

### Find and Replace These Placeholders

Open each HTML file and replace:

| Find | Replace With |
|------|--------------|
| `[YOUR TEAM NAME]` | Your actual business/team name |
| `(XXX) XXX-XXXX` | Your phone number |
| `+1XXXXXXXXXX` | Your phone number (for tel: links) |
| `contact@yourdomain.com` | Your actual email |
| `[Customer Name]` | Real customer names (for testimonials) |

### Files to Update:
- `site/index.html` (homepage)
- `site/asheville/new-homeowner.html`
- `site/asheville/break-in.html`
- `site/asheville/new-parent.html`
- `site/greenville/new-homeowner.html`

### Quick Replace Command (Optional)
If you have access to a code editor with find/replace:
1. Open the entire `site` folder
2. Find: `[YOUR TEAM NAME]`
3. Replace with: `Your Business Name`
4. Repeat for phone/email

---

## Step 2: Set Up Cal.com (Free Calendar Booking)

1. Go to [cal.com](https://cal.com) and create a free account
2. Set up your availability (when you can take consultation calls)
3. Create an event type called "Free Security Consultation" (15-30 min)
4. Go to **Event Types** → Click your event → **Embed**
5. Copy the embed code

### Add to Your Pages

In each HTML file, find this section:
```html
<div class="calendar-embed">
  <div class="calendar-placeholder">
    <!-- Replace this entire div with Cal.com embed -->
```

Replace the placeholder with your Cal.com embed code:
```html
<div class="calendar-embed">
  <iframe
    src="https://cal.com/YOUR-USERNAME/consultation"
    width="100%"
    height="600"
    frameborder="0">
  </iframe>
</div>
```

---

## Step 3: Add Your Logo

If you're using the Safe Home Security logo:

1. Get the logo image file
2. Save it to `site/images/logo.png`
3. Replace the text logo in each HTML file:

**Before:**
```html
<a href="#" class="logo">[YOUR TEAM NAME]</a>
```

**After:**
```html
<a href="#" class="logo">
  <img src="/images/logo.png" alt="Your Team Name" height="40">
</a>
```

---

## Step 4: Deploy (Free Hosting)

### Option A: Netlify (Recommended)

1. Go to [netlify.com](https://netlify.com) and sign up (free)
2. Drag and drop your `site` folder to deploy
3. Get a free URL like `yoursite.netlify.app`
4. (Optional) Connect your custom domain

### Option B: Vercel

1. Go to [vercel.com](https://vercel.com) and sign up
2. Import this repository or upload files
3. Deploy automatically

### Option C: GitHub Pages

1. Push this repo to GitHub
2. Go to Settings → Pages
3. Set source to main branch, `/site` folder

---

## Step 5: Set Up Tracking

### Facebook Pixel

1. Go to [Facebook Business Manager](https://business.facebook.com)
2. Create a Pixel under Events Manager
3. Copy your Pixel code
4. Add to the `<head>` of each HTML file:

```html
<!-- Facebook Pixel Code -->
<script>
  !function(f,b,e,v,n,t,s)
  {if(f.fbq)return;n=f.fbq=function(){n.callMethod?
  n.callMethod.apply(n,arguments):n.queue.push(arguments)};
  if(!f._fbq)f._fbq=n;n.push=n;n.loaded=!0;n.version='2.0';
  n.queue=[];t=b.createElement(e);t.async=!0;
  t.src=v;s=b.getElementsByTagName(e)[0];
  s.parentNode.insertBefore(t,s)}(window, document,'script',
  'https://connect.facebook.net/en_US/fbevents.js');
  fbq('init', 'YOUR_PIXEL_ID');
  fbq('track', 'PageView');
</script>
<!-- End Facebook Pixel Code -->
```

### Google Analytics 4

1. Go to [analytics.google.com](https://analytics.google.com)
2. Create a property for your site
3. Get your Measurement ID (G-XXXXXXXXXX)
4. Add to the `<head>` of each HTML file:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

---

## Step 6: Create Your Ads

### Facebook/Instagram Ads

1. Go to [Facebook Ads Manager](https://www.facebook.com/adsmanager)
2. Create a campaign with objective: **Leads** or **Traffic**
3. Target your specific audiences:

| Segment | Targeting |
|---------|-----------|
| New Homeowners | Recently moved, Zillow interest, age 25-55 |
| New Parents | Parents with children 0-1, baby products interest |
| Security-Minded | Home security interest, Ring/Nest interest |

4. Set location to your service areas (15-25 mile radius)
5. Link to the matching landing page:
   - New homeowner ad → `/asheville/new-homeowner.html`
   - Parent ad → `/asheville/new-parent.html`

### Google Ads

1. Go to [ads.google.com](https://ads.google.com)
2. Create a Search campaign
3. Target keywords like:
   - "security camera installation asheville"
   - "alarm system greenville sc"
   - "home security near me"

---

## Landing Page URLs (for your ads)

| Page | URL Path | Best For |
|------|----------|----------|
| Asheville - New Homeowner | `/asheville/new-homeowner.html` | Facebook: recently moved |
| Asheville - Break-in | `/asheville/break-in.html` | Retargeting, Nextdoor |
| Asheville - New Parent | `/asheville/new-parent.html` | Facebook: new parents |
| Greenville - New Homeowner | `/greenville/new-homeowner.html` | Facebook: recently moved |
| Homepage | `/index.html` | General brand searches |

---

## Adding More Pages

To add a new segment or location:

1. Copy an existing page (e.g., `asheville/new-homeowner.html`)
2. Update the location/segment-specific text
3. Update the `<title>` and `<meta description>`
4. Deploy

---

## Testing Your Site

Before going live:

1. [ ] All placeholder text is replaced
2. [ ] Phone links work (test on mobile)
3. [ ] Calendar booking works
4. [ ] Pages load fast
5. [ ] Looks good on mobile
6. [ ] Facebook Pixel fires (use Facebook Pixel Helper Chrome extension)
7. [ ] Google Analytics tracking works

---

## Need Help?

- **Cal.com setup**: [cal.com/docs](https://cal.com/docs)
- **Netlify deployment**: [docs.netlify.com](https://docs.netlify.com)
- **Facebook Ads**: [facebook.com/business/help](https://facebook.com/business/help)
- **Google Ads**: [support.google.com/google-ads](https://support.google.com/google-ads)
