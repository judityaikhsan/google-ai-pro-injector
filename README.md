# Gemini Injector by judith0x88

Chrome extension (Manifest V3) that injects Google One / AI Pro checkout offer tokens, so the subscription goes through as a free trial.

## What it does

- Intercepts the Play checkout on one.google.com and swaps the subscription items for the selected offer token.
- Layers: 12 months (first-time), 6 months (SS), 6 months, 6 months (backup) — stack them one after another.
- Adds a free YouTube Premium individual add-on token alongside the AI Pro subscription.
- Price guard: a banner on the checkout page tells you whether a free trial was detected. Green = free trial, safe to continue. Red = no free trial detected, do not subscribe.

## Install (load unpacked)

1. Download the latest release zip from the [Releases](../../releases) page and extract it — or clone this repo.
2. Open `chrome://extensions` and turn on **Developer mode**.
3. Click **Load unpacked** and pick the extracted folder.
4. Open `one.google.com/plans` and confirm the target account (U.S. region) is shown at the top left.

## Usage

1. Click the extension icon and select a layer, then refresh the page and confirm "Injection active" appears at the bottom right.
2. Click **Get discount** on the AI Pro card to open the Play checkout window.
3. Check the banner at the top: **green = free trial**. Do not proceed if it is red.
4. Add a card (U.S. tax-free ZIP code 97201), verify the total is **$0.00**, then subscribe.
5. To stack the next layer: return to the popup, switch layers, refresh, and click again.
6. When finished, go to play.google.com and turn off automatic renewal.

## Safety

- Only subscribe when the guard shows a free trial and the total is $0.00.
- Offer tokens can stop working or be revoked at any time — use an account you can afford to lose access to on a trial.
- This tool modifies checkout requests in your own browser; use it at your own risk.

## License

MIT — see [LICENSE](LICENSE).
