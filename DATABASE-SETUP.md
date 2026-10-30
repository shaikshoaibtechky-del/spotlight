# Connect the Spotlight site to a database (Supabase, free)

1. Go to supabase.com, create an account and a New project. Wait until it finishes starting.
2. SQL Editor -> New query -> paste everything from `supabase-setup.sql` -> Run.
3. Authentication -> Users -> Add user -> "Create new user". Enter YOUR admin email + a strong password. Tick "Auto confirm".
4. Authentication -> Sign In / Providers -> turn OFF "Allow new users to sign up" (so only you can be admin).
5. Project Settings -> API: copy the **Project URL** and the **anon public key**.
6. Open `index.html`, search for `YOUR_SUPABASE_URL`, and paste the two values:
   const SB={url:'https://xxxx.supabase.co',key:'eyJ...'};
   (The anon key is meant to be public. Never paste the "service_role" key.)
7. Upload the whole `site` folder to GoDaddy (public_html). Done.
8. Open the site -> Admin login -> use the email and password from step 3.
   First login: your current packages/prices are saved to the database on your first edit
   (change any price and back, or press Save in any admin tab).

What is shared now: bookings, packages, prices, add-ons, coupons, booking rules, text and links.
Not shared yet: photos/videos uploaded in the admin "Website" tab (still saved only in that browser).
Put those image/video files in the site folder instead, or ask for Supabase Storage to be added.
