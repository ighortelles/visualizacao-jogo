# Gabarito do Chart Battle

Gabarito dos 18 desafios: quais duplas de **Visualização + Variável Visual** pontuam, qual é a dupla preferida (★), qual é a armadilha de cada desafio e por quê.

> **Estado:** versão 1, aprovada pelo grupo em 24/11/2026. Ainda não passou por partidas reais; ajustes que vierem dos playtests devem ser registrados aqui.

## Como pontuar

O gabarito é **estrito**: só pontua o que está listado, sem defesa nem votação.

| Situação | Pontos |
|---|---:|
| Visualização aceita no desafio | 2 |
| Variável listada na linha dessa visualização | +1 |
| Dupla preferida (★) | +1 |
| Visualização fora da lista | 0 |

- Uma dupla vale 0, 2, 3 ou 4 pontos.
- A variável só pontua junto com uma visualização aceita, e só vale na linha em que aparece.
- A armadilha é a carta que mais se confunde com a resposta certa. Se for uma Visualização, a dupla vale 0; se for uma Variável, ela não soma o +1.

**Exemplo, desafio 14 (Sazonalidade turística):**

- 34 Gráfico de linhas múltiplas + 36 Posição vertical: **4 pontos**, porque a dupla tem ★.
- 19 Gráfico de barras + 41 Cor sequencial: **2 pontos**. Barras é aceita, mas Cor sequencial não está na linha de Barras.
- 32 Gráfico de área empilhada + 39 Área proporcional: **0**. Área empilhada é a armadilha deste desafio.

## Critérios

1. **Visualização aceita (2 pontos):** a técnica executa a tarefa do desafio usando só os dados que ele cita, sem distorcer.
2. **Variável listada (+1):** é um canal que aquela visualização usa para mostrar o dado do desafio, seja o dado em foco, seja a moldura de tempo ou de espaço.
3. **Dupla preferida (★, +1):** a dupla em que o canal do dado em foco é o mais eficaz. Há no máximo duas por desafio; posição horizontal e posição vertical contam como uma só quando o gráfico pode ser girado.
4. **Armadilha:** o erro clássico do desafio. Não pontua, e o porquê é lido em voz alta depois da conferência.

### Convenções

- Posição horizontal e posição vertical se equivalem em gráficos que podem ser girados: barras, boxplot e histograma.
- Em séries temporais, o tempo fica no eixo X e o valor no eixo Y.
- **Tamanho proporcional** vale para símbolos, como círculos e ícones. **Área proporcional** vale para fatias, faixas e regiões.
- **Mapa coroplético** pede taxa ou medida normalizada, como densidade ou proporção. Com total bruto por região, ele vira armadilha (desafio 09).

## Resumo

| # | Desafio | ★ Dupla preferida | Armadilha |
|---|---|---|---|
| 01 | Distribuição de categorias | 19 Barras + 37 Comprimento | 24 Histograma |
| 02 | Diferenças de magnitude | 19 Barras + 37 Comprimento | 23 Pizza, 31 Bolhas |
| 03 | Identificação de grupos | 21 Dispersão + 40 Cor categórica | 41 Cor sequencial |
| 04 | Valores positivos e negativos | 19 Barras + 42 Cor divergente | 23 Pizza |
| 05 | Correlação entre variáveis | 21 Dispersão + 35 Posição horizontal ou 36 Posição vertical | 20 Linhas |
| 06 | Destaque de informações | 19 Barras + 40 Cor categórica | 23 Pizza |
| 07 | Densidade populacional | 26 Mapa coroplético + 41 Cor sequencial | 30 Símbolos proporcionais |
| 08 | Distribuição de hospitais | 28 Mapa de pontos + 49 Posição geográfica | 26 Mapa coroplético, 27 Mapa de calor |
| 09 | Concentração de acidentes | 27 Mapa de calor + 41 Cor sequencial | 26 Mapa coroplético |
| 10 | Fluxo migratório | 29 Mapa de fluxos + 48 Espessura de linha ou 50 Direção do movimento | 26 Mapa coroplético |
| 11 | Temperatura regional | 27 Mapa de calor + 41 Cor sequencial | 30 Símbolos proporcionais |
| 12 | Acesso ao transporte público | 26 Mapa coroplético + 41 Cor sequencial | 23 Pizza, 30 Símbolos proporcionais |
| 13 | Evolução das vendas | 20 Linhas + 36 Posição vertical | 23 Pizza |
| 14 | Sazonalidade turística | 34 Linhas múltiplas + 36 Posição vertical; 33 Calendário + 41 Cor sequencial | 32 Área empilhada |
| 15 | Oscilação de temperatura | 20 Linhas + 36 Posição vertical | 22 Áreas |
| 16 | Crescimento populacional | 34 Linhas múltiplas + 40 Cor categórica ou 36 Posição vertical | 23 Pizza |
| 17 | Anomalias financeiras | 25 Boxplot + 36 Posição vertical ou 35 Posição horizontal; 20 Linhas + 36 Posição vertical | 23 Pizza, 32 Área empilhada |
| 18 | Comparação histórica | 34 Linhas múltiplas + 40 Cor categórica ou 36 Posição vertical | 32 Área empilhada |

