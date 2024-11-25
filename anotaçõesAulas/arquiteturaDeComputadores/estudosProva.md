a prova é escrita, sem consulta, mas colocarei os desenhos e tabelas das portas lógicas básicas na própria prova. A prova será realizada na sala 305.


# **Frame 07 – Modos de Endereçamento**

---

## Introdução

### Representação de Instruções
- **Formato Geral**:

- **Conjunto de Instruções (Instruction Set)**:
1. Indica o que o processador vai fazer.
2. Indica com que dado(s) a operação será realizada.

**Exemplos**:
- `Cod. Op. Op1. Op2. Op3.`
- `Cod. Op. Op1. Op2.`
- `Cod. Op. Op1.`

---

## Modos de Endereçamento

### Tipos de Endereçamento:
1. Imediato
2. Direto
3. Indireto
4. Por Registrador
5. Indireto Por Registrador
6. Por Deslocamento
7. Por Pilha

---

## Endereçamento Imediato

### Características:
- Modo mais simples de endereçamento.
- Usado como constante ou para inicializar variáveis.

### **Vantagens**:
- Não precisa acessar a memória para buscar o operando.
- Curto tempo de execução.
- O dado é transferido da memória principal para o registrador de instrução (RI) com a instrução.

### **Desvantagens**:
- Tamanho do dado limitado ao campo do operando.
- Alteração necessária do campo operando a cada execução.

**Formato**:
- `Cod. Operação (4 bits) | Operando (4 bits)`
- **Exemplo**: Instrução de 8 bits (0 a 15 ou -8 a 7).

---

## Endereçamento Direto

### Características:
- O operando indica um endereço na memória onde o dado está.

### **Vantagens**:
- Apenas um acesso à memória.
- Não requer cálculo do endereço do dado.

### **Desvantagens**:
- Espaço de endereçamento limitado.
- Mais lento que o imediato.

**Formato**:
- `Cod. Operação (4 bits) | Endereço x (4 bits)`
- **Exemplo**: Endereço de 0 a 255.

---

## Endereçamento Indireto

### Características:
- Campo de endereço contém referência para outro endereço na memória que contém o dado efetivo.

### **Vantagens**:
- Endereço do dado pode ser grande.
- Suporta maior espaço de endereçamento.

### **Desvantagens**:
- Requer dois acessos à memória.
- Mais ciclos de memória necessários.

**Formato**:
- `Cod. Operação (4 bits) | Endereço x (4 bits)`

---

## Endereçamento Por Registrador

### Características:
- Semelhante ao endereçamento direto, mas o campo do endereço aponta para um registrador, não para a memória.

### **Vantagens**:
- Acesso rápido (registradores estão na CPU).
- Não requer acesso à memória.
- Permite uso de dados maiores.

### **Desvantagens**:
- Número de registradores é limitado.

**Formato**:
- `Cod. Operação (4 bits) | Endereço R (4 bits)`

---

## Endereçamento Indireto Por Registrador

### Características:
- Campo de endereço aponta para um registrador que contém o endereço do dado na memória.

### **Vantagens**:
- Não possui limitação de endereços como o endereçamento direto.
- Reduz o número de acessos à memória.

### **Desvantagens**:
- Requer dois acessos até o operando.

**Formato**:
- `Cod. Operação (4 bits) | Endereço R (4 bits)`

---

## Endereçamento Por Deslocamento

### Características:
- Combinação de endereçamento direto e indireto por registrador.
- Possui subtipos:
1. **Relativo**
2. **Com Registrador Base**
3. **Por Indexação**

### **Vantagens**:
- Versátil e utilizado de várias formas.

### **Desvantagens**:
- Mais complexo de implementar.
- Pode requerer dois operandos.

---

### Subtipo: Endereçamento Relativo

- Usado para calcular endereços de instruções próximas.
- Utiliza o **Program Counter (PC)** para armazenar o endereço da instrução atual.

**Problema**: Campo de 4 bits não cobre todo o espaço da memória.  
**Solução**: Utiliza deslocamentos relativos ao endereço da instrução atual.

---

### Subtipo: Por Registrador Base

- Um registrador contém o endereço base, enquanto o campo de endereço é o deslocamento.
- Usado para acessar dados, não instruções.

### Aplicações:
- Implementação de segmentação de memória.

---

### Subtipo: Por Indexação

- O endereço base está no campo do endereço, e o deslocamento em um registrador.

**Variações**:
1. **Auto-Indexação**: Incremento automático durante o cálculo do endereço.
2. **Pós-Indexação**: Útil para acessar blocos de memória distantes.
3. **Pré-Indexação**: Acessa múltiplos endereços de uma região comum.

---

## Endereçamento Por Pilha

