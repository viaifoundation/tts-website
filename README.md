VI AI Foundation TTS Website
This public repository contains the static website for the VI AI Foundation TTS Devotional Audio service, hosted at tts-cdn.viaifoundation.org using GitHub Pages. The service allows users to generate audio for Bible devotionals in English, Simplified Chinese, and Traditional Chinese, supporting up to five voices per paragraph. The backend is hosted at tts.viaifoundation.org on an IONOS VPS using FastAPI with Python 3.14 no-GIL.
Project Structure

index.html: React frontend with Tailwind CSS for user interface (text input, voice selection, audio playback).
assets/: Favicon, logo, and other images.
CNAME: Configures GitHub Pages custom domain (tts-cdn.viaifoundation.org).
README.md: This documentation.

Setup

Clone the Repository:
git clone git@github.com:viaifoundation/tts-website.git
cd tts-website


Add Assets:
mkdir assets
# Copy from viaifoundation-website/assets/ or download
# e.g., curl -o assets/logo.png https://viaifoundation.org/assets/logo.png


Deploy to GitHub Pages:

In GitHub repo settings (https://github.com/viaifoundation/tts-website/settings/pages):
Source: Deploy from a branch.
Branch: main, folder /.


Add CNAME record in Cloudflare DNS: tts-cdn.viaifoundation.org → viaifoundation.github.io.
Commit and push:git add .
git commit -m "Initial TTS website setup"
git push origin main




Test:

Access https://tts-cdn.viaifoundation.org.
Verify API requests to https://tts.viaifoundation.org/api/ work.



Features

Language Support: English, Simplified Chinese (zh-CN), Traditional Chinese (zh-TW).
Voice Selection: Up to 5 voices per paragraph (e.g., zh-CN-XiaoxiaoNeural).
Authentication: JWT login for users.
Bible References: Auto-converts (e.g., "Roman 1:17" → "Roman 1章17节").
Analytics: Google Analytics (ID: G-PRGF9J964B).

Backend

Hosted in viaifoundation/devotion_audio_tts.
Deployed on IONOS VPS with FastCGI, Python 3.14 no-GIL.
SQLite for authentication and activity logging.

Contact

Email: contact@viaifoundation.org
Phone: 707-560-1777
Address: PO Box 3333, Saratoga, CA 95070

License
MIT License