# Chart Battle — Batalha dos Gráficos

Jogo educativo e competitivo de cartas para a disciplina de **Visualização de Dados**, com foco em **variáveis visuais**, **visualização de dados geoespaciais** e **visualização de séries temporais**.

> **Status do projeto:** protótipo físico em desenvolvimento. O baralho de 102 cartas já está representado em um HTML estático para impressão; as regras abaixo foram decididas pelo grupo e testadas por simulação (seção 12), mas ainda não em partidas reais. O gabarito dos 18 desafios está em [`gabarito.md`](./gabarito.md); **não há mecanismo de validação automática implementado.**

## 1. Conceito e objetivo

Em cada rodada, uma carta de **Dados** apresenta uma situação de análise (por exemplo, comparar a densidade populacional dos bairros ou identificar uma tendência temporal). Os participantes disputam pontos formando combinações de **Visualização** + **Variável Visual** que façam sentido para o problema, enquanto cartas de **Ação** alteram o andamento da partida.

O objetivo educativo não é decorar um único gráfico correto, mas justificar escolhas de representação, reconhecer alternativas aceitáveis e discutir seus limites. O objetivo competitivo é **chegar a 15 pontos**: a partida termina no fim da rodada em que alguém alcança a meta, e vence quem tiver mais pontos (seção 4).

### Conteúdos da disciplina

- **Variáveis visuais:** posição, comprimento, área, tamanho, cor, luminosidade, saturação, forma, orientação, textura e outras codificações.
- **Dados geoespaciais:** localização, densidade, distribuição espacial, mapas coropléticos, mapas de pontos e fluxos.
- **Séries temporais:** tendências, sazonalidade, variações, anomalias e comparação de séries.

## 2. Componentes e quantidades

| Categoria | IDs | Modelos únicos | Cópias por modelo | Cartas físicas |
|---|---|---:|---:|---:|
| Dados (desafios) | 01–18 | 18 | 1 | 18 |
| Visualização | 19–34 | 16 | 2 | 32 |
| Variáveis Visuais | 35–50 | 16 | 2 | 32 |
| Ação | 51–60 | 10 | 2 | 20 |
| **Total** | **01–60** | **60** | — | **102** |

**Importante:** os IDs representam **modelos de carta**, não instâncias únicas. Por exemplo, existem duas cartas físicas de ID 19 (Gráfico de barras), mas apenas uma de ID 01 (Distribuição de categorias).

Além das cartas, a partida usa:

- **1 folha de gabarito**, impressa de [`Chart_Battle_gabarito_A4.html`](./Chart_Battle_gabarito_A4.html) e dobrada ao meio (o mesmo conteúdo está em [`gabarito.md`](./gabarito.md));
- **1 dado de 6 lados**, usado por cinco cartas de Ação;
- **papel e caneta** para o placar.

A faixa sugerida é de **2 a 6 jogadores**. Pela simulação (seção 12), uma partida até 15 pontos dura de 8 a 10 rodadas, cerca de 20 a 30 minutos se cada rodada levar de 2 a 3,5 minutos. Esse tempo ainda não foi medido em partidas reais.

## 3. Preparação da partida

1. Separe as cartas em **quatro montes**, cada um embaralhado e virado para baixo: **Dados** (18), **Visualização** (32), **Variável Visual** (32) e **Ação** (20).
2. Cada jogador recebe **4 Visualizações, 3 Variáveis Visuais e 1 Ação**.
3. Deixe a folha do gabarito dobrada, com as justificativas para trás, junto com o dado e uma folha para o placar.
4. Todos rolam o dado, e quem tirar o maior número começa. Se houver empate, os empatados rolam de novo.

## 4. Como jogar

Todos respondem ao mesmo desafio ao mesmo tempo. Quem começa a rodada revela o desafio e confere as respostas; essa vez passa para a esquerda a cada rodada.

### Uma rodada

