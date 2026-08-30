# Privacy Policy — Data Watchdog (Privacy Monitor)

**Last updated:** 30 August 2026

Data Watchdog is a Chrome extension that shows you what data each website tries to access and lets you allow, block or spoof it per site.

## The short version

Data Watchdog does not collect, transmit, sell or share your personal information. Everything it records stays on your own computer. There is no account, no server, no analytics and no telemetry.

## What is stored, and where

All of the following is stored locally on your device using Chrome's `chrome.storage.local`, and never leaves it:

- **Your per-site settings** — which of the 22 categories you have set to Allow, Ask, Block, Spoof, Noise or Protect for each website, and any spoofing profile you have chosen (for example a city for location, or a GPU string for WebGL).
- **Per-site counters** — how many times each category was allowed or blocked on a site. These are counts only, capped at 300 sites, with the least-recently-used dropped beyond that.
- **A short-lived per-tab activity log** — the recent API calls a page made, held in memory only, capped at 80 entries per tab and 25 tabs, and discarded when the tab is closed or navigates. It is never written to disk.

You can view, export, edit and delete all of it at any time from the extension's options page. Uninstalling the extension removes it.

## The one network request

Data Watchdog makes exactly one outbound request, and only when you explicitly click for it:

**"Check my public IP"** in the popup sends a request to `https://api.ipify.org`, a public IP-echo service, and displays the IP it returns. It is not sent anywhere else and is not stored. It exists so you can see what a website would see — useful when checking WebRTC leak protection.

If you never click that button, the extension makes no network requests at all. Fonts are loaded from your own system rather than a CDN, and the extension contains no remote code.

Your use of api.ipify.org is subject to that service's own terms; it necessarily observes your IP address in order to report it back to you.

## What Data Watchdog can technically see

To do its job the extension has access to the pages you visit — that is what lets it observe and control what those pages request. It uses that access only to apply your settings and to show you the activity for the tab you are currently looking at. None of it is recorded beyond the local storage described above, and none of it is transmitted.

## Permissions and why they exist

| Permission | Why |
|---|---|
| `storage` | Save your per-site settings and counters on your device |
| `tabs` | Know which site the popup is showing, and clear per-tab state on navigation |
| `declarativeNetRequest` | Block requests to a fixed built-in list of ad/analytics domains on sites where you turned it on |
| `webRequest` | Observation only — used solely to name which tracker was seen so the UI can report it. No blocking capability is requested |
| `scripting` | Apply your chosen protections before a page's first script runs |
| Access to all sites | So you can enable protections on any site you choose |

## Children

Data Watchdog is not directed at children and collects no information from anyone.

## Changes

If this policy changes, the updated version will be published at this same address with a new "last updated" date.

## Contact

Questions about this policy: othmanriaz@gmail.com
