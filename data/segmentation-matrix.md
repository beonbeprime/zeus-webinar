# Matriz de Segmentacao Pos-Webinario

Framework de segmentacao por comportamento para follow-up inteligente.
Agentes responsaveis: crm-operations-specialist + followup-specialist + commercial-strategist.

---

## Principio Central

Follow-up aleatorio desperdiça recursos e irrita a audiencia.
Follow-up por comportamento maximiza conversao e respeita o momento de cada pessoa.

Regra: Priorizar quem demonstrou maior intencao de compra (ficou mais tempo, clicou no link, fez pergunta sobre preco).

---

## Segmentos Primarios (por comportamento no evento)

### Segmento 1 - QUENTE (prioridade maxima)

Criterio: Assistiu ao vivo + ficou ate o pitch + clicou no link de vendas mas nao comprou

| Campo | Detalhe |
|-------|---------|
| Perfil | Alta intencao de compra, objecao especifica impediu |
| Tamanho esperado | 5-15% dos presentes |
| Janela de oportunidade | 24h apos o evento |
| Canal prioritario | WhatsApp 1:1 > Email personalizado |
| Mensagem | "Oi [NOME], vi que voce acompanhou o webinario de perto. Ficou com alguma duvida sobre [PRODUTO]?" |
| Objetivo | Identificar e remover a objecao especifica |
| Follow-up maximo | 3 tentativas em 72h |

### Segmento 2 - MORNO-QUENTE

Criterio: Assistiu ao vivo + ficou ate o pitch + NAO clicou no link

| Campo | Detalhe |
|-------|---------|
| Perfil | Assistiu o pitch mas nao demonstrou interesse imediato |
| Tamanho esperado | 20-30% dos presentes |
| Janela de oportunidade | 24-48h apos o evento |
| Canal prioritario | Email sequencia + WhatsApp de grupo |
| Mensagem | Replay com prazo de urgencia + depoimento de aluno |
| Objetivo | Reengajar com replay e criar urgencia |
| Follow-up maximo | 4 emails em 5 dias |

### Segmento 3 - MORNO

Criterio: Assistiu ao vivo mas saiu antes do pitch (antes do bloco 8)

| Campo | Detalhe |
|-------|---------|
| Perfil | Interessado no conteudo mas nao chegou na oferta |
| Tamanho esperado | 20-40% dos inscritos |
| Janela de oportunidade | 48h apos o evento |
| Canal prioritario | Email com resumo do que perdeu + link replay |
| Mensagem | "Voce assistiu a maior parte do webinario mas precisou sair antes do encerramento. Separei o trecho que voce perdeu..." |
| Objetivo | Fazer assistir o pitch no replay |
| Follow-up maximo | 3 emails em 4 dias |

### Segmento 4 - FRIO (inscrito que nao apareceu)

Criterio: Se inscreveu mas nao assistiu ao vivo

| Campo | Detalhe |
|-------|---------|
| Perfil | Interesse inicial mas sem comprometimento de tempo |
| Tamanho esperado | 50-70% dos inscritos (benchmark: 30-50% comparecem) |
| Janela de oportunidade | 24h apos o evento |
| Canal prioritario | Email sequencia + WhatsApp de grupo |
| Mensagem | "Oi [NOME], voce se inscreveu mas nao pode participar. Ficou o replay disponivel por [PRAZO]." |
| Objetivo | Converter pelo replay |
| Follow-up maximo | 3 emails em 3 dias |

### Segmento 5 - COMPRADORES (apenas nurturing)

Criterio: Comprou durante ou apos o evento

| Campo | Detalhe |
|-------|---------|
| Perfil | Ja e cliente - foco em onboarding e satisfacao |
| Tamanho esperado | 3-15% dos presentes (benchmark de conversao) |
| Janela de oportunidade | Imediato - ate 2h apos a compra |
| Canal prioritario | Email de boas-vindas + WhatsApp de suporte |
| Mensagem | Email de boas-vindas com acesso, proximos passos e ponto de contato |
| Objetivo | Onboarding rapido + prevencao de chargeback |
| Follow-up | Sequencia de onboarding do produto (7-14 dias) |