1. **Aposta (opcional):** antes de revelar o desafio, quem quiser usar **Pontos Dobrados** coloca a carta na mesa.
2. **Revelar o desafio:** quem começa vira a carta do topo do monte de Dados e lê o problema em voz alta.
3. **Ações:** a partir de quem começa e seguindo para a esquerda, cada jogador pode usar **uma** Ação (seção 6).
4. **Escolher:** cada jogador separa **1 Visualização + 1 Variável Visual** e as deixa viradas para baixo. Todo mundo joga uma dupla em toda rodada; não existe passar.
5. **Revelar e justificar:** todos viram as cartas ao mesmo tempo, e cada um justifica a sua dupla em uma frase. A justificativa não vale pontos.
6. **Conferir:** quem começou a rodada olha a linha do desafio na folha do gabarito, ainda dobrada, e diz os pontos de cada um. Depois abre a dobra e lê em voz alta por que as respostas valem e por que a armadilha erra.
7. **Segunda Chance:** quem fez 0 e tem a carta Segunda Chance pode jogar outra dupla, conferida do mesmo jeito.
8. **Fechar a rodada:**
   - anote os pontos no placar;
   - as cartas jogadas vão para o descarte do seu tipo, e o desafio sai do jogo;
   - cada jogador completa a mão até ter 4 Visualizações e 3 Variáveis; quem tiver mais não descarta;
   - quem fez 0 na rodada compra 1 Ação, se tiver menos de 2;
   - a vez de começar passa para o jogador à esquerda.

### Pontuação

O gabarito é **estrito**: só pontuam as duplas listadas em [`gabarito.md`](./gabarito.md), sem defesa nem votação.

| Condição | Pontos |
|---|---:|
| Visualização aceita no desafio | 2 |
| Variável listada na linha dessa visualização | +1 |
| Dupla preferida (★) | +1 |
| Visualização fora da lista | 0 |

- Uma dupla vale 0, 2, 3 ou 4 pontos. Pontos Dobrados e Desafio Direto podem somar mais (seção 6).
- A variável só pontua junto com uma visualização aceita.

### Fim da partida e empate

- A partida termina no fim da rodada em que alguém chega a **15 pontos**, e vence quem tiver mais pontos.
- Em caso de empate, só os empatados jogam mais um desafio. Se empatarem de novo, dividem a vitória.
- Se os desafios acabarem antes, vence quem tiver mais pontos, com o mesmo desempate. Isso não aconteceu nas simulações.

### Falta de cartas

Se o monte de Visualização, Variável ou Ação acabar, embaralhe o descarte daquele tipo para formar um monte novo.

### Exemplo de rodada

**Desafio 07, Densidade populacional:** comparar a densidade populacional entre os bairros de uma cidade.

- Ana joga **Mapa coroplético (26) + Cor sequencial (41)** e faz 4 pontos: cada bairro é uma área, e uma escala ordenada de cores mostra a densidade. É a dupla preferida (★).
- Caio joga **Gráfico de barras (19) + Comprimento (37)** e faz 3 pontos: o gabarito aceita barras como ranking dos bairros, quando a posição no espaço não importa.
- Lia joga **Mapa de símbolos proporcionais (30) + Tamanho proporcional (38)** e faz 0: é a armadilha, porque símbolos proporcionais servem para totais, não para taxas como a densidade.

## 5. Regras de interpretação e avaliação

Estes princípios orientaram o gabarito. Na mesa, vale o que está em [`gabarito.md`](./gabarito.md).

- **Comece pela pergunta de análise:** o mesmo conjunto de dados pode admitir visualizações diferentes para objetivos diferentes.
- **Dados categóricos vs. quantitativos:** cor categórica/forma pode distinguir grupos; comprimento/posição ou cor sequencial pode representar quantidade, conforme a técnica.
- **Regiões geográficas:** mapas coropléticos devem usar, em geral, **taxas ou medidas normalizadas** para comparações entre áreas de tamanhos/populações diferentes, quando isso for pertinente. Densidade populacional é um exemplo adequado.
- **Mapas de pontos e fluxos:** a localização dos pontos e o sentido das setas têm papéis diferentes de tamanho e intensidade.
- **Séries temporais:** posições ordenadas no eixo temporal e escolhas de escala/granularidade alteram a leitura da tendência e da sazonalidade.
- **Não confundir técnica e variável:** “gráfico de linhas” é uma representação; “posição vertical” é um canal visual. Algumas combinações são possíveis, mas pouco informativas; é preciso justificar a codificação.
- **Acessibilidade e honestidade:** contraste, semântica das cores, escalas e distorções devem ser considerados na avaliação.

**Gabarito:** as duplas aceitas, a dupla preferida e a armadilha de cada um dos 18 desafios, com justificativas, estão em [`gabarito.md`](./gabarito.md). O verso das cartas de Dados **não** contém o gabarito.

## 6. Cartas de Ação

Há **10 modelos**, com **2 cópias** cada.

### Quando usar

