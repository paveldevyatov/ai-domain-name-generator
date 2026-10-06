![A pixel bloodhound in a fedora digging up a glowing treasure chest under a rainy noir street](cover.jpeg)

# 🔍 AI Domain Name Generator

A single, self-contained prompt that turns Claude, ChatGPT, or any other capable AI into a domain name generator and domain availability checker in one. Describe your project in a sentence - get the top 50 domains that are actually free to register.

- ⚡ **Checks thousands of variations in minutes** - names × zones, no manual lookups.
- 🎭 **Finds domains in 15 styles** - wordplay, metaphors, domain hacks (bit.ly), playful spellings (Flickr) and more.
- 🌍 **Supports 1,350+ zones!**
- 🏆 **Only free domains, best first** - the top 50, each scored out of 10; taken names never shown.
- 🙅 **Honest** - a zone it couldn't check is marked unchecked, never "available".
- 🔌 **Works anywhere** - paste into any AI, or install as a skill in Claude Code, Codex or Cursor.

Meet **Sherbark Holmes** 🐶🔍, the hound that sniffs out free domains. 🙌

👉 **The prompt lives here: [`PROMPT.md`](PROMPT.md)**

## 🚀 Usage

### 📋 As a prompt - any AI

1. Copy the entire contents of [`PROMPT.md`](PROMPT.md).
2. Paste it into Claude, ChatGPT, or any other capable AI.
3. Tell it about your project - keywords or a couple of sentences. Pick search styles and zones, or skip them and take the defaults.
4. Get the list. Say "show more" for the next 50, or ask for a different direction. ✅

### 🧩 As a skill - coding agents

Using Claude Code, Codex, Cursor or another coding agent? Install it as a skill:

```bash
npx skills add paveldevyatov/ai-domain-name-generator
```

It installs as `find-domain` and starts when you ask for a domain name or whether one is free (or run `/find-domain` in Claude Code).

## ⚙️ How it works

### ✍️ Generate - hundreds of names, not ten

From your description the AI builds hundreds of candidates in the styles you allow: blends (Pinterest), two words (YouTube), get-/try- prefixes, puns (Reddit), made-up words (Hulu), Latin roots (Lumen), metaphors (Slack), playful spellings (Flickr, Fiverr), domain hacks where the zone finishes the word (bit.ly), and your own language spelled in Latin letters (kinopoisk.ru). Default zones: .com .net .org .io .app .ai .co .dev, or any you name.

It steers away from weak names before checking: the radio test, digits, awkward word splits, too long, bad meanings in major languages, too close to a famous brand.

### ✅ Check - at the registry, not a guess

How much it can check depends on what your AI can do:

- 🖥️ **Coding agent with a terminal** - DNS first to drop the obviously taken names, then each zone's own registry: RDAP (the modern WHOIS) or classic whois, with a control query on a known-taken name so a broken server can't fake "free". If you have a registrar tool connected, finalists go through it too.
- 🌐 **Chat AI with web browsing** - asks the registries' RDAP servers directly. Zones that only have classic whois (like .co) can't be checked this way, and it says so.
- 💬 **No internet** - it still generates and ranks, says plainly that nothing was checked, and gives you links to check yourself.

It can check availability in 1,350+ of the 1,437 zones (about 1,200 when the AI only has web browsing); for the rest it tells you honestly. The prompt carries its own table of registry endpoints and "not found" markers for the popular and domain-hack zones, tested in October 2026.

### 🏆 Rank - the flawless name first

Only verified-free domains make the list, sorted by readability, memorability, radio test, length and fit to your project, each with a score out of 10 and the top pick marked. One line says exactly how many domains it checked, how many were taken, free, or impossible to check.

## ⚠️ Honest limits

- **"Free" in the registry isn't always registrable.** Reserved names only show up at a registrar. Confirm there before you buy.
- **Some zones can't be checked by machine.** They're reported as unchecked, never guessed.
- **Trademarks are on you.** The AI avoids famous brands, but a real trademark search is manual (TMview, USPTO). This is not legal advice.
- Availability changes by the minute; a name free today can be gone tomorrow.

## 📄 License

[MIT](LICENSE)
