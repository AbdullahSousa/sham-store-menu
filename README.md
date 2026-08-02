# Sham Store — Menu

A single-page, bilingual (English / عربي) store menu with WhatsApp checkout.
The catalog and admin panel are powered by a Supabase database + storage; the page
itself is a static `index.html` hosted free on Netlify.

- **Admin:** long-press the logo → sign in with your Supabase user.
- **Config:** the top of `index.html` — `SUPABASE_URL`, `SUPABASE_ANON_KEY`, `WHATSAPP_NUMBER`.

The `anon` key in `index.html` is **public by design** — Row Level Security in Supabase
lets anonymous visitors only *read*; all writes require the admin login. Never commit
the Supabase database password or the `service_role` key.

## Deploy
Connected to Netlify — every push to `main` auto-publishes.
