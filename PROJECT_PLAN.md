# Security Camera Lead Generation System

## Business Overview
**Company**: Security camera & alarm system installation
**Service Areas**:
- Asheville, NC area
- Greenville/Spartanburg, SC area

**Goal**: Capture local market for security system installations with minimal ad waste through hyper-targeted, personalized landing pages and ads.

---

## Phase 1: Strategy & Customer Segments

### Target Customer Segments

| Segment | Pain Point | Trigger Event | Where to Find Them |
|---------|------------|---------------|-------------------|
| **Recent Break-in Victims** | Fear, urgency, feeling violated | Police report filed, social media posts | Facebook groups, Nextdoor, local news comments |
| **New Homeowners** | Protecting investment, unfamiliar neighborhood | Home purchase | Real estate closing lists, "just moved" posts |
| **New Parents** | Baby safety, monitoring nursery | Birth/pregnancy | Parenting groups, baby product searches |
| **Home-based Business Owners** | Protecting inventory, liability | Started business | Small business groups, Etsy/craft sellers |
| **Vacation Home Owners** | Remote monitoring, peace of mind | Property sits empty | Airbnb host groups, real estate investors |
| **Previous Crime in Neighborhood** | Prevention, "it could happen to me" | News of nearby crime | Nextdoor, neighborhood Facebook groups |

### Geographic Targeting

#### Asheville, NC Area
- Asheville proper
- Biltmore area
- West Asheville
- North Asheville
- Black Mountain
- Weaverville
- Arden
- Fletcher

#### Greenville/Spartanburg, SC Area
- Greenville
- Spartanburg
- Greer
- Simpsonville
- Mauldin
- Taylors
- Five Forks
- Travelers Rest

---

## Phase 2: Website Architecture

### Site Structure

```
homepage (/)
├── /asheville/                    # Asheville hub page
│   ├── /asheville/new-homeowner/  # Segment-specific
│   ├── /asheville/new-parent/
│   ├── /asheville/break-in/
│   └── /asheville/[neighborhood]/ # Hyper-local
│
├── /greenville/                   # Greenville hub page
│   ├── /greenville/new-homeowner/
│   ├── /greenville/new-parent/
│   ├── /greenville/break-in/
│   └── /greenville/[neighborhood]/
│
├── /services/
│   ├── /services/cameras/
│   ├── /services/alarms/
│   └── /services/monitoring/
│
├── /about/
├── /contact/
└── /schedule/                     # Calendar booking
```

### Landing Page Formula (for each segment/location combo)

1. **Hero Section**:
   - Headline addressing their specific situation
   - Local imagery (recognize their area)
   - Clear CTA: "Schedule Free Consultation"

2. **Pain Point Section**:
   - Acknowledge their specific concern
   - Local crime statistics or relevant data

3. **Solution Section**:
   - How your service solves their problem
   - Specific package/recommendation for their situation

4. **Trust Section**:
   - Local testimonials (ideally from same area/segment)
   - "Serving [Area] for X years"
   - Licenses, certifications, insurance

5. **CTA Section**:
   - Calendar embed or chatbot
   - Phone number (local area code)
   - "Free consultation, no obligation"

---

## Phase 3: Lead Capture System

### Option A: Calendar Booking (Recommended)
- **Cal.com** (free, open source) or **Calendly**
- Embed directly on landing pages
- Collect: Name, Phone, Address, "What prompted you to reach out?"
- Auto-confirmation emails

### Option B: Chatbot + Calendar Hybrid
- Simple qualification chatbot:
  1. "Are you looking for cameras, alarms, or both?"
  2. "Is this for home or business?"
  3. "What's your zip code?"
  4. "What's prompting you to look into security?" (captures segment)
  5. → Routes to calendar booking

### Lead Qualification Data to Capture
- Full name
- Phone number
- Email
- Service address (for travel time calculation)
- Property type (home/business)
- What prompted their interest (segment identification)
- Preferred contact method
- Timeline (urgency indicator)

