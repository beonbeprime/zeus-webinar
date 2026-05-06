# Templates de Públicos Meta Ads para Webinários

## Estrutura de Públicos por Temperatura

### Públicos Frios (topo de funil — fase captação)

#### Camada 1 — Interesse Direto
Interesses que tocam diretamente no assunto do produto:
- Buscar por: nome do produto/tema + sinônimos
- Ex: "empreendedorismo", "negócios online", "marketing digital"
- Tamanho ideal: 500k - 2M pessoas por conjunto

#### Camada 2 — Interesse Adjacente
Interesses relacionados mas não diretos — pessoas com problemas similares:
- Ex: para "mentoria de negócios": "gestão de pequenas empresas", "finanças pessoais"
- Diversifica o topo de funil sem perder qualidade

#### Camada 3 — Comportamento
Comportamentos de compra e uso que indicam perfil:
- "Compradores engajados"
- "Pequenas empresas" (se B2B)
- Dispositivos usados (celular de última geração = maior poder de compra)

---

### Públicos Mornos (meio de funil — fase remarketing)

#### Engajamento com Perfil
- Pessoas que interagiram com o Instagram/Facebook nos últimos 30-60 dias
- Vídeo views: pessoas que assistiram 50%+ dos vídeos
- Salvamentos e compartilhamentos

#### Visitantes do Site
- Visitantes da LP nos últimos 30 dias sem inscrição
- Visitantes da página de checkout sem compra (se tiver pixel)

---

### Públicos Quentes (fundo de funil — conversão)

#### Listas Próprias
- Lista de emails de leads (upload CSV)
- Lista de clientes anteriores
- Lista de participantes de eventos anteriores

#### Lookalike
- LK 1% dos compradores = público mais qualificado
- LK 2-3% para escalar mantendo qualidade
- Nunca usar lookalike de lista genérica — sempre de compradores

---

## Templates por Nicho

### Negócios / Empreendedorismo
```yaml
publico_frio:
  interesses_diretos:
    - Empreendedorismo
    - Marketing digital
    - Negócios online
    - Administração de empresas
  interesses_adjacentes:
    - LinkedIn
    - Finanças pessoais
    - Produtividade
  faixa_etaria: 28-55
  genero: Todos

publico_morno:
  retargeting_site: 30 dias
  engajamento_perfil: 60 dias
  video_views: 50%+, últimos 30 dias

publico_quente:
  lista_leads: upload CSV
  lookalike_compradores: 1-3%
```

### Saúde e Bem-estar
```yaml
publico_frio:
  interesses_diretos:
    - Saúde e bem-estar
    - Nutrição
    - Fitness
    - Meditação
  interesses_adjacentes:
    - Culinária saudável
    - Yoga
    - Autocuidado
  faixa_etaria: 22-50
  genero: Feminino (70%) / Masculino (30%) — validar com dados

publico_morno:
  retargeting_site: 14 dias
  engajamento_perfil: 30 dias

publico_quente:
  lista_leads: upload CSV
  lookalike_compradores: 1-2%
```

### Carreira / Profissional
```yaml
publico_frio:
  interesses_diretos:
    - Desenvolvimento de carreira
    - Recursos humanos
    - Treinamento profissional
    - LinkedIn Learning
  interesses_adjacentes:
    - Liderança
    - Gestão de projetos
    - Soft skills
  faixa_etaria: 25-45
  genero: Todos

publico_morno:
  retargeting_site: 30 dias
  engajamento_perfil: 45 dias

publico_quente:
  lista_leads: upload CSV
  lookalike_compradores: 1-3%
```

---

## Exclusões Obrigatórias por Fase

### Fase Captação (públicos frios)
- Excluir: compradores existentes
- Excluir: inscritos que já converteram

### Fase Remarketing (públicos mornos)
- Excluir: compradores existentes
- Excluir: leads que já compraram

### Fase Carrinho (públicos quentes)
- Excluir: compradores existentes
- Manter: leads que assistiram mas não compraram

---

## Nomenclatura Padrão (naming convention)

```
[EVENTO] | [FASE] | [TEMPERATURA] | [PÚBLICO] | [CRIATIVO]

Exemplos:
WEB-VENDAS | CAP | FRIO | INT-EMPREEND | VID-HOOK01
WEB-VENDAS | RMK | MORNO | ENG-60D | CAR-DEPO01
WEB-VENDAS | CART | QUENTE | LK1-COMP | IMG-URG01
```

Fases: CAP (captação), AQC (aquecimento), RMK (remarketing), CART (carrinho)
Temperaturas: FRIO, MORNO, QUENTE
Tipos de criativo: VID (vídeo), CAR (carrossel), IMG (imagem estática)

---

## Orçamento Mínimo por Fase

| Fase | % do total | Mínimo diário por conjunto | Observação |
|------|-----------|---------------------------|------------|
| Captação | 60% | R$20/conjunto | Começar com 2-3 conjuntos |
| Remarketing | 25% | R$15/conjunto | Ativar em D-7 |
| Carrinho | 15% | R$30/conjunto | Concentrar no último dia |
