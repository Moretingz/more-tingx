# 🛡️ Snipe Shield

A chat window for streamers in Money SMP (or any SMP) that stops chat from giving away where enemies are, when you're about to be raided, or how close you are to finding someone's base. You still get to read and talk to your chat.

## How it protects you

| Protection | What it does |
|---|---|
| **Delay** | Every message waits a few seconds (20 by default) before you see it. |
| **Mods delete, you never see it** | If a mod deletes a message, times someone out or bans them in normal Twitch chat during that wait, it never shows up for you. Mods don't need any new tools or logins. |
| **Auto-filter** | Hides messages with coordinates (`1200, -340`), links (like links to another player's stream), and hint words (*behind, raid, warmer, base, tunnel, 👀…*). It also catches sneaky spellings like `b3h1nd`, `beeehiiind` and `b e h i n d`. Money amounts like `10,000` are **not** treated as coordinates. |
| **Player names** | Add the names of other SMP members and their bases, and any message mentioning them is hidden. |
| **Lockdown** (press **L**) | During a fight or a tense moment, only mods, VIPs and people you allow get through. Press L again to turn it off. |
| **Mod view** | Your mods open the same page and see every message with a countdown showing when it will reach you, so they know what to delete. |

Mods, VIPs and your "always-allowed" list skip the delay by default, so mods can still talk to you right away.

## Try it right now (no setup)

1. Download `index.html` from this repo (click it, then the download button).
2. Double-click it to open it in your browser.
3. In Settings, type **demo** as the channel and press **Connect**.
4. Click **Mod view** to watch spoilers get held, hidden and deleted.

To use it for real, type your Twitch channel name instead of `demo`. It reads chat without logging in.

## Get a link you can share with mods (free hosting)

1. On GitHub, go to this repo, then **Settings**, then **Pages**.
2. Under "Build and deployment", set **Source** to *Deploy from a branch*. Pick the branch that has `index.html`, choose `/ (root)`, and press **Save**.
3. After a minute, GitHub shows your link, something like `https://moretingz.github.io/more-tingx/`.

GitHub Pages is free for public repos. If this repo is private, make it public first or use the download method above.

## Everyday use

1. Open your link, go to **⚙️ Settings**, enter your channel, and press **Connect**.
2. Add the other SMP players' names under **Other players & place names**.
3. Press **Copy mod link** and send it to your mods. It includes your delay and word lists so their countdowns match yours.
4. **In OBS:** go to *Docks*, then *Custom Browser Docks*, and paste your **streamer link**. The protected chat now sits right in OBS. **Don't** add it to your stream as a scene source: it's for your eyes only, and your normal Twitch chat stays as it is for viewers.
5. Close or hide your normal Twitch chat while you play so you only read the protected one.

## Tips

- **Delay:** 15–30 seconds is a good range. Longer gives mods more time but makes talking with chat feel slower.
- **The word list is strict on purpose.** If it hides too much normal chat, open Settings and delete words like `left`, `right` or `hot`.
- The hidden-message counter is **off** by default. A sudden jump in hidden messages is itself a hint that someone is close.
- Settings are saved in your browser automatically.
- Tell your mods: *"If chat gives away where someone is, delete it or time them out right away. The streamer won't see it."*
