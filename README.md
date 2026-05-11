# Simulações de Redes de Sensores Sem Fio (WSN) em MATLAB

Este repositório contém um conjunto de práticas e simulações desenvolvidas em MATLAB para estudo de **Redes de Sensores Sem Fio (Wireless Sensor Networks - WSN)**, com foco em:

- Protocolos de acesso ao meio
- Problema de implosão em flooding
- Protocolos eficientes energeticamente
- Topologias de rede
- Modelos de confiabilidade
- Eficiência energética em comunicação multihop

As simulações possuem caráter didático e visual, permitindo compreender conceitos clássicos presentes em protocolos de WSN.

---

# Conteúdo do Repositório

## 1. Comparação entre CSMA e TDMA

Simulação visual comparando:

### CSMA (Carrier Sense Multiple Access)

- Acesso aleatório ao meio
- Possibilidade de colisões
- Desperdício energético

### TDMA (Time Division Multiple Access)

- Slots reservados
- Comunicação organizada
- Sem colisões

### Conceitos abordados

- Colisão de pacotes
- Eficiência energética
- Escalonamento temporal
- Redes organizadas vs. aleatórias

### Visualização

- Gráfico de Gantt mostrando transmissões dos nós

#### Pacotes

- 🟩 Verde → transmissão bem-sucedida
- 🟥 Vermelho → colisão
- 🟦 Azul → slot TDMA reservado

---

## 2. Simulação de Flooding e Problema da Implosão

Simulação clássica do protocolo Flooding em redes WSN.

### Objetivo

Visualizar o fenômeno da **implosão**, onde múltiplos nós recebem repetidamente a mesma informação, causando:

- Redundância
- Congestionamento
- Desperdício de energia

### Conceitos abordados

- Broadcast em redes WSN
- Redundância de mensagens
- Implosão de dados
- Sobrecarga de comunicação

### Elementos visuais

- Nós sensores
- Nó fonte
- Transmissões entre vizinhos
- Linhas pontilhadas representando implosão

---

## 3. Topologia de Rede de Sensores

Geração de uma topologia aleatória de rede.

### Objetivo

Visualizar:

- Distribuição espacial dos sensores
- Conectividade entre nós
- Densidade da rede

### Conceitos abordados

- Alcance de transmissão
- Redes ad hoc
- Matriz de adjacência
- Conectividade

### Resultado

- Nós distribuídos aleatoriamente
- Ligações entre sensores vizinhos
- Quantidade total de conexões

---

## 4. Protocolo SPIN (Sensor Protocols for Information via Negotiation)

Simulação do protocolo SPIN como solução para problemas do Flooding.

### Funcionamento

O protocolo é dividido em três fases:

1. **ADV** — anúncio de metadados  
2. **REQ** — requisição do dado  
3. **DATA** — envio real da informação  

### Objetivo

Demonstrar como o SPIN reduz:

- Redundância
- Consumo energético
- Transmissões desnecessárias

### Conceitos abordados

- Negociação de dados
- Metadados
- Eficiência energética
- Comunicação seletiva

### Visualização

- 🔵 Setas azuis → ADV
- 🟢 Setas verdes → REQ
- 🔴 Setas vermelhas → DATA
- Nós que ignoram dados redundantes

### Comparação energética

O script também gera um gráfico comparando:

- Flooding tradicional
- Protocolo SPIN

---

## 5. Confiabilidade de Nós Sensores

Simulação baseada no modelo exponencial de confiabilidade:

```math
R_k(t) = e^{-\lambda t}
```

### Objetivo

Analisar a probabilidade de sobrevivência de um nó sensor ao longo do tempo.

### Conceitos abordados

- Taxa de falha (\(\lambda\))
- Confiabilidade
- Sistemas tolerantes a falhas

### Resultado

- Curvas comparando diferentes taxas de falha

---

## 6. Comunicação Direta vs. Multihop

Simulação da eficiência energética da comunicação multihop.

### Modelo utilizado

Energia proporcional à distância elevada a \(n\):

```math
E \propto d^n
``` 

### Objetivo

Analisar a probabilidade de sobrevivência de um nó sensor ao longo do tempo.

### Conceitos abordados

- Taxa de falha (\(\lambda\))
- Confiabilidade
- Sistemas tolerantes a falhas

### Resultado

- Curvas comparando diferentes taxas de falha

---

## 6. Comunicação Direta vs. Multihop

Simulação da eficiência energética da comunicação multihop.

### Modelo utilizado

Energia proporcional à distância elevada a \(n\):

```math
E \propto d^n
```

### Objetivo

Comparar:

- Comunicação direta
- Comunicação com múltiplos saltos

### Conceitos abordados

- Multihop routing
- Economia de energia
- Atenuação de sinal
- Redes escaláveis

### Resultado

- Gráfico mostrando redução do consumo energético conforme aumenta o número de hops

---

# Tecnologias Utilizadas

- MATLAB
- Computação gráfica básica
- Simulação de redes
- Modelagem matemática
