# Setup de credenciais — QBR — Revisão Trimestral de Negócio pra Apresentar

**Nenhuma credencial necessária.** Esta solução é paste-based: você só cola os números e fatos do trimestre (meta, resultado, entregas, aprendizados) na conversa. Nada conecta em conta, nada pede token, nada sai do seu controle.

> Versão "auto" (preencher os resultados puxando os números direto das plataformas) é um upgrade opcional de implementação. Aí sim entraria uma conexão — sempre com as credenciais do SEU próprio ambiente, geradas por você, nunca embutidas no pacote. Caminhos possíveis:
>
> - **Meta Ads** — puxar investimento, vendas e ROAS do período (placeholders: `<SEU_META_ACCESS_TOKEN>`, `<SEU_AD_ACCOUNT_ID>`).
> - **Google Ads / Google Analytics** — puxar resultados de campanha e conversões (placeholders: `<SEU_GOOGLE_ADS_TOKEN>`, `<SEU_GA_PROPERTY_ID>`).
> - **CRM / financeiro** — puxar faturamento real e ticket médio atribuídos ao cliente (placeholders: `<SUA_CRM_URL>`, `<SUA_CRM_API_KEY>`).
>
> Em todos os casos: a credencial é SUA, fica na SUA infraestrutura, e a A ORDEM só implementa o fluxo. Isso não faz parte deste pacote da vitrine — é a etapa de implementação recorrente.
