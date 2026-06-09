How do I generate the firmware?

The easiest way is to use GitHub Actions. You don't need to install the ZMK toolchain locally. ZMK's recommended workflow is:

Create/fork a zmk-config repository on GitHub.
Put your lily58.keymap (and optionally lily58.conf) into the config/ folder.
Ensure build.yaml contains both halves of your keyboard.
Commit and push.
GitHub automatically builds the firmware and produces .uf2 files you can flash.

For a Lily58 Wireless with nRF52840 controllers, your build.yaml will look something like:

include:
  - board: nice_nano
    shield: lily58_left
  - board: nice_nano
    shield: lily58_right

(or possibly nice_nano@2.0.0 depending on the template/version you're using).

After you push:

1. Open your GitHub repository.
2. Click Actions.
3. Wait for the build to finish.
4. Download the firmware artifact ZIP.
5. Extract it.
6. Flash the generated lily58_left.uf2 and lily58_right.uf2 files to the appropriate halves.

If you already have a .keymap file and nothing else, send me:

your GitHub repository URL (or a screenshot of its files),
the controller you're using (nice!nano v2 or the Pro Micro nRF52840 clone),

Create your own custom keymap here https://nickcoutsos.github.io/keymap-editor/
And create your kemap image here https://keymap-drawer.streamlit.app/

<img width="984" height="1173" alt="my_keymap060826" src="https://github.com/user-attachments/assets/22001dee-1321-46b3-ac27-1ebf12ee9320" />
