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

## 📂 Estrutura de Pastas do Repositório (Umbrel Community App Store)

```text
OPL-Server-4UmbrelOS/
├── README.md                # Documentação e instruções do projeto (fica na raiz)
└── ps2-opl/                 # Pasta do App para a Loja do Umbrel OS 2.0
    ├── umbrel-app.yml       # Manifesto de aplicativo para a loja do Umbrel
    ├── docker-compose.yml   # Orquestração dos containers (Samba SMBv1 + Gerenciador Web)
    └── smb.conf             # Configuração otimizada para o PS2 OPL
