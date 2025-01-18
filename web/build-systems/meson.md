# Meson

Test for mingw-w64:

```meson
# meson.build
cc = meson.get_compiler('c')
is_windows = host_machine.system() == 'windows'
is_mingw = is_windows and cc.get_define('__MINGW32__') != ''
```
