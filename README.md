# GenMedia AI — Vercel + Supabase Ready

This repository is pre-wired to deploy to **Vercel** with **Supabase Auth & Storage**.

## Steps to deploy
1. Create a GitHub repo and push these files.
2. Create a Supabase project and copy the `PROJECT_URL` and `ANON_KEY` into Vercel env.
3. In Vercel, import the GitHub repo and deploy. Add environment variables (see `.env.example`).
4. In Supabase → Authentication → Settings → Redirect URLs add:
   - `https://your-app.vercel.app/api/auth/callback`
   - `http://localhost:3000/api/auth/callback`
5. Set up Stripe keys in Vercel if you want billing.
