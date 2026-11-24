# AGENTS.md — Instruções para agentes de IA

Este arquivo orienta agentes que leem, editam, revisam ou geram arquivos no repositório **Chart Battle**. **Leia também o `README.md` antes de alterar qualquer coisa.** O projeto está em prototipação acadêmica para Visualização de Dados.

## Missão

Preservar e evoluir um jogo físico de cartas competitivo e educativo que ensina escolhas de representação visual para **variáveis visuais**, **dados geoespaciais** e **séries temporais**. Há um HTML estático imprimível, regras decididas pelo grupo (testadas só por simulação) e um gabarito estrito. **Não apresente o protótipo como jogo digital funcional.**

## Fonte de verdade e estado atual

1. `README.md`: descrição, regras, Ações, catálogo, balanceamento por simulação e pontos ainda abertos.
2. `Chart_Battle_102_cartas_A4.html`: **implementação atual** das cartas e do layout imprimível; referência para texto, IDs e duplicação física.
3. `gabarito.md`: gabarito estrito dos 18 desafios (duplas aceitas, dupla preferida, armadilha e justificativas).
4. `Chart_Battle_gabarito_A4.html`: folha imprimível do gabarito, com exatamente os mesmos números e justificativas de `gabarito.md`.
5. `colinha.md` e `Chart_Battle_colinha_A4.html`: regras resumidas para a mesa, em 1 folha; repetem as regras do README com o mesmo texto nos dois arquivos.
6. `AGENTS.md`: restrições e checklist para trabalho de agentes, não substitui o catálogo.

Se houver divergência entre documentação e HTML, **informe a divergência** e proponha a reconciliação; não mude silenciosamente conteúdo, cores ou contagem. Registre ajustes importantes em ambos os documentos quando aplicável.

## Invariantes obrigatórias

| Grupo | IDs estáveis | Modelos | Multiplicador | Total |
|---|---|---:|---:|---:|
| Dados | 01–18 | 18 | ×1 | 18 |
| Visualização | 19–34 | 16 | ×2 | 32 |
| Variáveis Visuais | 35–50 | 16 | ×2 | 32 |
| Ação | 51–60 | 10 | ×2 | 20 |
| **Total** | **01–60** | **60** | — | **102** |

- IDs de 01 a 60 identificam **tipos**, não 102 instâncias numeradas separadamente.
- **Não incluir figuras, gráficos, mapas, ícones ilustrativos ou SVG no corpo das cartas de Dados**; enunciados e títulos apenas. O pequeno símbolo do cabeçalho que identifica a categoria faz parte da identidade visual, não de um exemplo de dados.
- Manter a **cor do cabeçalho e do fundo por categoria**; cores de **gráficos/ilustrações internos são independentes**, sem obrigação de monocromia.
- Paleta **atual do HTML**: Dados azul; Visualização violeta; Variáveis Visuais verde; Ação rosa/magenta. Não misturar identidades entre categorias, nem assumir que toda ilustração deve ter a cor da categoria.
- Manter o idioma `pt-BR`, acentuação, títulos legíveis e sem cortes.
- Preservar os **quatro montes** separados nas regras: Dados (18), Visualização (32), Variável Visual (32) e Ação (20).
- Não declarar como implementado nenhum gabarito, bot, sistema de jogo, pontuação automática ou testes que não existam no repositório.

## HTML e restrições de impressão

- Artefatos: três **HTML/CSS autocontidos**, `Chart_Battle_102_cartas_A4.html` (cartas), `Chart_Battle_gabarito_A4.html` (gabarito) e `Chart_Battle_colinha_A4.html` (colinha), com SVGs inline e sem dependências remotas; devem funcionar offline.
- **A4 retrato: 210 × 297 mm**, margem **interna** de **10 mm** em todos os lados.
- Páginas `.sheet` de 210 × 297 mm e grade `.card-grid` de 190 × 277 mm, com **3 colunas × 3 linhas**.
- Cartões `.card` com **61 × 88 mm** e espaçamento **3 mm**. Máximo 9 por folha, **12 folhas** para 102 cartas.
- A grade `.card-grid` é centralizada na folha (`justify-content` e `align-content: center`): margens efetivas de **10,5 mm** nas laterais e **13,5 mm** em cima e embaixo.
- A folha do gabarito é **uma única página A4**, com a dobra em **105 mm**: à esquerda só números, à direita as justificativas. Não deixe a tabela passar de uma página.
- A colinha também é **uma única página A4**, só frente, sem explicação das Ações (cada carta explica o próprio efeito).
- `@media print` deve ocultar elementos de interface (`.toolbar`, `.notes`) e evitar margens extras e escalas automáticas.
- A regra `@page { size: A4 portrait; margin: 0; }` é intencional: a margem de 1 cm está **dentro da folha**; margens adicionais do navegador prejudicam dimensões.
- Preserve quebras de página, não deixe cartas partidas ou conteúdo cortado. Verifique a última página (3 cartas).
- Nunca rasterizar ilustrações SVG sem necessidade; prefira preservar vetores e texto selecionável.

