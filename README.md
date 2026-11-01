# Rishan Das – Portfolio (single HTML file)

A glass-style, interactive portfolio website that lives in **one file: `index.html`**.
No server, no database and no build step. Put the file on any web host (or open it in a browser) and it works.

- **Size:** about 108 KB
- **Only outside files it loads:** Google Fonts (needs internet to show the nicest fonts)
- **Works on:** phones, tablets and computers

---

## What is on the page

| Section | What it shows |
|---|---|
| Home | Your name, roles, short intro, availability badge, buttons, code card, tech row |
| About | Who you are, how you work, stats, and a **working terminal** visitors can type into |
| Skills | Skill bars and a **3D cube** you can drag |
| Services | What you offer |
| Experience | Timeline |
| Projects | Cards with a filter (All / web / app) |
| Media | Picture gallery and an optional YouTube video |
| Blog | Short posts |
| Reviews | What clients say |
| FAQ | Questions and answers |
| Contact | Live local time, email, phone, WhatsApp, booking link, "what happens next", message form |

**Extras:** dark/light mode (◐), an **Effects** on/off button (⚡), a chatbot (💬) that answers from your own content and
can take a message, a startup screen, and a built-in **admin panel** (⚙) for editing everything.

---

## How to run it

### Easiest: open it
Double-click `index.html`. It opens in your browser. (Most things work this way, but a web server is better.)

### On your computer with XAMPP
1. Open the XAMPP Control Panel and press **Start** next to **Apache**.
2. Make the folder `C:\xampp\htdocs\portfolio\` and put `index.html` inside it.
3. Open **http://localhost/portfolio/** in your browser.

### See it on your phone
Your phone must be on the same Wi-Fi as the computer.
1. On the computer, open Command Prompt and type `ipconfig`. Find the line **IPv4 Address** (for example `192.168.1.5`).
2. On your phone, open `http://192.168.1.5/portfolio/` (use your own number).
3. If it does not open, allow **Apache** through Windows Firewall when Windows asks.

### Put it on the internet (free options)
| Host | How |
|---|---|
| Netlify Drop | Go to app.netlify.com/drop and drag `index.html` onto the page |
| GitHub Pages | Put `index.html` in a repository, then turn on Pages in the repository settings |
| Any web host | Upload `index.html` to the `public_html` folder |

Optional file: **`cv.pdf`**. The "Download CV" button looks for a file with this name in the same folder as `index.html`.
Save your CV with that name next to the page, or change the name or remove the button in the admin panel (**profile** tab).

---

## Editing your content (the admin panel)

1. Click **⚙ Admin** at the bottom right (on phones it is a round ⚙ icon). You can also add `#admin` to the end of the page address.
2. Enter the admin password. The starting password is **`admin123`**. Change it with the **Password** button inside the panel.
3. It asks for an optional name (used in the "devs on the panel" list in stats). You can skip it.
4. Pick a tab on the left and edit. Tabs: **stats, profile, about, skills, tech, services, exp, projects, media, blog, reviews, faq, contact, chatbot, database, theme**.
5. Press **Save** to preview your changes in your own browser.
6. Press **Download site**. This gives you a new `index.html` with your edits inside. **Upload it to your host to replace the old one.** Only then do visitors see the changes.

**Pictures:** while logged in, hover over any picture and press **Change**. The picture is stored inside the file when you press Download site.

**Colours:** the **theme** tab has three colour pickers. Everything on the page follows them.

> **Important:** edits are saved only in *your* browser until you download the file and upload it. The password is a simple lock,
> not real security: anyone can read the page's code. Do not treat it as protection for anything private.

---

## Things you should change (they are samples or placeholders)

| What | Where |
|---|---|
| Project names, descriptions, tags, links | **projects** tab |
| Reviews ("Client name") | **reviews** tab |
| Skill percentages, stats (25 projects, 3 years, 15 clients) | **skills** and **about** tabs |
| Experience (employer and college names) | **exp** tab |
| Blog posts | **blog** tab |
| GitHub, LinkedIn, Instagram links | **contact** tab, under socials |
| Booking link (`https://cal.com/` is a placeholder; empty it to hide the row) | **contact** tab |
| Admin password | **Password** button in the panel |

Your email, phone number, WhatsApp and location are already filled in on the **contact** tab.

---

## Making the contact form and chat messages reach your email

By default the form opens the visitor's own email app. For messages to arrive directly in your inbox, use **one** of these free services.

**Option A: Web3Forms (simplest, no account)**
1. Go to web3forms.com, enter your email, and they send you an **access key**.
2. In the admin panel open the **contact** tab and paste it into **Web3Forms access key**.

**Option B: Formspree**
1. Sign up at formspree.io and create a form. Copy the link, which looks like `https://formspree.io/f/xxxxxxx`.
2. In the admin panel open the **contact** tab and paste it into **Formspree link**.

