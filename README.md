# PNK Jewellers & Workshop — website

One-page site for PNK Jewellers, Palayamkottai, Tirunelveli. Free hosting on GitHub Pages at **https://pnkjewellers.github.io**.

## Files
- `index.html` — the whole website (design, English/Tamil text, animations, forms).
- `Code.gs` — optional Google Apps Script that saves every appointment request to a Google Sheet.

## Put the site online (free, about 5 minutes)
1. **Create the GitHub home for the shop**
   - Signed in as your own GitHub account, open https://github.com/organizations/plan and choose **Free**.
   - Organisation name: `pnkjewellers` (if taken, try `pnk-jewellers`; your site address follows this name).
2. **Create the repository**
   - In the new organisation: **New repository** → name it exactly `pnkjewellers.github.io` → Public → **Create**.
3. **Upload the site**
   - Click **Add file → Upload files**, drag in `index.html` (and this `README.md`), then **Commit changes**.
4. **Turn on GitHub Pages**
   - Repository **Settings → Pages** → Source: **Deploy from a branch** → Branch: `main`, folder `/ (root)` → **Save**.
   - Wait 1–2 minutes, then open **https://pnkjewellers.github.io**.

## Save appointment requests in Google Sheets (optional add-on, free)
1. Create a new Google Sheet named "PNK Appointments" (use the shop's Google account).
2. **Extensions → Apps Script**, delete the sample code, paste all of `Code.gs`, **Save**.
3. **Deploy → New deployment** → gear icon → **Web app**.
   - Execute as: **Me** · Who has access: **Anyone** → **Deploy** → allow the permissions.
4. Copy the **Web app URL**.
5. In `index.html`, find `var SHEET_URL = '';` and paste the URL between the quotes. Commit the change on GitHub.
6. Test: submit a request on the site — a new row appears in the "Appointments" tab.

How the form works: the visitor fills it in → checks a summary → taps **Send on WhatsApp**, which opens WhatsApp to +91 94431 15007 with the details ready to send. If `SHEET_URL` is set, a copy is also saved to the Sheet.

## After launch
- **Google Business Profile** → Edit profile → Website → `https://pnkjewellers.github.io`.
- **Google Search Console** (https://search.google.com/search-console) → add the site as a URL-prefix property, verify with the HTML-tag method (paste the tag inside `<head>` of `index.html`).
- Test on a few real phones: menu, EN/தமிழ், WhatsApp button, star rating, booking form.

## Making changes later
Open `index.html` on GitHub → pencil icon → edit → **Commit changes**. The live site updates in about a minute.
Text for both languages is near the bottom of the file (`var EN = {...}` and `var TA = {...}`).
