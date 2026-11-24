# Chart Battle — Batalha dos Gráficos

Jogo educativo e competitivo de cartas para a disciplina de **Visualização de Dados**, com foco em **variáveis visuais**, **visualização de dados geoespaciais** e **visualização de séries temporais**.

> **Status do projeto:** protótipo físico em desenvolvimento. O baralho de 102 cartas já está representado em um HTML estático para impressão; as regras e a pontuação abaixo são a proposta atual, ainda sujeita a testes. **Não há gabarito completo nem mecanismo de validação automática implementado.**

## 1. Conceito e objetivo

Em cada rodada, uma carta de **Dados** apresenta uma situação de análise (por exemplo, comparar a densidade populacional dos bairros ou identificar uma tendência temporal). Os participantes disputam pontos formando combinações de **Visualização** + **Variável Visual** que façam sentido para o problema, enquanto cartas de **Ação** alteram o andamento da partida.

O objetivo educativo não é decorar um único gráfico correto, mas justificar escolhas de representação, reconhecer alternativas aceitáveis e discutir seus limites. O objetivo competitivo proposto é **ser o primeiro a alcançar 15 pontos**, respeitando as regras de encerramento e desempate descritas abaixo.

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

A sugestão de faixa para o protótipo é **2–6 jogadores**, com duração estimada de **15–25 minutos** (ainda não aferida em partidas reais).

## 3. Preparação da partida (proposta)

1. Separe as **18 cartas de Dados** em um monte exclusivo, embaralhado e virado para baixo.
2. Embaralhe as **84 cartas dos jogadores** (32 de Visualização, 32 de Variáveis Visuais e 20 de Ação) em outro monte.
3. Distribua **5 cartas do monte dos jogadores para cada participante**.
4. Deixe um espaço central para o desafio revelado e outro para o descarte das cartas dos jogadores.
5. Escolha o jogador inicial e revele a primeira carta de Dados.

**Atenção ao balanceamento:** o monte misto pode distribuir mãos com poucas cartas combináveis, já que inclui Ações. Esse aspecto precisa ser testado; futuras versões podem separar ou controlar o número inicial de cada tipo de carta.

## 4. Como jogar (regras propostas)

### Uma rodada

1. **Revelar o desafio:** apresente uma carta de Dados e leia o problema em voz alta.
2. **Propor uma representação:** seguindo a ordem de turnos, cada participante pode baixar **1 carta de Visualização + 1 carta de Variável Visual** que, juntas, respondam ao desafio, ou passar.
3. **Justificar:** o jogador explica brevemente por que a escolha atende à pergunta e que propriedade dos dados será codificada pela variável visual.
4. **Avaliar:** compare a proposta com o gabarito do desafio (ainda a produzir); diferentes combinações podem ser aceitas, desde que justificadas.
5. **Aplicar a pontuação:** registre a pontuação obtida conforme a tabela abaixo.
6. **Repor a mão:** após resolver as jogadas, cada jogador que utilizou cartas compra do monte dos jogadores até retornar a **5 cartas**, caso haja cartas disponíveis.
7. **Encerrar a rodada:** descarte o desafio utilizado e revele outro para a próxima rodada.

Como as cartas de Ação são parte do baralho, sua utilização deve seguir a indicação de timing da seção 6. Uma partida pode terminar antes de esgotar os 18 desafios.

### Pontuação proposta

| Condição | Pontos |
|---|---:|
| Escolha de Visualização adequada ao desafio | +2 |
| Escolha de Variável Visual adequada à representação e ao desafio | +1 |
| Combinação preferencial, conforme critérios do desafio | +1 bônus |
| Combinação totalmente inadequada | 0 |

- Uma jogada pode somar **0 a 4 pontos**; o bônus só existe se os critérios forem satisfeitos.
- Uma representação pode ser **válida sem ser a preferida**; o gabarito deve explicar essa diferença.
- O conjunto de critérios precisa ser escrito e testado para impedir avaliações arbitrárias ou contraditórias.
- O jogador que chegar a **15 pontos** vence. Se mais de um atingir o limite na mesma rodada e houver empate na maior pontuação, realize um **desafio de desempate**. Caso o monte de Dados se esgote, vence a maior pontuação, com desempate da mesma forma.

### Exemplo de rodada

**Desafio 07 — Densidade populacional:** comparar a densidade populacional entre bairros de uma cidade.

