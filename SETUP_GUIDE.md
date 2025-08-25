# Form Data Collection Setup Guide

This guide will help you set up form data collection for your static GitHub Pages site.

## Option 1: Formspree (Recommended - Easiest)

### Setup Steps:

1. **Create a Formspree account:**

   - Go to [formspree.io](https://formspree.io)
   - Sign up for a free account
   - Create a new form

2. **Get your form endpoint:**

   - After creating a form, you'll get a URL like: `https://formspree.io/f/xaybzwkd`
   - Replace `YOUR_FORMSPREE_ID` in the HTML file with your actual form ID

3. **Update the form action:**

   ```html
   <form
     action="https://formspree.io/f/YOUR_ACTUAL_FORM_ID"
     method="POST"
   ></form>
   ```

4. **Add hidden fields for better organization:**
   ```html
   <input
     type="hidden"
     name="_subject"
     value="New Course Inquiry - Indian Cyber Club"
   />
   <input
     type="hidden"
     name="_next"
     value="https://yourusername.github.io/your-repo-name/thank-you.html"
   />
   ```

### Benefits:

- ✅ Free tier available (100 submissions/month)
- ✅ No backend required
- ✅ Email notifications
- ✅ Spam protection
- ✅ Data export to CSV/Excel
- ✅ Works perfectly with static sites

---

## Option 2: Netlify Forms (Alternative)

### Setup Steps:

1. **Deploy to Netlify:**

   - Push your code to GitHub
   - Connect your repo to Netlify
   - Deploy

2. **Add form attributes:**

   ```html
   <form name="inquiry" method="POST" data-netlify="true"></form>
   ```

3. **Add hidden input for Netlify:**
   ```html
   <input type="hidden" name="form-name" value="inquiry" />
   ```

### Benefits:

- ✅ Free tier available
- ✅ Built-in spam protection
- ✅ Email notifications
- ✅ Form submissions dashboard

---

## Option 3: Google Sheets (Advanced)

### Setup Steps:

1. **Create a Google Sheet:**

   - Create a new Google Sheet
   - Add headers: Timestamp, Full Name, Email, Phone, etc.

2. **Set up Google Apps Script:**

   - Use the `google-apps-script.gs` file provided
   - Deploy as a web app
   - Get the web app URL

3. **Update the JavaScript:**
   - Replace `YOUR_GOOGLE_APPS_SCRIPT_URL_HERE` with your actual URL

### Benefits:

- ✅ Data stored in Google Sheets
- ✅ Easy to analyze and export
- ✅ Free with Google account

---

## Option 4: EmailJS (Email Only)

### Setup Steps:

1. **Sign up for EmailJS:**

   - Go to [emailjs.com](https://emailjs.com)
   - Create account and email template

2. **Add EmailJS script:**

   ```html
   <script src="https://cdn.jsdelivr.net/npm/@emailjs/browser@3/dist/email.min.js"></script>
   ```

3. **Update JavaScript to use EmailJS**

### Benefits:

- ✅ Sends emails directly
- ✅ Free tier available
- ✅ Custom email templates

---

## Current Implementation

The form is currently set up for **Formspree** (Option 1). To complete the setup:

1. **Replace the form action URL:**

   ```html
   <form action="https://formspree.io/f/YOUR_FORMSPREE_ID" method="POST"></form>
   ```

2. **Add these hidden fields for better organization:**

   ```html
   <input
     type="hidden"
     name="_subject"
     value="New Course Inquiry - Indian Cyber Club"
   />
   <input type="hidden" name="_captcha" value="false" />
   ```

3. **Optional: Create a thank you page:**
   - Create `thank-you.html` with a success message
   - Add: `<input type="hidden" name="_next" value="https://yourusername.github.io/your-repo-name/thank-you.html">`

## Form Fields Being Collected

The form collects the following data:

- **Personal Information:** Full Name, Email, Phone, Age
- **Course Interest:** Course Selection, Preferred Start Date
- **Background:** Education Level, Profession, Experience
- **Additional Info:** How they heard about you, Comments, Newsletter subscription

## Testing

1. Fill out the form with test data
2. Submit and check your Formspree dashboard
3. Verify email notifications are working
4. Test form validation

## Security & Privacy

- Formspree includes spam protection
- Data is encrypted in transit
- Consider adding a privacy policy page
- Ensure GDPR compliance if serving EU users

## Troubleshooting

**Form not submitting:**

- Check form action URL is correct
- Verify all required fields are filled
- Check browser console for errors

**No email notifications:**

- Check Formspree dashboard settings
- Verify email address in Formspree account
- Check spam folder

**Data not appearing:**

- Check Formspree dashboard
- Verify form ID is correct
- Check form field names match
  Copyright 2025 licenser.author

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

     https://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
-->