Then press **Save**, **Download site**, and upload the new `index.html`. The chatbot's "leave a message" flow uses the same settings.
The key is visible in the page code. That is normal for these services and it can only send messages to you.

---

## Counting visitors (optional)

A single file cannot store numbers by itself, so visitor counting uses a free **Supabase** database.

1. Make a free project at supabase.com.
2. Open `supabase-setup.sql` (provided with this page). Replace the word `CHANGE-ME` with your own secret password, paste the whole file into Supabase's **SQL Editor**, and press **Run**.
3. In Supabase open **Project Settings, then API**. Copy the **Project URL** and the **anon public key**.
4. In the admin panel open the **database** tab and paste both. Press **Save**, **Download site**, and upload.
5. Open the **stats** tab. It asks for your secret password, then shows visits, unique visitors, devices, sources, most-viewed sections, messages and the people who logged into the panel.

Without Supabase, the **stats** tab only shows visits from your own device.
Visitors can only add counts. They cannot read the numbers.

---

## Chatbot

The 💬 button opens an assistant that answers from your own content: projects, skills, services, experience, availability, contact details and FAQ.
It also collects a message (name, email, text) and sends it the same way the contact form does.
It is **not an AI**: it matches keywords, so it never invents answers.

To add your own answers, open the **chatbot** tab. Add items with keywords (separated by commas) and the reply.
You can also change the greeting and the "I don't know" message there.

---

## Terminal

In the **About** section visitors can type: `help`, `whoami`, `skills`, `projects`, `services`, `contact`, `theme`, `effects` and `clear`.
The up and down arrow keys bring back earlier commands.

---

## Effects and speed

The background has stars, a galaxy, northern lights, falling code, floating code snippets, a grid, 3D shapes and glowing dots.
Effects are **on by default**. Visitors can turn them off with the ⚡ **Effects** button (top right on phones, in the side menu on computers).
Their choice is remembered on their device. If a device is slow, the page shows a one-time hint pointing to this button.

---

## For developers: how the file is built

`index.html` has three parts:

1. `<style>`: all the CSS.
2. `<script id="siteData" type="application/json">`: **all your content** as JSON. The admin panel edits this.
3. Two `<script>` blocks: the page builder (draws every section from the JSON, plus the admin panel) and the interactive effects.

You can edit the JSON directly in a text editor. The top-level keys are:
`profile, about, skills, tech, services, exp, projects, media, blog, reviews, faq, contact, chatbot, database, theme`.
Keep it valid JSON (quotes and commas).

Things the page stores in your browser: your theme and effects choice, your unsaved admin edits, and a random visitor ID
(used only for counting unique visitors when Supabase is set up). No names or IP addresses are stored.
Depending on where your visitors live, you may want a short privacy note on the site.

**Browsers:** current versions of Chrome, Edge, Safari (16.4 or newer) and Firefox (128 or newer).

---

## Troubleshooting

| Problem | What to do |
|---|---|
| Page shows "Not Found" in XAMPP | Check the file is `C:\xampp\htdocs\portfolio\index.html` and the address is `http://localhost/portfolio/` |
| I see a list of files, not my site | The file is not named exactly `index.html` (Windows may hide `.txt` on the end) |
| The ⚙ Admin button does nothing | Reload with Ctrl+F5. Make sure you are using the newest `index.html` |
| My edits disappeared | Edits are saved per browser until you download the file. Press **Download site** and upload it. If you uploaded a different version of the file, older unsaved edits are ignored |
| Hindi, Odia or Japanese text looks like boxes | You are offline. The fonts load from Google Fonts |
| Page feels slow | Press the ⚡ **Effects** button to turn the background effects off |
| Messages don't reach my email | Add a Web3Forms key or Formspree link (see above) and upload the new file |
| Stats ask for a password and fail | Use the secret you put in `supabase-setup.sql`. Check the URL and key in the **database** tab |
| Download CV does nothing | Put a file named `cv.pdf` in the same folder as `index.html` |

---

## Optional: a separate CSS file

`index.html` keeps its styling inside the file, so it stays a single file. If you prefer the styling in its own file, use the pair
**`index-linked.html`** and **`style.css`**:

1. Put both files in the same folder.
2. Rename `index-linked.html` to `index.html` (or open it as it is).
3. To change the look, edit `style.css`. The first block at the top (`:root`) holds the colours.

Keep both files together when you upload them. The look is the same as the single file. The admin panel's **Download site** button
saves the page without the CSS, so upload your `style.css` again only if you changed it.

---

## Need real logins and edits that go live for everyone?

Use the full-stack version (`fullstack-portfolio.zip`: PHP and MySQL). It has real admin accounts, saves edits
for every visitor instantly, stores messages in a database and has its own setup page. See its `START-HERE.md`.

## Credits

Fonts from Google Fonts: Bricolage Grotesque, Noto Sans Devanagari, Noto Sans JP, N
