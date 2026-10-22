# Putting Gamer Translator on gamertranslator.com

## 1. Put the site files in the repo

If Claude is linked to GitHub, Claude pushes these for you. Otherwise, upload them yourself:

1. Open https://github.com/321zena-rgb/gamer-translator
2. Tap **Add file → Upload files**.
3. Add `index.html`, `README.md`, `CNAME` and `.nojekyll`. The `.nojekyll` file is optional.
4. Tap **Commit changes**.

## 2. Turn on GitHub Pages

1. In the repo, go to **Settings → Pages**.
2. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
3. Set **Branch** to **main** and the folder to **/ (root)**, then tap **Save**.
4. Under **Custom domain**, type `gamertranslator.com` and tap **Save**.

## 3. Point the domain at GitHub (GoDaddy)

1. Sign in at godaddy.com and go to **My Products → gamertranslator.com → DNS** (or **Manage DNS**).
2. **Delete** the existing **A** record named `@` that points to "Parked" or a GoDaddy address. If **Forwarding** is turned on for the domain, turn it off.
3. **Add** four **A** records, each with Name `@`:
   - `185.199.108.153`
   - `185.199.109.153`
   - `185.199.110.153`
   - `185.199.111.153`
4. Find the **CNAME** record named `www`, or add one, and set its value to `321zena-rgb.github.io`.
5. Save.

## 4. Wait, then turn on the padlock

DNS changes take anywhere from a few minutes to a few hours. When GitHub's Pages settings show a green "DNS check successful", tick **Enforce HTTPS**. The certificate can take up to an hour to show up.

## 5. Try it on your phone

- Open https://gamertranslator.com
- Tap **Record**, allow the microphone, and talk. The words should appear and get translated.
- Tap **Upload** and pick a short voice memo. The first time, it downloads a listening engine of about 40 MB, so use Wi-Fi.
