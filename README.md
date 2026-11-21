# 🛡️ Snipe Shield

A chat window for streamers in Money SMP (or any SMP) that stops chat from giving away where enemies are, when you're about to be raided, or how close you are to finding someone's base. You still get to read and talk to your chat.

## Getting started

Open the page. A short setup guide asks three things:

1. **Your Twitch channel name.** You can paste the whole `twitch.tv/...` link.
2. **Who else is on the SMP:** other players, their nicknames, bases and landmarks.
3. **How strict it should be:**
   - 🙂 **Chill:** 10s delay. Only hides obvious hints (*behind you*, *raid*, coordinates).
   - 🛡️ **Balanced** (recommended): 20s delay. Also hides directions and hot/cold hints.
   - 🔒 **Max:** 30s delay. Very strict word list, and hides first-time chatters.

At the end it gives you a **mod link** to send to your mods. That's all the setup there is.

Want to look around first? Click **"Try it with fake chat"** in the setup guide.

## What protects you

| | What it does | Work for mods |
|---|---|---|
| ⏱ **Delay** | Every message waits before you see it. | none |
| 🚫 **Auto-filter** | Hides coordinates, links (like links to another player's stream), hint words and SMP player names. It also catches sneaky spellings like `b3h1nd`, `beeehiiind` and `b e h i n d`. Money amounts like `10,000` are fine. | none |
| ↪ **Reply check** | A reply to a spoiler message is hidden too, even if the reply itself looks innocent ("yeah he's right there"). | none |
| 🔇 **Auto-mute** | Anyone who gets 3 strikes (a hidden hint or a message a mod deleted) is hidden for the rest of the stream. | none |
| 🌊 **Surge shield** | When lots of *different* people start dropping hints at once (usually means someone is near you), only mods and VIPs get through for 60 seconds. You get **no warning**, because a warning would itself tip you off. | none |
| 🆕 **First-time chatters** | Option to hide brand-new chatters, who are often alt accounts showing up mid-raid. On in Max. | none |
| 🗑 **Mod deletes** | Anything a mod deletes or times out in normal Twitch chat during the delay never reaches you. | delete as usual |
| 🔒 **Lockdown** (press **L**) | Only mods, VIPs and allowed users get through. | none |

Mods and VIPs skip the delay, so they can still talk to you right away.

## For mods

Open the mod link. You'll see every message with a countdown to when it reaches the streamer:

- **Yellow** = waiting. A red tint means a first-time chatter or someone with strikes, so check those first.
- **Green** = the streamer saw it. **Grey** = hidden automatically. **Red** = deleted by a mod.
- Use the buttons at the top to show only **Waiting** messages when chat is busy.
- **⏱** copies a 10-minute timeout command you can paste into Twitch chat.
- **Open Twitch mod chat** opens Twitch chat in a small window next to this page.

### Chat commands (mods only)

Type these in **normal Twitch chat**. The streamer's page follows them, and the streamer **never sees** these messages, so `!ss name SteveBase` doesn't spoil anything.

| Command | What it does |
|---|---|
| `!ss lock` / `!ss lock 5` | Lockdown (optionally for 5 minutes). It's **silent** on the streamer's screen. |
| `!ss unlock` | End lockdown |
| `!ss mute name` / `!ss unmute name` | Hide or un-hide everything from one person |
| `!ss allow name` | Treat someone like a mod |
| `!ss name Steve` | Hide messages mentioning a player or place |
| `!ss word tunnel` / `!ss unword tunnel` | Add or remove a spoiler word |
| `!ss delay 30` | Change the delay |
| `!ss clear` | Wipe the streamer's screen if something slipped through |

## Settings

Click **⚙️ Settings**. The basics are at the top: channel, strictness level, SMP names and a **"Test a message"** box. Type something in it to see whether it would be hidden. Everything else is under **Advanced settings**.

Shortcuts: **L** = lockdown, **C** = clear your screen, **Esc** = close settings.

## Using it while you stream

- **In OBS:** go to *Docks*, then *Custom Browser Docks*, and paste your **streamer link** (Settings → Copy streamer link). **Don't** add it to your stream as a scene source: it's for your eyes only.
- Close or hide your normal Twitch chat while you play.
- Messages that @mention you are highlighted in purple.

## Hosting (getting a link)

1. On GitHub, go to the repo, then **Settings**, then **Pages**.
2. Set **Source** to *Deploy from a branch*, pick the branch with `index.html`, choose `/ (root)`, and click **Save**.
3. After a minute you'll get a link like `https://moretingz.github.io/more-tingx/`.

GitHub Pages is free for public repos. You can also just download `index.html` and double-click it.

## Tips

- If too much normal chat gets hidden, try **Chill**, or remove words like `left`/`right` under Advanced → Spoiler words.
- The hidden-message counter is off for the streamer by default. A sudden jump would be a hint in itself.
- Mutes and strikes reset when you reload the page. Settings are saved.
