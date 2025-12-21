## Introdução

O diretório _"Templates"_ (ou "Modelos" em português) no Linux é um diretório especial localizado no diretório pessoal do usuário (geralmente em `~/Templates`) que serve como um repositório para arquivos modelo.

Esses modelos funcionam como "esqueletos" de documentos, permitindo a criação rápida de novos arquivos com configurações pré-definidas, como margens, fontes, fórmulas ou layouts, sem a necessidade de configurar tudo manualmente cada vez.

A pasta é reconhecida pelo ambiente gráfico _GNOME_, especialmente pelo gerenciador de arquivos _Nautilus_, e seus arquivos aparecem automaticamente no menu de contexto (botão direito do mouse) ao selecionar a opção "Criar Novo Documento".

## Usabilidade

- O diretório "Templates" é parte do padrão de hierarquia de arquivos do sistema (FHS - Filesystem Hierarchy Standard), que define a estrutura organizacional dos arquivos no Linux.

- Ele é especialmente útil para agilizar a criação de documentos com o LibreOffice (Writer, Calc, Impress), onde modelos de planilhas, relatórios ou apresentações podem ser salvos e reutilizados com um único clique.

- Para que a pasta funcione corretamente, é necessário que o caminho seja definido no arquivo de configuração do usuário (`~/.config/user-dirs.dirs`), com a variável `XDG_TEMPLATES_DIR` apontando para `$HOME/Modelos`.

- Além de documentos do LibreOffice, é possível salvar modelos de arquivos de texto, scripts em Python ou Bash, arquivos HTML, ou até arquivos vazios, organizando-os em subpastas para facilitar a gestão.

- A pasta é case-sensitive, o que significa que "Templates" e "templates" são considerados diretórios diferentes.

<img src="../../assets/menu-contexto.png" alt="Imagem de referência" data-align="center">

> Imagem de referência de como fica o menu após criar os arquivos.
