# Complexe

**Complexe** is an AI-powered flashcard app built for [Shipaton 2026](https://www.revenuecat.com/blog/company/announcing-shipaton-2026). It leverages cognitive science—specifically **dual coding theory** (pairing verbal and visual info) combined with the keyword/mnemonic method—to create flashcards that act like a memory coach, not just a digitized notebook.

## The Concept

Instead of simply digitizing flashcards, Complexe compresses and re-encodes them:
1. **Input**: You can provide information in two ways: upload a PDF document, or enter a short topic/title (100-200 words) and let the app automatically search the internet to gather the required data.
2. **Compression**: The AI first breaks down chapters and topics into smaller 5-6 sentence paragraphs. Then, it distills each paragraph into two formats: a **1-2 sentence summary** (the core explanation) and a **3-4 word anchor phrase** (the hook). It also generates a memorable image to pair with it.
3. **The Hook**: The front of the card shows the compressed 3-4 word phrase and image as a memory trigger. 
4. **The Full Idea**: The flip side contains the 1-2 sentence summary. The phrase is a hook back to this full idea, not a replacement for it.

*Example: "Mitochondria is the powerhouse of the cell" collapses into "Cell's power plant" with a power-plant-shaped mitochondria image.*

## Tech Stack & Architecture

- **Framework**: React Native via Expo (Managed workflow for fast iteration, EAS Build/Submit)
- **Backend/AI**: Backend proxy handling Claude (for text compression) and an Image API (for visual generation)
- **Monetization**: RevenueCat SDK for paywall and entitlement management
- **Local Data**: Local storage for decks and the basic review loop

## Monetization Model

AI text and image generation carry real per-use costs. Complexe utilizes a natural freemium model:
- **Free Tier**: X free cards/generations per day. (Enforced server-side per anonymous user ID).
- **Pro Tier**: Unlimited generations with a subscription, powered by **RevenueCat**.

## Roadmap (Shipaton 2026)

- **Weeks 1–2 (now–Aug 26)**: Build the walking skeleton — input → Claude compression → image generation → flip card. Focus on testing compression quality and image latency.
- **Week 3 (Aug 27–Sep 2)**: Local storage for decks/cards, basic review loop (Leitner box — three buckets).
- **Week 4 (Sep 3–9)**: RevenueCat integration — products in App Store Connect/Play Console, entitlement gating, sandbox testing.
- **Week 5 (Sep 10–16)**: Onboarding, app icon, store listing assets, content moderation pass on generated images.
- **Week 6 (Sep 17–23)**: Submit to App Store and Google Play. Buffer for first-time developer/AI-app scrutiny.
- **Week 7 (Sep 24–30)**: Buffer for rejections/resubmissions, bug fixes, and #BuildInPublic content.

## Setup

1. Install dependencies:
   ```bash
   npm install
   ```

2. Start the development server:
   ```bash
   npx expo start
   ```
