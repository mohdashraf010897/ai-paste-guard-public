# Privacy Policy

**Effective date:** September 29, 2026

## What the extension does

AI Paste Guard is a Chrome extension that checks text you paste into ChatGPT
(chatgpt.com), Claude (claude.ai), and Gemini (gemini.google.com) before the site
receives it. If it finds a high-confidence secret such as an API key, token, private key,
or a password inside a connection string, it pauses the paste so you can redact it,
cancel, or paste anyway. All detection runs on your device.

## What it reads

- The text you paste on the three supported sites, only at the moment you paste it, and
  only to scan it for secrets.

It does not read typed text, uploaded files, or images. It does not read pages on any
other site.

## What it stores

Everything below is stored on your device in local extension storage
(`chrome.storage.local`). Nothing is stored in synced storage (`chrome.storage.sync`),
and nothing leaves your device.

| Data | Where | Kept until |
| --- | --- | --- |
| The text you paste | Content script memory in the tab, only while a decision is pending | Cleared when you decide, when you turn the site off, or when you leave the page |
| Settings (which sites are on, whether to mask personal info, which rules are off) | Local extension storage | You change them, reset, or uninstall |
| Counts per rule and the review-ask state | Local extension storage | You reset counts or uninstall |

The text you paste stays in the tab's memory only while the dialog is open. The only text
that ever enters the page is the text you choose to insert.

## What it never does

- It never sends, sells, or shares your data.
- It never transmits the text you paste anywhere.
- It never tracks your browsing.
- It has no account, no analytics, no telemetry, no crash reporting, and no remote
  configuration.
- It makes no network requests and contacts no server.

## Feedback links

The popup has "Send feedback" and "Report a missed secret" links, and the pause dialog has
"Not a secret? Report a false alarm". They do nothing until you click them. When you click
one, your browser opens a prefilled issue in the public
[ai-paste-guard-public](https://github.com/mohdashraf010897/ai-paste-guard-public) GitHub
repository that contains only the extension version, the relevant rule IDs, and the host
(for example `chatgpt.com`). It never includes the text you pasted. You review and submit
the issue yourself; once submitted it is public and lives on GitHub under GitHub's terms.

## Permissions and why

- **`storage`** — to save your on/off settings and local counts on this device.
- **Content scripts on chatgpt.com, claude.ai, and gemini.google.com** — to check pasted
  text on those sites before the site receives it. The extension runs on no other sites
  and requests no host permissions.

## How to delete everything

- **Reset counts** in the popup clears the local counters.
- **Reset to defaults** in the popup restores default settings.
- **Uninstall** the extension to remove all of its local storage.

## Known limits

AI Paste Guard does not check typed text, files, images, iframes, or other sites; tabs
opened before you installed it need a reload; a site that reads the clipboard directly
bypasses the paste event; and detection covers the listed formats, not every possible
secret. It is not DLP and does not replace your organization's security tools.

## Limited Use

AI Paste Guard's use of data complies with the Chrome Web Store User Data Policy, including
the Limited Use requirements. Pasted text is processed only on your device to provide the
extension's single purpose. It is not transferred, sold, used for advertising, or read by
anyone.

## Changes to this policy

If the extension's data behavior ever changes, this policy and the Chrome Web Store
disclosures are updated before the change ships, and the effective date above changes.
Earlier versions remain in this file's Git history.

## Contact

For privacy questions,
[open an issue](https://github.com/mohdashraf010897/ai-paste-guard-public/issues) in the
public ai-paste-guard-public repository (GitHub sign-in required to post). Do not include
secrets or pasted text in an issue.
