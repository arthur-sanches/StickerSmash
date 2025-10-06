# StickerSmash

A cross-platform mobile app built with [Expo](https://expo.dev) that lets you pick a photo from your device's library, place fun emoji stickers on top of it, and save the result back to your camera roll.

## Features

- Pick any image from your device's photo library
- Browse and place emoji stickers anywhere on the image using drag gestures
- Save the final stickered image to your media library
- Works on iOS, Android, and web
- Light and dark mode support

## Tech Stack

- [Expo](https://expo.dev) ~54 with Expo Router (file-based routing)
- React Native 0.81 with the New Architecture enabled
- `expo-image-picker` — photo library access
- `expo-media-library` — saving images to device storage
- `react-native-gesture-handler` + `react-native-reanimated` — smooth drag-and-drop sticker interactions
- `react-native-view-shot` / `dom-to-image` — capturing and exporting the composed image
- TypeScript

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org) (LTS recommended)
- [Expo CLI](https://docs.expo.dev/get-started/installation/) — install globally with `npm install -g expo-cli` or use `npx expo`
- For iOS: Xcode (macOS only)
- For Android: Android Studio with an emulator or a physical device with the [Expo Go](https://expo.dev/client) app

### Install dependencies

```bash
cd StickerSmash
npm install
```

### Run the app

| Platform | Command |
|----------|---------|
| Start dev server (all platforms) | `npm start` |
| Android | `npm run android` |
| iOS | `npm run ios` |
| Web | `npm run web` |

After running `npm start`, scan the QR code with the Expo Go app (Android) or the Camera app (iOS) to open the project on a physical device.

## Project Structure

```
StickerSmash/
├── app/
│   ├── _layout.tsx          # Root layout
│   ├── +not-found.tsx       # 404 screen
│   └── (tabs)/
│       ├── _layout.tsx      # Tab bar configuration
│       ├── index.tsx        # Main sticker editor screen
│       └── about.tsx        # About screen
├── assets/
│   └── images/              # App icons, splash screen, and sticker images
└── components/
    ├── Button.tsx
    ├── CircleButton.tsx
    ├── EmojiList.tsx        # Horizontal emoji picker list
    ├── EmojiPicker.tsx      # Modal emoji picker
    ├── EmojiSticker.tsx     # Draggable sticker component
    ├── IconButton.tsx
    └── ImageViewer.tsx      # Displays the selected or placeholder image
```

## Linting

```bash
npm run lint
```