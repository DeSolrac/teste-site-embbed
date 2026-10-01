# teste-site-embbed

Site de teste para validar o embed do motor de reservas HMAX em domínio externo (GitHub Pages).

**URL pública:** https://desolrac.github.io/teste-site-embbed/

## Como usar

1. No dashboard STG do HMAX (https://stg-hmax-dashboard.web.app), abra a propriedade do hotel que você quer testar
2. Vá na aba **"Site próprio (Embed)"** — habilite o toggle
3. Em **Domínios autorizados**, adicione: `desolrac.github.io`
4. Salve
5. Edite [`index.html`](./index.html) deste repo e troque `SLUG_DO_HOTEL` pelo slug real do hotel
6. Commit + push — o GitHub Pages republica em ~1 min
7. Abra https://desolrac.github.io/teste-site-embbed/ e teste

## Ambiente

- Widget servido por: `https://stg-hmax-widget.web.app/widget.js`
- API STG: `https://dev-channel-manager-api-bjt7hfa5oa-uc.a.run.app`
- Dash STG: `https://stg-hmax-dashboard.web.app`

Tudo em **STG** — não afeta produção.

## Troubleshooting

| Sintoma | Causa provável |
|---|---|
| Widget não renderiza | Domínio `desolrac.github.io` não foi adicionado na lista de domínios autorizados |
| Erro de "hotel desconhecido" | `SLUG_DO_HOTEL` não foi trocado pelo slug real |
| Erro CORS no console | Módulo mestre "Reservas no Site Próprio" não foi habilitado no dash (ação de SUPER_ADMIN) |

## Links

- Task: HMAXX-4601 (ClickUp)
- PR: https://github.com/hmax-web/hmax-booking-dashboard/pull/748
