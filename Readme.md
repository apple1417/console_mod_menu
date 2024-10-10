# Console Mod Menu
A console-based mod menu for [pyunrealsdk](https://github.com/bl-sdk/pyunrealsdk/) following the
[mods_base](https://github.com/bl-sdk/mods_base/) layout.

Should be entirely game agnostic, so useful during development before having made a proper,
gui-based mod menu.

### Optional Extra Modules
If some extra modules are available, the menu enables a few extra features. These are optional, the
menu will gracefully degrade if they are not available.

If the `keybinds.raw_keybinds` module is present, allows binding a key from a raw key press. See
the implementation in
[oak-mod-manager](https://github.com/bl-sdk/oak-mod-manager/blob/master/src/keybinds/raw_keybinds.py)
for what interface this is expected to have.

If the function `ui_utils.show_hud_message` is present, it is used to notify when a key has been
bound from one of the raw presses from above. This function should take a title as the first arg and
a message as the second (both positionally), and show them in a temporary message on screen.
