# QR Code Generator for Adobe Illustrator

A Adobe Illustrator script that generates a vector QR code directly in your active document. Supports URLs, emails, phone numbers, SMS, Wi-Fi, and plain text. Outputs a grouped object with a white background, sized and positioned relative to the active artboard.

> QR engine by [Kazuhiko Arase](https://github.com/kazuhikoarase/qrcode-generator) (MIT licence)

---
<img width="704" height="520" alt="QR-Pro" src="https://github.com/user-attachments/assets/370832f5-281a-4da2-91df-937133e039f1" />
---

## Features

- Generates a fully vector QR code — no rasterization, scales to any size
- Supports multiple content types: Website, Email, Phone, SMS, Wi-Fi, Plain text
- Type dropdown auto-fills the correct format prefix (e.g. `mailto:`, `WIFI:T:WPA;S:...`)
- White background included and grouped together with the QR modules
- Respects the document's ruler units (mm, cm, in, pt, px)
- Positioned relative to the active artboard
- Press **Enter** to generate without clicking the button

---

## Requirements

- Adobe Illustrator CC or later
- An open document

---

## Installation

1. Download `qr-generator.jsx`
2. Place it in your Illustrator scripts folder:
   - **Windows:** `C:\Program Files\Adobe\Adobe Illustrator [version]\Presets\en_US\Scripts\`
   - **macOS:** `/Applications/Adobe Illustrator [version]/Presets/en_US/Scripts/`
3. Restart Illustrator
4. Access via **File → Scripts → qr-generator**

Alternatively, run it directly at any time via **File → Scripts → Other Script...** without restarting.

---

## Usage

1. Open a document in Illustrator
2. Run the script via **File → Scripts → qr-generator** (or Other Script...)
3. In the dialog:
   - Select the **content type** from the dropdown
   - Enter your **URL, email address, phone number**, etc.
   - Set the **QR code size** and **white border margin** in your document's units
   - Choose an **error correction level** (M ~15% is a good default)
4. Press **Enter** or click **Generate QR Code**

The QR code is placed in the top-left area of the active artboard as a grouped object named `QR_code`.

---

## Error Correction Levels

| Level | Recovery capacity | Recommended when |
|-------|------------------|------------------|
| L ~7% | ~7% | Clean, controlled environments |
| M ~15% | ~15% | General use (default) |
| Q ~25% | ~25% | Slightly dirty or worn surfaces |
| H ~30% | ~30% | Logo overlays or harsh conditions |

---

## Wi-Fi QR Code Format

When using the **Wi-Fi** type, the pre-filled format is:

```
WIFI:T:WPA;S:MyNetwork;P:MyPassword;;
```

Replace `MyNetwork` with your SSID and `MyPassword` with your password. Change `WPA` to `WEP` or `nopass` if applicable.

---

## License

MIT — free to use, modify, and distribute.