## Desafio por desafio

### 01 · Distribuição de categorias

*Uma loja deseja comparar a quantidade de produtos vendidos em cinco categorias diferentes.*

| Visualização aceita (2 pontos) | Variáveis listadas (+1; ★ = preferida, +1) |
|---|---|
| 19 Gráfico de barras | ★ 37 Comprimento · 36 Posição vertical · 35 Posição horizontal |
| 23 Gráfico de pizza | 39 Área proporcional |

**Armadilha:** 24 Histograma.

**Por que essas respostas:** Barras: comprimento alinhado é o canal mais preciso para comparar quantidades. Pizza só passa porque são poucas categorias.

**Por que a armadilha erra:** Histograma agrupa valores numéricos em intervalos; categorias não são intervalos.

### 02 · Diferenças de magnitude

*Uma empresa precisa representar a receita de dez departamentos, destacando diferenças quantitativas.*

| Visualização aceita (2 pontos) | Variáveis listadas (+1; ★ = preferida, +1) |
|---|---|
| 19 Gráfico de barras | ★ 37 Comprimento · 36 Posição vertical · 35 Posição horizontal |

**Armadilha:** 23 Gráfico de pizza, 31 Gráfico de bolhas.

**Por que essas respostas:** Barras com base comum: o comprimento mostra a diferença exata entre os dez departamentos.

**Por que a armadilha erra:** Pizza com dez fatias quase iguais esconde as diferenças; nas bolhas, a área engana mais que o comprimento.

### 03 · Identificação de grupos

*Uma pesquisa contém indivíduos pertencentes a quatro grupos distintos. É necessário diferenciá-los visualmente.*

| Visualização aceita (2 pontos) | Variáveis listadas (+1; ★ = preferida, +1) |
|---|---|
| 21 Gráfico de dispersão | ★ 40 Cor categórica · 45 Forma geométrica · 46 Orientação |
| 31 Gráfico de bolhas | 40 Cor categórica |

**Armadilha:** 41 Cor sequencial.

**Por que essas respostas:** Grupos sem ordem pedem canal categórico: a cor é o mais rápido; forma e orientação funcionam com poucos grupos.

**Por que a armadilha erra:** Cor sequencial sugere uma ordem, do claro ao escuro, que os grupos não têm.

### 04 · Valores positivos e negativos

*Uma empresa deseja representar lucros e prejuízos de suas filiais.*

| Visualização aceita (2 pontos) | Variáveis listadas (+1; ★ = preferida, +1) |
|---|---|
| 19 Gráfico de barras | ★ 42 Cor divergente · 36 Posição vertical · 37 Comprimento · 35 Posição horizontal |
| 30 Mapa de símbolos proporcionais | 42 Cor divergente · 49 Posição geográfica |

**Armadilha:** 23 Gráfico de pizza.

**Por que essas respostas:** Barras a partir do zero mostram o sinal; a cor divergente separa lucro de prejuízo. Símbolos no mapa mostram onde fica cada filial.

**Por que a armadilha erra:** Pizza mostra partes de um todo; não existe fatia negativa.

### 05 · Correlação entre variáveis

*Um pesquisador deseja investigar a relação entre horas de estudo e notas obtidas.*

| Visualização aceita (2 pontos) | Variáveis listadas (+1; ★ = preferida, +1) |
|---|---|
| 21 Gráfico de dispersão | ★ 35 Posição horizontal · ★ 36 Posição vertical |
| 31 Gráfico de bolhas | 35 Posição horizontal · 36 Posição vertical |

**Armadilha:** 20 Gráfico de linhas.