Uma proposta plausível é **Mapa coroplético (26)** + **Cor sequencial (41)**: cada bairro é uma área geográfica e uma escala ordenada de cores representa a densidade. Essa é uma **combinação de exemplo**, não um registro de gabarito oficial finalizado. Um gráfico de barras poderia ser defensável caso a ênfase fosse exclusivamente a comparação de bairros, e não sua posição no espaço.

## 5. Regras de interpretação e avaliação

- **Comece pela pergunta de análise:** o mesmo conjunto de dados pode admitir visualizações diferentes para objetivos diferentes.
- **Dados categóricos vs. quantitativos:** cor categórica/forma pode distinguir grupos; comprimento/posição ou cor sequencial pode representar quantidade, conforme a técnica.
- **Regiões geográficas:** mapas coropléticos devem usar, em geral, **taxas ou medidas normalizadas** para comparações entre áreas de tamanhos/populações diferentes, quando isso for pertinente. Densidade populacional é um exemplo adequado.
- **Mapas de pontos e fluxos:** a localização dos pontos e o sentido das setas têm papéis diferentes de tamanho e intensidade.
- **Séries temporais:** posições ordenadas no eixo temporal e escolhas de escala/granularidade alteram a leitura da tendência e da sazonalidade.
- **Não confundir técnica e variável:** “gráfico de linhas” é uma representação; “posição vertical” é um canal visual. Algumas combinações são possíveis, mas pouco informativas; é preciso justificar a codificação.
- **Acessibilidade e honestidade:** contraste, semântica das cores, escalas e distorções devem ser considerados na avaliação.

**Pendente para tornar o jogo plenamente reproduzível:** criar uma matriz/gabarito de compatibilidade para todos os 18 desafios, com combinações aceitas, preferenciais, inadequadas e respectivas justificativas. O verso das cartas de Dados **não** contém atualmente esse gabarito no HTML.

## 6. Cartas de Ação

Há **10 modelos**, cada um com **2 cópias**. Seus efeitos impressos já estão definidos (tabela abaixo). O seguinte protocolo de uso é **provisório**, para permitir testes: no seu turno, o jogador pode usar até **uma** Ação antes de propor a combinação; ela vai para o descarte após resolver o efeito. As ações que se referem à próxima jogada, como Pontos Dobrados, podem permanecer como lembrete até serem consumidas. Ações que criam novos desafios precisam de regras de desempate e descarte consistentes.

**Decisões ainda a validar:** se Ação substitui ou acompanha a jogada; quando exatamente pode ser usada; como tratar Bloqueio quando só há dois participantes; o que acontece com um desafio substituído; e como resolver a falta de cartas para compra. Até o playtest, priorize o texto de cada carta e o consenso da mesa.

| ID | Carta | Aplicação / efeito | Cópias |
|---|---|---|---:|
| 51 | Troca de Mão | Troque suas cartas com outro jogador. | 2 |
| 52 | Compra Forçada | Escolha um adversário para comprar duas cartas. | 2 |
| 53 | Bloqueio | Impeça um adversário de participar da próxima rodada. | 2 |
| 54 | Segunda Chance | Tente uma nova combinação após uma resposta inadequada. | 2 |
| 55 | Pontos Dobrados | Dobre os pontos obtidos na sua próxima combinação válida. | 2 |
| 56 | Desafio Surpresa | Substitua o desafio atual por outro do baralho. | 2 |
| 57 | Roubo de Carta | Retire aleatoriamente uma carta da mão de outro jogador. | 2 |
| 58 | Troca Estratégica | Descarte até três cartas e compre a mesma quantidade. | 2 |
| 59 | Desafio Direto | Escolha um adversário para competir em um novo desafio; quem pontuar mais ganha dois pontos adicionais. | 2 |
| 60 | Visão Privilegiada | Consulte as respostas aceitas de um desafio antes de jogar suas cartas. | 2 |

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
| 38 | Tamanho proporcional | Magnitude por tamanho. | 2 |
| 39 | Área proporcional | Quantidades por área. | 2 |
| 40 | Cor categórica | Diferenciação de grupos. | 2 |
| 41 | Cor sequencial | Valores numéricos ordenados. | 2 |
| 42 | Cor divergente | Valores em torno de uma referência. | 2 |
| 43 | Saturação da cor | Variação de intensidade. | 2 |
| 44 | Luminosidade | Ordenação por claro e escuro. | 2 |
| 45 | Forma geométrica | Diferenciação de categorias. | 2 |
| 46 | Orientação | Distinção visual por direção. | 2 |
| 47 | Textura | Diferenciação por padrões. | 2 |
| 48 | Espessura de linha | Codificação de intensidade ou magnitude. | 2 |
| 49 | Posição geográfica | Localização por coordenadas. | 2 |
| 50 | Direção do movimento | Indicação de sentido de fluxos. | 2 |

