# TOTP Viewer

TOTP Viewer is a simple web application for generating and displaying Time-based One-Time Passwords (TOTP).  
You can input your secret key via QR code, BASE32, or otpauth URI using various methods.

## Features

- Generate and display TOTP (RFC 6238)
- Input secret key via:
  - QR code (camera, image file, clipboard)
  - otpauth URI or BASE32 secret (manual input)
- Automatic time synchronization with server
- Toggle TOTP visibility (Show/Hide)
- Copy TOTP to clipboard with one click
- Visual countdown for remaining seconds

## How to Use

1. Open totp_viewer.html in your browser.
2. On first launch, the scanner page appears. Input your secret key by:
    - **Scanning QR code with camera**
    - **Selecting an image file**
    - **Pasting from clipboard**
    - **Entering otpauth URI or BASE32 secret manually**
3. Once the secret is read, you will be redirected to the TOTP display page.
4. TOTP is hidden by default. Click "Show" to reveal it.
5. Click the TOTP digits to copy them to your clipboard.

## URL Parameters

You can open the TOTP page directly with query parameters:

```
?a=ACCOUNT&s=SECRET&d=DESCRIPTION
```

Example:
```
totp_viewer.html?a=example@example.com&s=JBSWY3DPEHPK3PXP&d=Google
```

- `a`: Account name
- `s`: BASE32 secret
- `d`: Description (optional)

## Notes

- Secrets are processed only in your browser and never sent externally.
- Clipboard and camera features require HTTPS or localhost.
- If server time sync fails, local time is used.

## License

MIT License

---

For more details, see the source code in totp_viewer.html.
