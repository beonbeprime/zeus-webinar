# Guia de Formatação Nativa WhatsApp

## Formatação de Texto

| Efeito | Sintaxe | Exemplo |
|--------|---------|---------|
| Negrito | *texto* | *Evento ao vivo hoje!* |
| Itálico | _texto_ | _Vagas limitadas_ |
| Riscado | ~texto~ | ~Preço normal R$997~ |
| Monospace | ```texto``` | ```Link: bit.ly/evento``` |

## Regras Obrigatórias

### Tamanho por Tipo
- Lembretes de evento: máx 300 caracteres
- Mensagens de aquecimento: 200-500 caracteres
- Mensagens de conteúdo: até 800 caracteres
- Nunca mais de 1.200 caracteres em uma mensagem

### Emojis
- Máx 3 emojis por mensagem
- Usar no início ou final de frase (nunca no meio de palavras)
- Emojis de alta conversão para webinários: 🎯 🔥 ⚡ 🚀 💡 ✅ 📌 ⏰ 🎁

### Horários
- NUNCA enviar entre 22h e 07h
- Lembretes: preferir 08h, 18h ou 20h
- Urgência: 10h e 20h no dia de fechamento

### Quebra de Parágrafos
- Máx 2-3 linhas por parágrafo
- Linha em branco entre parágrafos
- Nunca bloco de texto corrido

---

## Templates Validados

### Boas-vindas ao Grupo
```
Olá, pessoal! 👋

Bem-vindos ao grupo *[NOME DO EVENTO]*.

Aqui vou compartilhar conteúdo exclusivo antes do evento e manter vocês informados sobre tudo.

Vai ser incrível. Animados?
```

### Lembrete D-1
```
⏰ *Amanhã é o grande dia!*

[Nome do evento] começa às [hora]h.

Bloqueia na agenda agora para não perder.

Nos vemos lá!
```

### Lembrete D-0 (2h antes)
```
🔥 Em *2 horas* começa!

Acesse pelo link: [link]

Chega antes do horário para pegar o lugar na frente. 😄
```

### Lembrete D-0 (30min)
```
⚡ *Começando em 30 minutos!*

Link de acesso: [link]

Quem vai assistir ao vivo, manda um ✅ aqui!
```

### Abertura do Carrinho (D+1)
```
🎁 *O replay está no ar!*

E o carrinho está aberto por tempo limitado.

Assiste aqui: [link-replay]

Garante sua vaga aqui: [link-checkout]

Carrinho fecha [data] à meia-noite.
```

### Urgência Penúltimo Dia
```
⏰ *Carrinho fecha amanhã!*

Depois disso não tem como entrar no [produto].

Se ainda está em dúvida, me chama no privado. 💬

Link para garantir: [link]
```

### Último Dia
```
🚨 *HOJE É O ÚLTIMO DIA!*

O carrinho fecha à meia-noite.

_Não vou conseguir fazer exceção depois disso._

Garante aqui: [link]
```

---

## Checklist de Qualidade (verificar antes de enviar)

- [ ] Formatação correta (asteriscos, underscores)?
- [ ] Máx 3 emojis?
- [ ] Tamanho adequado para o tipo de mensagem?
- [ ] Horário de envio entre 07h e 22h?
- [ ] Link presente quando necessário?
- [ ] Linha em branco entre parágrafos?
- [ ] Não tem travessão (—) ou outros caracteres especiais?

---

## Formatos de Mídia Suportados

| Tipo | Formato | Uso no Webinário |
|------|---------|-----------------|
| Imagem | JPG, PNG (máx 16MB) | Cards de aquecimento, prova social |
| Vídeo | MP4 (máx 16MB) | Teaser do evento, depoimentos curtos |
| Áudio | MP3, OGG | Mensagem de voz do expert |
| Documento | PDF (máx 100MB) | Material de aquecimento, workbook |
| Link | URL direta | Sempre usar texto âncora, não URL nua |

## Evolution API — Endpoints Relevantes

```bash
# Enviar texto
POST /message/sendText/{instance}
{
  "number": "GROUP_ID@g.us",
  "text": "mensagem"
}

# Enviar imagem
POST /message/sendMedia/{instance}
{
  "number": "GROUP_ID@g.us",
  "mediatype": "image",
  "media": "URL_ou_base64",
  "caption": "legenda"
}

# Buscar grupos
GET /group/fetchAllGroups/{instance}?getParticipants=false
```