---

## Phase 4: Advertising Strategy

### Facebook/Instagram Ads (Demographic Targeting)

| Segment | Targeting Options |
|---------|------------------|
| New Homeowners | Recently moved, Zillow/Realtor.com interests |
| New Parents | Parents of 0-1 year olds, baby product interests |
| Home Business | Small business owners, Etsy, crafting interests |
| General Security | Home security interests, Ring/Nest interests |

**Ad Creative Formula**:
- Image: Local landmark or neighborhood + security imagery
- Headline: "[Location] Homeowners: [Pain Point]"
- Body: Speak to their specific situation
- CTA: "Get Free Quote" → Segment+Location landing page

### Google Ads (Intent Targeting)

**Keywords to Target**:
- "security camera installation [city]"
- "alarm system installer near me"
- "home security [city]"
- "security cameras [neighborhood]"
- "break in [city]" (careful - may be news searches)

**Negative Keywords**:
- DIY, how to install, wireless (if not your thing)
- jobs, careers, hiring
- reviews (unless you have great ones)

---

## Phase 5: Technical Implementation

### Recommended Tech Stack

| Component | Recommendation | Why |
|-----------|---------------|-----|
| **Framework** | Next.js or Astro | Fast, SEO-friendly, easy landing pages |
| **Hosting** | Vercel or Netlify | Free tier, automatic deploys |
| **Styling** | Tailwind CSS | Fast to build, responsive |
| **Calendar** | Cal.com embed | Free, professional, customizable |
| **Analytics** | Google Analytics 4 + Facebook Pixel | Track ad conversions |
| **Forms** | Native + webhook to email/CRM | Simple, reliable |

### Tracking Requirements
- Facebook Pixel on all pages (for ad optimization)
- Google Analytics with conversion goals
- UTM parameters on all ad links
- Track: Page views, form starts, form completions, calendar bookings

---

## Phase 6: Implementation Checklist

### Week 1: Foundation
- [ ] Choose and set up tech stack
- [ ] Build base site template
- [ ] Create homepage
- [ ] Set up calendar booking (Cal.com)
- [ ] Set up analytics & tracking

### Week 2: Landing Pages - Round 1
- [ ] Asheville hub page
- [ ] Greenville hub page
- [ ] 2-3 segment pages per location (start with highest value)

### Week 3: Ads Setup
- [ ] Facebook Business Manager setup
- [ ] Create ad audiences for each segment
- [ ] Design ad creatives (3-5 per segment)
- [ ] Google Ads account setup
- [ ] Create search campaigns for each location

### Week 4: Launch & Optimize
- [ ] Launch with small budget ($10-20/day)
- [ ] Monitor which segments/locations perform
- [ ] Create more pages for winning segments
- [ ] A/B test headlines and CTAs

---

## Budget Considerations

### Startup Costs
- Domain: ~$15/year
- Hosting: Free (Vercel/Netlify free tier)
- Calendar: Free (Cal.com)
- Total tech: ~$15

### Ongoing Ad Spend (Suggested Starting Point)
- Facebook/Instagram: $300-500/month
- Google Ads: $300-500/month
- Start small, scale what works

### Cost Per Lead Targets
- Good: < $30/lead
- Great: < $15/lead
- Track and optimize ruthlessly

---

## Success Metrics

| Metric | Target | How to Track |
|--------|--------|--------------|
| Cost per click | < $2 | Ad platforms |
| Landing page conversion | > 5% | GA4 |
| Cost per lead | < $30 | Ad spend ÷ bookings |
| Show rate | > 70% | Manual tracking |
| Close rate | > 30% | Manual tracking |
| Customer acquisition cost | < $200 | All costs ÷ customers |

---

## Next Steps

1. **Decide**: Tech stack and calendar solution
2. **Build**: Base website with 1 location + 1 segment
3. **Test**: Run small ad campaign to validate
4. **Scale**: Expand to more segments/locations based on results
