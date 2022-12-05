# flatpak-restrictions
Flatpak permissions I use to improve security.

These overrides assume you are using Wayland. If you are using X11, **do not** revoke these permissions:
  share=ipc
  socket=x11
  socket=fallback-x11
Removing these permissions from apps while using X11 will prevent them from starting. 

These overrides work well for me. If you want to use them on your system, you may need to change them to fit your needs. 