- Cada jogador pode usar **uma Ação por rodada**, na sua vez, depois da revelação do desafio e antes da escolha das duplas.
- Há duas exceções de momento, e as duas contam como a Ação da rodada: **Pontos Dobrados** é usada antes da revelação, como aposta, e **Segunda Chance**, depois da conferência.
- A Ação usada vai para o descarte de Ações.
- Cada jogador começa com 1 Ação. Quem fizer 0 numa rodada compra 1 Ação no fim dela, se tiver menos de 2.
- Com 2 jogadores, todas as Ações continuam no jogo.

### Efeitos

| ID | Carta | Texto da carta | Detalhes |
|---|---|---|---|
| 51 | Troca de Mão | Troque suas cartas com um adversário. Ele rola o dado: com 5 ou 6, escapa. | Trocam-se as Visualizações e as Variáveis; as Ações ficam com cada um. Se o alvo escapar, a carta é gasta mesmo assim. |
| 52 | Compra Extra | Role o dado e compre 1 carta (1–2), 2 (3–4) ou 3 (5–6), de Visualização ou de Variável, como quiser. | As cartas extras ficam na mão; a reposição nunca obriga a descartar. |
| 53 | Bloqueio | Impeça um adversário de jogar a próxima rodada. Ele rola o dado: com 5 ou 6, escapa. | O bloqueado fica fora da rodada inteira: não aposta, não usa nem compra Ação e não joga dupla. Se fosse a vez dele de começar, começa quem está à esquerda. |
| 54 | Segunda Chance | Tente uma nova combinação após uma resposta inadequada. | Só depois da conferência, se a sua dupla valeu 0. A nova dupla é conferida normalmente. |
| 55 | Pontos Dobrados | Antes de revelar o desafio, aposte: se a sua dupla desta rodada pontuar, os pontos dobram. | Se a dupla não pontuar, a carta é perdida. Vale também para a dupla da Segunda Chance; os +2 do Desafio Direto não dobram. |
| 56 | Desafio Surpresa | Substitua o desafio atual por outro do baralho. | O novo desafio vale para todos; o antigo vai para o fundo do monte de Dados. |
| 57 | Roubo de Carta | Todos os adversários rolam o dado. Quem tirar 1 ou 2 entrega a você 1 carta ao acaso. | A carta sai da mão inteira do adversário e pode ser uma Ação. |
| 58 | Troca Estratégica | Descarte até três cartas e compre a mesma quantidade. | Compre do mesmo tipo das descartadas (Visualização ou Variável). |
| 59 | Desafio Direto | Escolha um adversário. Nesta rodada, quem fizer mais pontos entre vocês dois ganha +2. Empate com pontos: rolem o dado. | Se os dois fizerem 0, ninguém ganha. No empate com pontos, quem tirar mais no dado leva os +2; se empatar no dado, rolem de novo. |
| 60 | Visão Privilegiada | Consulte as respostas aceitas de um desafio antes de jogar suas cartas. | Olhe sozinho a linha do desafio da rodada na folha dobrada, sem abrir as justificativas. |

## 7. Catálogo completo de cartas

### 7.1 Dados — 18 cartas únicas

Seis desafios tratam de codificação/percepção visual (01–06), seis de geoespacialidade (07–12) e seis de séries temporais (13–18). **As cartas de Dados não contêm figuras** no HTML; somente identificação, título e enunciado.