**Por que essas respostas:** Duas medidas numéricas, uma em cada eixo: a nuvem de pontos mostra se uma cresce com a outra. Nas bolhas, o tamanho fica sem uso.

**Por que a armadilha erra:** Linhas ligam pontos em sequência, e aqui não há ordem entre os alunos.

### 06 · Destaque de informações

*Um analista precisa destacar três produtos com desempenho abaixo da meta em um conjunto de vinte produtos.*

| Visualização aceita (2 pontos) | Variáveis listadas (+1; ★ = preferida, +1) |
|---|---|
| 19 Gráfico de barras | ★ 40 Cor categórica · 43 Saturação da cor · 44 Luminosidade · 47 Textura · 42 Cor divergente |

**Armadilha:** 23 Gráfico de pizza.

**Por que essas respostas:** Uma cor de destaque contra o resto em cinza faz os três saltarem aos olhos; saturação, luminosidade e textura também destacam.

**Por que a armadilha erra:** Pizza com vinte fatias não deixa comparar nem destacar.

### 07 · Densidade populacional

*Uma prefeitura deseja comparar a densidade populacional entre os bairros de uma cidade.*

| Visualização aceita (2 pontos) | Variáveis listadas (+1; ★ = preferida, +1) |
|---|---|
| 26 Mapa coroplético | ★ 41 Cor sequencial · 44 Luminosidade · 43 Saturação da cor · 49 Posição geográfica |
| 27 Mapa de calor | 41 Cor sequencial · 44 Luminosidade · 43 Saturação da cor · 49 Posição geográfica |
| 19 Gráfico de barras (ranking) | 37 Comprimento · 36 Posição vertical · 35 Posição horizontal |

**Armadilha:** 30 Mapa de símbolos proporcionais.

**Por que essas respostas:** Densidade já é taxa por área: pinte cada bairro numa escala ordenada. Barras servem como ranking, sem o mapa.

**Por que a armadilha erra:** Símbolos proporcionais servem para totais; para uma taxa, o tamanho do círculo engana.

### 08 · Distribuição de hospitais

*Uma secretaria de saúde deseja visualizar a localização dos hospitais em uma região.*

| Visualização aceita (2 pontos) | Variáveis listadas (+1; ★ = preferida, +1) |
|---|---|
| 28 Mapa de pontos | ★ 49 Posição geográfica |
| 30 Mapa de símbolos proporcionais | 49 Posição geográfica |

**Armadilha:** 26 Mapa coroplético, 27 Mapa de calor.

**Por que essas respostas:** A pergunta é onde fica cada hospital: um ponto em cada coordenada. Símbolos também marcam o local.

**Por que a armadilha erra:** Coroplético e mapa de calor resumem por área e apagam a posição de cada hospital.

### 09 · Concentração de acidentes

*Um órgão de trânsito deseja identificar áreas com maior concentração de acidentes.*

| Visualização aceita (2 pontos) | Variáveis listadas (+1; ★ = preferida, +1) |
|---|---|
| 27 Mapa de calor | ★ 41 Cor sequencial · 44 Luminosidade · 43 Saturação da cor · 49 Posição geográfica |
| 28 Mapa de pontos | 49 Posição geográfica |
| 30 Mapa de símbolos proporcionais | 38 Tamanho proporcional · 39 Área proporcional · 49 Posição geográfica |

**Armadilha:** 26 Mapa coroplético.

**Por que essas respostas:** O mapa de calor mostra onde os acidentes se acumulam, sem depender do contorno dos bairros. Pontos e símbolos também mostram os focos.

**Por que a armadilha erra:** Coroplético com total bruto: bairro grande parece perigoso só por ser grande.

### 10 · Fluxo migratório

*Um pesquisador deseja representar os fluxos migratórios entre diferentes estados brasileiros.*

| Visualização aceita (2 pontos) | Variáveis listadas (+1; ★ = preferida, +1) |
|---|---|
| 29 Mapa de fluxos | ★ 48 Espessura de linha · ★ 50 Direção do movimento · 49 Posição geográfica |
| 27 Mapa de calor (origem × destino) | 41 Cor sequencial · 44 Luminosidade · 43 Saturação da cor |

**Armadilha:** 26 Mapa coroplético.

**Por que essas respostas:** Fluxo tem origem, destino e volume: a seta dá o sentido e a espessura, a quantidade. Uma matriz origem × destino em mapa de calor também serve.

