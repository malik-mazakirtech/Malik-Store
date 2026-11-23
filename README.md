# Malik Store — reconstructed demo
Editable HTML, CSS and vanilla JavaScript. No npm dependencies.

## Run on Windows
Open index.html directly, or run `py -m http.server 8092` in this folder and visit http://localhost:8092.
Docker: `docker compose up --build -d`, then visit http://localhost:8092. Container port is 80. `/health` returns ok under nginx.

## GitHub / AutoDeployOps
Create your own empty GitHub repository. Upload the CONTENTS of this folder so index.html and Dockerfile are at repository root. Select the actual branch (normally main) in AutoDeployOps. Use this repository's HTTPS URL. Choose the supplied Dockerfile and container port 80 when configurable.
In YOUR repository Settings > Webhooks, use the exact webhook URL and secret supplied by AutoDeployOps; Content type application/json; event Push. Keep your Cloudflare tunnel and local platform running. Do not guess the endpoint or use this store's port as the platform webhook port.
To test a visible update, change `Demo v1` to `Demo v2` in index.html, commit and push to the configured branch. Check GitHub Recent deliveries, platform pipeline logs, and the deployed site's footer. A successful HTTP delivery alone does not prove deployment succeeded.

## Edit
Pages: index.html, About.html, Products.html, gallery.html, Contact.html, Privacy & Pollicy.html. lec1.html is a compatibility copy of Home.
Shared styling: assets/style.css. Interactions: assets/app.js. Search, dark theme, gallery lightbox, demo order dialog, back-to-top and form validation are implemented.

## Reconstruction notes
Based on supplied code and sampled video frames. Original full-resolution assets were unavailable. Logo recovered from video; product and gallery images are cropped video frames (limited resolution); home background is replacement imagery. Some gallery crops differ from the original framing. Styling follows the teal navbar, large home heading, full-width Shop Now, central form and three-column footer shown in the recording. About page uses supplied source. Unsupported customer-count claims were replaced with qualitative features.
This is a deployment demonstration, not a real checkout. Contact form does not send or store messages. Contact details came from supplied source and must be confirmed before real use. No payment backend or WhatsApp integration is configured. Floating contact opens Contact page. Privacy page describes actual demo behavior.
Docker and real AutoDeployOps webhook execution require your local platform and are not verified here.

Validation: JavaScript syntax and all local HTML links/image files checked. Automated browser execution was blocked by environment socket permissions; browser interactions and Docker runtime remain unverified.