Alguns itens (por exemplo, **área proporcional** e **tamanho proporcional**) têm sobreposição conceitual deliberada no protótipo; as definições podem ser refinadas para evitar ambiguidade. Além disso, mapas e séries temporais podem exigir **mais de um canal visual** na prática, mesmo que a mecânica inicial peça uma só carta de Variável Visual.

## 8. Arquivo HTML e impressão

O artefato imprimível atual é [`Chart_Battle_102_cartas_A4.html`](./Chart_Battle_102_cartas_A4.html). Trata-se de um **documento HTML estático e autocontido**, com CSS e ilustrações vetoriais inline; **não é um jogo digital interativo** e não implementa regras, pontuação ou validação.

### Características técnicas já presentes

- **102 cartas** distribuídas em **12 páginas A4** com até **9 cartas por página**, na grade de 3 colunas × 3 linhas (11 páginas completas e uma página com 3 cartas).
- Página A4 retrato (**210 × 297 mm**), com **margem interna de 10 mm** em CSS.
- Cada carta mede aproximadamente **61 × 88 mm**; espaçamento entre cartas de **3 mm**.
- Cores do layout por categoria: **Dados = azul-escuro/azul-claro**, **Visualização = violeta/lilás**, **Variáveis Visuais = verde/verde-claro**, **Ação = rosa/magenta-rosado**.
- As cores das **figuras internas são livres** e **não devem ser forçadas à paleta do cabeçalho**.
- **Dados sem figuras**; outras categorias com ilustrações SVG.
- Barra de impressão no navegador e estilos específicos para `@media print`.

### Como imprimir ou exportar PDF

1. Baixe/abra `Chart_Battle_102_cartas_A4.html` em um navegador moderno.
2. Clique em **Imprimir / Salvar em PDF** (ou use `Ctrl+P`).
3. Selecione **A4**, **retrato**, **100%** de escala e **sem margens adicionais** no navegador (o documento já reserva 1 cm em cada lado).
4. Ative **gráficos/cores de fundo**, quando o navegador oferecer essa opção.
5. Desative cabeçalhos e rodapés gerados pelo navegador; confira a pré-visualização antes de cortar.
6. Recorte as cartas pelas bordas. Para cartas opacas e duráveis, use papel mais firme, plástico protetor ou sleeves.

**Nota:** o CSS usa `@page { size: A4 portrait; margin: 0 }` para que a folha incorpore a própria margem de 10 mm. A margem física e a escala devem ser verificadas em impressão-teste. Não imprimir com “ajustar à página” se isso redimensionar as cartas.

## 9. Estrutura mínima sugerida do repositório

```text
chart-battle/
├── README.md
├── AGENTS.md
└── Chart_Battle_102_cartas_A4.html
```

Ainda não há sistema de build, framework JavaScript, testes automatizados, arquivos de dados separados ou licença definida. Uma evolução possível é extrair as 60 definições para um JSON/YAML e gerar o HTML a partir de um template, mantendo gabarito e regras versionados.

## 10. Próximas etapas

- [ ] Definir e revisar a **matriz de compatibilidade** das 18 cartas de Dados com cartas de Visualização e Variável Visual.
- [ ] Fixar o momento de uso e resolução das **10 Ações**, inclusive casos de disputa e falta de cartas.
- [ ] Realizar playtests com **2, 3, 4 e 6 pessoas**, registrando duração, taxa de mãos sem combinação e frequência de ações.
- [ ] Ajustar balanceamento do monte de 84 cartas e a meta de 15 pontos conforme evidências.
- [ ] Revisar a precisão conceitual dos exemplos de visualização e suas legendas.
- [ ] Testar impressão real em A4, conferindo margem de 1 cm, corte e legibilidade.
- [ ] Opcional: criar o **verso das cartas**, manual de regras diagramado e fichas de pontuação.
- [ ] Opcional: automatizar a geração do baralho, o gabarito e os testes estruturais.

## 11. Convenções do projeto

- **Idioma:** português brasileiro (`pt-BR`).
- **Numeração estável:** IDs 01–60; replicar modelos **19–60 exatamente duas vezes** e **01–18 uma vez**.
- **Princípio didático:** valorizar justificativa e adequação ao objetivo, não apenas respostas por associação mecânica.
- **Escopo:** projeto acadêmico de prototipação, não produto finalizado ou jogo digital completo.

---

*Documento alinhado ao protótipo HTML atual e às decisões de design registradas até 23/11/2026.*
