# 𐑦𐑵𐑕𐑑𐑨𐑤𐑦 𐑧𐑵 𐑤𐑦𐑵𐑪𐑒𐑕𐑩

𐑧𐑵 𐑨𐑤𐑦𐑨𐑢 𐑤𐑦𐑵𐑜𐑝𐑩𐑢: [English](LINUX.md), [Esperanto](LINUX.eo.md), [Есперанто](LINUX.eo-cyrl.md), [𐑧𐑕𐑐𐑧𐑮𐑨𐑵𐑑𐑩](LINUX.eo-shaw.md)

---

𐑫𐑨𐑤𐑓𐑧𐑮𐑫𐑪 `/usr/share/X11/xkb/symbols/epo` 𐑒𐑨𐑢 𐑨𐑤𐑛𐑩𐑵𐑪 𐑤𐑨 𐑕𐑧𐑒𐑝𐑨𐑵 𐑑𐑧𐑒𐑕𐑑𐑩𐑚𐑤𐑩𐑒𐑩𐑵 𐑨𐑤 𐑤𐑨 𐑓𐑦𐑵𐑩 𐑛𐑧 𐑤𐑨 𐑛𐑩𐑕𐑦𐑧𐑮𐑩

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

𐑫𐑨𐑤𐑓𐑧𐑮𐑫𐑪 `/usr/share/X11/xkb/rules/evdev.xml` 𐑒𐑨𐑢 𐑧𐑵𐑦𐑜𐑪 𐑤𐑨 𐑕𐑧𐑒𐑝𐑨𐑵 𐑑𐑧𐑒𐑕𐑑𐑩𐑚𐑤𐑩𐑒𐑩𐑵 𐑐𐑩𐑕𐑑 𐑤𐑨 𐑝𐑨𐑮𐑦𐑨𐑵𐑑𐑩 `Esperanto (legacy)`

```
<variant>
  <configItem>
    <name>colemak_eo</name>
    <description>Esperanto (Colemak)</description>
  </configItem>
</variant>
```

𐑐𐑩𐑕𐑑𐑧 𐑨𐑤𐑛𐑩𐑵𐑪 `Esperanto (Colemak)` 𐑐𐑧𐑮 𐑤𐑨 𐑨𐑜𐑩𐑮𐑛𐑩𐑢 𐑛𐑧 𐑝𐑦𐑨 𐑓𐑧𐑵𐑧𐑕𐑑𐑮𐑦𐑤𐑩 \(DE\)

𐑕𐑧 𐑫𐑨𐑤𐑕𐑪𐑒𐑔𐑧𐑕𐑧, 𐑕𐑧𐑵𐑛𐑪 𐑐𐑮𐑩𐑚𐑤𐑧𐑫𐑩𐑵 \(issue\) 𐑨𐑤 𐑗𐑦 𐑑𐑦𐑪 𐑜𐑦𐑑 𐑛𐑧𐑐𐑩𐑵𐑧𐑢𐑩 𐑗𐑧 [GitHub.com](https://github.com/salif/colemak-eo/issues/new/choose)

[𐑫𐑨𐑤𐑨𐑵𐑑𐑨𐑘𐑧𐑵](./README.eo-shaw.md)
