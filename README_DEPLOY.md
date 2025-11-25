# Deployment Instructions (Vercel + Supabase)

## 1) Create GitHub repo
- Push this folder to a new GitHub repository.

## 2) Create Supabase project
- Go to https://app.supabase.com and create project (free tier).
- From Project Settings > API copy: `PROJECT_URL` and `anon key`.
- In Supabase Auth > Settings > Redirect URLs add:
  - `https://your-app.vercel.app/api/auth/callback`
  - `http://localhost:3000/api/auth/callback`

## 3) Vercel setup
- Go to https://vercel.com → New Project → Import from GitHub.
- Add Environment Variables in Vercel project settings (both Production & Preview):
  - NEXT_PUBLIC_SUPABASE_URL = your PROJECT_URL
  - NEXT_PUBLIC_SUPABASE_ANON_KEY = your ANON_KEY
  - OPENAI_API_KEY = (optional) your OpenAI key
  - NEXT_PUBLIC_APP_URL = https://your-app.vercel.app

## 4) Deploy
- Deploy and visit https://your-app.vercel.app/demo.

## Notes
- Supabase magic links require a working email provider (free tier uses Supabase built-in).
- For storing generated images, use Supabase Storage (create a bucket and upload URLs).
