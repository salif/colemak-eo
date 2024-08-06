# Instalando no Linux

Tradução: [english](LINUX.md), [esperanto](LINUX.eo.md), [中文](LINUX.zh-CN.md), [español](LINUX.es.md), [العربية](LINUX.ar.md), [русский](LINUX.ru.md), [bahasa](LINUX.id.md), [türkçe](LINUX.tr.md), [български](LINUX.bg.md)

---

Não sou especialista em instalação de layouts de teclado; essas instruções podem não funcionar para todos os usuários do Linux.

## Siga estas instruções

**1.** Primeiro, faça backup de alguns arquivos executando estes comandos:

```bash
cp /usr/share/X11/xkb/symbols/epo /usr/share/X11/xkb/symbols/epo.old
cp /usr/share/X11/xkb/rules/evdev.xml /usr/share/X11/xkb/rules/evdev.xml.old
```

Se você receber um erro, primeiro execute este comando: `su root`, tente executar os comandos novamente ou substitua `cp` por `sudo cp`.

**2.** Abrir arquivo `/usr/share/X11/xkb/symbols/epo` e anexe o seguinte bloco de texto no final do arquivo:

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

**3.** Abrir arquivo `/usr/share/X11/xkb/rules/evdev.xml` e insira o seguinte bloco de texto após a variante `Esperanto (legacy)`:

```xml
<variant>
  <configItem>
    <name>colemak_eo</name>
    <description>Esperanto (Colemak)</description>
  </configItem>
</variant>
```

**4.** Em seguida, adicione `Esperanto (Colemak)` através das configurações do seu ambiente de trabalho.

## Desinstalando

Para desinstalar, restaure os arquivos antigos ou desfaça tudo o que você fez:

```bash
mv /usr/share/X11/xkb/symbols/epo.old /usr/share/X11/xkb/symbols/epo
mv /usr/share/X11/xkb/rules/evdev.xml.old /usr/share/X11/xkb/rules/evdev.xml
```

## Atualizando

Desinstale a versão antiga e instale a nova versão.

---

Esta página contém texto traduzido automaticamente

---

[← Voltar](./README.pt.md)