**Por que a armadilha erra:** Coroplético mostra o saldo de cada estado, não quem foi para onde.

### 11 · Temperatura regional

*Um meteorologista precisa representar a distribuição espacial da temperatura em um estado.*

| Visualização aceita (2 pontos) | Variáveis listadas (+1; ★ = preferida, +1) |
|---|---|
| 27 Mapa de calor | ★ 41 Cor sequencial · 42 Cor divergente · 44 Luminosidade · 43 Saturação da cor · 49 Posição geográfica |
| 26 Mapa coroplético | 41 Cor sequencial · 42 Cor divergente · 44 Luminosidade · 43 Saturação da cor · 49 Posição geográfica |
| 28 Mapa de pontos | 41 Cor sequencial · 42 Cor divergente · 44 Luminosidade · 49 Posição geográfica |

**Armadilha:** 30 Mapa de símbolos proporcionais.

**Por que essas respostas:** A temperatura muda de forma contínua: o mapa de calor pinta essa superfície. Coroplético (média por município) e pontos (estações) também servem.

**Por que a armadilha erra:** °C não tem zero verdadeiro, então o tamanho do símbolo engana.

### 12 · Acesso ao transporte público

*Uma prefeitura deseja comparar a proporção de moradores atendidos pelo transporte público em diferentes bairros.*

| Visualização aceita (2 pontos) | Variáveis listadas (+1; ★ = preferida, +1) |
|---|---|
| 26 Mapa coroplético | ★ 41 Cor sequencial · 44 Luminosidade · 43 Saturação da cor · 49 Posição geográfica |
| 19 Gráfico de barras (ranking) | 37 Comprimento · 36 Posição vertical · 35 Posição horizontal |

**Armadilha:** 23 Gráfico de pizza, 30 Mapa de símbolos proporcionais.

**Por que essas respostas:** Proporção por bairro é uma taxa: pinte cada bairro numa escala ordenada. Barras servem como ranking.

**Por que a armadilha erra:** Pizza por bairro não compara bairros; símbolos proporcionais servem para totais, não para proporções.

### 13 · Evolução das vendas

*Uma empresa deseja acompanhar o faturamento mensal durante três anos.*

| Visualização aceita (2 pontos) | Variáveis listadas (+1; ★ = preferida, +1) |
|---|---|
| 20 Gráfico de linhas | ★ 36 Posição vertical · 35 Posição horizontal |
| 22 Gráfico de áreas | 36 Posição vertical · 39 Área proporcional · 35 Posição horizontal |
| 19 Gráfico de barras | 37 Comprimento · 36 Posição vertical · 35 Posição horizontal |
| 34 Gráfico de linhas múltiplas (um ano por linha) | 36 Posição vertical · 40 Cor categórica · 35 Posição horizontal |

**Armadilha:** 23 Gráfico de pizza.

**Por que essas respostas:** Tempo no eixo X e valor no Y: a linha mostra a tendência mês a mês. Áreas e barras também servem; linhas múltiplas comparam os três anos.

**Por que a armadilha erra:** Pizza perde a ordem do tempo.

### 14 · Sazonalidade turística

*Uma cidade deseja identificar períodos de maior e menor fluxo turístico ao longo de cinco anos.*

| Visualização aceita (2 pontos) | Variáveis listadas (+1; ★ = preferida, +1) |
|---|---|
| 34 Gráfico de linhas múltiplas | ★ 36 Posição vertical · 40 Cor categórica · 35 Posição horizontal |
| 33 Gráfico de calendário | ★ 41 Cor sequencial · 44 Luminosidade |
| 20 Gráfico de linhas | 36 Posição vertical · 35 Posição horizontal |
| 27 Mapa de calor (ano × mês) | 41 Cor sequencial · 44 Luminosidade |
| 22 Gráfico de áreas | 36 Posição vertical · 39 Área proporcional · 35 Posição horizontal |
| 19 Gráfico de barras | 37 Comprimento · 36 Posição vertical · 35 Posição horizontal |

**Armadilha:** 32 Gráfico de área empilhada.

**Por que essas respostas:** Sazonalidade é um ciclo: uma linha por ano sobreposta, ou um calendário, revela os picos. Mapa de calor ano × mês também.

**Por que a armadilha erra:** Área empilhada soma os anos e esconde o ciclo de cada um.

### 15 · Oscilação de temperatura

