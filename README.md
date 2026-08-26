# 🔓 Secure Messenger

A lightweight, single-file web app for encoding and decoding text messages using a shared secret key. Built with plain HTML, CSS, and JavaScript — no dependencies, no server, no build step.

### 🔗 [**Try the Live Demo →**](https://cryptographytool-1.wasmer.app/)

[![Live Demo](https://img.shields.io/badge/Live%20Demo-cryptographytool--1.wasmer.app-7c9aff?style=for-the-badge)](https://cryptographytool-1.wasmer.app/)

## Features

- **Encrypt** a message and **decrypt** it back using one of four methods
- Clean, dark-themed, responsive UI (works on desktop and mobile)
- One-click copy of encrypted/decrypted results
- Friendly inline error messages (missing key, missing text, bad input, etc.)
- Runs entirely in the browser — nothing is sent to a server

## Encryption Methods

| Method | Description | Security Level |
|---|---|---|
| ⚡ **XOR Cipher** | XORs each character with a repeating key, then Base64-encodes the result | Key-dependent, but not cryptographically secure |
| ↻ **Caesar Cipher** | Classic alphabet shift, with the shift amount derived from the key | Toy cipher — trivially breakable |
| 📦 **Base64** | Standard encoding, not encryption | None — instantly reversible by anyone |
| 🔄 **Reverse Text** | Reverses the character order | None — just for fun |

> ⚠️ **Important:** None of these methods provide real security. They're suitable for games, puzzles, or light obfuscation between friends — **not** for passwords, personal data, or anything sensitive. For real secure messaging, use an established end-to-end encrypted platform (Signal, etc.) or a vetted cryptographic library.

## How to Use

1. Open `index.html` in any modern web browser, or try the [live demo](https://cryptographytool-1.wasmer.app/).
2. **To encrypt:**
   - Choose a method from the dropdown.
   - Enter a secret key (required for XOR and Caesar).
   - Type your message.
   - Click **Encrypt message**, then copy the result to share with a friend.
3. **To decrypt:**
   - Choose the *same* method used to encrypt.
   - Enter the *same* key.
   - Paste the encrypted text.
   - Click **Decrypt message** to reveal the original.

## Project Structure

```
index.html   # Everything: markup, styles, and logic in one file
```

## Tech Stack

- Plain HTML5 / CSS3 (custom properties for theming)
- Vanilla JavaScript (no frameworks or libraries)
- `btoa` / `atob` for Base64 handling
- Clipboard API for copy-to-clipboard

## Browser Support

Works in any modern browser that supports the Clipboard API and ES6 (Chrome, Firefox, Edge, Safari — recent versions).

## License

Free to use, modify, and share for personal or educational projects.
