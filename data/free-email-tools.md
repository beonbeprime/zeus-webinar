# Ferramentas de Email Gratuitas para Webinários

## Ferramenta Padrão: Brevo (ex-Sendinblue)

### Por que Brevo?
- 300 emails/dia gratuito para sempre (sem expiração)
- Automação de email incluída no plano gratuito
- Interface em português
- Suporte a triggers (inscrição → sequência inicia automaticamente)
- Sem limite de contatos no plano gratuito
- Templates de email com editor visual

### Como Configurar
1. Criar conta: brevo.com
2. Verificar domínio de envio (DNS TXT e DKIM)
3. Importar lista: Contatos → Importar CSV (campos: email, FIRSTNAME, data_inscricao)
4. Criar automação: Automações → Criar fluxo → trigger "Contato adicionado à lista"
5. Adicionar emails com delay (ex: E1=0 dias, E2=4 dias, E3=6 dias, etc.)
6. Configurar horário de envio em cada etapa

### Limites do Plano Gratuito
- 300 emails/dia
- Contatos ilimitados
- 9.000 emails/mês
- Automações incluídas
- Sem A/B test (plano pago)

### Para Webinários Grandes (>300 inscritos/dia)
- Brevo Starter: R$30-60/mês (20.000 emails/mês)
- Ou distribuir envios em horários diferentes (spread the 300/day)

---

## Alternativa 1: MailerLite

### Plano Gratuito
- 1.000 contatos
- 12.000 emails/mês
- Automações incluídas
- Interface mais moderna que Mailchimp

### Quando Usar
- Webinários com até 1.000 inscritos
- Prefere interface mais visual
- Precisa de landing pages integradas

### Como Configurar
1. Criar conta: mailerlite.com
2. Verificar domínio
3. Criar grupo "Webinar [nome]"
4. Criar automação com trigger "Adicionado ao grupo"
5. Adicionar emails com delay em dias

---

## Alternativa 2: Mailchimp

### Plano Gratuito (muito limitado)
- 500 contatos
- 1.000 emails/mês
- Automações apenas no plano pago

### Não Recomendado Para
- Sequências automáticas completas (requer plano pago)
- Webinários com mais de 500 inscritos

---

## Alternativa 3: ActiveCampaign (14 dias gratuito)

### Quando Usar
- Teste de sequência completa em até 14 dias
- Projeto de curto prazo sem custo
- Migrar para pago após validação

### Plano Pago Mínimo
- $15/mês para até 1.000 contatos
- Automações avançadas + CRM incluídos

---

## Comparativo

| Ferramenta | Emails/mês grátis | Contatos | Automação | Recomendação |
|-----------|------------------|----------|-----------|--------------|
| Brevo | 9.000 (300/dia) | Ilimitados | Sim | PADRÃO |
| MailerLite | 12.000 | 1.000 | Sim | Alternativa |
| Mailchimp | 1.000 | 500 | Não (grátis) | Evitar |
| ActiveCampaign | 14 dias trial | - | Sim | Teste rápido |

---

## Estrutura CSV para Import

```
email,FIRSTNAME,data_inscricao,webinar_nome
joao@email.com,João,2026-06-15,Webinar Vendas
maria@email.com,Maria,2026-06-15,Webinar Vendas
```

## Configuração de SPF/DKIM (obrigatório para entregabilidade)

No painel DNS do domínio, adicionar:
- TXT: `v=spf1 include:spf.brevo.com ~all`
- CNAME: `mail._domainkey` → valor fornecido pelo Brevo

Sem isso, emails vão para spam.
