
# 📱 Install PixelExperience on Xiaomi Mi A3 (`laurel_sprout`)

This guide walks you through the steps to flash PixelExperience on your Mi A3 device. It is adapted from the official [PixelExperience](https://wiki.pixelexperience.org/devices/laurel_sprout/install/) instructions.

---

## ⚠️ Warnings

- **Unlocking the bootloader will erase all data** – Back up your important files.
- Do **not skip** any steps. Follow everything carefully.
- You are responsible for any risk caused by improper flashing.

---

## ✅ Requirements

- A PC with **ADB and Fastboot** installed  
  👉 [ADB Setup Guide](https://developer.android.com/tools/adb)
- USB Debugging **enabled** on the device
- Boot into the **stock OS at least once** and test SMS, calls, VoLTE/VoWiFi
- Unlocked Bootloader

---

## 🔓 Unlock the Bootloader

> Only needs to be done once per device.

```bash
adb reboot bootloader
fastboot devices
fastboot oem unlock
````

* Confirm the unlock on the phone screen.
* Device will reboot and erase all data.
* Re-enable USB debugging afterward.

---

## 📦 Flash PixelExperience Recovery

1. Download the official **PixelExperience Recovery**:
   👉 [Download Recovery](https://download.pixelexperience.org/laurel_sprout/)

2. Boot into fastboot mode:

```bash
adb reboot bootloader
```

3. Flash the recovery:

```bash
fastboot flash boot <recovery_filename>.img
```

4. Boot into recovery:

```text
Power off → Hold Volume Up + Power → Release when "MI" logo appears
```

---

## 💽 Install PixelExperience ROM

1. Download the latest PixelExperience `.zip` file:
   👉 [Download ROM](https://download.pixelexperience.org/laurel_sprout/)

2. In Recovery:

   * Tap `Factory Reset` → `Format Data / Factory Reset` → Confirm

3. Go back to the main menu → `Apply Update` → `Apply from ADB`

4. On your PC:

```bash
adb sideload <rom_filename>.zip
```

> ⚠ If the transfer stops at 47% with an error like `adb: failed to read command`, don’t worry — that’s normal.

---

## 🔁 First Boot

* Once sideload completes:
  Tap back arrow → `Reboot System Now`
* First boot may take up to **15 minutes**
* Do not interrupt it!

---

## 💬 Help & Support

If you followed all steps and still face issues:

* Join the [PixelExperience Telegram Group](https://t.me/pixelexperience)
* Mention your device name: `laurel_sprout`

---

## 🙏 Credits

* [PixelExperience Project](https://pixelexperience.org)
* Device Maintainers
* AOSP / Android Open Source Community

---

> 📅 Last updated: 2024
>
> 📜 Licensed under [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/)


