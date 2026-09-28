# Imposter Bits

Hide a secret file inside an ordinary picture, and get it back later with a password.

Imposter Bits is a small Windows app I built with C# and Windows Forms. It's a friendly window on top of [Steghide](https://steghide.sourceforge.net/), so you don't have to touch the command line.

## What it does

- **Embed:** pick an image, pick the file you want to hide, choose a password. You get a new image that looks the same but carries your secret.
- **Extract:** pick that image, enter the password, and your file comes back out.

Works with **JPEG** and **BMP** images.

## Install

There's nothing to install.

1. Download **Imposter Bits.exe**
2. Double-click it

The first time you open it, it sets itself up in a few seconds. After that it starts instantly.

Windows may warn about an "unknown publisher" because the app isn't code-signed. Click **More info**, then **Run anyway**.

## How to use it

**To hide a file**
1. Select an image
2. Select the secret file
3. Enter a password
4. Click **Embed** and choose where to save the new image

**To get it back**
1. Click **Switch** to open the Extract screen
2. Select the image with the hidden file
3. Enter the password
4. Click **Extract** and choose where to save it

Tip: when you extract, give the file its original extension (like `.txt`), or Windows won't know how to open it.

## Good to know

- Forget the password and the secret is gone. There is no recovery.
- Use the saved image as-is. Re-saving, compressing, or sending it through apps that shrink pictures (like WhatsApp or Instagram) can destroy the hidden data. Send it as a file or document instead.
- This hides that a file exists, but it isn't a substitute for proper security tools.
- On first launch the app unpacks Steghide into `%LocalAppData%\ImposterBits`. Delete that folder if you ever want to remove it.

## Built with

- C# / Windows Forms (.NET Framework)
- [Steghide](https://steghide.sourceforge.net/), which is GPL-licensed and packed inside the app

## License

Imposter Bits is released under the [MIT License](LICENSE).

It includes [Steghide](https://steghide.sourceforge.net/), a separate program licensed under the GNU GPL v2. Its source code is available from the link above. Steghide's license applies to Steghide only, not to Imposter Bits' own code.
