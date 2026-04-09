# 📋 Documentação Técnica do Servidor — `ctlinux01`
> **Data de coleta:** 08 de abril de 2026 | **Sistema:** Ubuntu Server 24.04.4 LTS | **Ambiente:** Docker-CE

---

## 1️⃣ Informações Gerais do Servidor

| Categoria | Descrição | Configuração |
|-----------|-----------|--------------|
| 🖥️ Geral | Nome do Servidor (Hostname) | `ctlinux01` |
| 🖥️ Geral | Sistema Operacional | Ubuntu 24.04.4 LTS (Noble Numbat) |
| 🖥️ Geral | Codinome da Versão | noble |
| 🖥️ Geral | Família do SO | Debian/Ubuntu |
| 🖥️ Geral | Kernel (Núcleo do Sistema) | Linux 6.8.0-106-generic |
| 🖥️ Geral | Arquitetura | x86-64 (64 bits) |
| 🖥️ Geral | Tipo de Máquina | Máquina Virtual (vm) |
| 🖥️ Geral | Plataforma de Virtualização | Oracle VirtualBox |
| 🖥️ Geral | Fabricante do Hardware Virtual | innotek GmbH |
| 🖥️ Geral | Versão do Firmware | VirtualBox (01/12/2006) |
| 🖥️ Geral | ID da Máquina | `05c2865e767d44c4870777b482ba0652` |
| 🖥️ Geral | ID de Boot Atual | `de43dae62ccf4a8ca8562dab3be83563` |
| ⏱️ Geral | Tempo de Atividade (Uptime) | 50 minutos |
| 👤 Geral | Usuários Conectados | 2 usuários ativos |
| 📊 Geral | Carga do Sistema (Load Average) | 0.00 / 0.00 / 0.00 (1min / 5min / 15min) |

> **💬 Para o gestor:** Este servidor é uma máquina virtual rodando em VirtualBox, com o sistema Ubuntu Server 24.04 LTS — uma versão estável e com suporte de longo prazo (até 2029). No momento da coleta, o servidor estava ativo há apenas 50 minutos, com carga praticamente zero, ou seja, ocioso e sem sobrecarga.

---

## 2️⃣ Informações de Hardware do Servidor

### 💾 Memória RAM e Swap

| Categoria | Descrição | Configuração |
|-----------|-----------|--------------|
| 💾 Memória | Total de RAM | 3.915 MB (~4 GB) |
| 💾 Memória | RAM em Uso | 513 MB |
| 💾 Memória | RAM Livre | 3.026 MB |
| 💾 Memória | RAM Disponível (com cache) | 3.402 MB |
| 💾 Memória | Memória Compartilhada | 1 MB |
| 💾 Memória | Buffer/Cache | 593 MB |
| 🔄 Swap | Total de Swap | 3.914 MB (~4 GB) |
| 🔄 Swap | Swap em Uso | 0 MB |
| 🔄 Swap | Swap Livre | 3.914 MB |

### 💿 Discos e Armazenamento

| Categoria | Descrição | Configuração |
|-----------|-----------|--------------|
| 💿 Disco | Disco Principal | `sda` — 50 GB (HDD Virtual) |
| 💿 Disco | Partição de Boot | `sda2` — 2 GB montada em `/boot` |
| 💿 Disco | Partição Principal (LVM) | `sda3` — 48 GB |
| 💿 Disco | Volume Lógico (LVM) | `ubuntu--vg-ubuntu--lv` — 48 GB montado em `/` |
| 💿 Disco | Drive Óptico Virtual | `sr0` — 1.024 MB (rom) |

### 📁 Uso do Sistema de Arquivos

| Categoria | Descrição | Tamanho Total | Em Uso | Disponível | % Uso |
|-----------|-----------|--------------|--------|------------|-------|
| 📁 Filesystem | Raiz do Sistema `/` | 47 GB | 8,3 GB | 37 GB | 19% |
| 📁 Filesystem | Boot `/boot` | 2,0 GB | 198 MB | 1,6 GB | 11% |
| 📁 Filesystem | Memória Temporária `/run` | 392 MB | 1,2 MB | 391 MB | 1% |
| 📁 Filesystem | Memória Compartilhada `/dev/shm` | 2,0 GB | 0 | 2,0 GB | 0% |
| 📁 Filesystem | Temporário `/run/lock` | 5,0 MB | 0 | 5,0 MB | 0% |
| 📁 Filesystem | Usuário `/run/user/1000` | 392 MB | 12 KB | 392 MB | 1% |

> **💬 Para o gestor:** O servidor possui 4 GB de memória RAM, utilizando apenas 513 MB no momento — bem dentro do limite saudável. O disco principal tem 50 GB, com 37 GB ainda livres (uso de apenas 19%). Não há risco imediato de falta de espaço, mas recomenda-se monitoramento periódico, especialmente com o crescimento de dados gerados pelos containers Docker.

