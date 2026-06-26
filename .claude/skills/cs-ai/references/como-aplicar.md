# Como aplicar — CS AI — Resumo da Carteira + Risco de Churn

> Você aplica sozinho, em minutos. Não precisa instalar nem conectar nada. Você só cola as conversas que já tem.

## Passo a passo
1. Escolha os clientes que quer analisar (pode ser a carteira inteira ou só os que te preocupam).
2. Exporte a conversa de cada um no WhatsApp (veja o "Como exportar do WhatsApp" abaixo). Pode ser um grupo de cliente ou o atendimento individual.
3. Junte também o histórico de atendimento de cada cliente: o que foi pedido, prazos, o que ficou pendente, situação de pagamento. Pode ser colado de um CRM, planilha ou de memória mesmo.
4. Abra uma conversa nova no Claude (ou ChatGPT). Cole o prompt do arquivo `SKILL.md`.
5. No fim do prompt, cole os seus dados: contexto da carteira, as conversas e o histórico por cliente.
6. Envie. Você recebe: resumo da carteira, lista de satisfeitos, lista de em risco, alertas de churn e as próximas ações priorizadas por cliente.
7. Comece pelas ações P1 (os clientes que podem cancelar hoje). Rode de novo toda semana — vira um ritual de CS.

## Como exportar a conversa do WhatsApp
- **No celular (Android ou iPhone):** abra a conversa ou o grupo do cliente → toque no nome no topo → role até **"Exportar conversa"** → escolha **"Sem mídia"** (só o texto, mais leve e mais limpo pra colar) → mande pro seu e-mail ou salve. O arquivo `.txt` que sai é exatamente o que você cola no prompt.
- **No WhatsApp Web / Desktop:** abra a conversa → menu (três pontos) → **"Mais"** → **"Exportar conversa"**.
- **Atalho sem exportar:** se for pouca conversa, dá pra simplesmente selecionar e copiar as últimas mensagens direto da tela e colar. Para vários clientes, exportar é mais rápido.
- Dica: separe por cliente com um cabeçalho ("=== Cliente: Padaria do João ===") antes de colar, pra análise sair organizada.

## Roteiro do vídeo (gravar — alvo 4-6 min, sem emoji)
- 0:00 — A dor: "você tem 15, 30, 50 clientes e não consegue acompanhar quem está bem e quem está prestes a sumir."
- 0:30 — O que essa solução faz: um head de CS sênior lê suas conversas e te entrega quem está satisfeito, quem está em risco e quem pode cancelar — com o que fazer.
- 1:00 — Como exportar a conversa do WhatsApp (mostrar na tela: abrir conversa, menu, "Exportar conversa", "Sem mídia").
- 2:00 — Colar o prompt + os dados de 2-3 clientes de exemplo (usar conversa fictícia, nunca dado real de cliente na gravação).
- 2:50 — Ler a saída ao vivo: resumo da carteira, o cliente em risco, o alerta de churn, e a tabela de próximas ações (quem ligar hoje).
- 4:30 — Fecho: o resultado esperado + "se quiser isso rodando de forma recorrente, puxando as conversas sozinho na sua operação, me chama" (contato).

## Erros comuns
- Colar só uma frase solta: quanto mais contexto da conversa e do histórico, mais sólida a classificação. Com pouco sinal, a solução marca [SINAL FRACO] — e aí vale completar.
- Esquecer o histórico de atendimento (prazos, pendências, pagamento): só a conversa lê o tom, mas atraso de entrega e atraso de pagamento são os maiores gatilhos de churn — inclua.
- Misturar clientes sem separar: use um cabeçalho por cliente pra saída sair limpa.
