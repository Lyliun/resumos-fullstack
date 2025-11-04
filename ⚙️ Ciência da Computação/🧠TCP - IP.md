# 🧠 Modelos de Camada — OSI e TCP/IP

> Estruturas conceituais que explicam como a comunicação acontece entre dispositivos em uma rede.

---

## 🧩 Modelo OSI (Open Systems Interconnection)

O **modelo OSI** é uma **referência teórica** criada pela ISO para padronizar a comunicação em redes.  
Ele divide o processo em **7 camadas**, cada uma com uma função específica:

|Nº|Camada|Função Principal|
|---|---|---|
|7|**Aplicação**|Interface entre usuário e rede (HTTP, FTP, SMTP)|
|6|**Apresentação**|Traduz dados (criptografia, compressão, formato)|
|5|**Sessão**|Gerencia conexões e sessões entre dispositivos|
|4|**Transporte**|Garante a entrega dos dados (TCP, UDP)|
|3|**Rede**|Define rotas e endereços IP (IP, ICMP)|
|2|**Enlace de Dados**|Controla a transmissão física (Ethernet, MAC)|
|1|**Física**|Transmite bits pelo meio físico (cabos, rádio, sinais)|

🧠 **Dica pra lembrar:**

> “**F**ísica, **E**nlace, **R**ede, **T**ransporte, **S**essão, **A**presentação, **A**plicação”  
> → **FERTSAA** (ou “**F**eliz **E**studante **R**ede **T**ransmite **S**abendo **A**plicar **A**ulas”) 😄

---

## 🌍 Modelo TCP/IP

O **modelo TCP/IP** é uma **implementação prática** do modelo OSI, usado na **Internet**.  
Possui **4 camadas**, que correspondem a grupos de camadas do OSI:

|Camada TCP/IP|Equivalência no OSI|Função|
|---|---|---|
|**Aplicação**|5, 6, 7|Protocolos como HTTP, FTP, DNS, SMTP|
|**Transporte**|4|Controle de fluxo e entrega (TCP, UDP)|
|**Internet**|3|Endereçamento e roteamento (IP)|
|**Acesso à Rede**|1, 2|Comunicação física (Ethernet, Wi-Fi)|

---

## 🔄 Comparativo OSI x TCP/IP

|Característica|OSI|TCP/IP|
|---|---|---|
|Camadas|7|4|
|Tipo|Modelo conceitual|Modelo prático (usado na Internet)|
|Criação|ISO (1984)|DARPA/DoD (anos 70)|
|Principal uso|Referência didática|Implementação real em redes|

---

## 🚀 Resumo Rápido (TL;DR)

> O modelo **OSI** é **teórico** e tem **7 camadas**, já o **TCP/IP** é **prático** e tem **4 camadas**.  
> Ambos explicam como os dados viajam de um dispositivo a outro na rede.
---

## 🏷️ Tags

#redes #modeloOSI #TCPIP #networking #generation #fundamentos