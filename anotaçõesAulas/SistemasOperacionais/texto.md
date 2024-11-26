# **Gerência de I/O no Linux - Kernel 6**
### Sistemas Operacionais - Engenharia de Software
<!-- Scoped style -->
<style scoped>
h1 {
  color: blue;
}
</style>

Obs: o tema de gerência de I/O pode ser mais restrito em termos de conteúdo. O grupo não precisa ficar restrito a versão específica do SO escolhido. Ex: se não encontrou informações sobre Linux 2.6, pode ver em versões >=3 o < 2
  
---

## **Introdução e Definição**
- **Gerência de I/O no Linux:**
  - Responsável pela comunicação entre software e dispositivos de entrada/saída.
  - Garantir desempenho, eficiência e suporte a diversos dispositivos.

- **Kernel 6:**
  - Última versão do Linux, trazendo **otimizações em I/O**, como suporte a novos dispositivos e aprimoramento no escalonamento.

---

## **Classes de Dispositivos Suportados**
1. **Orientados a Bloco:**
   - Processam dados em blocos (ex.: discos rígidos, SSDs).
   - Operações otimizadas para leitura e gravação.

2. **Orientados a Caractere:**
   - Processam dados sequencialmente (ex.: teclados, terminais).
   - Operações mais simples e diretas.

3. **Outros:**
   - Dispositivos como GPUs, webcams e controladores de rede.

---

## **Interação entre Kernel e Driver**
### Estratégias de Comunicação:
1. **Controlada por Programa:**
   - O software controla diretamente os dispositivos.
   - Exemplo: transferências síncronas.

2. **Controlada por Eventos:**
   - O hardware gera interrupções tratadas pelo kernel.
   - Exemplo: teclas pressionadas ou dados recebidos.

3. **DMA (Direct Memory Access):**
   - Transferência direta entre dispositivo e memória.
   - Reduz carga da CPU, ideal para discos e redes.

---

## **Escalonamento de E/S**
- **O que é?**
  - Técnica para organizar e priorizar requisições de dispositivos.
  
- **Exemplo no Kernel 6:**
  - **CFQ (Completely Fair Queueing):** Mantém balanceamento entre processos.
  - **NOOP Scheduler:** Para dispositivos rápidos como SSDs.
  - **Deadline Scheduler:** Garante tempo máximo de atendimento.

---

## **Limite de Dispositivos Suportados**
- **Por que existem limites?**
  - Gestão de recursos do kernel.
  - Evita sobrecarga em sistemas de alto desempenho.

- **Exemplo prático:**
  - Kernel 6 suporta milhões de dispositivos virtuais e físicos em grandes servidores.

---

## **Diferenciais e Curiosidades**
1. **Melhorias no Kernel 6:**
   - Novo suporte para dispositivos NVMe.
   - Redução de latência em sistemas com alta carga de I/O.
   - Melhor uso de threads para paralelismo em operações de leitura/gravação.

2. **Curiosidade:**
   - O Kernel Linux é usado por **97% dos supercomputadores**, mostrando a eficiência de sua gerência de I/O.

---

## **Vantagens da Gerência de I/O no Linux**
- Suporte a uma vasta gama de dispositivos.
- Arquitetura modular para drivers.
- Eficiência em sistemas embarcados e servidores de alta performance.

---

## **Desafios Atuais**
- Gerenciar a complexidade de novos dispositivos (ex.: GPUs modernas).
- Garantir segurança e isolamento entre processos em operações de E/S.
- Otimizar operações para dispositivos NVMe e redes de alta velocidade.

---

## **Referências**
- **Artigos e Sites:**
  - [Gerenciamento de Processos no Linux: do nascimento ao encerramento](https://sempreupdate.com.br/linux/gerenciamento-de-processos-no-linux-do-nascimento-ao-encerramento/)
  - [Gerenciamento de Processos no Linux - Prioridade e NICE](https://linuxsemfronteiras.com.br/gerenciamento-de-processos-no-linux/)
  - [Sistemas operacionais/Gerência de dispositivos de entrada e saída](https://pt.wikibooks.org/wiki/Sistemas_operacionais/Ger%C3%AAncia_de_dispositivos_de_entrada_e_sa%C3%ADda)
  - [Linux Kernel 6.7 Unveiled: A Comprehensive Look at New Features and Enhancements](https://www.youtube.com/watch?v=Ece_xtPh470)

---

# Perguntas?
