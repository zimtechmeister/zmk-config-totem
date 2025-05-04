# TODO:
- [ ] In vim when "d ^G" it will type "de" because there needs to be some delay before hold behavior can trigger
- [ ] Add some option to hold down the tap key from homerow-mod like in qmk i could tap and hold the key and it would send hold down the tap key
- [ ] you should copy from this [repo](https://github.com/urob/zmk-config)
- [ ] read [this](https://zmk.dev/docs/keymaps/behaviors/hold-tap?examples=home_row_mods)
---

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="/docs/images/TOTEM_logo_dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="/docs/images/TOTEM_logo_bright.svg">
  <img alt="TOTEM logo font" src="/docs/images/TOTEM_logo_bright.svg">
</picture>

# ZMK CONFIG FOR THE TOTEM SPLIT KEYBOARD

[Here](https://github.com/GEIGEIGEIST/totem) you can find the hardware files and build guide.\
[Here](https://github.com/GEIGEIGEIST/qmk-config-totem) you can find the QMK config for the TOTEM.

TOTEM is a 38 key column-staggered split keyboard running [ZMK](https://zmk.dev/) or [QMK](https://docs.qmk.fm/). It's meant to be used with a SEEED XIAO BLE or RP2040.


![TOTEM layout](/docs/images/TOTEM_layout.svg)



## HOW TO USE

- fork this repo
- `git clone` your repo, to create a local copy on your PC (you can use the [command line](https://www.atlassian.com/git/tutorials) or [github desktop](https://desktop.github.com/))
- adjust the totem.keymap file (find all the keycodes on [the zmk docs pages](https://zmk.dev/docs/codes/))
- `git push` your repo to your fork
- on the GitHub page of your fork navigate to "Actions"
- scroll down and unzip the `firmware.zip` archive that contains the latest firmware
- connect the left half of the TOTEM to your PC, press reset twice
- the keyboard should now appear as a mass storage device
- drag'n'drop the `totem_left-seeeduino_xiao_ble-zmk.uf2` file from the archive onto the storage device
- repeat this process with the right half and the `totem_right-seeeduino_xiao_ble-zmk.uf2` file.

---

## TOTEM

- [TOTEM](https://github.com/eigatech/zmk-config/tree/totem)
- [TOTEM Dongle](https://github.com/eigatech/zmk-config/tree/totem-dongle)
- [TOTEM Prospector](https://github.com/eigatech/zmk-config/tree/totem-prospector)

## Dongle Flashing

Dongle configs use Seeed Xiao Ble microcontrollers housed in a nifty 3D printed [case](https://www.printables.com/model/522586-seeed-xiao-ble-case).

1. Turn all controllers off
2. Flash the dongle controller with the **appropriate** `settings_reset` file.
3. Flash the dongle controller with the `dongle` file.
4. Flash the first half with the the `settings_reset` file.
5. Flash the first half with the `left` or `right` files.
6. Repeat steps 4 and 5 for the other half.

> [!WARNING]  
> When using both Nice!Nano and Seeed XIAO microcontrollers, make sure you are flashing them with the correct files!

## ZMK Keymap Editor

Nick Coutsos' [Keymap Editor](https://nickcoutsos.github.io/keymap-editor/) is a user-friendly, browser-based WYSIWYG app designed to make editing your keymap file easier. It supports conditional layers, behaviors, combo and macro editing, rotary encoders, and more.

## Shops and other useful links

Kits, Prebuilts, Parts:
- [kbd.news](https://kbd.news/vendors) - mechanical keyboard vendors list
- [42keebs.eu](http://42keebs.eu/) - diy kits, including Corne, switches and other parts
- [keeb.supply](https://keeb.supply/) - diy kits and prebuilts, including TOTEM, tools and other parts
- [splitkb.com](https://splitkb.com/) - diy kits, including Corne, switches, tools and other parts
- [bastardkb.com](https://bastardkb.com/) - diy kits and prebuilts, including Charybdis (wired only w/ qmk)
- [typeractive.xyz](https://typeractive.xyz/) - diy kits and prebuilts, including Corne w/ nice!views, switches, tools and other parts

Documentation and guides:
- [ZMK Firmware Documentation](https://zmk.dev/docs)
- [Eren's Wireless Charybdis Mini Guide](https://github.com/erenatas/charybdis-wireless-3x6)