*Um pesquisador deseja visualizar a variação da temperatura registrada a cada hora durante uma semana.*

| Visualização aceita (2 pontos) | Variáveis listadas (+1; ★ = preferida, +1) |
|---|---|
| 20 Gráfico de linhas | ★ 36 Posição vertical · 35 Posição horizontal |
| 34 Gráfico de linhas múltiplas (um dia por linha) | 36 Posição vertical · 40 Cor categórica · 35 Posição horizontal |
| 27 Mapa de calor (dia × hora) | 41 Cor sequencial · 44 Luminosidade · 42 Cor divergente |
| 25 Boxplot (um por dia) | 36 Posição vertical · 35 Posição horizontal |

**Armadilha:** 22 Gráfico de áreas.

**Por que essas respostas:** Medidas a cada hora formam uma série contínua: a linha mostra a oscilação. Também servem uma linha por dia, mapa de calor dia × hora e boxplot por dia.

**Por que a armadilha erra:** Áreas sugerem quantidade a partir do zero, e °C não tem zero verdadeiro.

### 16 · Crescimento populacional

*Um município deseja comparar a evolução da população de três bairros ao longo de vinte anos.*

| Visualização aceita (2 pontos) | Variáveis listadas (+1; ★ = preferida, +1) |
|---|---|
| 34 Gráfico de linhas múltiplas | ★ 40 Cor categórica · ★ 36 Posição vertical · 45 Forma geométrica · 47 Textura · 35 Posição horizontal |
| 20 Gráfico de linhas | 40 Cor categórica · 36 Posição vertical · 35 Posição horizontal |
| 32 Gráfico de área empilhada | 40 Cor categórica · 39 Área proporcional · 35 Posição horizontal |

**Armadilha:** 23 Gráfico de pizza.

**Por que essas respostas:** Três séries no mesmo eixo de tempo; a cor ou a posição separam os bairros. Área empilhada vale se o total também interessar.

**Por que a armadilha erra:** Pizza mostra um momento só e perde a evolução.

### 17 · Anomalias financeiras

*Um banco deseja identificar movimentações atípicas no volume diário de transações.*

| Visualização aceita (2 pontos) | Variáveis listadas (+1; ★ = preferida, +1) |
|---|---|
| 25 Boxplot | ★ 36 Posição vertical · ★ 35 Posição horizontal |
| 20 Gráfico de linhas | ★ 36 Posição vertical · 35 Posição horizontal |
| 33 Gráfico de calendário | 41 Cor sequencial · 44 Luminosidade |
| 24 Histograma | 35 Posição horizontal |

**Armadilha:** 23 Gráfico de pizza, 32 Gráfico de área empilhada.

**Por que essas respostas:** O boxplot marca os valores fora do padrão; a linha mostra em que dia aconteceram. Calendário e histograma também revelam os extremos.

**Por que a armadilha erra:** Pizza e área empilhada não mostram um dia fora do padrão.

### 18 · Comparação histórica

*Um analista deseja comparar o consumo mensal de energia elétrica entre dois anos diferentes.*

| Visualização aceita (2 pontos) | Variáveis listadas (+1; ★ = preferida, +1) |
|---|---|
| 34 Gráfico de linhas múltiplas | ★ 40 Cor categórica · ★ 36 Posição vertical · 45 Forma geométrica · 47 Textura · 35 Posição horizontal |
| 19 Gráfico de barras (agrupadas por mês) | 40 Cor categórica · 37 Comprimento · 36 Posição vertical · 35 Posição horizontal |
| 20 Gráfico de linhas | 40 Cor categórica · 36 Posição vertical · 35 Posição horizontal |

**Armadilha:** 32 Gráfico de área empilhada.

**Por que essas respostas:** Dois anos sobrepostos no mesmo eixo de meses: a diferença aparece mês a mês. Barras agrupadas por mês também comparam.

**Por que a armadilha erra:** Área empilhada soma os dois anos, e essa soma não responde à pergunta.

## Cobertura das cartas

Todas as 16 Visualizações e as 16 Variáveis Visuais pontuam em pelo menos um desafio. Oito pontuam em um único desafio: 23 Gráfico de pizza (01), 24 Histograma (17), 29 Mapa de fluxos (10), 32 Gráfico de área empilhada (16), 38 Tamanho proporcional (09), 46 Orientação (03), 48 Espessura de linha (10), 50 Direção do movimento (10).
