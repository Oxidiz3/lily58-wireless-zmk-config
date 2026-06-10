How do I generate the firmware?

The easiest way is to use GitHub Actions. You don't need to install the ZMK toolchain locally. ZMK's recommended workflow is:

Click into config/*.keymap. Paste your new keymap commit and push.

After you push:

1. Open your GitHub repository.
2. Click Actions.
3. Wait for the build to finish.
4. Download the firmware artifact ZIP.
5. Extract it.
6. Flash the generated lily58_left.uf2 and lily58_right.uf2 files to the appropriate halves. Do this by plugging the board into a usb and hitting the reset button twice. Then when the board shows up as a storage drive you can drag the correct uf2 file into the storage.

Create your own custom keymap here https://nickcoutsos.github.io/keymap-editor/
And create your kemap image here https://keymap-drawer.streamlit.app/

<img width="984" height="1173" alt="my_keymap" src="https://github.com/user-attachments/assets/372256a9-ab81-4ab7-8aba-f3469d97562e" />
