# HOWMANYTIMEYOUUNLOCKYOURPHONE
Why

Everyone knows they use their phone "too much". Nobody knows what that means.

A number like 80 pickups a day is abstract. The same number expressed as effort, weight lifted and distance traveled over a year, or a lifetime, is not. This app makes the habit visible without lecturing anyone.

Built as Day 4 of the Trosku 30-day challenge: one app per day, built with Claude Code, filmed for Reels.

How it works
Find your number. The app walks you through your phone's settings to find your real pickup count (iPhone Screen Time or Android Digital Wellbeing).
Come back. The app notices you left to look it up and greets you when you return.
Enter it. One number, nothing else. No account, no tracking.
The reveal. Your number translated into a day, a year and a lifetime, shown as physical effort, weight and distance, ending with a verdict.
Challenge a friend. Send a link, they enter their number, you both see a side-by-side comparison.
Features
Guided navigation for iPhone (menu names in English, exactly as shown on the device) and Android (search-based path, since menu names differ between manufacturers)
Live exit detection: the Page Visibility API detects when you switch to Settings and reacts when you return
Dot-grid visualization where every dot is one pickup
Real-world conversions: effort, weight lifted and distance traveled, scaled to day, year and lifetime
Verdict screen with a short, dry summary of your habit
Friend duel through URL parameters, fully serverless
Instagram Story export: a 9:16 image of your result, ready to share
Privacy by design: no backend, no analytics, your number never leaves the browser (except in the duel link you choose to send)
<!-- TODO: dodaj countdown do sledećeg otključavanja ako je ušao u finalnu verziju -->
Tech highlights
Problem	Solution
Knowing the user went to Settings	visibilitychange event with a timestamp, so the return feels intentional
Multiplayer without a server	Challenger's number is encoded in the share URL, the comparison is computed on the client
Shareable result image	Canvas API renders a 1080×1920 story image in the browser
Different phones, different menus	iOS gets exact English menu paths, Android gets search keywords that work across Samsung, Xiaomi and stock Android
Serbian audience on iPhone	iOS has no Serbian system language, so UI copy is Serbian while menu names stay in English
<!-- TODO: potvrdi stack (jedan HTML fajl? framework?) i uskladi -->
Data sources

Only statistics with a clear source were used. If a number couldn't be verified, it was left out.

Stat	Source
58 pickups per day (device-measured)	RescueTime, 2019
186 pickups per day (self-reported)	Reviews.org, 2026
6.13 million internet users in Serbia	DataReportal, 2026
Run locally
bash
git clone https://github.com/stefanpesovic/koliko-puta-dnevno.git
cd koliko-puta-dnevno
open index.html

To test the duel, open the share link from the result screen in a second browser tab.

Author

Stefan Pešović · Full-stack & AI developer GitHub · Trosku on Instagram
