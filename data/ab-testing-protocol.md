# Protocolo de A/B Testing - Webinario Infalivel

Guia operacional para testar, medir e otimizar cada etapa do funil de webinario.
Agente responsavel: diagnostics-specialist + metrics-analyst.

---

## Principios do A/B Testing no Webinario

1. Testar UMA variavel por vez - nunca mudar headline E cor ao mesmo tempo
2. Minimo de trafego para significancia: 100 cliques por variante antes de decidir
3. Testar em sequencia, nao simultaneamente (webinario e ao vivo, nao split real)
4. Registrar TUDO - data, variante, resultado, decisao
5. Vencedor vira controle e o proximo teste parte dele

---

## O que Testar e em que Ordem

### PRIORIDADE 1 - Pagina de Captura (maior impacto no volume)

| Elemento | Variante A (controle) | Variante B (challenger) | Metrica |
|----------|----------------------|------------------------|---------|
| Headline principal | Versao atual | Versao com verbo diferente | Taxa de captura (%) |
| Subheadline | Com prazo | Sem prazo | Taxa de captura (%) |
| CTA do formulario | "Quero participar gratuitamente" | "Garantir minha vaga" | Taxa de captura (%) |
| Foto/imagem | Especialista sorrindo | Especialista sério | Taxa de captura (%) |
| Cor do botao | Botao atual | Botao com cor de contraste | Cliques no CTA (%) |
| Formato do formulario | Nome + Email | Apenas Email | Taxa de captura (%) |

Benchmark: taxa de captura minima 25%. Se abaixo, testar headline primeiro.

### PRIORIDADE 2 - Email de Confirmacao e Lembretes (impacto no comparecimento)

| Elemento | Variante A | Variante B | Metrica |
|----------|-----------|-----------|---------|
| Assunto email confirmacao | "Sua vaga esta confirmada!" | "[NOME], sua vaga para [EVENTO] esta garantida" | Abertura (%) |
| Assunto lembrete D-1 | "Amanha e o dia!" | "Lembrete: [EVENTO] e amanha as [HORA]" | Abertura e clique (%) |
| Assunto lembrete D-0 | "E hoje! Acesse agora" | "[NOME], o webinario comeca em 2 horas" | Abertura e clique (%) |
| Formato do email | Texto simples | HTML com design | CTR (%) |
| Incluir agenda | Com agenda detalhada | Sem agenda | CTR (%) |

Benchmark: abertura emails 30%+, CTR 10%+.

### PRIORIDADE 3 - Criativos de Captacao (impacto no CPL)

| Elemento | Variante A | Variante B | Metrica |
|----------|-----------|-----------|---------|
| Hook 0-3s | Pergunta direta | Statement chocante | CTR (%) |
| Formato | Video falando para camera | Video com texto sobre imagem | CPL (R$) |
| CTA no criativo | "Clique para se inscrever" | "Garanta sua vaga gratuita" | CTR e CPL |
| Angulo da dor | Medo de perder algo | Desejo de ganhar algo | CTR e qualidade do lead |
| Duracao do video | Video curto 15s | Video longo 60s | CPL e show rate |

Benchmark: CPL < R$10, CTR > 2%.

### PRIORIDADE 4 - Roteiro do Webinario (impacto na conversao)

| Elemento | Variante A | Variante B | Metrica |
|----------|-----------|-----------|---------|
| Duracao do conteudo | 60 min conteudo | 45 min conteudo | Retencao no pitch |
| Transicao bloco 7 > 8 | Transicao direta | Transicao com story pessoal | Audiencia no pitch (%) |
| Ancoragem de preco | Valor total R$X | Comparacao "custa menos que Y" | Taxa de conversao (%) |
| Numero de bonus | 2 bonus | 4 bonus | Taxa de conversao (%) |
| Garantia | 7 dias | 30 dias | Taxa de conversao (%) |

Benchmark: conversao 3%+ dos presentes no pitch.

### PRIORIDADE 5 - Pagina de Replay (impacto no faturamento pos-evento)

| Elemento | Variante A | Variante B | Metrica |
|----------|-----------|-----------|---------|
| Prazo do replay | 24h | 48h | Conversao replay (%) |
| Mensagem urgencia | Contador regressivo | Texto de prazo | CTR e conversao |
| Posicao do CTA | CTA acima do video | CTA abaixo do video | Cliques (%) |
| Bonus extra replay | Sem bonus adicional | Bonus exclusivo para quem assistiu replay | Conversao replay (%) |

---

## Protocolo de Decisao

### Quando mudar a variante

Mudar para a Variante B quando:
- Variante B tem performance >= 20% melhor que A
- Minimo de 100 cliques ou 3 webinarios completos avaliados
- Melhora e consistente (nao apenas em 1 edicao)

Manter Variante A quando:
- Diferenca menor que 10%
- Resultado inconsistente entre edicoes
- Variante B tem CPL melhor mas show rate pior (avaliar impacto no funil completo)

### Registro obrigatorio de cada teste

```yaml
teste:
  id: "AB-001"
  data_inicio: "YYYY-MM-DD"
  data_fim: "YYYY-MM-DD"
  elemento_testado: "Headline pagina de captura"
  variante_a: "Aprenda como criar seu primeiro webinario"
  variante_b: "Crie seu primeiro webinario em 90 minutos"
  edicoes_testadas: 3
  resultado_a:
    metrica: taxa_captura
    valor: "23%"
  resultado_b:
    metrica: taxa_captura
    valor: "31%"
  decisao: "Variante B venceu - +35% de captura"
  novo_controle: "Variante B"
  proximo_teste: "Subheadline com prazo"
```

---

## Cadencia de Testes

| Semana | Foco | Elemento |
|--------|------|---------|
| 1 | Pagina de captura | Headline |
| 2 | Pagina de captura | CTA do formulario |
| 3 | Email de lembrete | Assunto do D-0 |
| 4 | Criativo | Hook 0-3s |
| 5 | Roteiro | Transicao bloco 7 > 8 |
| 6 | Oferta | Numero de bonus |
| 7 | Replay | Prazo de disponibilizacao |
| 8 | Consolidar aprendizados | - |

Repetir ciclo com novos desafios a partir das fraquezas identificadas.

---

## Metricas de Controle por Fase

| Fase | Metrica Primaria | Metrica Secundaria |
|------|-----------------|-------------------|
| Captacao | CPL | Taxa de captura |
| Pre-evento | Taxa de abertura email | CTR de lembretes |
| Evento | % audiencia no pitch | Conversao presentes |
| Replay | Conversao replay | CTR replay |
| Comercial | Conversao follow-up 1:1 | Downsell rate |
| ROAS total | ROAS consolidado | CAC por canal |

Arquivo de registro: `data/project-registry.yaml` (aba ab-tests).
