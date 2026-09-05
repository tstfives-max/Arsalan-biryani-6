# Arsalan AI - Voice Assistant for Arsalan Biryani

A premium, highly interactive voice AI assistant for restaurants built with Next.js, Tailwind CSS, Framer Motion, and the Google Gemini API.

## Features
- 🎙️ **Voice First**: Built-in Web Speech API integration for natural conversations.
- 🧠 **Gemini Powered**: Intelligent, contextual responses using Gemini 2.5 Flash.
- 🎨 **Premium UI**: Dark mode, food-focused aesthetic with Framer Motion animations.
- 📱 **Mobile Optimized**: Designed for QR-code access and one-handed use.
- ⚙️ **Configurable**: Centralized `restaurantConfig.ts` for menu, prices, and facts.

## Getting Started

### 1. Install Dependencies
```bash
npm install
```

### 2. Configure Environment Variables
Copy the `.env.example` file to `.env` or `.env.local`:
```bash
cp .env.example .env.local
```
Get a Gemini API Key from [Google AI Studio](https://aistudio.google.com/app/apikey) and add it to your `.env.local` file:
```
GEMINI_API_KEY=your_actual_api_key_here
```

### 3. Customize Restaurant Data
Edit `src/config/restaurantConfig.ts` to update the menu, prices, location, and timings. The AI personality is automatically generated based on this file.

### 4. Run Development Server
```bash
npm run dev
```
Open [http://localhost:3000](http://localhost:3000) in your browser.

## Architecture & Security
- The Gemini API is accessed strictly via a secure Server API Route (`src/app/api/chat/route.ts`).
- **Never expose the `GEMINI_API_KEY` in frontend components.**
- `.env` and `.env.local` are included in `.gitignore` by default in Next.js.
