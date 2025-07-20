# SlotSet Updates Server

This repository hosts static update files for [Expo](https://expo.dev/) apps. Use it to deliver over‑the‑air updates built with `expo export`.

## Setup

Install dependencies for the deploy script:

```bash
npm ci
```

## Export updates

Run `expo export` in your app and copy the generated contents into the `public` folder of this repo. The default structure from Expo already includes bundles and manifests for both Android and iOS.

## Configure the app

Set the `updates.url` field in `app.json` or `app.config.ts` to your GitHub Pages URL. For example:

```json
{
  "updates": {
    "url": "https://<user>.github.io/slotset-updates"
  }
}
```

Expo Updates will automatically check this URL for the latest manifest and download the platform specific bundle referenced inside.

## Deploy

Publish the `public` directory to GitHub Pages:

```bash
npm run deploy
```

## Versions

- Expo SDK: `53.0.19`
- Expo Updates: `0.28.17`
