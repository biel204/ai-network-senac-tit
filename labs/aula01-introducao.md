1) Importar a imagem (.OVA)
Abra o VirtualBox<br>
Clique em 📁 Arquivo → Importar Appliance<br>

Clique em 📂 e selecione:<br>

Downloads\UbuntuServer-OnPremises.ova<br>
Clique em ➡️ Avançar<br>
Revise as configurações (pode manter padrão)<br>
Clique em ✔️ Importar<br>
Aguarde a conclusão<br>
🌐 2) Configurar Rede em modo Bridge (Ponte)<br>
Selecione a VM importada
Clique em ⚙️ Configurações
Vá em 🌐 Rede
Em Adaptador 1:
✔️ Marcar: Habilitar placa de rede
📡 Em “Conectado a”: Bridge Adapter (Adaptador em Ponte)
🔌 Em “Nome”: selecione a placa de rede cabeada
Exemplo: Ethernet, Realtek, Intel(R) Ethernet
Clique em ✔️ OK

📌 Importante: Use sempre a interface cabeada do laboratório (não Wi-Fi).

▶️ 3) Iniciar a Máquina Virtual
Selecione a VM
Clique em ▶️ Iniciar
Aguarde o boot do Ubuntu Server 22.04.4 LTS
🔎 4) Descobrir o IP da VM

Dentro da VM, execute:

ip a

ou:

hostname -I

📌 Anote o IP (exemplo: 192.168.0.105)

🔐 5) Acesso remoto via SSH

No próprio Windows (PowerShell ou CMD):

ssh usuario@IP_DA_VM

Exemplo:

ssh aluno@192.168.0.105

👉 Se aparecer:

Are you sure you want to continue connecting (yes/no)?

Digite:

yes
⚠️ Dicas rápidas (evita erro comum)
✔️ VM e PC devem estar na mesma rede
✔️ Bridge precisa estar na placa Ethernet correta
✔️ Se não pegar IP:
Reinicie a VM
Verifique cabo de rede conectado

✔️ Se SSH falhar:

sudo systemctl status ssh
✅ Resultado esperado
VM rodando normalmente
IP válido na rede local
Acesso remoto via SSH funcionando


---

🧠 Avaliação do Hardware
🖥️ Processador
Intel Core i7-14700K
✔️ Excelente para virtualização (alto número de núcleos e threads)
✔️ Suporte a Intel VT-x/VT-d (necessário para VMs)
💾 Memória RAM
32 GB RAM
✔️ Muito acima do necessário
📌 Recomendação prática:
VM Ubuntu Server: 2 GB a 4 GB já é suficiente
Pode rodar várias VMs simultaneamente sem impacto
🗄️ Armazenamento
1 TB
✔️ Espaço confortável para múltiplas VMs
📌 OVA típico: ~5–20 GB (dependendo da imagem)
🎮 Placa de Vídeo
12 GB VRAM
✔️ Pouco relevante para VirtualBox (uso básico)
✔️ Só faz diferença em:
IA com GPU (fora do VirtualBox)
Softwares específicos (CUDA, etc.)
⚙️ Configuração recomendada da VM

Para seu caso (laboratório + IA básica + SSH):

🔧 Sistema
RAM: 4096 MB (4 GB)
CPU: 2 a 4 núcleos
Vídeo: padrão (sem necessidade de ajuste)
🌐 Rede
✔️ Bridge (como você já mencionou)
✔️ Interface: Ethernet
🚀 O que seu PC consegue fazer

Com essa máquina, você pode:

✔️ Rodar 3–6 VMs simultaneamente com estabilidade
✔️ Criar laboratório completo de redes (cliente + servidor + firewall)
✔️ Testar IA em ambiente Linux sem travamento
✔️ Rodar containers (Docker) dentro da VM sem problemas
⚠️ Ajustes importantes (vale conferir)
1. Virtualização na BIOS
Certifique-se que está ativada
Intel VT-x / Virtualization Technology
2. Hyper-V (Windows)

No Windows 11:

Pode causar lentidão no VirtualBox
Se necessário, desative:
bcdedit /set hypervisorlaunchtype off

(Reiniciar após)

3. Disco da VM
Prefira disco dinâmico (VDI) se criar novas VMs
Melhor uso de espaço
📊 Conclusão técnica

Sua máquina está sobredimensionada para esse cenário:

Não terá gargalo de CPU
RAM suficiente para múltiplos ambientes
Rede em bridge funcionará sem impacto
SSH será instantâneo

---

Há um ponto inconsistente: 10.24.82.22 não é endereço de rede para máscara /24 (255.255.255.0).
Com /24, a rede correta seria 10.24.82.0 (hosts de .1 a .254).

Dado o gateway 10.24.82.1, a rede válida é:

Rede: 10.24.82.0/24
Gateway: 10.24.82.1
DNS: 10.24.40.190
📊 Tabela corrigida de endereçamento
| 🖥️ Servidor        | 🌐 Hostname      | 🔢 Endereço IP   | 🧩 Máscara        | 🚪 Gateway       | 📡 DNS            | 📝 Função                |
|-------------------|------------------|------------------|-------------------|------------------|-------------------|--------------------------|
| 🖥️ Servidor 1     | srv-web          | 10.24.82.10      | 255.255.255.0     | 10.24.82.1       | 10.24.40.190      | 🌍 Web                   |
| 🖥️ Servidor 2     | srv-db           | 10.24.82.20      | 255.255.255.0     | 10.24.82.1       | 10.24.40.190      | 🗄️ Banco de Dados        |
🔎 Observações técnicas
Faixa válida: 10.24.82.1 – 10.24.82.254
.1 já está em uso (gateway) → evite
.0 (rede) e .255 (broadcast) → não utilizáveis
Os IPs .10 e .20 são seguros (fora de ranges comuns de DHCP)
⚠️ Validação recomendada

Antes de aplicar:

Verifique se não há DHCP distribuindo IP nessa faixa

Teste disponibilidade:

ping 10.24.82.10
ping 10.24.82.20

Ou use:

arp-scan -l