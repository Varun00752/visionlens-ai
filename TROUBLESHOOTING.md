# Troubleshooting

## "Could not download the AI model"
- **Online?** The model is downloaded from the internet. Check your connection and click **Retry loading model**.
- **Use localhost.** Run the page with Live Server or `python -m http.server 8000` rather than only double-clicking the file.
- **Claude's hosted preview blocks outside downloads.** The model cannot load there. This is a restriction of the preview, not a bug in your code. Run it on your laptop.
- **Firewall, college Wi-Fi or VPN** may block `cdn.jsdelivr.net` or `storage.googleapis.com`. Try a mobile hotspot.
- Open the browser console (F12, then Console tab) to see the exact error.

## Webcam does not start
- Click **Allow** when the browser asks for camera permission. If you blocked it, click the lock icon in the address bar and allow the camera, then reload.
- The camera works only on `http://localhost` or `https://`.
- Close other apps using the camera (Zoom, Teams, Meet).
- Try Chrome or Edge.

## Prediction looks wrong
- Use a clear, well-lit photo with one main object.
- MobileNet knows only 1,000 categories, so the top guess may be the closest match.
- A low confidence percentage means the model is unsure.

## Page looks broken
- Make sure you copied the full file, from `<!DOCTYPE html>` to `</html>`, and saved it as `index.html` (not `index.html.txt`).