## Estrutura atual do HTML

- Cada página é `section.sheet` com `div.card-grid`.
- Cada carta é `article.card` com classe de categoria `dados`, `visualizacao`, `variavel` ou `acao`.
- O cabeçalho contém `.cat` e `.num`.
- As cartas de Dados usam `.body.data-only`, `.data-tag`, `h2` e `p` — **sem `.illustration`**.
- As outras usam `h2`, `.illustration` contendo um SVG e `.caption`.
- Não há JavaScript de aplicação; há apenas o botão HTML de impressão (`window.print()`).
- No gabarito, cada desafio é uma linha `tr[data-desafio]`. Visualizações usam `.chip.v`, variáveis `.chip.r` (`.chip.r.star` para a dupla preferida) e armadilhas `.chip.x`.

Se quiser refatorar para geração baseada em dados, preserve a saída HTML estática, as classes de categoria ou um contrato equivalente, e a correspondência 1:1 com os IDs e textos aprovados. Evite introduzir dependências externas desnecessárias.

## Regras e limites de implementação

As regras estão nas seções 3, 4 e 6 do README e foram decididas pelo grupo em 24/11/2026: quatro montes separados; mão de 4 Visualizações, 3 Variáveis Visuais e 1 Ação; todos respondem ao mesmo desafio ao mesmo tempo e justificam em uma frase; quem começou a rodada confere no gabarito estrito; pontos **+2** visualização aceita, **+1** variável listada, **+1** dupla preferida (★); meta de **15 pontos**; uma Ação por rodada; cinco Ações usam um dado de 6 lados. O balanceamento foi testado só por simulação (README, seção 12).

**Nunca invente ou cristalize como definitivo**:

- Mudanças no gabarito sem decisão explícita do grupo. `gabarito.md` e `Chart_Battle_gabarito_A4.html` mudam sempre juntos.
- Mudança de regra sem revisar a colinha. `colinha.md` e `Chart_Battle_colinha_A4.html` mudam sempre juntos.
- Mudanças nas regras ou nos textos das Ações sem decisão explícita do grupo. Ao mudar o texto de uma Ação, atualize juntos o HTML e a seção 6 do README.
- Alegações de que a duração e o balanceamento foram comprovados por playtests: os números do README vêm de simulação.

Ao propor novas regras, indique **“proposta”** e atualize documentação apenas depois de uma decisão explícita ou de um teste registrado. **Aceite múltiplas codificações válidas quando a justificativa e a pergunta de análise permitirem.**

## Critérios científicos/didáticos

- Diferenciar **tipo de gráfico/mapa** de **variável visual** (canal de codificação).
- Associar escolha de visualização ao **objetivo da pergunta**, não somente ao tipo de arquivo/conjunto de dados.
- Mapas coropléticos: cuidado com totais brutos e normalização (taxas, densidades) quando relevante.
- Cor categórica para classes e sequencial/divergente para quantidades ordenadas ou variação em torno de referência, conforme o problema.
- Séries temporais: respeitar ordenação, granularidade e continuidade; não impor linhas para dados que não suportam interpretação contínua.
- Considerar acessibilidade, contraste, leitura em impressão e evitar escalas enganosas.
- Não chamar todo uso de cor de “cor sequencial”; não tratar tamanho de símbolo e área como equivalentes em qualquer situação.

## Fluxo de trabalho recomendado

1. **Inspecione** `README.md` e o HTML, identifique impacto em regras, catálogo, impressão e estilo.
2. **Defina o escopo:** alterações de texto, layout, regras, balanceamento, dados ou geração de novas cartas. Evite mudanças fora do pedido.
3. **Implemente** respeitando os invariantes de contagem, códigos, idioma, margem e paleta.
4. **Valide** a estrutura; se alterar layout, confira visualmente PDF ou pré-visualização de impressão em A4.
5. **Documente** decisões e limitações. Explique resultados com clareza e não alegue ter testado o que não testou.

## Checklist mínimo de validação

