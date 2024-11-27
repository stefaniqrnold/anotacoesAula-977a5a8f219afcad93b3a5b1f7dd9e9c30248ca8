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
**Gerência de I/O no Linux:**
  - Responsável pela comunicação entre software e dispositivos de entrada/saída.
  - Garantir desempenho, eficiência e suporte a diversos dispositivos.

**Kernel 6:**
  - Última versão do Linux, trazendo **otimizações em I/O**, como suporte a novos dispositivos e aprimoramento no escalonamento.

---
     
### Classes de dispositivos suportados
**Orientados a Bloco:**
 - Processam dados em blocos (ex.: discos rígidos, SSDs).
 - Operações otimizadas para leitura e gravação.

**Orientados a Caractere:**
 - Processam dados sequencialmente (ex.: teclados, terminais).
 - Operações mais simples e diretas.

**Outros:**
 - Dispositivos como GPUs, webcams e controladores de rede.

---

### Estratégias de Comunicação kernel-driver:

1.  **Controlada por Programa:**

    - Software controla diretamente os dispositivos.
    - Exemplo: transferências síncronas.

2.  **Controlada por Eventos:**

    - Hardware gera interrupções tratadas pelo kernel.
    - Exemplo: teclas pressionadas ou dados recebidos.

3.  **DMA (Direct Memory Access):**
    - Transferência direta entre dispositivo e memória.
    - Reduz carga da CPU, ideal para discos e redes.
    
---

## Algoritmos de Escalonamento de I/O

- **O que é?**

  - Métodos para gerenciar a ordem de requisições de entrada/saída.

- **Exemplo no Kernel 6:**
  - **CFQ:** Balanceia requisições de E/S entre processos.
  - **NOOP:** Simples, ideal para SSDs, processa na ordem de chegada.
  - **Deadline:** Garante atendimento das requisições dentro de um tempo máximo.

---

## Limite de dispositivos suportados
**Por que existem limites?**
  - Gestão de recursos do kernel.
  - Evita sobrecarga em sistemas de alto desempenho.

**Exemplo prático:**
  - **Kernel 6 e suporte a dispositivos**: O Kernel Linux 6.6, lançado em outubro de 2023, trouxe melhorias significativas no suporte a dispositivos virtuais e físicos. Ele inclui suporte aprimorado para dispositivos ARM64, melhorias na gestão de energia, compatibilidade com drivers e segurança, entre outras funcionalidades.

---

## Diferenciais e curiosidades 
**Melhorias no Kernel 6:**
   - Novo suporte para dispositivos NVMe.
   - Redução de latência em sistemas com alta carga de I/O.
   - Melhor uso de threads para paralelismo em operações de leitura/gravação.
---
## Diferenciais e curiosidades
**Kernel Linux e supercomputadores:**
    O Linux é realmente amplamente utilizado em supercomputadores. De acordo com dados recentes, o Linux está presente em quase todos os supercomputadores mais poderosos do mundo. Em 2017, por exemplo, 99,6% dos supercomputadores listados na Top500.org estavam rodando Linux. (https://top500.org/)

---

## Vantagens da Gerência de I/O no Linux

- **Suporte a uma vasta gama de dispositivos:**

  - Compatibilidade com diversos tipos de hardware, desde dispositivos antigos até os mais modernos.

- **Arquitetura modular para drivers:**

  - Facilita a adição e atualização de drivers sem necessidade de recompilar o kernel inteiro.

- **Eficiência em sistemas embarcados e servidores de alta performance:**
  - Otimizações específicas para diferentes cenários de uso, garantindo desempenho e estabilidade.

---

## **Referências**
GARRELS, M. The Linux Documentation Project. Disponível em: <https://tldp.org/>. Acesso em: 24 nov. 2024.

LINUX NETWORK. Linux kernel 6.7 unveiled: A comprehensive look at new features and enhancements. Disponível em: <https://www.youtube.com/watch?v=Ece_xtPh470>. Acesso em: 26 nov. 2024.

---

## **Referências**
Man7.org (Michael kerrisk) Linux/UNIX programming training. Disponível em: <https://man7.org/training/>. Acesso em: 26 nov. 2024.

NEGROMONTE, E. Linux Kernel 6.6: tudo o que você precisa saber. Disponível em: <https://sempreupdate.com.br/linux/kernel/linux-kernel-6-6-tudo-o-que-voce-precisa-saber/>. Acesso em: 26 nov. 2024.

The Linux Kernel documentation — The Linux Kernel documentation. Disponível em: <https://www.kernel.org/doc/html/latest/index.html>. Acesso em: 26 nov. 2024.

---
# Obrigado Pela Atenção!
## **Perguntas?**

nicolas.soares@sou.unijui.edu.br
stefani.camargo@sou.unijui.edu.br



