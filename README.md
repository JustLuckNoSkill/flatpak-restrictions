# flatpak-restrictions

Restrictive flatpak permission for better security. Override files are located in `~/.local/share/flatpak/overrides`. These overrides work well for me. If you want to use them on your system, you may need to change them to fit your needs.

# Windowing Systems

These overrides assume you are using Wayland. If you are using X11, **do not** revoke `share=ipc`, `socket=x11`, or `socket=fallback-x11`.
Removing these permissions from apps while using X11 will prevent them from starting. 

If you want to use a Chromium-based browser with Wayland, type `chrome://flags` in the URL bar and search for `#ozone-platform-hint`. Set this to `Wayland` and restart the browser. X11-related permissions can be revoked from the browser after this.

# Filesystem Access

Giving applications access to all of your files introduces unnecessary risk. This can be mitigated by giving applications access only to files they need. For example, rather than giving `org.gnome.eog` access to `host`, you can give it access only to directories where you keep images (i.e. `xdg-download` or `xdg-pictures`).

# Network Access

Revoking an application's network access can greatly improve privacy; there is no possibility of an application transmitting data if it cannot access the internet. However, denying network access can severely reduce functionality. For example, you cannot use `org.gnome.Calculator` to calculate exchange rates if it has no network access. You should still revoke network access when you can, but doing so for all apps probably isn't practical.

# Suggestions

If there is an application you want to be added here, submit an issue or pull request and I'll get to it as soon as I can.
