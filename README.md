# Obsidian Overseer — Website

Landing page for the **Obsidian Overseer** Discord bot.

## Setup

1. **Bot invite link**  
   Open `index.html` and find the script at the bottom. Replace `YOUR_BOT_CLIENT_ID` with your bot’s **Application (Client) ID** from the [Discord Developer Portal](https://discord.com/developers/applications) → your application → OAuth2 → Client ID.

   ```js
   const BOT_CLIENT_ID = 'YOUR_BOT_CLIENT_ID';  // e.g. '1234567890123456789'
   ```

2. **Developers**  
   The “Developers” section lists **Danger!** by default (from the bot’s config). To add or change developers, edit the `<div class="dev-list" id="dev-list">` section and add more `<span class="dev-badge">Name</span>` elements.

3. **Privacy Policy & Terms of Service**  
   The Privacy Policy and Terms of Service are in the Legal section with tab buttons. Edit the text inside the `#privacy` and `#terms` divs in `index.html` to match your own policies.

## Contents

- **Description** — What the bot does (voice, economy, Warframe, moderation, etc.).
- **Invite** — Button that links to the Discord OAuth2 invite URL (after you set `BOT_CLIENT_ID`).
- **Developers** — Listed developers (default: Danger!).
- **Legal** — Tabs for Privacy Policy and Terms of Service.

## Hosting

You can host the site anywhere that serves static files (e.g. Netlify, GitHub Pages, or any web server). Upload `index.html` (and optionally this README). No build step required.
