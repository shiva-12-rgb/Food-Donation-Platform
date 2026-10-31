# 🍲 ShareBite – Food Donation Platform

**Hackathon problem:** HACK-P197, Food Donation Platform (Food & Restaurant, intermediate)
**Built by:** Shiva Sai Chiluveru
**Live demo:** https://claude.ai/artifact/Fx6GYhif8UMaz2557c2zx2

ShareBite connects restaurants, caterers, shops and community kitchens (donors) with charitable organizations (recipients) so safe surplus food can be listed, requested, collected and tracked from listing to completion.

> ShareBite is a coordination platform, **not** a food-safety certification system. Donors are responsible for following applicable local food-safety rules.

---

## Features

### Donor
- Donor profile (business name, type, area, demo address and phone)
- Create food listings with: title, description, category, dietary type, quantity and unit, preparation time, use-by guidance, handling and storage notes, pickup location, and pickup window
- Required safety declaration before a listing can be published
- Dashboard: active listings, pending requests, completed donations, total portions donated
- Accept or reject requests (with reason), and verify the recipient's 4-digit pickup code to mark food as picked up

### Recipient organization
- Organization profile (type, area, people served)
- Browse and search available listings, with filters for category, dietary type and area
- Request a quantity, name the collector, add a note, and cancel while a request is pending or accepted
- Confirm receipt to complete the donation
- Dashboard: pending, accepted and completed requests, and portions received

### Admin
- Remove or restore listings (with a reason)
- Handle reports: Reviewed, Action taken or Dismissed
- Approve or revoke recipient organization verification

### Platform
- **Status workflow:** Pending → Accepted / Rejected → Picked Up → Completed (plus Cancelled)
- **Status history** timeline for every request (who, from, to, when, note)
- **Confirmation screens** after every key action
- **Double-booking prevention:** a request holds its quantity, and rejecting or cancelling releases it
- **Auto-expiry:** listings expire after the pickup window ends
- **Impact page:** estimated meals redistributed and a category breakdown
- **Food Safety and Limitations page**
- Responsive layout with light and dark mode

---

## Sample data
- 5 donors, 3 recipient organizations and 1 admin view
- 12 sample listings (one already expired), using demo Hyderabad addresses
- 6 sample requests covering every status, and 2 sample reports
- A **Reset demo data** link in the footer restores the original data

All names, addresses and phone numbers are demo data. No real personal information is used.

---

## How to use the demo
1. Use the **Donor / Recipient / Admin** buttons at the top to switch roles, and the dropdown to switch organization.
2. **Donor:** open *New listing*, fill in the form, tick the safety declaration and publish.
3. **Recipient:** open *Browse food*, expand a listing, enter a quantity and collector name, and press *Request*.
4. **Donor:** open *Dashboard* and accept the request.
5. **Recipient:** open *My requests* to see the pickup code.
6. **Donor:** enter that code and press *Confirm pickup*.
7. **Recipient:** press *Confirm receipt* to complete the donation.
8. **Admin:** try removing a listing, handling a report, and verifying an organization.

---

## Tech stack
- Single-file front end: HTML, CSS and vanilla JavaScript (`index.html`)
- No build step and no dependencies
- Data stored in the browser's `localStorage`

## Run locally
```bash
git clone <your-repo-url>
cd <your-repo-folder>
# open index.html in any modern browser
```

---

## Food-safety assumptions
- The platform does not inspect, test or certify food.
- Donors must provide accurate preparation, handling and use-by information and follow applicable local food-safety rules.
- Recipients should inspect food at pickup and decline anything that looks unsafe.
- Cooked meals, dairy and meat are high-risk foods and need clear time and temperature handling.
- Listings expire automatically, and quantities and pickup deadlines are shown clearly to reduce missed collections.

## Operational limitations
- Prototype only: no real backend, authentication or multi-user sync, since data lives in one browser
- No delivery logistics or route planning
- No temperature monitoring or food testing
- Charity verification is a manual admin toggle, not a real document check
- No real email, SMS or push notifications
- Meal estimates are approximate (1 portion or item = 1 meal; 1 kg ≈ 2.5 meals)

## Future scope
Map view, automatic matching by distance and dietary category, pickup reminders, multilingual support (English, Hindi, Telugu), real authentication and a database backend.
