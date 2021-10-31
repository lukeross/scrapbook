# Disabling rounded screen corners on Android

- Ensure developer mode, USB development is active.

- Plug in to PC

- On the PC run:

  ```sh
  adb shell settings put secure sysui_rounded_size 1
  adb shell settings put secure sysui_rounded_content_padding 5
  ```

## To Reset

- Run:

  ```sh
  adb shell settings delete secure sysui_rounded_size
  adb shell settings delete secure sysui_rounded_content_padding
  ```
