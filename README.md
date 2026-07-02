Repositório dedicado ao estudo prático de Redes de Computadores. Este laboratório inicial demonstra a interconexão e o roteamento de pacotes entre duas sub-redes distintas utilizando um roteador central e comandos CLI do IOS Cisco.

---

### Cenário e Topologia

A estrutura da rede foi dividida da seguinte forma:

| Rede | Sub-rede | Interface no Roteador | Dispositivos |
| :--- | :--- | :--- | :--- |
| **REDE A** | `192.168.1.0/24` | `GigabitEthernet 0/0` | `Switch1` ➔ `Laptop1` |
| **REDE B** | `192.168.0.0/24` | `GigabitEthernet 0/1` | `Switch0` ➔ `Laptop0` |

>  **Status do Teste:** O tráfego ICMP (Ping) entre o `Laptop0` e o `Laptop1` foi testado via modo de simulação e apresentou o status **"Successful"**, validando que as tabelas de roteamento e gateways estão conversando perfeitamente.

---

###  Configuração Aplicada

Os comandos executados no terminal do roteador para isolar, proteger e ativar as interfaces foram documentados no arquivo de script deste repositório.

* O passo a passo dos comandos CLI pode ser consultado diretamente no arquivo [config-roteador.ios](./config-roteador.ios).

#### Resumo dos comandos utilizados:
* `hostname nexus` — Define o nome do dispositivo.
* `ip address [IP] [MÁSCARA]` — Atribui o gateway da sub-rede à interface.
* `no shutdown` — Ativa a interface (muda os LEDs de vermelho para verde).
* `copy running-config startup-config` — Salva as configurações na memória NVRAM.
