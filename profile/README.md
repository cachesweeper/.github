<p align="center">
  <a href="https://cachesweeper.com"><img src="https://cachesweeper.com/assets/og-image.jpg" width="100%" alt="CacheSweeper. Cache cleared. Sanity restored."></a>
</p>

<p align="center">
  <a href="https://chromewebstore.google.com/detail/cachesweeper/pbonkgfajlgnahmegmiegdmogmpnilif"><b>Add to Chrome for free</b></a> ·
  <a href="https://cachesweeper.com">Website</a> ·
  <a href="https://cachesweeper.com/guides/clear-cache-one-site-chrome">Guide</a> ·
  <a href="https://cachesweeper.com/support">Support</a> ·
  <a href="https://cachesweeper.com/privacy">Privacy</a> ·
  <a href="https://cachesweeper.com/terms">Terms</a>
</p>

**CacheSweeper is a Chrome extension that clears the cache, cookies and site storage for the site you're on, then reloads the tab.** One click on the toolbar icon, or <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>X</kbd> (<kbd>Cmd</kbd>+<kbd>Shift</kbd>+<kbd>X</kbd> on Mac). Every other site stays exactly as it was, logins included. Built for everyone, tuned for developers.

## Why it exists

You shipped a fix, but the page still shows yesterday's version. Or a site is acting up and the advice is always the same: "clear your cache". Chrome's way is to open Settings, dig into Privacy and security, open the browsing-data dialog, pick a time range, tick the boxes, confirm, go back to your tab and reload.

And because that dialog works on every site at once, you've just been signed out of your email, your dashboards and every other tab you had open.

CacheSweeper does the job for the one site you're on, in one step, and shows you what it removed.

## How it works

