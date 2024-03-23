# ZMK Firmware for Reviung41 keyboard

This is a repository for a ZMK Firmware for Reviung41 with Nice!Nano v2 keyboard.

## Default keymap

This layout is heavily inspired from [Watchman 42-key layout](https://github.com/aroum/Watchman-layouts)

## FAQ

- [FAQ](#faq)
  - [How to change the keymap?](#how-to-change-the-keymap)
  - [How to flash the keyboard?](#how-to-flash-the-keyboard)
  - [Problems](#problems)
    - [I'm getting File Transfer Error after copying firmware to the keyboard](#im-getting-file-transfer-error-after-copying-firmware-to-the-keyboard)

### How to change the keymap?

1. Fork or use this repository as a template https://github.com/FT256/reviung41-zmk.
2. Enable Github Actions for your repository.

You have two options on how to configure your desired keymap:

#### Option 1. Keymap Editor

1. Open [Keymap Editor](https://nickcoutsos.github.io/keymap-editor/).
2. Connect it to your Github account and give an access to your repository to Keymap Editor's app.
3. Make changes to your keymap and press `Save` - it will trigger software build. Wait for it to complete.
4. Grab the `firmware.zip` archive.

#### Option 2. Manual

1. Make changes to the [reviung41.keymap](config/reviung41.keymap) file using your favorite text editor.
2. Commit changes to your repository.
3. Go to `Actions` tab in your Github repository, locate the latest build and wait for it to complete.
4. Grab the `firmware.zip` archive

### How to flash the keyboard?

1. Obtain `firmware.zip`
2. Unzip `firmware.zip` - you should have `reviung41-nice_nano_v2-zmk.uf2` file
3. Connect your keyboard to the PC via USB-C cable
4. Press `RESET` button **twice** to enter DFU mode - you should see new USB device in your file manager
5. Copy the corresponding firmware to the root directory of the new USB device
6. Disconnect keyboard from the PC


### Problems

#### I'm getting File Transfer Error after copying firmware to the keyboard

It's OK. Proof: https://zmk.dev/docs/troubleshooting#file-transfer-error
