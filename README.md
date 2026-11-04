# Woodpecker for iPhone (no Xcode)

This folder is a complete web app. You host it once at a free web address (GitHub
Pages), then add it to your iPhone's Home Screen. It opens full-screen like a normal
app, works offline, and saves your place automatically.

Total time: about 10 minutes, once. You only need a Mac or PC with a web browser.

---

## Part A — Put the app online with GitHub Pages (on your Mac)

### Step 1. Unzip this folder
Double-click `Woodpecker-iPhone.zip` in Finder. You'll get these 7 files:

```
index.html   sw.js   manifest.webmanifest
icon-192.png   icon-512.png   apple-touch-icon.png   README.md
```

GitHub won't unzip anything for you, so you upload these **individual files**,
not the .zip.

### Step 2. Create a free GitHub account
Go to **github.com** → **Sign up**. Pick a username carefully: it becomes part of
your app's address (`https://USERNAME.github.io/...`). Verify your email.

### Step 3. Create a repository
1. Signed in, click the **+** (top right) → **New repository**.
2. **Repository name:** `woodpecker` (lowercase, no spaces).
3. Set it to **Public**. GitHub Pages is free only for public repositories.
4. Leave "Add a README" **unticked**.
5. Click **Create repository**.

### Step 4. Upload the files
1. On the new, empty repository page, click the link **"uploading an existing file"**.
   (Or: **Add file → Upload files**.)
2. In Finder, select all 7 files from Step 1 and drag them into the browser window.
   They must sit at the **top level**: you should see `index.html` listed, not a
   folder containing it.
3. Scroll down and click **Commit changes**.

### Step 5. Turn on GitHub Pages
1. In the repository, click **Settings** (top tab bar).
2. In the left sidebar, click **Pages**.
3. Under **Build and deployment → Source**, choose **Deploy from a branch**.
4. Under **Branch**, choose `main` and folder `/ (root)`, then click **Save**.
5. Wait 1–2 minutes and refresh the page. A box appears at the top:
   **"Your site is live at https://USERNAME.github.io/woodpecker/"**.

### Step 6. Check it on your Mac
Open that address. You should see the Woodpecker home screen with "+ New set".
If you get a 404 error, wait another minute. Pages can take up to 10 minutes the
first time.

> ⚠️ **Don't upload `puzzles.json`** (your book's positions). A public repository
> can be seen by anyone. You'll load it straight onto the phone in Part B.

---

## Part B — Install on your iPhone

### Step 7. Add to Home Screen
1. On the iPhone, open `https://USERNAME.github.io/woodpecker/` in **Safari** or **Chrome**.
2. **Safari:** tap the **Share** button (on newer iOS it's inside the **•••** menu),
   then **Add to Home Screen** → **Add**.
   **Chrome:** tap the **Share** icon in the address bar → **Add to Home Screen** → **Add**.
3. A woodpecker icon appears on your Home Screen. **Always open the app from this icon.**
   iOS keeps a Home Screen app's data permanently, while a plain browser tab's data
   can be cleared after a few weeks without use.

### Step 8. Load your book
1. Get `bookscan/puzzles.json` onto the phone: AirDrop it from the Mac (choose
   **Save to Files**), or put it in iCloud Drive.
2. Open the Woodpecker app → **Import bookscan output (puzzles.json)** → pick the file.
3. It asks about the puzzles flagged "needs review":
   **OK** = include them, **Cancel** = leave them out.
4. You'll get one set per chapter (Easy / Intermediate / Advanced). Tap one to start.

---

## Picking up where you left off
- Progress is saved after every puzzle and whenever you switch apps or lock the phone.
  The cycle clock pauses while the app is in the background.
- When you reopen, the home screen shows **Jump back in → Continue**.
- **Back up progress** creates a .json file (on iPhone choose **Save to Files**).
  **Restore backup** on another device or browser carries everything across.
  Each device keeps its own copy, so there's no automatic sync.

## Training tip: Solve depth
Many engine-derived lines in the book scan are 6+ moves long. Under
**Appearance → Solve depth** you can set a puzzle to count as solved after your
first 1, 2 or 3 correct moves. Any checkmating move always counts as solved.

---

## Updating the app later
1. On github.com, open your `woodpecker` repository → **Add file → Upload files**.
2. Drag in the changed file(s), e.g. a new `index.html`. Same names overwrite the old ones.
3. **Commit changes**. The site updates in about a minute.
4. On the iPhone, open the app while online, then close it fully (swipe it away) and
   reopen it. Your sets and progress are kept, because they live on the phone, not on GitHub.

Tip: tap **Back up progress** before big updates, just in case.

## Troubleshooting
| Problem | Fix |
|---|---|
| 404 "There isn't a GitHub Pages site here" | Wait a few minutes; check Settings → Pages shows a live address; make sure `index.html` is at the top level of the repo, not inside a folder. |
| Page loads but has no icon / not full-screen | Delete the Home Screen icon and add it again after the site has fully loaded once. |
| Still seeing the old version after an update | Open the app online, close it fully, reopen it. Repeat once if needed. |
| "Analysis" says *Offline — material estimate* | The engine downloads the first time you use it online; after that it's cached. |
| Progress missing | You probably opened the site in a browser tab instead of from the Home Screen icon. Those are separate storage areas. Use **Back up / Restore** to move progress between them. |
