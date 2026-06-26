# Setup de credenciais — CS AI — Resumo da Carteira + Risco de Churn

**Nenhuma credencial necessária.** Esta solução é paste-based: você só cola as suas próprias conversas (exportadas do WhatsApp) e o histórico de atendimento na conversa. Nada conecta no seu WhatsApp, nada pede token, nada sai do seu controle.

> Versão "auto" (puxar as conversas direto, sem exportar à mão) é um upgrade opcional de implementação. Aí sim entraria uma conexão — sempre com as credenciais do SEU próprio ambiente, geradas por você, nunca embutidas no pacote. Caminhos possíveis:
>
> - **Evolution API** — instância própria de WhatsApp (placeholders: `<SUA_EVOLUTION_URL>`, `<SUA_EVOLUTION_API_KEY>`, `<SUA_INSTANCIA>`).
> - **Z-API** — gateway de WhatsApp (placeholders: `<SEU_ZAPI_INSTANCE_ID>`, `<SEU_ZAPI_TOKEN>`, `<SEU_ZAPI_CLIENT_TOKEN>`).
> - **Claude no navegador** — uma automação que lê as conversas pela própria tela, sem API, usando a sua sessão já logada.
>
> Em todos os casos: a credencial é SUA, fica na SUA infraestrutura, e a A ORDEM só implementa o fluxo. Isso não faz parte deste pacote da vitrine — é a etapa de implementação recorrente.