| ID | Carta | Desafio | Cópias |
|---|---|---|---:|
| 01 | Distribuição de categorias | Uma loja deseja comparar a quantidade de produtos vendidos em cinco categorias diferentes. | 1 |
| 02 | Diferenças de magnitude | Uma empresa precisa representar a receita de dez departamentos, destacando diferenças quantitativas. | 1 |
| 03 | Identificação de grupos | Uma pesquisa contém indivíduos pertencentes a quatro grupos distintos. É necessário diferenciá-los visualmente. | 1 |
| 04 | Valores positivos e negativos | Uma empresa deseja representar lucros e prejuízos de suas filiais. | 1 |
| 05 | Correlação entre variáveis | Um pesquisador deseja investigar a relação entre horas de estudo e notas obtidas. | 1 |
| 06 | Destaque de informações | Um analista precisa destacar três produtos com desempenho abaixo da meta em um conjunto de vinte produtos. | 1 |
| 07 | Densidade populacional | Uma prefeitura deseja comparar a densidade populacional entre os bairros de uma cidade. | 1 |
| 08 | Distribuição de hospitais | Uma secretaria de saúde deseja visualizar a localização dos hospitais em uma região. | 1 |
| 09 | Concentração de acidentes | Um órgão de trânsito deseja identificar áreas com maior concentração de acidentes. | 1 |
| 10 | Fluxo migratório | Um pesquisador deseja representar os fluxos migratórios entre diferentes estados brasileiros. | 1 |
| 11 | Temperatura regional | Um meteorologista precisa representar a distribuição espacial da temperatura em um estado. | 1 |
| 12 | Acesso ao transporte público | Uma prefeitura deseja comparar a proporção de moradores atendidos pelo transporte público em diferentes bairros. | 1 |
| 13 | Evolução das vendas | Uma empresa deseja acompanhar o faturamento mensal durante três anos. | 1 |
| 14 | Sazonalidade turística | Uma cidade deseja identificar períodos de maior e menor fluxo turístico ao longo de cinco anos. | 1 |
| 15 | Oscilação de temperatura | Um pesquisador deseja visualizar a variação da temperatura registrada a cada hora durante uma semana. | 1 |
| 16 | Crescimento populacional | Um município deseja comparar a evolução da população de três bairros ao longo de vinte anos. | 1 |
| 17 | Anomalias financeiras | Um banco deseja identificar movimentações atípicas no volume diário de transações. | 1 |
| 18 | Comparação histórica | Um analista deseja comparar o consumo mensal de energia elétrica entre dois anos diferentes. | 1 |

### 7.2 Visualização — 16 modelos, 2 cópias cada

| ID | Carta | Aplicação / efeito | Cópias |
|---|---|---|---:|
| 19 | Gráfico de barras | Comparar categorias. | 2 |
| 20 | Gráfico de linhas | Evolução temporal. | 2 |
| 21 | Gráfico de dispersão | Relação entre variáveis. | 2 |
| 22 | Gráfico de áreas | Evolução de magnitudes. | 2 |
| 23 | Gráfico de pizza | Proporções de um total. | 2 |
| 24 | Histograma | Distribuição de frequências. | 2 |
| 25 | Boxplot | Distribuição e valores extremos. | 2 |
| 26 | Mapa coroplético | Valores associados a regiões. | 2 |
| 27 | Mapa de calor | Intensidade em uma matriz ou espaço. | 2 |
| 28 | Mapa de pontos | Localização de ocorrências. | 2 |
| 29 | Mapa de fluxos | Deslocamentos entre regiões. | 2 |
| 30 | Mapa de símbolos proporcionais | Magnitudes em localizações. | 2 |
| 31 | Gráfico de bolhas | Relação entre variáveis e magnitude. | 2 |
| 32 | Gráfico de área empilhada | Evolução de componentes de um total. | 2 |
| 33 | Gráfico de calendário | Padrões ao longo dos dias. | 2 |
| 34 | Gráfico de linhas múltiplas | Comparação de séries temporais. | 2 |

### 7.3 Variáveis Visuais — 16 modelos, 2 cópias cada

| ID | Carta | Aplicação / efeito | Cópias |
|---|---|---|---:|
| 35 | Posição horizontal | Valores em um eixo X. | 2 |
| 36 | Posição vertical | Valores em um eixo Y. | 2 |
| 37 | Comprimento | Comparação de magnitudes. | 2 |
| 38 | Tamanho proporcional | Magnitude pelo tamanho de símbolos (círculos, ícones). | 2 |
| 39 | Área proporcional | Quantidades pela área de fatias, faixas ou regiões. | 2 |
| 40 | Cor categórica | Diferenciação de grupos. | 2 |
| 41 | Cor sequencial | Valores numéricos ordenados. | 2 |
| 42 | Cor divergente | Valores em torno de uma referência. | 2 |
| 43 | Saturação da cor | Variação de intensidade. | 2 |
| 44 | Luminosidade | Ordenação por claro e escuro. | 2 |
| 45 | Forma geométrica | Diferenciação de categorias. | 2 |
| 46 | Orientação | Diferenciação pela inclinação da marca. | 2 |
| 47 | Textura | Diferenciação por padrões. | 2 |
| 48 | Espessura de linha | Codificação de intensidade ou magnitude. | 2 |
| 49 | Posição geográfica | Localização por coordenadas. | 2 |
| 50 | Direção do movimento | Indicação de sentido de fluxos. | 2 |

**Tamanho proporcional** (38) vale para símbolos, como círculos e ícones; **Área proporcional** (39), para fatias, faixas e regiões. **Orientação** (46) é a inclinação da marca; **Direção do movimento** (50), o sentido de um fluxo. Além disso, mapas e séries temporais podem exigir **mais de um canal visual** na prática, mesmo que a mecânica peça uma só carta de Variável Visual.

