# Elementor GA4 Lead Tracking

A small, plugin-free snippet that sends **Google Analytics 4 events** when a visitor becomes a lead on an Elementor website:

| Event | When it fires |
|---|---|
| `generate_lead` | An Elementor form is submitted successfully |
| `whatsapp_click` | A WhatsApp link (wa.me / api.whatsapp.com) is clicked |
| `email_click` | A `mailto:` link is clicked |
| `phone_click` | A `tel:` link is clicked |

Based on the lead tracking setup I use on my own website, [sairashakeel.com](https://sairashakeel.com/).

## Requirements

- WordPress with **Elementor Pro** (or PRO Elements) forms
- GA4 already installed, for example with **Google Site Kit**, so `gtag` is available on the page

## Installation

1. In WordPress go to **Elementor > Custom Code > Add New**.
2. Paste the contents of [`lead-tracking.html`](lead-tracking.html).
3. Set **Location** to `</body> - End` and **Conditions** to **Entire Site**.
4. Publish.

## Mark the events as key events in GA4

1. Submit a test form and click a WhatsApp, email or phone link (while logged out).
2. In GA4 go to **Admin > Events > Recent events**. New events can take up to 24 hours to appear.
3. Click the star next to `generate_lead` (and the click events if you want to count them as conversions).

## Notes

- If Site Kit's **Exclude logged-in users** option is on, GA4 is not loaded while you are logged in, so your own tests won't be counted. Test in a private window.
- WhatsApp links are recorded without the pre-filled message text.
- Nothing typed into forms (names, emails, phone numbers) is sent to Google Analytics.

## Author

**Saira Shakeel**, freelance web designer, local SEO and AI automation specialist  
[sairashakeel.com](https://sairashakeel.com/) · [LinkedIn](https://www.linkedin.com/in/sairashakeel/)
