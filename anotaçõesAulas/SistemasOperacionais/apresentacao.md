---
# configurações do marp
marp: true
theme: gradient
class:  
- blue # classe azul do tema
- lead # centralizar

paginate: true 

title: Gerência de I/O no Linux - Kernel 6
description: slides para apresentação no dia 26/11/24 para a materia de Sistemas Operacionais
author: Stéfani Arnold
keywords: linux, kernel 6, I/O

# canto dos slides
header: 'Kernel 6 - Linux'

---

# **Gerência de I/O no Linux - Kernel 6**
## Sistemas Operacionais - Engenharia de Software e Ciência da Computação
### **Stéfani Arnold e Nicolas Hass**
### `Módulo 02/2024`

---

## Introdução e Definição
- **Gerência de I/O no Linux:**
  - Responsável pela comunicação entre software e dispositivos de entrada/saída.
  - Garantir desempenho, eficiência e suporte a diversos dispositivos.

- **Kernel 6:**
  - Última versão do Linux, trazendo **otimizações em I/O**, como suporte a novos dispositivos e aprimoramento no escalonamento.

---
     
### Classes de dispositivos suportados
1. **Orientados a Bloco:**
   - Processam dados em blocos (ex.: discos rígidos, SSDs).
   - Operações otimizadas para leitura e gravação.

2. **Orientados a Caractere:**
   - Processam dados sequencialmente (ex.: teclados, terminais).
   - Operações mais simples e diretas.

3. **Outros:**
   - Dispositivos como GPUs, webcams e controladores de rede.

---

## Interação entre kernel e driver

### Estratégias de Comunicação:

1. **Controlada por Programa:**
   - O software controla diretamente os dispositivos.
   - Exemplo: transferências síncronas.

2. **Controlada por Eventos:**
   - O hardware gera interrupções tratadas pelo kernel.
   - Exemplo: teclas pressionadas ou dados recebidos.

---

## Interação entre kernel e driver

### Estratégias de Comunicação:

3. **DMA (Direct Memory Access):**
   - Transferência direta entre dispositivo e memória.
   - Reduz carga da CPU, ideal para discos e redes.

---

## Escalonamento de E/S: 

- **O que é?**
  - Técnica para organizar e priorizar requisições de dispositivos.
  
- **Exemplo no Kernel 6:**
  - **CFQ (Completely Fair Queueing):** Mantém balanceamento entre processos.
  - **NOOP Scheduler:** Para dispositivos rápidos como SSDs.
  - **Deadline Scheduler:** Garante tempo máximo de atendimento.

---

## Limite de dispositivos suportados
- **Por que existem limites?**
  - Gestão de recursos do kernel.
  - Evita sobrecarga em sistemas de alto desempenho.

- **Exemplo prático:**
  - Kernel 6 suporta milhões de dispositivos virtuais e físicos em grandes servidores.

---

## Diferenciais e curiosidades 
1. **Melhorias no Kernel 6:**
   - Novo suporte para dispositivos NVMe.
   - Redução de latência em sistemas com alta carga de I/O.
   - Melhor uso de threads para paralelismo em operações de leitura/gravação.

2. **Curiosidade:**
   - O Kernel Linux é usado por **97% dos supercomputadores**, mostrando a eficiência de sua gerência de I/O.

---

## Vantagens da Gerência de I/O no Linux
- **Suporte a uma vasta gama de dispositivos.**
- **Arquitetura modular para drivers.**
- **Eficiência em sistemas embarcados e servidores de alta performance.**

---

## Desafios Atuais
- Gerenciar a complexidade de novos dispositivos (ex.: GPUs modernas).
- Garantir segurança e isolamento entre processos em operações de E/S.
- Otimizar operações para dispositivos NVMe e redes de alta velocidade.

---

## Referências
- GARRELS, M. The Linux Documentation Project. Disponível em: <https://tldp.org/>. Acesso em: 24 nov. 2024.

- LINUX NETWORK. Linux kernel 6.7 unveiled: A comprehensive look at new features and enhancements. Disponível em: <https://www.youtube.com/watch?v=Ece_xtPh470>. Acesso em: 26 nov. 2024.

---

## Referências
- Man7.org (Michael kerrisk) Linux/UNIX programming training. Disponível em: <https://man7.org/training/>. Acesso em: 26 nov. 2024.

- The Linux Kernel documentation — The Linux Kernel documentation. Disponível em: <https://www.kernel.org/doc/html/latest/index.html>. Acesso em: 26 nov. 2024.

---

# Perguntas?

nicolas.soares@sou.unijui.edu.br
stefani.camargo@sou.unijui.edu.br