## 8. Arquivos HTML e impressão

Há dois arquivos para imprimir, ambos **HTML estáticos e autocontidos**, com CSS e ilustrações vetoriais inline, que funcionam sem internet:

- [`Chart_Battle_102_cartas_A4.html`](./Chart_Battle_102_cartas_A4.html): as 102 cartas, em 12 folhas;
- [`Chart_Battle_gabarito_A4.html`](./Chart_Battle_gabarito_A4.html): o gabarito, em 1 folha.

Nenhum dos dois **é um jogo digital interativo** nem implementa regras, pontuação ou validação.

### Características técnicas já presentes

- **102 cartas** distribuídas em **12 páginas A4** com até **9 cartas por página**, na grade de 3 colunas × 3 linhas (11 páginas completas e uma página com 3 cartas).
- Página A4 retrato (**210 × 297 mm**), com **margem interna de 10 mm** em CSS. A grade das cartas fica centralizada: **10,5 mm** nas laterais e **13,5 mm** em cima e embaixo.
- Cada carta mede aproximadamente **61 × 88 mm**; espaçamento entre cartas de **3 mm**.
- Cores do layout por categoria: **Dados = azul-escuro/azul-claro**, **Visualização = violeta/lilás**, **Variáveis Visuais = verde/verde-claro**, **Ação = rosa/magenta-rosado**.
- As cores das **figuras internas são livres** e **não devem ser forçadas à paleta do cabeçalho**.
- **Dados sem figuras**; outras categorias com ilustrações SVG.
- Barra de impressão no navegador e estilos específicos para `@media print`.

### Folha do gabarito

Uma folha A4 com uma linha tracejada no meio. À esquerda ficam só números: o desafio, as visualizações aceitas com as suas variáveis (★ marca a dupla preferida) e a armadilha. À direita ficam as justificativas. Depois de imprimir, dobre a folha para trás na linha tracejada: quem confere vê só os números e abre a dobra para ler os porquês.

### Como imprimir ou exportar PDF

1. Baixe/abra o arquivo em um navegador moderno.
2. Clique em **Imprimir / Salvar em PDF** (ou use `Ctrl+P`).
3. Selecione **A4**, **retrato**, **100%** de escala e **sem margens adicionais** no navegador (o documento já reserva a margem).
4. Ative **gráficos/cores de fundo**, quando o navegador oferecer essa opção.
5. Desative cabeçalhos e rodapés gerados pelo navegador; confira a pré-visualização antes de cortar.
6. Recorte as cartas pelas bordas. Para cartas opacas e duráveis, use papel mais firme, plástico protetor ou sleeves. A folha do gabarito não é recortada, só dobrada.

**Nota:** o CSS usa `@page { size: A4 portrait; margin: 0 }` para que a folha incorpore a própria margem de 10 mm. A margem física e a escala devem ser verificadas em impressão-teste. Não imprimir com “ajustar à página” se isso redimensionar as cartas. No PDF gerado pelo Firefox em 24/11/2026, as medidas conferem: 12 páginas de cartas com as margens acima e o gabarito em 1 página.

## 9. Estrutura mínima sugerida do repositório

```text
chart-battle/
├── README.md
├── AGENTS.md
├── gabarito.md
├── Chart_Battle_102_cartas_A4.html
├── Chart_Battle_gabarito_A4.html
└── 2026_2_Jogos_enunciado.pdf
```

Ainda não há sistema de build, framework JavaScript, testes automatizados, arquivos de dados separados ou licença definida. Uma evolução possível é extrair as 60 definições para um JSON/YAML e gerar o HTML a partir de um template, mantendo gabarito e regras versionados.

## 10. Próximas etapas

- [x] Definir e revisar a **matriz de compatibilidade** das 18 cartas de Dados com cartas de Visualização e Variável Visual ([`gabarito.md`](./gabarito.md)).
- [x] Fixar o momento de uso e resolução das **10 Ações**, inclusive casos de disputa e falta de cartas (seções 4 e 6).
- [ ] Realizar playtests com **2, 3, 4 e 6 pessoas**, registrando duração, taxa de mãos sem combinação e frequência de ações. A simulação já foi feita (seção 12); faltam partidas reais.
- [x] Ajustar o balanceamento dos montes e a meta de 15 pontos, por simulação (seção 12).
- [x] Revisar a precisão conceitual dos exemplos de visualização e suas legendas: histograma, boxplot, mapa de calor, saturação, direção do movimento, cor única nos canais visuais e legendas 38, 39 e 46.
- [ ] Testar impressão real em A4, conferindo margem, corte e legibilidade. O PDF pelo Firefox foi conferido em 24/11/2026; falta imprimir em papel.
- [ ] Opcional: criar o **verso das cartas**, manual de regras diagramado e fichas de pontuação.
- [ ] Opcional: automatizar a geração do baralho, o gabarito e os testes estruturais.

