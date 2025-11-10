# Calendar Integration & Email Setup Guide

## Quick Setup: Email Notifications with Formspree (5 minutes)

This is the fastest way to start receiving consultation requests via email.

### Steps:

1. **Go to Formspree.io** and create a free account
2. **Create a new form** and set the email to: `amplifycreativestudios@gmail.com`
3. **Copy your form ID** (looks like: `mabcdefg`)
4. **In index.html**, find this line:**
   ```html
   <form id="contactForm" action="https://formspree.io/f/xyzabcde" method="POST">
   ```
5. **Replace `xyzabcde`** with your actual Formspree form ID

**That's it!** When someone submits the form, you'll receive an email at amplifycreativestudios@gmail.com with all the details including their preferred date and time.

---

## Advanced Option 1: Google Calendar Integration (Recommended)

This requires more setup but provides real-time availability and automatic calendar booking.

### Using Calendly (Easiest - No Coding)

**Pros:** 
- Shows real-time availability from your Google Calendar
- Automatically adds bookings to your calendar
- Sends confirmation emails to both parties
- Prevents double-bookings
- Mobile-friendly

**Setup Steps:**

1. **Sign up at [Calendly.com](https://calendly.com)**
2. **Connect your Google Calendar**
3. **Create an event type** (e.g., "Free Consultation - 30 min")
4. **Set your availability hours** (9 AM - 7 PM)
5. **Copy your Calendly link** (e.g., `https://calendly.com/amplify-studios/consultation`)

6. **Replace the form with Calendly embed:**
   - Option A: Replace entire form section with Calendly widget
   - Option B: Keep form, add "Schedule via Calendly" button

**Here's the code to embed Calendly:**

```html
<!-- Replace form section with this -->
<div style="min-height:630px">
  <iframe 
    src="https://calendly.com/YOUR-USERNAME/consultation" 
    width="100%" 
    height="630" 
    frameborder="0"
    style="border-radius:12px">
  </iframe>
</div>
```

---

## Advanced Option 2: Custom Google Calendar API Integration

**This requires development work but gives you full control.**

### What You Need:
- Google Calendar API access
- Backend server (Node.js, Python, PHP, etc.)
- Google Cloud Project

### High-Level Steps:

1. **Enable Google Calendar API** in Google Cloud Console
2. **Create OAuth 2.0 credentials**
3. **Build backend endpoint** to:
   - Check calendar availability
   - Create calendar events
   - Send confirmation emails
4. **Update your form** to call your backend API

### Example Backend Endpoint (Node.js):

```javascript
// POST /api/book-consultation
const { google } = require('googleapis');

async function bookConsultation(req, res) {
  const { name, email, date, time, service, message } = req.body;
  
  // Initialize Google Calendar API
  const calendar = google.calendar({ version: 'v3', auth });
  
  // Create event
  const event = {
    summary: `Consultation: ${name} - ${service}`,
    description: `Email: ${email}\n\nDetails: ${message}`,
    start: {
      dateTime: `${date}T${convertTo24Hour(time)}:00`,
      timeZone: 'America/New_York',
    },
    end: {
      dateTime: `${date}T${addHour(time)}:00`,
      timeZone: 'America/New_York',
    },
    attendees: [
      { email: 'amplifycreativestudios@gmail.com' },
      { email: email }
    ]
  };
  
  // Insert into calendar
  const result = await calendar.events.insert({
    calendarId: 'primary',
    resource: event,
    sendUpdates: 'all' // Sends email to both parties
  });
  
  res.json({ success: true, eventId: result.data.id });
}
```

---

## Hybrid Solution: Formspree + Calendly Link

**Best of both worlds - Simple to set up, professional experience:**

1. **Keep the current form** for general inquiries
2. **Add Calendly button** as primary booking option
3. **Let users choose** between form or calendar booking

### Update the form section:

```html
<div class="inline" style="margin-bottom:20px">
  <a href="https://calendly.com/amplify-studios/consultation" 
     target="_blank" 
     class="btn" 
     style="flex:1">
    📅 View Available Times (Recommended)
  </a>
  <span class="muted" style="align-self:center">or fill out form below</span>
</div>

<!-- Keep existing form -->
<form id="contactForm" action="https://formspree.io/f/YOUR-ID" method="POST">
  ...
</form>
```

---

## Which Option Should You Choose?

### Choose **Formspree** (Option 1) if:
- ✅ You want something working in 5 minutes
- ✅ You're okay manually managing your calendar
- ✅ You want to review requests before confirming

### Choose **Calendly** if:
- ✅ You want clients to book directly into your calendar
- ✅ You want to prevent double-bookings
- ✅ You want automated email confirmations
- ✅ You need real-time availability display

### Choose **Custom API** if:
- ✅ You have development resources
- ✅ You need complete customization
- ✅ You want to integrate with your own CRM/database
- ✅ You need advanced features (payment, custom workflows, etc.)

---

## Recommended Setup (For Most Studios):

**I recommend the Hybrid approach:**

1. ✅ **Set up Formspree** for immediate email notifications (5 min)
2. ✅ **Set up Calendly** for professional calendar booking (30 min)
3. ✅ **Offer both options** on your website - let clients choose

This gives you:
- Immediate functionality
- Professional calendar integration
- Flexibility for different client preferences
- No coding required

---

## Need Help?

- **Formspree Issues:** support@formspree.io
- **Calendly Issues:** help.calendly.com
- **Custom Development:** Consider hiring a developer on Upwork/Fiverr

---

## Quick Start Checklist

- [ ] Sign up for Formspree
- [ ] Create form with your email
- [ ] Replace form action in index.html
- [ ] Test the form submission
- [ ] (Optional) Sign up for Calendly
- [ ] (Optional) Connect G Calendar to Calendly
- [ ] (Optional) Add Calendly link to website

---

**Questions?** The hybrid approach (Formspree + Calendly) is what most professional studios use and requires zero coding!
