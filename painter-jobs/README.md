# Job Tracker (painter jobs, time & pay)

One file: `index.html`. Hosted for free with GitHub Pages, data stored in **your own Google account**.

## How it works day to day
1. **Clock In**: one tap. At a brand-new place it guesses the street address and shows it in a box so you can fix it before anything is saved. After that the address is yours: every later clock-in or clock-out at that job reuses it and never guesses again, even if you're parked a bit away. Your recent job sites also show up as one-tap buttons, and pay is pre-filled from last time.
2. **Clock Out**: one tap. You land on the job page. Add what you did, the pay and photos if you want.
3. **Jobs tab**: every job by date. Search by address or notes, or pick a date. Open any job to see earlier jobs at the same address.
4. **Pay tab**: what you're owed, what you've been paid, hours, average $/hour and a month-by-month total. "Mark paid in full" is one tap.

## Put it online (same way as Letters)
1. In your GitHub repo choose **Add file → Upload files**, upload the `painter-jobs` folder's `index.html`, and commit.
2. Repo **Settings → Pages**: deploy from the main branch (you probably already did this for Letters).
3. Open `https://YOURNAME.github.io/REPO/painter-jobs/` on your phone and use **Add to Home Screen**.

## Turn on Google sync (one time, ~5 min)
Creates a Google Sheet called "Painter Job Tracker" and a Drive folder "Painter Jobs/<address>" for photos. Sign in with the same Google account on any phone and everything shows up.

1. <https://console.cloud.google.com/> → create a project.
2. **APIs & Services → Library**: enable **Google Drive API** and **Google Sheets API**.
3. **OAuth consent screen**: External, add your app name and email, add yourself as a **Test user**.
4. **Credentials → Create credentials → OAuth client ID → Web application**. Under **Authorized JavaScript origins** add `https://YOURNAME.github.io`.
5. Paste the Client ID into the app's **Settings** tab and tap **Save & sync**.

The app only has the `drive.file` permission, so it can only see files it created itself.

## Good to know
- It works offline and saves on the phone first. Tap **Sync** (top right) when you have signal. It also syncs by itself a few seconds after changes while you're signed in.
- The Google Sheet is readable by you. Open it any time, or share it with someone.
- Location needs permission the first time. If it can't find you, pick or type the address instead.
- Address lookup uses OpenStreetMap's free service, so addresses are usually right but you can edit them on the job page.
