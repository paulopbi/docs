## Introdução

**Os gerenciadores de pacotes no Linux são ferramentas de software que automatizam o processo de instalação, atualização, configuração e remoção de programas de computador de maneira consistente**, eles são essenciais em sistemas operacionais tipo _Unix_, como o _Linux_, que consistem de centenas ou milhares de pacotes distintos, facilitando a identificação, instalação e atualização do sistema. os pacotes contêm metadados, como o nome do software, descrição, número de versão, fornecedor, checksum e uma lista de dependências necessárias para o software funcionar corretamente.

**Os gerenciadores de pacotes funcionam por meio de repositórios, que são coleções de softwares e suas respectivas informações, como descrições, versões e dependências**, quando um usuário deseja instalar ou atualizar um software, o gerenciador consulta o repositório para verificar se há uma versão mais recente disponível e, se houver, baixa o software e suas dependências automaticamente, isso resolve o problema conhecido como "Inferno de dependências", garantindo que todos os pacotes necessários estejam presentes e compatíveis com o sistema.

Cada distribuição Linux tem seu gerenciador de pacotes padrão no _Debian_ o gerenciador de pacotes padrão é o _APT (Advanced Packaging Tool)_, mas nós não precisamos ficar presos a ele apenas, podemos instalar outros gerenciadores como o _Pacman_ que é padrão no _Arch Linux_.

## Pacman (Arch Linux)

O _Pacman_ é o gerenciador de pacotes padrão do _Arch Linux_, ele é escrito na linguagem _C_ e é bem rápido também contendo uma biblioteca gigante de repositórios.

### Comandos

```bash
# instalação
sudo pacman -S nome_do_pacote nome_do_outro_pacote

# Remove
sudo pacman -R nome_do_pacote
```

> [!NOTE]
> É importante lembrar do comando `sudo` ao utilizar os gerenciadores de pacote, você precisa ser um super usuário para instalar ou remover pacotes.
