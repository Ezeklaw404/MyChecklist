# Checklist

A fast, offline-first checklist app for Android. Organize items into nested
categories, reorder freely, and mark things done without ever needing a
network connection.

## Features

- **Nested categories** — organize checklists into categories, and categories
  into subcategories, as deep as you need
- **Drag-to-reorder** — reorder categories and items by dragging
- **Flexible completion states** — mark items done with a strikethrough, or
  hide them entirely (toggleable per list)
- **Fully offline** — all data lives in a local SQLite database on-device;
  no account, no internet required
- **Fast** — built for quick capture and quick checking-off, not friction

## Tech Stack

- [React Native](https://reactnative.dev/) (via [Expo](https://expo.dev/))
- TypeScript
- [expo-sqlite](https://docs.expo.dev/versions/latest/sdk/sqlite/) for local storage
- [React Navigation](https://reactnavigation.org/) for screen flow

## Project Structure

    /src
      /components   Shared UI (Checkbox, DraggableRow, etc.)
      /features
        /categories Screens + logic for browsing and nesting categories
        /checklist  Screens + logic for items inside a category
      /data
        db.ts           SQLite setup and schema
        categoryRepo.ts Category CRUD
        itemRepo.ts     Item CRUD
      /navigation   Navigation stack/config
      /types        Shared TypeScript types

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (LTS)
- [Expo Go](https://expo.dev/client) app on your Android device (for
  development), or Android Studio if you want an emulator

### Install & Run

    git clone https://github.com/<your-username>/checklist.git
    cd checklist
    npm install
    npx expo start

Scan the QR code with the Expo Go app on your Android phone to run it live.

### Build a standalone APK

    npx eas build -p android --profile preview

## Roadmap

- [ ] Category CRUD + nesting
- [ ] Checklist item CRUD
- [ ] Drag-to-reorder
- [ ] Strikethrough / hide toggle for completed items
- [ ] Rename / delete categories and items
- [ ] Settings screen
- [ ] Standalone APK build

## License

MIT