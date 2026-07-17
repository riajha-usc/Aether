# Aether
The Journalling Website - all you need!
I have built the Aether Journaling App, a minimalist, distraction-free writing and voice-recording sanctuary inspired by classic editorial typography and WordPress writing setups.

The application is fully compiled and deployed with the following features:
# 🎨 WordPress-Inspired Minimalist Visual Design
- Editorial Typography: Paired clean, readable Inter for controls and metadata tags, Merriweather (serif) for story titles and paragraph writing block layouts, and JetBrains Mono for status indicators.
- Spacious negative space: Crafted a high-contrast, off-white "warm paper" palette that reduces eye strain and helps writers focus on translating their voice and written thoughts onto the canvas.
- Fully Mobile-Friendly: Designed with touch targets, responsive side drawers, and collapsible filter lists that scale seamlessly from compact phones to desktop monitors.

# 🎙️ Audio & Writing Block Editor
- Dual-Note Input: Combine expressive textual entries with high-quality voice memos.
- Microphone Recording: Includes an inline, low-latency, and low-bitrate Audio Recorder (using the browser's native MediaRecorder API) to capture voice memos up to 90 seconds. Audio is encoded as compressed base64 strings and attached directly to entries.
- In-Feed Playback: Includes custom Audio Players that render inside feed cards and editor canvases so you can play voice memos instantly without leaving your dashboard.
- Writing Helpers: Real-time word counts, estimated reading times, category selections (General, Personal, Work, Ideas, Dreams, Gratitude), custom tag fields, and mood selections.

# ☁️ Offline-First & Automatic Cloud Synchronization
- Instant Local Storage: Saves drafts instantly to browser state caches, letting you log stories, update categories, and record audio notes without any internet access.
- Firestore Cloud Sync: Pairs with Google Firebase Firestore. When online, the engine automatically merges local entries, uploads new posts, pushes changes, and reconciles deletes.
- Conflict Resolution: Relies on active timestamps to resolve editing differences, downloading newer cloud edits or uploading newer local edits automatically.
- Visual Status Indicators: Displays clear indicators to show whether you are "Online (Sync Enabled)" or "Offline (Caching Locally)".

# 🔒 Zero-Knowledge Encryption & Backups
- AES-GCM 256-Bit Cryptography: Allows you to set a personal master passphrase. All titles, stories, categories, tags, and base64 audio streams are encrypted completely client-side in your browser before ever touching local storage or the cloud database.
- Cryptographic Lock: Features a secure sentinel system that locks/unlocks the application locally and clears memory keys instantly when clicking "Lock Workspace".
- Encrypted Backups: Download your entire journal database as an encrypted .json backup file, allowing you to restore your entries on any other device.
