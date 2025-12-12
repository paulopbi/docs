## Introdução

As chaves `ssh` podem nos ajudar bastante a otimizar alguns processos repetitivos ao atualizar um repositório no Github, como ter que fazer autenticação toda vez que fizer um *_push* para o repositório.

`SSH Keys` (chaves SSH) são um par de chaves criptográficas usadas para autenticação segura em sistemas remotos, substituindo o uso de senhas. O par consiste em:

- **Chave Privada** (private key): Fica **APENAS** no seu computador. Nunca compartilhe!

- **Chave Pública** (public key): Pode ser compartilhada com qualquer serviço/servidor.

### Vantagens do SSH

- **Mais seguro:** É bem mais seguro que senhas, e ainda resiste a ataques brute-force.

- **Evita utilizar senha:** Com o `SSH` não há a necessidade de digitar a senha a cada conexão.

- Suporte a automação com scripts, CI/CD, deploys.

## Gerando a chave SSH

Primeiro temos que executar o `ssh-keygen` que é uma ferramente essencial para a criação e gerenciamento de chaves de autenticação SSH no linux.

```bash
# Gera um par de chaves RSA de 4096 bits (padrão atual)
ssh-keygen -t rsa -b 4096 -C "seu-email@exemplo.com"

# Ou para Ed25519 (mais moderno e seguro)
ssh-keygen -t ed25519 -C "seu-email@exemplo.com"
```

> [!WARNING]
> 
> Caso vá utilizar essa chave no github, é importante que seja um email cadastrado no github.

Após isso, serão criado alguns arquivos no diretório `~/.ssh/`, a estrutura criada será a seguinte:

```textile
~/.ssh/
├── id_rsa          # CHAVE PRIVADA (NUNCA COMPARTILHE!)
├── id_rsa.pub      # Chave pública (pode compartilhar)
└── known_hosts     # Servidores conhecidos
```

## Criando Agente SSH

Após os passos acima, é necessário criar o agente ssh.

```bash
eval "$(ssh-agent -s)"
```

Depois desses passos, a chave foi criada com sucesso. SSH Keys são uma habilidade **essencial** para qualquer desenvolvedor ou administrador de sistemas.
