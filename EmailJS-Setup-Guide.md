# EmailJS Setup Guide

## Step 1: Create EmailJS Account
1. Go to [https://www.emailjs.com/](https://www.emailjs.com/)
2. Sign up for a free account
3. Verify your email address

## Step 2: Add Email Service
1. Go to "Email Services" in your EmailJS dashboard
2. Click "Add New Service"
3. Choose your email provider (Gmail recommended)
4. Follow the setup instructions for your chosen provider
5. Note down your **Service ID**

## Step 3: Create Email Template
1. Go to "Email Templates" in your dashboard
2. Click "Create New Template"
3. Use this template content:

**Subject:** New message from {{from_name}} - {{subject}}

**Content:**
```
Hello Niveditha,

You have received a new message from your portfolio website:

From: {{from_name}}
Email: {{from_email}}
Subject: {{subject}}

Message:
{{message}}

Best regards,
Your Portfolio Contact Form
```

4. Save the template and note down your **Template ID**

## Step 4: Get Your Public Key
1. Go to "Account" in your dashboard
2. Find your **Public Key** in the API Keys section

## Step 5: Update Your HTML File
Replace these placeholders in your `index.html` file:

1. `YOUR_PUBLIC_KEY` - Replace with your actual public key
2. `YOUR_SERVICE_ID` - Replace with your service ID  
3. `YOUR_TEMPLATE_ID` - Replace with your template ID

## Example:
```javascript
emailjs.init('user_1234567890abcdef'); // Your public key
emailjs.sendForm('service_gmail', 'template_contact', this) // Your service and template IDs
```

## Step 6: Test Your Form
1. Open your portfolio website
2. Fill out the contact form
3. Check your email inbox for the message

## Free Plan Limits
- 200 emails per month
- EmailJS branding in emails
- Basic support

That's it! Your contact form will now send emails directly to your inbox.