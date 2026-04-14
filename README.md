# Our Solar System — Interactive Demo

Simple, beautiful single-page demo that visualizes the Sun and the eight planets with orbit animations and a side panel to show details.

Usage
- Open `index.html` in a browser (double-click or use a local server).

Features
- Animated orbits with CSS
- Click or hover a planet to see details
- Pause/Play motion button
- Keyboard arrow navigation between planets

Development
- No build step required. For local development, you can run a simple static server e.g.:

```powershell
# From the repository root
python -m http.server 8000
# or using Node
npx http-server -c-1
```

Then visit `http://localhost:8000` in your browser.

Why ngrok is needed:

Signup and install ngrok. Jenkins is running locally on my computer, which means GitHub cannot access it directly over the internet. Since GitHub webhooks require a publicly reachable URL to send push event notifications, I use ngrok to expose my local Jenkins server through a temporary public URL.

This allows GitHub to communicate with Jenkins and trigger builds automatically whenever changes are pushed to the repository.

For example, if Jenkins is running on port 8080, ngrok can be started with:

ngrok http 8080

ngrok then provides a public HTTPS URL, which is used in the GitHub webhook payload, for example:

https://your-ngrok-url/github-webhook/

Without ngrok, Jenkins can still run builds manually on the local machine, but automatic GitHub-triggered builds would not work.







Files
- `index.html` — main markup
- `styles.css` — visuals and layout
- `script.js` — planet data + interactivity

License
MIT — feel free to adapt for demos or learning.
