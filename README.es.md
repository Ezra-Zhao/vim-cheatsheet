# Vim Cheatsheet · Hoja de referencia de comandos Vim

> 🌍 [中文](README.md) · [Português](README.pt.md)

Una **hoja de referencia de una sola página** con 30 usos reales de Vim: salir y guardar, moverte rápido, operadores con objetos de texto, buscar y reemplazar, modo visual, y macros con registros. Cada entrada responde solo tres preguntas: **qué hace, unas teclas listas para copiar y pegar, y etiquetas de uso**. Sin comandos inventados: casi todas las entradas se ejecutaron sin interfaz en el Vim 9.1 local (vim-tiny) y se comprobó el archivo resultante; las pocas que una compilación tiny no puede ejecutar (portapapeles del sistema, `:nohlsearch`, deshacer persistente, guardado con sudo) están verificadas contra las opciones de compilación y el comportamiento documentado de Vim, y así se indica en la propia entrada.

## Para quién es

Para quien acaba de pelearse con «¿cómo salgo de Vim?» y para quien lleva años usando solo `i` y `:wq`. Si buscar y reemplazar, el modo visual por bloques o las macros te obligan a buscar cada vez, esta hoja te lo deja claro de una vez.

## Cómo usarla

1. Ve directo a **[CHEATSHEET.md](CHEATSHEET.md)**: el cuerpo de la referencia; las explicaciones en inglés las entiende cualquier desarrollador.
2. Necesitas Vim: incluido en Linux y macOS; en Windows, WSL o gVim. Para practicar basta cualquier archivo de texto.
3. Sigue el orden de la hoja —salir/guardar → moverse → editar → buscar y reemplazar → visual → macros— y prueba cada entrada a mano. En una hora las dominas.

## Pruébalo en 30 segundos

```bash
vim --version | head -1            # imprime la versión (p. ej. VIM - Vi IMproved 9.1): Vim está
vim --version | grep clipboard     # solo con +clipboard hay portapapeles del sistema ("+y)
vimtutor                           # el tutorial interactivo oficial de 30 minutos
```

## Un ~/.vimrc listo para usar

```vim
set number relativenumber   " números de línea: absoluto en la actual, relativos alrededor
set expandtab shiftwidth=2  " Tab inserta espacios, un nivel de sangría = 2
set ignorecase smartcase    " búsqueda sin distinción de mayúsculas, salvo que escribas una
set undofile                " historial de deshacer en archivo: sobrevive a cerrar Vim
```

Guárdalo en `~/.vimrc` y reabre Vim: números de línea, sangría y búsqueda quedan a tu manera de una vez.

## Qué incluye

| Categoría | Contenido |
|---|---|
| 🚪 Salir y guardar | :w/:q/:wq y ZZ / :q! y ZQ / diferencia entre :x y :wq / guardar con sudo / abrir en una línea o búsqueda (5) |
| 🧭 Movimiento | hjkl y w b e (y W B E) / 0 ^ $ y gg G / f F t T con ; , / % y { } / Ctrl-d/u/f/b y H M L / gj gk por línea visual (6) |
| ✏️ Edición | i a I A o O / x dd yy p P con conteos / u Ctrl-r y . / operador + movimiento / objetos de texto / r ~ y sangría / J y :m (7) |
| 🔍 Buscar y reemplazar | / ? n N y * # / :s con banderas g c / :%s y rangos / ajustes de búsqueda y :noh / :g y :v (5) |
| 👁 Modo visual | v V Ctrl-v, los tres modos / inserción en bloque y al final del bloque / gv y o (3) |
| 🎙 Macros y más | grabar y reproducir macros (ejemplo completo) / registros y portapapeles / :! y :r ! / ajustes de supervivencia en ~/.vimrc (4) |

La documentación oficial es solo https://www.vim.org/docs.php; cada comando está verificado contra Vim 9.1: todo lo que el vim-tiny local puede ejecutar se probó sin interfaz, y lo que depende de opciones de compilación ausentes (+clipboard, +persistent_undo, +extra_search) se indica tal cual en el texto.

## Contribuciones bienvenidas

¿Un comando incorrecto, una explicación desactualizada o una traducción mejorable? Los *pull requests* son bienvenidos. Mantén el formato (descripción / bloque de código / etiquetas) y **solo comandos reales y verificados; ante la duda, mejor no incluirlo**.

## 📚 Más hojas de referencia

Otras hojas del mismo autor, también en 中文 / Español / Português:

- [FFmpeg 命令速查表](https://github.com/Ezra-Zhao/ffmpeg-cheatsheet) — 28 comandos de audio y vídeo
- [Git 实战速查表](https://github.com/Ezra-Zhao/git-cheatsheet) — 30 comandos diarios y de rescate
- [Docker 命令速查表](https://github.com/Ezra-Zhao/docker-cheatsheet) — 28 comandos de contenedores
- [curl 命令速查表](https://github.com/Ezra-Zhao/curl-cheatsheet) — 29 comandos para depurar APIs
- [正则表达式速查表](https://github.com/Ezra-Zhao/regex-cheatsheet) — 30 patrones prácticos de expresiones regulares
- [jq 命令速查表](https://github.com/Ezra-Zhao/jq-cheatsheet) — 30 filtros para JSON
- [终端神器速查表](https://github.com/Ezra-Zhao/terminal-superpowers-cheatsheet) — 14 herramientas de eficiencia para la terminal
- [Adobe 免费替代速查表](https://github.com/Ezra-Zhao/adobe-free-alternatives-cheatsheet) — 16 alternativas gratuitas a Adobe
- [退订省钱速查表](https://github.com/Ezra-Zhao/desubscribe-cheatsheet) — 10 sustituciones de suscripciones, ≈ $1,260/año de ahorro
- [kubectl 命令速查表](https://github.com/Ezra-Zhao/kubectl-cheatsheet) — comandos habituales de Kubernetes
- [SQL 查询速查表](https://github.com/Ezra-Zhao/sql-cheatsheet) — consultas y funciones SQL habituales
- [SSH 命令速查表](https://github.com/Ezra-Zhao/ssh-cheatsheet) — 28 comandos de conexión, claves y túneles SSH

## Licencia

MIT © 2026 Guangyi Zhao. Ver [LICENSE](LICENSE).
