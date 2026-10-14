# Wirelet feedback

Report a bug or suggest an idea for Wirelet, the browser extension that modifies HTTP request and response headers.

Install Wirelet: [Chrome Web Store](https://chromewebstore.google.com/detail/bljgefhnlagohdjnogbdnomlidbkbkem) · [Microsoft Edge Add-ons](https://microsoftedge.microsoft.com/addons/detail/eakjkekgdahclbmojnbiilneemmkgjeh).

- **Bug:** in Wirelet, open the settings, then "Report a problem" and "Open on GitHub": the form comes filled with a short diagnostics text (no address, header, value or key). You can also [open the bug form](https://github.com/Wirelet/feedback/issues/new?template=bug.yml) directly.
- **Idea:** [suggest an idea](https://github.com/Wirelet/feedback/issues/new?template=idea.yml).
- **Email:** wirelet.dev@gmail.com

Issues here are public: never paste a token, a key or a private address.

Privacy: [PRIVACY.md](PRIVACY.md).

## Verify the package yourself

1. Download `wirelet-<version>-chrome.zip` (or `-edge.zip`) from this repository's [releases](https://github.com/Wirelet/feedback/releases) and compare its SHA-256 with `SHA256SUMS.txt` (`shasum -a 256 wirelet-1.0.2-chrome.zip`).
2. `unzip -p wirelet-1.0.2-chrome.zip manifest.json` shows its `permissions`, its `optional_host_permissions` and its `content_security_policy` (`connect-src 'none'`).
3. `unzip -p wirelet-1.0.2-chrome.zip '*.js' | grep -c "fetch("` prints `0`: its code makes no network request.
