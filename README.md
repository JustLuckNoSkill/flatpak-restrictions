# flatpak-restrictions

Flatpak permissions I use to improve security. Override files are located in `~/.local/share/flatpak/overrides`.

These overrides assume you are using Wayland. If you are using X11, **do not** revoke `share=ipc`, `socket=x11`, or `socket=fallback-x11`.
Removing these permissions from apps while using X11 will prevent them from starting. 

If you want to use a Chromium-based browser with Wayland, type `chrome://flags` in the URL bar and search for `#ozone-platform-hint`. Set this to `Wayland` and restart the browser. X11-related permissions can be revoked from the browser after this.

These overrides work well for me. If you want to use them on your system, you may need to change them to fit your needs.
