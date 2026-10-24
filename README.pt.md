# Vim Cheatsheet · Cola de referência de comandos Vim

> 🌍 [中文](README.md) · [Español](README.es.md)

Uma **cola de uma página só** com 30 usos reais do Vim: sair e salvar, mover-se rápido, operadores com objetos de texto, buscar e substituir, modo visual, e macros com registradores. Cada entrada responde a apenas três perguntas: **o que ela faz, teclas prontas para copiar e colar, e etiquetas de uso**. Sem comandos inventados: quase todas as entradas foram executadas sem interface no Vim 9.1 local (vim-tiny) e o arquivo resultante foi conferido; as poucas que uma compilação tiny não executa (área de transferência do sistema, `:nohlsearch`, desfazer persistente, salvamento com sudo) foram verificadas contra as opções de compilação e o comportamento documentado do Vim, e isso fica indicado na própria entrada.

## Para quem é

Para quem acabou de travar no «como é que eu saio do Vim?» e para quem há anos usa só `i` e `:wq`. Se buscar e substituir, o modo visual em bloco ou as macros te fazem pesquisar toda vez, esta cola resolve isso de uma vez.

## Como usar

1. Vá direto ao **[CHEATSHEET.md](CHEATSHEET.md)**: o corpo da referência; as explicações em inglês qualquer desenvolvedor entende.
2. Você precisa do Vim: já vem no Linux e no macOS; no Windows, use WSL ou gVim. Para praticar, qualquer arquivo de texto serve.
3. Siga a ordem da cola —sair/salvar → mover → editar → buscar e substituir → visual → macros— e teste cada entrada na mão. Em uma hora você domina tudo.

## Teste em 30 segundos

```bash
vim --version | head -1            # imprime a versão (ex.: VIM - Vi IMproved 9.1): o Vim está lá
vim --version | grep clipboard     # só com +clipboard há área de transferência do sistema ("+y)
vimtutor                           # o tutorial interativo oficial de 30 minutos
```

## Um ~/.vimrc pronto para usar

```vim
set number relativenumber   " números de linha: absoluto na atual, relativos ao redor
set expandtab shiftwidth=2  " Tab vira espaços, um nível de recuo = 2
set ignorecase smartcase    " busca ignora maiúsculas, a menos que você digite uma
set undofile                " histórico de desfazer em arquivo: sobrevive a fechar o Vim
```

Salve em `~/.vimrc` e reabra o Vim: números de linha, recuo e busca ficam do seu jeito de uma vez.

## O que está incluído

| Categoria | Conteúdo |
|---|---|
| 🚪 Sair e salvar | :w/:q/:wq e ZZ / :q! e ZQ / diferença entre :x e :wq / salvar com sudo / abrir numa linha ou busca (5) |
| 🧭 Movimento | hjkl e w b e (e W B E) / 0 ^ $ e gg G / f F t T com ; , / % e { } / Ctrl-d/u/f/b e H M L / gj gk por linha de exibição (6) |
| ✏️ Edição | i a I A o O / x dd yy p P com contagens / u Ctrl-r e . / operador + movimento / objetos de texto / r ~ e recuo / J e :m (7) |
| 🔍 Buscar e substituir | / ? n N e * # / :s com flags g c / :%s e intervalos / ajustes de busca e :noh / :g e :v (5) |
| 👁 Modo visual | v V Ctrl-v, os três modos / inserção em bloco e no fim do bloco / gv e o (3) |
| 🎙 Macros e mais | gravar e reproduzir macros (exemplo completo) / registradores e área de transferência / :! e :r ! / ajustes de sobrevivência no ~/.vimrc (4) |

A documentação oficial é só https://www.vim.org/docs.php; cada comando foi verificado contra o Vim 9.1: tudo o que o vim-tiny local consegue executar foi testado sem interface, e o que depende de opções de compilação ausentes (+clipboard, +persistent_undo, +extra_search) está indicado como tal no texto.

## Contribuições são bem-vindas

Achou um comando errado, uma explicação desatualizada ou uma tradução a melhorar? *Pull requests* são bem-vindos. Mantenha o formato (descrição / bloco de código / etiquetas) e **só comandos reais e verificados; na dúvida, melhor não incluir**.

## 📚 Mais folhas de referência

Outras colas do mesmo autor, também em 中文 / Español / Português:

- [FFmpeg 命令速查表](https://github.com/Ezra-Zhao/ffmpeg-cheatsheet) — 28 comandos de áudio e vídeo
- [Git 实战速查表](https://github.com/Ezra-Zhao/git-cheatsheet) — 30 comandos do dia a dia e de resgate
- [Docker 命令速查表](https://github.com/Ezra-Zhao/docker-cheatsheet) — 28 comandos de contêineres
- [curl 命令速查表](https://github.com/Ezra-Zhao/curl-cheatsheet) — 29 comandos para depurar APIs
- [正则表达式速查表](https://github.com/Ezra-Zhao/regex-cheatsheet) — 30 padrões práticos de expressões regulares
- [jq 命令速查表](https://github.com/Ezra-Zhao/jq-cheatsheet) — 30 filtros para JSON
- [终端神器速查表](https://github.com/Ezra-Zhao/terminal-superpowers-cheatsheet) — 14 ferramentas de eficiência para o terminal
- [Adobe 免费替代速查表](https://github.com/Ezra-Zhao/adobe-free-alternatives-cheatsheet) — 16 alternativas gratuitas ao Adobe
- [退订省钱速查表](https://github.com/Ezra-Zhao/desubscribe-cheatsheet) — 10 trocas de assinaturas, ≈ $1,260/ano de economia
- [kubectl 命令速查表](https://github.com/Ezra-Zhao/kubectl-cheatsheet) — comandos habituais de Kubernetes
- [SQL 查询速查表](https://github.com/Ezra-Zhao/sql-cheatsheet) — consultas e funções SQL habituais
- [SSH 命令速查表](https://github.com/Ezra-Zhao/ssh-cheatsheet) — 28 comandos de conexão, chaves e túneis SSH

## Licença

MIT © 2026 Guangyi Zhao. Veja [LICENSE](LICENSE).