- [ ] Exatamente **102** ocorrências de `article.card` e **12** `section.sheet`.
- [ ] Classes de categoria: `dados=18`, `visualizacao=32`, `variavel=32`, `acao=20`.
- [ ] Exatamente **60 IDs distintos**: 01–18 uma vez e 19–60 duas vezes.
- [ ] Todas as cartas têm cabeçalho com categoria, número, título e texto adequado.
- [ ] **Nenhuma carta de Dados contém `.illustration` ou SVG de figura**.
- [ ] As ilustrações internas podem ter diferentes cores; layout por categoria permanece consistente.
- [ ] Cada folha mantém A4 e a margem interna de **10 mm**.
- [ ] Nenhum texto aparece fora da borda ou cortado na impressão.
- [ ] HTML abre offline sem imagens ou bibliotecas externas.
- [ ] README e AGENTS refletem alterações relevantes de contrato/escopo.
- [ ] Textos das Ações iguais no HTML e na seção 6 do README.
- [ ] `gabarito.md` só usa números e nomes de cartas que existem no HTML.
- [ ] `gabarito.md` e `Chart_Battle_gabarito_A4.html` têm os mesmos números (verificação abaixo), e a folha cabe em 1 página A4.
- [ ] A colinha segue as regras do README, tem o mesmo texto em `colinha.md` e no HTML, e cabe em 1 página A4.

### Exemplo de verificação rápida (Python + BeautifulSoup, se disponível)

```python
from collections import Counter
from bs4 import BeautifulSoup

html = open("Chart_Battle_102_cartas_A4.html", encoding="utf-8").read()
soup = BeautifulSoup(html, "html.parser")
cards = soup.select("article.card")
assert len(cards) == 102
assert len(soup.select("section.sheet")) == 12

counts = Counter(
    next(c for c in ("dados", "visualizacao", "variavel", "acao") if c in card["class"])
    for card in cards
)
assert counts == {"dados": 18, "visualizacao": 32, "variavel": 32, "acao": 20}

ids = Counter(int(card.select_one(".num").get_text(strip=True)) for card in cards)
assert set(ids) == set(range(1, 61))
assert all(ids[i] == (1 if i <= 18 else 2) for i in range(1, 61))
assert all(card.select_one(".illustration") is None for card in soup.select(".card.dados"))
```

**Observação:** o exemplo depende de `beautifulsoup4` apenas para verificação local; **não** é dependência do HTML em produção e não implica que um sistema de testes esteja implementado no repositório.

### Verificação do gabarito (`gabarito.md` × folha HTML)

```python
import re
from bs4 import BeautifulSoup

md = open("gabarito.md", encoding="utf-8").read()
key_md = {}
for sec in re.split(r"^### (?=\d{2} · )", md, flags=re.M)[1:]:
    rows = re.findall(r"^\| (\d{2}) [^|]+\| (.+) \|$", sec, flags=re.M)
    acc = {int(v): [(int(r), bool(s)) for s, r in re.findall(r"(★ )?(\d{2}) ", vs + " ")] for v, vs in rows}
    traps = [int(t) for t in re.findall(r"(\d{2}) ", re.search(r"\*\*Armadilha:\*\* (.+)", sec).group(1))]
    key_md[int(sec[:2])] = (acc, traps)

soup = BeautifulSoup(open("Chart_Battle_gabarito_A4.html", encoding="utf-8").read(), "html.parser")
key_html = {}
for tr in soup.select("tr[data-desafio]"):
    acc = {}
    for grp in tr.select(".grp"):
        v = int(grp.select_one(".chip.v").get_text())
        acc[v] = [(int(c.get_text().lstrip("★")), "star" in c["class"]) for c in grp.select(".chip.r")]
    key_html[int(tr["data-desafio"])] = (acc, [int(c.get_text()) for c in tr.select(".chip.x")])

assert sorted(key_md) == list(range(1, 19))
assert key_md == key_html, "gabarito.md e Chart_Battle_gabarito_A4.html divergem"
```

## Prioridades para contribuições futuras

1. **Playtests reais** com 2, 3, 4 e 6 pessoas, registrando duração, dúvidas de regra e desafios difíceis.
2. **Ajustes no gabarito e nas regras** a partir dos playtests, sempre com decisão do grupo.
3. **Automação da geração** das cartas a partir de fonte estruturada, se útil.
4. Verso das cartas, identidade visual de corte, testes automatizados e acessibilidade.

## Comunicação de mudanças

Ao concluir uma tarefa, informe: **o que mudou**, **quais arquivos foram afetados**, **como foi verificado** e **o que continua pendente**. Se uma sugestão contradiz requisitos do usuário ou dados existentes, sinalize e solicite decisão em vez de substituir silenciosamente a especificação.
