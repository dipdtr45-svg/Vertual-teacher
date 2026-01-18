# Deploying to Netlify

This project is a Vite React app. To deploy on Netlify:

1. Connect this GitHub repository to Netlify from the Netlify dashboard (Sites → New site → Import from Git).
2. Set build command to: `npm run build`
3. Set publish directory to: `dist`
4. Add the environment variable `GEMINI_API_KEY` in Site settings → Build & deploy → Environment → Environment variables.
   - Do NOT commit your API key to the repository. Use Netlify's UI to store secrets.
5. (Optional) If you need a preview before full deploy, run locally:
   - `npm install`
   - `npm run dev` (Vite dev server)

If you need automatic deploys on push, Netlify will do that when the repo is connected. For SPA routing we already added a redirect in `netlify.toml` so all routes will serve `index.html`. 