---

## 3️⃣ Informações de Rede do Servidor

### 🌐 Interfaces de Rede

| Categoria | Descrição | Configuração |
|-----------|-----------|--------------|
| 🌐 Rede | Interface de Loopback | `lo` — 127.0.0.1/8 (interna) |
| 🌐 Rede | Interface Principal | `enp0s3` — Status: **UP** |
| 🌐 Rede | Endereço IPv4 (Principal) | `10.24.82.217/24` |
| 🌐 Rede | Endereço IPv6 (Link) | `fe80::a00:27ff:fe6e:e113/64` |
| 🌐 Rede | Endereço MAC (enp0s3) | `08:00:27:6e:e1:13` (Intel Corporation) |
| 🌐 Rede | MTU (enp0s3) | 1500 bytes |
| 🐳 Docker | Interface Docker Bridge | `docker0` — Status: **UP** |
| 🐳 Docker | Endereço IPv4 (Docker) | `172.17.0.1/16` |
| 🐳 Docker | Endereço MAC (docker0) | `c2:4b:1e:7d:8e:0f` |
| 🐳 Docker | Interface Virtual Container | `vethe4a9069` — Status: **UP** |
| 🐳 Docker | MAC (Interface Virtual) | `32:45:af:c1:61:bf` |

### 🛣️ Roteamento

| Categoria | Descrição | Configuração |
|-----------|-----------|--------------|
| 🛣️ Roteamento | Gateway Padrão | `10.24.82.1` via `enp0s3` |
| 🛣️ Roteamento | Rede Local | `10.24.82.0/24` via `enp0s3` |
| 🛣️ Roteamento | Rede Docker | `172.17.0.0/16` via `docker0` |

### 🔍 DNS (Resolução de Nomes)

| Categoria | Descrição | Configuração |
|-----------|-----------|--------------|
| 🔍 DNS | Servidor DNS Primário | `8.8.8.8` (Google) |
| 🔍 DNS | Servidor DNS Secundário | `8.8.4.4` (Google) |
| 🔍 DNS | Modo resolv.conf | stub |
| 🔍 DNS | DNSSEC | Não suportado |
| 🔍 DNS | LLMNR | Desativado |
| 🔍 DNS | mDNS | Desativado |

### 📡 Conectividade (Teste de Ping)

| Categoria | Descrição | Resultado |
|-----------|-----------|-----------|
| 📡 Conectividade | Ping para `8.8.8.8` (Google DNS) | ✅ 5/5 pacotes recebidos — 0% de perda |
| 📡 Conectividade | Latência média para `8.8.8.8` | 6,03 ms |
| 📡 Conectividade | Ping para `google.com.br` | ✅ 5/5 pacotes recebidos — 0% de perda |
| 📡 Conectividade | Latência média para `google.com.br` | 19,01 ms |

### 🔌 Portas em Escuta (Serviços Ativos na Rede)

| Categoria | Porta | Protocolo | Descrição |
|-----------|-------|-----------|-----------|
| 🔌 Portas | `22` | TCP | SSH — Acesso remoto seguro ao servidor |
| 🔌 Portas | `53` | TCP/UDP | DNS local (127.0.0.53 e 127.0.0.54) |
| 🔌 Portas | `9000` | TCP | Portainer — Painel de gerenciamento Docker |

> **💬 Para o gestor:** O servidor está conectado à rede com endereço IP `10.24.82.217` e com acesso pleno à internet (0% de perda nos testes). Ele possui uma rede interna exclusiva para os containers Docker (`172.17.0.0/16`), que é isolada da rede principal. Estão abertas apenas 3 portas de comunicação: acesso remoto seguro (SSH na porta 22), resolução de nomes interna (DNS na porta 53) e o painel de gerenciamento visual dos containers (Portainer na porta 9000).

---

## 4️⃣ Informações de Serviços e Processos

