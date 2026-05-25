# dealflows-keepalive

  External cron pinger for **dealflows.net** (Houston Roof Claims prod).

  Hits `/api/health` every 5 minutes 24/7 via GitHub Actions so the Replit Reserved VM never goes fully cold — guaranteeing the auto-caller is alive and ready at 9:00 AM CT every business morning.

  ## Why a separate public repo

  - Public repos get **unlimited** GitHub Actions minutes (private repos cap at 2000/mo)
  - A 5-min cron = ~8,640 runs/month — well over the private free tier
  - Zero secrets in this repo — only curls a public health endpoint

  ## Related

  The main app has a complementary **Morning-Open Sentinel** that detects and SMS-alerts David within 5 min if zero outbound calls fire after 9:00 AM CT — that's the alarm. This repo is the **prevention**.
  