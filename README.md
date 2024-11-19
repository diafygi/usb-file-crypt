# USB File Encryption Tool

This is a standalone HTML file you can put on a USB drive and use it to encrypt and decrypt files on the drive without having to use any special software.

## How to use

Copy `usb_file_crypt.html` to your USB drive.

On the system you have the files you want to encrypt and put on the USB drive:

1. Open `usb_file_crypt.html` in a web browser.
2. In the webpage's Encrypt section, select the file from the local filesystem you want to encrypt.
3. Input an encryption password.
4. Click "Encrypt".
5. Wait for the file to encrypt (may take a bit for large files).
6. When done encrypting, click the "Save to USB drive" link.
7. A file picker should pop up and you can save the encrypted `.enc` file to your USB drive.
8. Close the webpage, unmount, and unplug your USB drive, and take it to the other system where you want to transfer the files.

On the system where you want to copy the files to:

1. Open usb_file_crypt.html in a web browser.
2. In the webpage's Decrypt section, select the file from the local filesystem you want to decrypt.
3. Input an decryption password (same password as you used to encrypt it).
4. Click "Decrypt".
5. Wait for the file to decrypt (may take a bit for large files).
6. When done decrypting, click the "Save to local filesystem" link.
7. A file picker should pop up and you can save the decrypted file to your local filesystem.
8. When you're done, you can simply close the webpage and delete the encrypted `.enc` file on your USB drive.

## Limitations

As part of encrypting/decrypting, the webpage loads the entire file into memory, which can crash your browser if the file you're trying to encrypt/decrypt is larger than your systems free memory.

Browsers are limited to saving only one file at a time, so this tool is limited to encrypting/decrypting only single files. If you have a lot of files you want to transfer, I recommend creating a `.zip` file first and then encrypting that.

## Why I made this

I made this because I couldn't find a way to make an encrypted USB drive that could be accessed using only default OS software on Windows, MacOS, and Linux. Each OS generally has a way to do encrypted USB drives, but they aren't cross-compatible with each other. So, for example, you can't make an encrypted USB drive on Ubuntu and be able to read it on stock Windows.

There's lots of special software you can use to do encrypted files on USB drives, but using it means each system has to have the software installed (which I don't want to have to do just to do ad-hoc file transfers securely).

So I made a small HTML file that you can keep on your USB drive, and then on whatever system you plug your USB drive into, you can open the HTML file in that system's browser and use it to encrypt/decrypt the files on your USB drive.

## Copyright

Released under MIT license.