## 11. Convenções do projeto

- **Idioma:** português brasileiro (`pt-BR`).
- **Numeração estável:** IDs 01–60; replicar modelos **19–60 exatamente duas vezes** e **01–18 uma vez**.
- **Princípio didático:** valorizar justificativa e adequação ao objetivo, não apenas respostas por associação mecânica.
- **Escopo:** projeto acadêmico de prototipação, não produto finalizado ou jogo digital completo.

## 12. Balanceamento (simulação)

As regras das seções 3, 4 e 6 foram escolhidas com uma simulação de Monte Carlo: milhares de partidas por cenário, com jogadores que às vezes erram a melhor dupla e com o gabarito de [`gabarito.md`](./gabarito.md). O script da simulação não faz parte do repositório. **Simulação não substitui playtest:** os números abaixo mostram tendências, não o comportamento de uma turma real.

### Por que as regras mudaram

Com as regras anteriores (monte único de 84 cartas, mão de 5, jogadas em ordem):

- 17% das mãos iniciais não formavam nenhuma dupla, e a mão inicial respondia só 25% dos desafios;
- 87% das jogadas valiam 0, uma média de 0,34 ponto por jogador por rodada;
- em 62% a 87% das partidas, os 18 desafios acabavam antes de alguém chegar a 15 pontos.

Com os quatro montes e a mão de 4 Visualizações + 3 Variáveis, a mão inicial responde 53% dos desafios, 47% das jogadas valem 0, cada jogador faz cerca de 1,4 ponto por rodada e todas as partidas simuladas terminaram pela meta.

### Duração com meta de 15 pontos

| Jogadores | Rodadas (mediana) | 80% das partidas | Empate no topo |
|---|---:|---|---:|
| 2 | 10 | 7 a 13 | 3% |
| 3 | 9 | 7 a 12 | 5% |
| 4 | 9 | 7 a 11 | 6% |
| 6 | 8 | 6 a 10 | 7% |

### Peso do conhecimento

Um jogador que sempre escolhe a melhor dupla da mão vence 39% das partidas de 4 jogadores (o acaso daria 25%) e 64% das partidas de 2 (o acaso daria 50%). O que mais pesa é ter a visualização certa na mão.

### Dificuldade dos desafios

A chance de a mão inicial ter uma dupla que pontua vai de 23% a 24% nos desafios 02 e 06, que só aceitam barras, até 86% no desafio 14. A média é 52%.

### Força das Ações

Chance de vencer de quem começa a partida com a carta. Sem carta extra, a chance é de 25% com 4 jogadores e de 50% com 2.

| Carta | 4 jogadores | 2 jogadores |
|---|---:|---:|
| Pontos Dobrados | 34% | 57% |
| Desafio Direto | 31% | 53% |
| Troca de Mão | 30% | 58% |
| Troca Estratégica | 30% | 55% |
| Desafio Surpresa | 29% | 55% |
| Bloqueio | 27% | 56% |
| Compra Extra | 27% | 52% |
| Roubo de Carta | 26% | 50% |
| Segunda Chance | 26% | 52% |
| Visão Privilegiada | 25% | 52% |

Decisões que vieram daí:

- **Compra Forçada** virou **Compra Extra**. Como estava, ela dava cartas ao adversário e subia a chance dele de responder de 53% para 61% a 68%.
- **Pontos Dobrados** virou aposta. Dobrando a próxima dupla válida, quem começava com ela vencia de 37% a 42% das partidas de 4.
- **Troca de Mão** e **Bloqueio** ganharam a defesa no dado. Sem ela, com 2 jogadores, levavam a chance de vencer a 61% e 59%.
- **Roubo de Carta** virou uma rolagem coletiva, para pôr o dado em jogo; a força dela quase não mudou.
- **Segunda Chance** e **Visão Privilegiada** continuam fracas, mas não atrapalham, e a Visão Privilegiada tem valor didático.

---

*Documento alinhado ao protótipo HTML atual e às decisões de design registradas até 24/11/2026.*
