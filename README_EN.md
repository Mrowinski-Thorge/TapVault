# TapVault - Secure Mobile Vault

**TapVault** is a mobile-friendly, zero-server, open-source vault application for securely storing and sharing secrets. It uses a unique unlock mechanism: secrets are only decrypted after a user executes a specified number of "taps" or "shakes" on their device. All encryption and data storage is performed locally in the browser—no server ever sees your data.

---

## 🚀 Features

- **Create Vaults:** Store secret messages, optionally give them a title, and secure them with a required number of taps or shakes.
- **Unlock by Tap or Shake:** Choose between tap or shake mode for unlocking; the number of required actions is adjustable.
- **AES-256-GCM Encryption:** Secrets are encrypted (demo uses Base64 for simplicity, but recommended is AES-GCM for production).
- **Offline & Private:** All data is stored locally in your browser (`localStorage`). No accounts or servers required.
- **Share Vaults:** Share vaults via link or QR code (deep linking supported).
- **Recent & My Vaults:** Quick access to recently created and all stored vaults.
- **Dark/Light Mode:** Theme toggle for better usability.
- **Haptic Feedback:** Vibration on interactions for supported devices.
- **Settings:** Customize default unlock mode, required actions, salt length for encryption, and more.
- **Mobile-first UI:** Responsive, app-like interface with bottom navigation.
- **Open Source:** Free to use under the MIT license.

---

## 🛠 How It Works

1. **Create a Vault:**
   - Enter a secret message and optional title.
   - Choose unlock mode: **Tap** or **Shake**.
   - Set the number of required actions (e.g., 50 taps).
   - The secret is encrypted and stored locally. A unique vault ID is generated.

2. **Share a Vault:**
   - Copy the vault's unlock link (including the ID) or use the device's share feature.
   - The recipient can open the link and unlock the vault by performing the required actions.

3. **Unlock a Vault:**
   - On the unlock screen, perform the required number of taps or shakes.
   - After reaching the required number, the secret is decrypted and displayed.
   - Optionally, copy the decrypted secret to your clipboard.

---

## ⚠️ Security Note

- **Demo Version:** The included demo uses Base64 encoding for simplicity. For real use, integrate AES-256-GCM encryption in `encryptMessage` and `decryptMessage` functions.
- **No Server:** All vault data is stored in your browser. If you clear site data, your vaults are lost.
- **Open Source:** Review and contribute to improve security and features!

---

## 📦 Installation & Usage

No installation needed—just open the HTML file in your browser or deploy it as a static site.

### To Run Locally

1. Download `index.html`.
2. Open it in your mobile or desktop browser.

### To Deploy

- Deploy as a static site (GitHub Pages, Vercel, Netlify, etc.).
- No server or backend required.

---

## 🖥️ File Structure

- `index.html` — Main app UI & logic (single file app)
- All code (HTML, CSS, JS) is in one file for easy deployment.

---

## 📝 Customization

- Adjust default settings in the `loadSettings()` method.
- Replace demo encryption with real AES-GCM in `encryptMessage` and `decryptMessage`.
- Style/theme variables can be tweaked in the CSS section at the top.

---

## 📱 Screenshots

*Add screenshots here for App UI, Vault creation, Unlock process, etc.*

---

## 🤝 Contributing

Contributions are welcome! Open issues or pull requests for improvements or bug fixes.

---

## 🛡️ License

MIT License. See [LICENSE](LICENSE) for details.

---

## 👏 Credits

- Inspired by the need for private, easy-to-use, no-server secret sharing.
- Icons and UI inspired by iOS Human Interface Guidelines.

