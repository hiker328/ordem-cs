# Setup de credenciais — Churn Radar — Score de Risco de Churn + Playbook por Faixa

**Nenhuma credencial necessária.** Esta solução é paste-based: você só cola a lista de clientes e os critérios de cada um (pagamento, engajamento, resultado, relacionamento, tempo de casa) na conversa. Nada conecta em conta, nada pede token, nada sai do seu controle.

> Versão "auto" (alimentar o score puxando os critérios direto dos seus sistemas) é um upgrade opcional de implementação. Aí sim entraria uma conexão — sempre com as credenciais do SEU próprio ambiente, geradas por você, nunca embutidas no pacote. Caminhos possíveis:
>
> - **Financeiro / cobrança** — puxar a situação de pagamento de cada cliente pra alimentar o critério "pagamento" (placeholders: `<SEU_FINANCEIRO_URL>`, `<SEU_FINANCEIRO_API_KEY>`).
> - **CRM** — puxar última interação, tempo de casa e ticket (placeholders: `<SUA_CRM_URL>`, `<SUA_CRM_API_KEY>`).
> - **WhatsApp** (Evolution API / Z-API) — medir engajamento pela data da última conversa e tempo de resposta (placeholders: `<SUA_EVOLUTION_URL>`, `<SUA_EVOLUTION_API_KEY>`, `<SUA_INSTANCIA>`).
>
> Em todos os casos: a credencial é SUA, fica na SUA infraestrutura, e a A ORDEM só implementa o fluxo. Isso não faz parte deste pacote da vitrine — é a etapa de implementação recorrente.