| Categoria | Serviço | Descrição | Status |
|-----------|---------|-----------|--------|
| 🐳 Docker | `docker.service` | Motor principal do Docker (Container Engine) | ✅ Ativo |
| 🐳 Docker | `containerd.service` | Runtime de containers (base do Docker) | ✅ Ativo |
| 🐳 Docker | `portainer.service` | Painel web de gerenciamento de containers | ✅ Ativo |
| 🔐 Segurança | `ssh.service` | Servidor SSH para acesso remoto seguro | ✅ Ativo |
| 🔐 Segurança | `polkit.service` | Gerenciador de permissões e autorizações | ✅ Ativo |
| 🌐 Rede | `systemd-networkd.service` | Gerenciamento de configurações de rede | ✅ Ativo |
| 🌐 Rede | `systemd-resolved.service` | Resolução de nomes DNS | ✅ Ativo |
| ⏱️ Sistema | `systemd-timesyncd.service` | Sincronização de data e hora pela rede (NTP) | ✅ Ativo |
| 📋 Sistema | `systemd-journald.service` | Coleta e armazenamento de logs do sistema | ✅ Ativo |
| 📋 Sistema | `rsyslog.service` | Serviço de registro de logs do sistema | ✅ Ativo |
| 👤 Sistema | `systemd-logind.service` | Gerenciamento de login de usuários | ✅ Ativo |
| ⚙️ Sistema | `systemd-udevd.service` | Gerenciamento de dispositivos de hardware | ✅ Ativo |
| 🖥️ Sistema | `getty@tty1.service` | Terminal de login no console local | ✅ Ativo |
| 🖥️ Sistema | `user@1000.service` | Sessão ativa do usuário (UID 1000) | ✅ Ativo |
| 💾 Sistema | `udisks2.service` | Gerenciador de discos e volumes | ✅ Ativo |
| 💾 Sistema | `multipathd.service` | Controlador de caminhos múltiplos de disco | ✅ Ativo |
| 🔧 Sistema | `dbus.service` | Barramento de mensagens entre processos | ✅ Ativo |
| 🔧 Sistema | `cron.service` | Agendador de tarefas automáticas | ✅ Ativo |
| 📡 Sistema | `ModemManager.service` | Gerenciador de modems de comunicação | ✅ Ativo |
| 🔋 Sistema | `upower.service` | Daemon de gerenciamento de energia | ✅ Ativo |
| 🔄 Atualização | `fwupd.service` | Serviço de atualização de firmware de hardware | ✅ Ativo |
| 🔄 Atualização | `unattended-upgrades.service` | Atualizações automáticas de segurança | ✅ Ativo |

> **💬 Para o gestor:** Todos os 22 serviços monitorados estão funcionando normalmente (status "Ativo"). Os mais importantes para o negócio são: o **Docker** (motor que executa os containers/aplicações), o **Portainer** (painel visual para gerenciar os containers sem precisar de linha de comando) e o **SSH** (permite que a equipe técnica acesse o servidor remotamente com segurança). O serviço de **atualizações automáticas** também está ativo, aplicando correções de segurança sem intervenção manual.

---

## 5️⃣ Informações de Softwares com Atualização Disponível

> ⚠️ **Atenção:** Os pacotes abaixo possuem versões mais recentes disponíveis e aguardam atualização.

### 🐳 Componentes Docker

| Categoria | Pacote | Versão Atual | Versão Disponível |
|-----------|--------|-------------|-------------------|
| 🐳 Docker | `docker-ce` | 5:29.2.1 | **5:29.4.0** |
| 🐳 Docker | `docker-ce-cli` | 5:29.2.1 | **5:29.4.0** |
| 🐳 Docker | `docker-ce-rootless-extras` | 5:29.2.1 | **5:29.4.0** |
| 🐳 Docker | `docker-buildx-plugin` | 0.31.1 | **0.33.0** |
| 🐳 Docker | `docker-compose-plugin` | 5.1.0 | **5.1.1** |
| 🐳 Docker | `containerd.io` | 2.2.1 | **2.2.2** |

### 🐧 Kernel e Sistema Operacional

| Categoria | Pacote | Versão Atual | Versão Disponível |
|-----------|--------|-------------|-------------------|
| 🐧 Kernel | `linux-generic` | 6.8.0-106.106 | **6.8.0-107.107** |
| 🐧 Kernel | `linux-image-generic` | 6.8.0-106.106 | **6.8.0-107.107** |
| 🐧 Kernel | `linux-headers-generic` | 6.8.0-106.106 | **6.8.0-107.107** |
| 🐧 Kernel | `linux-libc-dev` | 6.8.0-106.106 | **6.8.0-107.107** |
| 🐧 Kernel | `linux-tools-common` | 6.8.0-106.106 | **6.8.0-107.107** |
| 🐧 Kernel | `linux-base` | 4.5ubuntu9+24.04.1 | **4.5ubuntu9+24.04.2** |

### 🔐 Segurança e Criptografia

| Categoria | Pacote | Versão Atual | Versão Disponível |
|-----------|--------|-------------|-------------------|
| 🔐 Segurança | `openssl` | 3.0.13-0ubuntu3.7 | **3.0.13-0ubuntu3.9** |
| 🔐 Segurança | `libssl3t64` | 3.0.13-0ubuntu3.7 | **3.0.13-0ubuntu3.9** |

### ⚙️ Systemd e Subsistemas

