# OPL-Server-4UmbrelOS 🎮

> ** Aviso:** Este projeto foi totalmente **VIBECODADO** por alguém que não sabe nada de programação! 

##  Objetivo do Projeto
A minha intenção com este projeto é criar uma ferramenta semelhante ao **OPL Server do El Mariolo**, mas adaptada para rodar dentro do **UmbrelOS**. A ideia é facilitar a vida de quem tem um homelab ou servidor caseiro e quer hospedar e gerenciar suas ISOs de forma prática.

---

##  Aviso Importante de Segurança
O PlayStation 2 e o Open PS2 Loader (OPL) utilizam o protocolo legado **SMBv1 (dialeto NT1)** com autenticação **NTLMv1**. Esse protocolo é antigo e possui vulnerabilidades conhecidas em redes públicas.  
- **NUNCA** faça redirecionamento de portas (port forwarding) das portas `1024`, `445` ou `139` para a internet pública!  
- Utilize **estritamente em sua rede local (LAN)** doméstica e confiável.  
- Este container foi configurado na porta **`1024`** para não conflitar com as portas nativas do Umbrel OS e permitir conexão direta sem complicações.

---

## 📂 Estrutura de Pastas do Projeto

```text
OPL-Server-4UmbrelOS/
├── docker-compose.yml       # Orquestração dos containers (Samba SMBv1 + Gerenciador Web)
├── smb.conf                 # Configuração otimizada para o PS2 OPL
├── README.md                # Instruções e documentação
└── data/
    └── PS2SMB/
        ├── DVD/             # Jogos em formato DVD (acima de 700 MB)
        ├── CD/              # Jogos em formato CD (até 700 MB)
        ├── ART/             # Capas e artes de jogos (_COV.jpg, etc)
        ├── CFG/             # Arquivos de configurações (.cfg)
        ├── VMC/             # Memory Cards Virtuais (.bin)
        ├── THM/             # Temas do menu do OPL
        ├── APPS/            # Aplicativos e emuladores ELF
        └── POPS/            # Jogos de PS1 (POPStarter)
