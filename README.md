# DLInGeek Discord Bot (Beta)

A Discord bot for managing movie/show requests and monitoring torrent downloads via Deluge.  
Currently in **beta** — expect ongoing improvements!

---

## Features

- Request movies or shows by name with `/requests`  
- Validates requests against the OMDb API (requires API key)  
- Shows current torrent download status from Deluge Web UI via `/status`  
- Simple slash commands for easy interaction  

---

## Prerequisites

- **Node.js v18 or newer installed** (https://nodejs.org/)  
- A Discord bot token with proper permissions  
- Deluge Web UI URL and password for torrent status  
- OMDb API key for validating movie/show requests (free tier available)  

---

## Setup Instructions

### 1. Clone this repository

```bash
git clone https://github.com/yourusername/dlingeek-discord-bot.git
cd dlingeek-discord-bot
# Install dependencies
npm install
# Create and configure your .env file
Create a .env file in the root directory and edit it with your own values
DISCORD_TOKEN=your_discord_bot_token_here
DELUGE_URL=https://deluge.yourdomain.com    # Replace with your actual Deluge Web UI URL
DELUGE_PASSWORD=your_deluge_password_here
OMDB_API_KEY=your_omdb_api_key_here          # Replace with your OMDb API key
IMPORTANT:

You must set the DELUGE_URL and DELUGE_PASSWORD correctly or the /status command will fail.

The /requests command requires a valid OMDB_API_KEY to validate movie/show titles.

Without correct .env values, commands may not work or return errors.

Register slash commands
node deploy-commands.js
Start the bot
node index.js
Usage
/requests <title> — Requests a movie/show after validating it on OMDb.

/status — Shows active torrent downloads from your Deluge instance.

Troubleshooting Tips
Ensure Node.js v18+ is installed.

Double-check .env values are correct and saved.

If commands don't show up, run deploy-commands.js again.

Check your API keys and Deluge URL accessibility.

Notes
This bot is in beta, so expect some bugs and improvements over time.
---

## Future Plans

I’m currently using the OMDb API for validating movie/show requests, but **I’m planning to switch to TMDb (The Movie Database) API** in a future update.  
TMDb offers more detailed data and better support for TV shows and movies. Stay tuned for improvements!