| Categoria | Pacote | Versão Atual | Versão Disponível |
|-----------|--------|-------------|-------------------|
| ⚙️ Systemd | `systemd` | 255.4-1ubuntu8.12 | **255.4-1ubuntu8.15** |
| ⚙️ Systemd | `systemd-resolved` | 255.4-1ubuntu8.12 | **255.4-1ubuntu8.15** |
| ⚙️ Systemd | `systemd-timesyncd` | 255.4-1ubuntu8.12 | **255.4-1ubuntu8.15** |
| ⚙️ Systemd | `systemd-sysv` | 255.4-1ubuntu8.12 | **255.4-1ubuntu8.15** |
| ⚙️ Systemd | `libsystemd0` | 255.4-1ubuntu8.12 | **255.4-1ubuntu8.15** |
| ⚙️ Systemd | `libnss-systemd` | 255.4-1ubuntu8.12 | **255.4-1ubuntu8.15** |
| ⚙️ Systemd | `libpam-systemd` | 255.4-1ubuntu8.12 | **255.4-1ubuntu8.15** |

### 🌐 Rede e DNS

| Categoria | Pacote | Versão Atual | Versão Disponível |
|-----------|--------|-------------|-------------------|
| 🌐 Rede | `bind9-dnsutils` | 1:9.18.39-0ubuntu0.24.04.2 | **1:9.18.39-0ubuntu0.24.04.3** |
| 🌐 Rede | `bind9-host` | 1:9.18.39-0ubuntu0.24.04.2 | **1:9.18.39-0ubuntu0.24.04.3** |
| 🌐 Rede | `bind9-libs` | 1:9.18.39-0ubuntu0.24.04.2 | **1:9.18.39-0ubuntu0.24.04.3** |
| 🌐 Rede | `netplan.io` | 1.1.2-8ubuntu1~24.04.1 | **1.1.2-8ubuntu1~24.04.2** |
| 🌐 Rede | `netplan-generator` | 1.1.2-8ubuntu1~24.04.1 | **1.1.2-8ubuntu1~24.04.2** |
| 🌐 Rede | `nftables` | 1.0.9-1build1 | **1.0.9-1ubuntu0.1** |

### 🗓️ Fuso Horário e Data

| Categoria | Pacote | Versão Atual | Versão Disponível |
|-----------|--------|-------------|-------------------|
| 🗓️ Data/Hora | `tzdata` | 2025b-0ubuntu0.24.04.1 | **2026a-0ubuntu0.24.04.1** |

### 📦 Demais Pacotes com Atualização

| Categoria | Pacote | Versão Atual | Versão Disponível |
|-----------|--------|-------------|-------------------|
| 📦 Utilitários | `coreutils` | 9.4-3ubuntu6.1 | **9.4-3ubuntu6.2** |
| 📦 Utilitários | `fwupd` | 1.9.33 | **1.9.34** |
| 📦 Utilitários | `lshw` | 02.19...2build3 | **02.19...24.04.1** |
| 📦 Utilitários | `sosreport` | 4.9.2 | **4.10.2** |
| 📦 Utilitários | `pollinate` | 4.33-3.1ubuntu1.1 | **4.33-3.1ubuntu1.3** |
| 📦 Python | `python3-jwt` | 2.7.0-1 | **2.7.0-1ubuntu0.1** |
| 📦 Python | `python3-openssl` | 23.2.0-1 | **23.2.0-1ubuntu0.1** |
| 📦 Python | `python3-pyasn1` | 0.4.8-4ubuntu0.1 | **0.4.8-4ubuntu0.2** |
| 📦 Python | `python3-netplan` | 1.1.2-8ubuntu1~24.04.1 | **1.1.2-8ubuntu1~24.04.2** |
| 📦 Bibliotecas | `libarchive13t64` | 3.7.2-2ubuntu0.5 | **3.7.2-2ubuntu0.6** |
| 📦 Bibliotecas | `libtiff6` | 4.5.1+git230720-4ubuntu2.4 | **4.5.1+git230720-4ubuntu2.5** |
| 📦 Ferramentas | `binutils` | 2.42-4ubuntu2.8 | **2.42-4ubuntu2.10** |
| 📦 Drivers | `ubuntu-drivers-common` | 1:0.9.7.6ubuntu3.5 | **1:0.9.7.6ubuntu3.6** |
| 📦 Dispositivos | `udev` | 255.4-1ubuntu8.12 | **255.4-1ubuntu8.15** |

> **💬 Para o gestor:** Existem **49 pacotes** aguardando atualização neste servidor, incluindo atualizações importantes de segurança (OpenSSL) e do próprio Docker (nova versão 29.4.0 disponível). Recomenda-se agendar uma janela de manutenção para aplicar essas atualizações, especialmente as relacionadas ao Kernel do sistema e ao Docker, pois podem exigir reinicialização do servidor. A atualização do Kernel melhora a estabilidade e corrige vulnerabilidades de segurança conhecidas.

---

*📄 Documento gerado automaticamente com base nas informações coletadas no servidor `ctlinux01` em 08/04/2026.*
