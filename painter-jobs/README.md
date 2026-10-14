# Job Tracker (painter jobs & pay)

A single-file web app: `index.html`. No install, no server, no account needed.

## What it does
- **Jobs**: name, customer, location (with a Map link), date, status, hours, and notes on what you did.
- **Photos**: add from your camera or gallery. They're resized and stored on the phone, and one tap copies them to your Google Drive.
- **Pay**: set what each job pays, record payments (amount, date, note), see what you're still owed, and tap "Mark paid in full".
- **Summary**: totals, average $/hour, and a month-by-month breakdown. Export to CSV.
- **Backup**: export or import a JSON file of your jobs and pay.

## Using it on your phone
Host the folder (GitHub Pages works: Settings → Pages → deploy from branch, then open `/painter-jobs/`), open the link on your phone, and use "Add to Home Screen". Data stays in that browser on that device, so use the Backup button regularly.

You can also just open `index.html` locally to try it. Google Drive sign-in needs it served over `https://` (or `localhost`).

## Turning on Google Drive photo backup (one-time, ~5 min)
1. Go to <https://console.cloud.google.com/>, create a project (any name).
2. **APIs & Services → Library** → enable **Google Drive API**.
3. **APIs & Services → OAuth consent screen** → External, fill in the app name and your email, and add yourself as a **Test user**.
4. **Credentials → Create credentials → OAuth client ID → Web application**. Under **Authorized JavaScript origins**, add the address where you host the app (e.g. `https://YOURNAME.github.io`).
5. Copy the Client ID into the app's **Settings** tab.
6. Open a job with photos and tap **Save to Google Drive**. Photos land in `Painter Jobs/<date> - <job name>/`.

The app uses the `drive.file` scope, so it can only see files it created, never the rest of your Drive.