---

## Segmentos Secundarios (por perfil de engajamento)

### Sub-segmento A - Perguntou sobre preco durante o evento

- Inclui em: Segmento 1 (QUENTE) independente do comportamento geral
- Acao adicional: Resposta 1:1 direta com link de vendas

### Sub-segmento B - Comentou muito no chat / interagiu

- Inclui em: Um nivel acima do seu segmento (Morno vira Quente, Frio vira Morno)
- Acao adicional: Mencionar interacao especifica na mensagem 1:1

### Sub-segmento C - Assistiu o replay mas nao comprou

- Criterio: Abriu o email de replay e assistiu (rastreado pelo pixel)
- Coloca em: Segmento 1 (QUENTE) com urgencia do prazo do replay
- Acao: Mensagem 1:1 na ultima hora antes do prazo fechar

---

## Fluxo de Automacao por Segmento

```
Evento encerrado
|
+-- [COMPROU] -> Fluxo onboarding (sai do follow-up comercial)
|
+-- [ASSISTIU + CLICOU] -> Segmento 1 - WhatsApp 1:1 em 2h
|
+-- [ASSISTIU + NAO CLICOU] -> Verificar saiu antes/depois do pitch
|   |
|   +-- [Saiu antes do bloco 8] -> Segmento 3 - Email "voce perdeu o melhor"
|   |
|   +-- [Ficou ate o pitch] -> Segmento 2 - Email replay + urgencia
|
+-- [NAO ASSISTIU] -> Segmento 4 - Email replay imediato
```

---

## Templates de Mensagem por Segmento

### Segmento 1 - WhatsApp 1:1 (enviar em 1-2h)

```
Oi [NOME]! Tayoba aqui (ou [ESPECIALISTA]).

Vi que voce acompanhou tudo hoje e queria saber: ficou com alguma duvida sobre [PRODUTO]?

Frequentemente as pessoas ficam na duvida sobre [OBJECAO COMUM 1] ou [OBJECAO COMUM 2].

Posso te ajudar a clarear qualquer coisa. E so responder aqui.

O link ainda esta ativo por [PRAZO]: [LINK]
```

### Segmento 4 - Email (enviar em 30 min apos encerrar)

Assunto: "[NOME], o webinario ja acabou - mas o replay ficou para voce"

```
Oi [NOME],

Sei que nem sempre da pra participar ao vivo - a vida nao para.

Por isso gravei tudo e separei o replay especialmente para quem se inscreveu mas nao pode estar la.

O replay fica disponivel por [PRAZO] horas. Depois disso, sai do ar.

Acesse aqui: [LINK REPLAY]

[NOME DO ESPECIALISTA]

P.S. Dentro do replay tem uma oferta especial que eu fiz para quem estava ao vivo. Ela tambem vale para quem assistir o replay - mas so ate [PRAZO].
```

---

## Downsell - Quando e Para Quem

Acionar downsell apenas para Segmentos 1, 2 e 3 que nao converteram apos o follow-up principal.

| Gatilho | Timing | Produto do downsell |
|---------|--------|-------------------|
| Nao comprou apos 3 toques no Segmento 1 | 72h apos o evento | Versao lite ou produto mais barato |
| Segmento 2 nao converteu apos replay | 5 dias apos o evento | Ticket 50-70% do principal |
| Segmento 3 nao viu o replay | 6 dias apos o evento | Modulo avulso ou workshop |

Regra: downsell so faz sentido se o ticket alternativo for genuinamente util para o perfil. Nao e desistencia - e inteligencia comercial.

---

## KPIs de Segmentacao

| Metrica | Benchmark | Alerta |
|---------|-----------|--------|
| Taxa de conversao Segmento 1 | 20-40% | < 15% |
| Taxa de conversao Segmento 2 via replay | 8-15% | < 5% |
| Taxa de conversao Segmento 4 via replay | 3-8% | < 2% |
| Taxa de downsell | 5-15% dos nao convertidos | < 3% |
| Tempo medio de resposta 1:1 | < 2h pos-evento | > 6h |

Arquivo de registro e atualizacao: `data/project-registry.yaml`.
