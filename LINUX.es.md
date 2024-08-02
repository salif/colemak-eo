# Instalación en Linux

Traducción: [english](LINUX.md), [esperanto](LINUX.eo.md), [中文](LINUX.zh-CN.md), [العربية](LINUX.ar.md), [português](LINUX.pt.md), [русский](LINUX.ru.md), [bahasa](LINUX.id.md), [türkçe](LINUX.tr.md), [български](LINUX.bg.md)

---

No soy un experto en instalar distribuciones de teclado; es posible que estas instrucciones no funcionen para todos los usuarios de Linux.

## Siga estas instrucciones

**1.** Primero, haga una copia de seguridad de algunos archivos ejecutando estos comandos:

```bash
cp /usr/share/X11/xkb/symbols/epo /usr/share/X11/xkb/symbols/epo.old
cp /usr/share/X11/xkb/rules/evdev.xml /usr/share/X11/xkb/rules/evdev.xml.old
```

Si recibe un error, primero ejecute este comando: `su -l root`, luego intente ejecutar los comandos nuevamente o reemplace `cp` con `sudo cp`.

**2.** Abrir documento `/usr/share/X11/xkb/symbols/epo` y agregue el siguiente bloque de texto al final del archivo:

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

**3.** Abrir documento `/usr/share/X11/xkb/rules/evdev.xml` e inserte el siguiente bloque de texto después de la variante `Esperanto (legacy)`:

```xml
<variant>
  <configItem>
    <name>colemak_eo</name>
    <description>Esperanto (Colemak)</description>
  </configItem>
</variant>
```

**4.** Luego añade `Esperanto (Colemak)` a través de la configuración de su entorno de escritorio.

## Desinstalando

Para desinstalar, restaurar los archivos antiguos o deshacer todo lo que hiciste:

```bash
mv /usr/share/X11/xkb/symbols/epo.old /usr/share/X11/xkb/symbols/epo
mv /usr/share/X11/xkb/rules/evdev.xml.old /usr/share/X11/xkb/rules/evdev.xml
```

## Actualización

Desinstale la versión anterior e instale la nueva versión.

---

Esta página contiene texto traducido automáticamente

---

[← Volver](./README.es.md)