### Características:
- A pilha é usada para armazenar dados, com o topo marcado por um apontador.
- Dados carregados da pilha para registradores do processador.

### **Vantagens**:
- Simples de implementar.

### **Desvantagens**:
- Difícil de utilizar eficientemente.

---

## Encerramento

"Uma crença é uma alavanca que, uma vez puxada, move quase tudo na vida de uma pessoa."  
— **Sam Harris**

---

# **Frame 08 – Flip-Flops e Latches**

---

## Circuitos Digitais

### Introdução
- Sistemas digitais são compostos por **circuitos combinacionais** e **elementos de memória**.
- Tipos de circuitos lógicos:
  1. **Circuitos combinatórios**:
     - Saída depende apenas das entradas atuais.
     - Não possuem memória.
  2. **Circuitos sequenciais**:
     - Saída depende das entradas atuais **e do estado anterior**.
     - Possuem memória.

---

## Circuitos Sequenciais

### Características
- A saída depende de combinações das entradas **e das variáveis de estado**.
- **Memória**: Lembram entradas passadas.
- Usados em casos onde o comportamento futuro depende do passado.

### Exemplo
- Um **alarme** que permanece acionado (mesmo após o sensor ser desativado) até que seja feito o **reset**.

---

## Conceitos Básicos

- **Estado**:
  - Representado por variáveis que armazenam informações relevantes sobre o circuito.
- **Biestáveis**:
  - Elementos de memória que possuem dois estados de saída.
  - Tipos: **Flip-Flops** e **Latches**.

---

## Diferença entre Latches e Flip-Flops

1. **Latches**:
   - Sensíveis ao **nível** dos sinais de entrada.
2. **Flip-Flops**:
   - Sensíveis à **borda** dos sinais de entrada (subida ou descida).

### Tipos:
- RS (SR)
- D
- JK
- T

---

## Latch RS (Set-Reset)

- **Entradas**: S (Set) e R (Reset).
- **Saídas**: Q e Q' (ou Q inverso).

### Estados:
1. **Set**: Define `Q = 1`.
2. **Reset**: Define `Q = 0`.
3. **Mantém Estado**: Nenhuma alteração.
4. **Proibido**: Ambos S e R iguais a 1.

---

### Latch RS - Tabela Verdade

| Estado       | S | R | Q(t+1) |
|--------------|---|---|--------|
| Mantém Estado| 0 | 0 | Q(t)   |
| Reset        | 0 | 1 | 0      |
| Set          | 1 | 0 | 1      |
| Proibido     | 1 | 1 | Indeterminado |

**Resumo**:
- O circuito "lembra" o último estado em que uma das entradas foi 1.
- `S = R = 1` é proibido, pois resultaria em inconsistência.

---

## Circuitos Síncronos e Assíncronos

1. **Assíncronos**:
   - Alterações nas saídas ocorrem a qualquer instante, conforme mudanças nas entradas.
2. **Síncronos**:
   - Alterações ocorrem em instantes específicos, sincronizados com um sinal de **relógio (clock)**.

---

## Relógio (Clock)

- Pulsos retangulares ou onda quadrada.
- **Características**:
  - **Período**: Intervalo entre transições consecutivas.
  - **Frequência**: Inverso do período.
  - **Duty-Cycle**: Relação entre o tempo ativo e o período.

---

## Latch RS com Clock

- Inclui uma entrada de **Clock (C)**.
- Funciona como um latch RS básico, mas sincronizado pelo sinal de clock.

---

## Latch D

- Um latch simplificado com uma única entrada **D**.
- **Funcionamento**:
  - `C = 1`: Saída Q segue o valor de D.
  - `C = 0`: Saída Q mantém o valor anterior.

### Vantagem:
- Não possui configuração proibida.

---

## Latch JK

- **Entradas**: J (Set) e K (Reset).
- Combina a funcionalidade do latch RS, mas resolve a configuração proibida.

### Tabela Verdade:

| Estado       | J | K | Q(t+1) |
|--------------|---|---|--------|
| Mantém Estado| 0 | 0 | Q(t)   |
| Reset        | 0 | 1 | 0      |
| Set          | 1 | 0 | 1      |
| Inverte      | 1 | 1 | Q'(t)  |

**Resumo**:
- Com `J = K = 1`, o estado inverte continuamente enquanto o clock está ativo.

---

## Flip-Flop T

- Versão simplificada do Flip-Flop JK.
- **Entrada**: T.
- **Funcionamento**:
  - `T = 1`: Saída Q alterna entre 0 e 1 a cada pulso de clock.
  - `T = 0`: Saída Q mantém o estado.

---

## Conclusão

"Não se pode criar experiência. É preciso passar por ela."  
— **Albert Camus** (1913–1960)

---