1. [Install CacheSweeper from the Chrome Web Store](https://chromewebstore.google.com/detail/cachesweeper/pbonkgfajlgnahmegmiegdmogmpnilif). It's free.
2. Open the site that's misbehaving.
3. Press <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>X</kbd>, or click the CacheSweeper icon in your toolbar.
4. CacheSweeper clears that site's data, reloads the tab and shows a small summary card on the page: which types it removed, how many cookies, and how much space it freed.

Three ways to clear:

- **Keyboard:** <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>X</kbd> (<kbd>Cmd</kbd>+<kbd>Shift</kbd>+<kbd>X</kbd> on Mac). Change it at `chrome://extensions/shortcuts`.
- **Toolbar icon:** one click.
- **Right-click the toolbar icon:** Clear Cache Now, switch profile, open settings.

Everything else lives on the settings page: right-click the toolbar icon and choose Settings.

## When you'd reach for it

- You deployed, but the browser keeps serving the old CSS or JavaScript bundle.
- A login is stuck in a loop and you want fresh cookies for one site, not a sign-out everywhere.
- You're testing a first-run or onboarding flow again and again, and localStorage keeps remembering the last run.
- A service worker keeps handing back an old build (Premium unregisters it and reloads without the cache).
- A form wizard or checkout keeps restoring half-finished state from sessionStorage (Premium).
- A shopping cart, image or page layout looks broken and a fresh start usually fixes it.
- You like a tidy browser, on a schedule you choose (Premium).

## What it clears

By default a clear touches **only the site you're on** (per-origin scope). Switch per-origin scope off and CacheSweeper clears every site at once. Each type has its own switch, per profile.

| Data | What it is | Free | Premium |
|---|---|:---:|:---:|
| HTTP cache | The browser's network cache: old CSS, JavaScript and images | ✓ | ✓ |
| Cookies | Session and persistent cookies | ✓ | ✓ |
| localStorage | Persistent key/value storage for the site | ✓ | ✓ |
| IndexedDB | The site's client-side database | ✓ | ✓ |
| CacheStorage | The service worker's fetch cache | ✓ | ✓ |
| File systems (OPFS) | The origin private file system (off by default) | ✓ | ✓ |
| sessionStorage | Tab-level state: multi-step forms, checkout progress, one-time tokens |  | ✓ |
| Service workers | The service worker registration itself, not just its cache |  | ✓ |
| Browsing history | Opt-in, off by default | ✓ | ✓ |
| Download history | Opt-in, off by default (the list, not the files) | ✓ | ✓ |
| Autofill form data | Opt-in, off by default | ✓ | ✓ |

**Passwords are never touched.** Chrome no longer lets extensions clear them, and CacheSweeper doesn't ask to.

## Free, for good

- **Five storage types on by default:** HTTP cache, cookies, localStorage, IndexedDB and CacheStorage, plus a sixth you can switch on: the origin private file system (OPFS). Each has its own switch.
- **Per-origin scope, on by default:** clear the current site and leave every other site alone.
- **Auto-reload:** the tab reloads after every clear, so you see the fresh version (you can turn it off).
- **Clear summary:** a card on the page after each clear with the types removed, cookies counted and space freed, measured from the site's own storage report before and after.
- **Confirm before clearing:** an optional prompt; decline and nothing is cleared.
- **Two ready-made profiles:** Default for every site, and Localhost for `localhost` and `127.0.0.1`. Switch from the toolbar icon's right-click menu.
- **Chrome's own list:** browsing history, download history and autofill data, the same items as Chrome's Clear browsing data, off by default, one toggle each.
- **sessionStorage stays safe:** Chrome's own localStorage removal also wipes sessionStorage in your open tabs as a side effect. On the free tier CacheSweeper puts it straight back, so a clear never loses tab state you didn't ask to lose.

## Premium: Deep Clean and automation

$3 a month or $29 once. Everything in Free, plus:

- **sessionStorage, cleared properly.** Chrome's browsing-data dialog and its data-clearing API have no sessionStorage option, so tools built only on them can't reach it. CacheSweeper Premium clears it inside every open tab of the site, without closing a single tab.
- **Scheduled clearing.** Clear on a timer (every 30 minutes, hour, 4 hours, 12 hours or once a day), when Chrome starts, or after your computer has been idle for 5 minutes. Scheduled clears cover every site except protected ones and report through a system notification.
- **Tab-close clearing.** Close a site's tab and CacheSweeper clears that site's data automatically.
- **Protected domains.** The sites you never want signed out of. Protected domains are skipped by every clear, including the automatic ones, on any port (`localhost` also protects `localhost:3000`).
- **Unlimited profiles.** A profile per project or environment (localhost, staging, production), and CacheSweeper switches to the right one by domain.
- **Import and export profiles.** Save your profiles to a file and load them on another machine.
- **Service worker registrations.** Unregister the site's service worker, not just its cache.
- **Time range.** Clear only the last 15 minutes, hour, day, week or month, or everything.
- **Metrics dashboard.** Data freed, number of clears, cookies removed, automated clears, and your 30 most recent clears by trigger.
- **Bypass-cache reload.** Reload without the HTTP cache, so the next load is truly fresh.

## Free vs Premium

| Feature | Free | Premium |
|---|:---:|:---:|
| HTTP cache, cookies, localStorage, IndexedDB, CacheStorage, OPFS | ✓ | ✓ |
| sessionStorage |  | ✓ |
| Service workers |  | ✓ |
| Browsing history, download history, autofill data (opt-in) | ✓ | ✓ |
| Keyboard shortcut | ✓ | ✓ |
| Auto-reload toggle | ✓ | ✓ |
| Confirm before clearing | ✓ | ✓ |
| Bypass-cache reload |  | ✓ |
| Time range selector |  | ✓ |
| Per-origin scope | ✓ | ✓ |
| Protected domains |  | ✓ |
| Profiles | 2 (Default + Localhost) | Unlimited |
| Domain auto-switching |  | ✓ |
| Export and import profiles |  | ✓ |
| Scheduled and automated clearing |  | ✓ |
| Clear on tab close |  | ✓ |
| Clear summary and notifications | ✓ | ✓ |
| Metrics dashboard |  | ✓ |

## Pricing

| Plan | Price | What you get |
|---|---|---|
| Free | $0, for good | All the core clearing, per-site or everywhere, with the shortcut, auto-reload and the summary card |
| Premium Monthly | $3 a month | Everything in Premium. Renews monthly; cancel any time and keep access to the end of the paid month |
| Premium Lifetime | $29 once | Everything in Premium, including future Premium features. No recurring charges. By month ten of Monthly you'd have paid for Lifetime already |

**Getting Premium:** choose a plan on [cachesweeper.com](https://cachesweeper.com/#pricing), pay through Lemon Squeezy (our merchant of record, which handles payment, tax and receipts), then paste your license key on the Premium tab of CacheSweeper's settings. No account to create.

Every Premium purchase comes with a **30-day money-back guarantee**, no questions asked: email support@cachesweeper.com or ask Lemon Squeezy. There's no trial to expire: the free tier is the trial, and nothing nags you to upgrade.

## Privacy, plainly

- Runs locally in your browser. No ads, no analytics, no tracking, no account.
- Your browsing data never leaves your browser. The only data CacheSweeper sends is a Premium license key: to Lemon Squeezy's license service to activate it, then about once a day to confirm it's still valid.
- The settings page loads its fonts and icons from Google Fonts and jsDelivr, like most web pages do; nothing about your browsing or settings goes with them.
- It never reads page content. Cookie values are never read: cookies are only counted for the summary.
- Your settings and profiles are saved with Chrome's storage API. If you use Chrome sync, Google syncs them for you; the license key stays in that one browser.

Full policy: [cachesweeper.com/privacy](https://cachesweeper.com/privacy)

## Permissions, explained

| Permission | Why CacheSweeper needs it |
|---|---|
| `browsingData` | The clearing engine: the Chrome API that deletes cache, cookies and storage. |
| All URLs + `scripting` | Runs a small script in the site's tabs to show the clear summary, ask the optional confirmation, measure how much storage a clear freed, and clear or preserve sessionStorage (Chrome's clearing API can't reach it). It never reads page content, and nothing is sent anywhere. |
| `tabs` | Reads the current tab's address to scope a clear to that site and pick the right profile, finds the site's other open tabs for sessionStorage, and notices when a tab closes for tab-close clearing. |
| `activeTab` | Keeps the toolbar icon, shortcut and right-click menu working on the current tab if you limit CacheSweeper's site access to "On click". |
| `notifications` | A system notification after a scheduled clear, or when a clear can't run on the current page. |
| `contextMenus` | The right-click menu on the toolbar icon. It adds nothing to web pages. |
| `storage` | Saves your profiles and preferences locally. |
| `alarms` | Runs scheduled clears on the timer you set, and re-checks a Premium license about once a day. |
| `idle` | Clears when your computer goes idle, if you turn that option on. |
| `cookies` | Counts how many cookies a clear removes, for the summary and metrics. Counts only; cookie values are never used, stored or sent. |

If a permission isn't needed for clearing, CacheSweeper doesn't request it.

## Notes for developers

- **Localhost profile.** Applies to `localhost` and `127.0.0.1`, so your dev-server settings stay separate from everyday browsing.
- **Cookies are per host, not per port.** Chrome keeps one cookie jar per host, shared by every port, so clearing cookies on `localhost:3000` also clears them for `localhost:5173`. CacheSweeper tells you when that happens. Every other storage type stays separate per port.
- **sessionStorage and Chrome's API.** Chrome's localStorage removal empties sessionStorage in the site's open tabs as a side effect. CacheSweeper snapshots it before the clear and restores it after, unless you've chosen to clear it (Premium).
- **Pages it can't clear.** Chrome doesn't let extensions run on `chrome://` pages, the New Tab page or other extensions' pages. Open a website and clear from that tab.
- **Still signed into Google?** When you're signed in to Chrome itself, Google refreshes the cookies that keep your Google Account signed in, even after Chrome's own Clear browsing data. Every other site signs out normally.
- **Built on Manifest V3.** A background service worker, no remote code: every script ships in the package.

## FAQ

<details>
<summary><b>Will it sign me out of everything?</b></summary>

No. By default it clears only the site you're on. Switch per-origin scope off if you want every site cleared at once.
</details>

<details>
<summary><b>Does it work on all websites?</b></summary>

It works on any `http://` or `https://` page. It can't run on Chrome's own pages (`chrome://`, `about:` and the New Tab page), the same as every other extension.
</details>

<details>
<summary><b>Will it clear my passwords or download history?</b></summary>

Not unless you switch them on. Browsing history, download history and autofill data are separate toggles under "Chrome's own list" in the settings, off by default. Passwords are never touched: Chrome no longer lets extensions clear them. Out of the box it clears developer storage (cache, cookies, localStorage, IndexedDB, CacheStorage) for the site you're on.
</details>

<details>
<summary><b>What's the keyboard shortcut?</b></summary>

<kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>X</kbd> on Windows and Linux, <kbd>Cmd</kbd>+<kbd>Shift</kbd>+<kbd>X</kbd> on Mac. Change it at `chrome://extensions/shortcuts`.
</details>

<details>
<summary><b>How does the Localhost profile work?</b></summary>

CacheSweeper comes with two profiles: Default (every site) and Localhost (`localhost` and `127.0.0.1`). Switch between them from the toolbar icon's right-click menu or on the settings page. Premium adds unlimited profiles that switch automatically by domain.
</details>

<details>
<summary><b>Why does it need access to all URLs?</b></summary>

Because it clears whatever site you're on, it can't know the sites in advance. Host access lets it show the summary card and the optional confirmation in that site's tab, measure how much storage a clear freed, clear or preserve sessionStorage in the site's open tabs, and count the site's cookies. It never reads page content and sends nothing anywhere.
</details>

<details>
<summary><b>Why clear sessionStorage?</b></summary>

sessionStorage is scoped to a tab and can survive reloads and hard refreshes, keeping stale auth tokens or half-finished UI state around. Chrome's standard browsing-data controls don't expose it, so CacheSweeper Premium clears it directly in the site's open tabs.
</details>

<details>
<summary><b>Why am I still signed into Google after clearing?</b></summary>

That's Chrome, not CacheSweeper. When you're signed in to Chrome itself, Google automatically refreshes the cookies that keep your Google Account signed in. Chrome's own Clear browsing data works the same way. Every other site signs out normally. To sign out of Google too, sign out of Chrome first, or turn off "Allow Chrome sign-in" in Chrome's settings.
</details>

<details>
<summary><b>Is there a free trial for Premium?</b></summary>

The free tier is genuinely full-featured. Install it, use it daily, and upgrade only if you need sessionStorage, scheduled clearing or unlimited profiles. There's no trial to expire and nothing nags you to upgrade.
</details>

## Guides

- [How to clear cache and cookies for one site in Chrome](https://cachesweeper.com/guides/clear-cache-one-site-chrome)

## Support

Questions, bugs or ideas: email [support@cachesweeper.com](mailto:support@cachesweeper.com) (a human reads every message) or visit [cachesweeper.com/support](https://cachesweeper.com/support).

<p align="center">
  <a href="https://chromewebstore.google.com/detail/cachesweeper/pbonkgfajlgnahmegmiegdmogmpnilif"><b>Add CacheSweeper to Chrome for free</b></a><br>
  <sub>Cache cleared. Sanity restored.</sub>
</p>
