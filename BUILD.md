# ARIIA Chatbot - Build Guide

## Project Overview
This is a TypeScript-based chatbot application for Eagle Eye Defense.

## Prerequisites
- Node.js (v16 or higher)
- npm or yarn
- For APK builds: React Native CLI or Expo CLI
- For Android APK: Android SDK, Java JDK 11+

## Installation

```bash
# Extract the project files from ariia-chatbot.zip
unzip ariia-chatbot.zip

# Navigate to project directory
cd ariia-chatbot

# Install dependencies
npm install
# or
yarn install
```

## Development

```bash
# Build TypeScript
npm run build

# Run development server (if applicable)
npm start

# Run tests
npm test
```

## Building APK

### Option 1: React Native CLI
```bash
cd android
./gradlew assembleRelease
```

### Option 2: Expo (if using Expo)
```bash
expo build:android
```

### Option 3: EAS Build (recommended for Expo projects)
```bash
eas build --platform android --type apk
```

## Output
- APK file will be generated in: `android/app/build/outputs/apk/release/`
- Or via Expo/EAS, download from build dashboard

## Troubleshooting
- Clear node_modules: `rm -rf node_modules && npm install`
- Clear Android cache: `cd android && ./gradlew clean`
- Check Node version: `node --version`

## Project Structure
- `/src` - Source TypeScript code
- `/android` - Android native code and build configuration
- `/ios` - iOS native code (if applicable)
- `tsconfig.json` - TypeScript configuration
- `package.json` - Node dependencies and scripts

