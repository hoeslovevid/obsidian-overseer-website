# Obsidian Overseer — Website

Landing page for the **Obsidian Overseer** Discord bot.

## Setup

1. **Bot invite link**  
   Open `index.html` and find the script at the bottom. Replace `YOUR_BOT_CLIENT_ID` with your bot’s **Application (Client) ID** from the [Discord Developer Portal](https://discord.com/developers/applications) → your application → OAuth2 → Client ID.

   ```js
   const BOT_CLIENT_ID = 'YOUR_BOT_CLIENT_ID';  // e.g. '1234567890123456789'
   ```

2. **Contact the team**  
   To show contact options on the website, set one or both in the script:
   - `DISCORD_SERVER_INVITE` — Your Discord server invite URL (e.g. `https://discord.gg/your-invite`). Shows a “Join our Discord” button for support and feedback.
   - `CONTACT_EMAIL` — A support email (e.g. `support@example.com`). Shows an “Email us” button that opens the user’s mail client.

3. **Contact form (messages to your Discord)**  
   - **GitHub Pages:** In `contact.html`, set `CONTACT_WEBHOOK_URL` to your Discord channel webhook URL (from **Edit Channel** → **Integrations** → **Webhooks** → **New Webhook**). The form will post directly to Discord. The webhook URL will be visible in the repo and in “View Source,” so use a **private** channel and if it’s abused, delete the webhook and create a new one.
   - **Netlify (optional, webhook hidden):** Deploy to [Netlify](https://netlify.com), leave `CONTACT_WEBHOOK_URL` empty in the script, and in Netlify → **Site settings** → **Environment variables** add `CONTACT_WEBHOOK_URL` with your webhook URL. The form will use the serverless function and the webhook stays server-side only.

4. **Developers**  
   The “Developers” section lists **Danger!** by default (from the bot’s config). To add or change developers, edit the `<div class="dev-list" id="dev-list">` section and add more `<span class="dev-badge">Name</span>` elements.

5. **Privacy Policy & Terms of Service**  
   The Privacy Policy and Terms of Service are in the Legal section with tab buttons. Edit the text inside the `#privacy` and `#terms` divs in `index.html` to match your own policies.

## Contents

- **Hero & invite** — Headline and prominent “Add to Discord” button (Discord-style blue).
- **Features** — What the bot does (voice, economy, Warframe, moderation, etc.).
- **Contact the team** — Discord server and/or email links (set `DISCORD_SERVER_INVITE` and `CONTACT_EMAIL` in the script).
- **Contact form** — “Send us a message” form; posts to a Discord channel via the webhook URL you set.
- **Developers** — Listed developers (default: Danger!).
- **Legal** — Tabs for Privacy Policy and Terms of Service.

## Hosting

- **GitHub Pages:** Publish the repo (e.g. from the `main` branch). Set `CONTACT_WEBHOOK_URL` in `contact.html` so the form posts to Discord. No build step. The webhook URL will be visible in the repo; use a private channel and rotate the webhook if needed.
- **Netlify (optional):** Deploy the same repo to Netlify and set `CONTACT_WEBHOOK_URL` in the dashboard (env) instead of in the script so the webhook stays hidden.
