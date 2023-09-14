# „:Install on Linux“

„:---“

---

„:First, backup some files. Run these commands“:

```shell
cp /usr/share/X11/xkb/symbols/epo /usr/share/X11/xkb/symbols/epo.old
cp /usr/share/X11/xkb/rules/evdev.xml /usr/share/X11/xkb/rules/evdev.xml.old
```

„:Open file“ `/usr/share/X11/xkb/symbols/epo` „:and append the following text block at the end of the file“

```
// github.com/salif/colemak-eo
partial alphanumeric_keys
xkb_symbols "colemak_eo" {

  include "us(colemak)"

  name[Group1]= "Esperanto (Colemak)";

  key <AD01> {[ jcircumflex, Jcircumflex, q,            Q          ]};
  key <AD02> {[ scircumflex, Scircumflex, w,            W          ]};
  key <AD09> {[ ubreve,      Ubreve,      y,            Y          ]};
  key <AD11> {[ gcircumflex, Gcircumflex, bracketleft,  braceleft  ]};
  key <AD12> {[ hcircumflex, Hcircumflex, bracketright, braceright ]};
  key <AB02> {[ ccircumflex, Ccircumflex, x,            X          ]};

  include "level3(ralt_switch)"
};
```

„:Open file“ `/usr/share/X11/xkb/rules/evdev.xml` „:and insert the following text block after the“ `Esperanto (legacy)` variant.

```xml
<variant>
  <configItem>
    <name>colemak_eo</name>
    <description>Esperanto (Colemak)</description>
  </configItem>
</variant>
```

„:Then add“ `Esperanto (Colemak)` „:via the settings of your desktop environment“.

## „:Uninstalling“

„:To uninstall undo everything you did or restore the old files“:

```
mv /usr/share/X11/xkb/symbols/epo.old /usr/share/X11/xkb/symbols/epo
mv /usr/share/X11/xkb/rules/evdev.xml.old /usr/share/X11/xkb/rules/evdev.xml
```

## „:Updating“

„:Uninstall the old version and install the new version“.

---

„:This page contains automatically translated text“

---

[„:← Back“](./README„:--“)
