# Como aplicar — Churn Radar — Score de Risco de Churn + Playbook por Faixa

> Você aplica sozinho, em minutos. Não precisa instalar nem conectar nada. Você só cola a lista de clientes e o que sabe de cada um.

## Passo a passo
1. Liste os clientes que quer pontuar (pode ser a carteira inteira ou só um grupo).
2. Para cada cliente, anote o que souber dos critérios: pagamento (em dia / atrasado), engajamento (responde rápido / sumido), resultado entregue vs combinado, relacionamento (caloroso / frio / reclamando), tempo de casa e ticket.
3. Decida se quer dar mais peso a algum critério (ex.: pagamento pesa mais). Se não quiser, a solução usa peso igual.
4. Abra uma conversa nova no Claude (ou ChatGPT). Cole o prompt do arquivo `SKILL.md`.
5. No fim do prompt, cole os seus dados: a lista de clientes com os critérios de cada um e o contexto da carteira.
6. Envie. Você recebe: os critérios e pesos, a tabela de risco ranqueada, o detalhe dos clientes em risco, o playbook por faixa e a lista de quem contatar hoje x esta semana.
7. Comece pela lista "Hoje" (risco alto). Rode de novo toda semana ou quinzena — o score vira um placar de retenção.

## Como montar os dados de cada cliente
- **Não precisa de planilha sofisticada:** uma linha por cliente já basta, ex.: "Cliente X — paga em dia, sumiu há 10 dias, resultado abaixo do combinado, tom frio, 7 meses de casa, R$ 2.000".
- **Pagamento e engajamento são os critérios mais fortes:** se só tiver tempo pra dois, comece por esses.
- **O que não souber, deixe em branco:** a solução marca [VERIFICAR] e pontua o resto, sem chutar.
- Dica: puxe o pagamento do financeiro e o engajamento do WhatsApp/CRM — são os dois que mais antecipam churn.

## Roteiro do vídeo (gravar — alvo 4-6 min, sem emoji)
- 0:00 — A dor: "você só descobre que o cliente vai cancelar quando ele manda a mensagem avisando — aí já é tarde."
- 0:30 — O que essa solução faz: pontua cada cliente por critérios objetivos e te entrega um ranking de risco com a ação certa por faixa.
- 1:00 — Mostrar como montar os dados: uma linha por cliente com pagamento, engajamento, resultado, relacionamento, tempo de casa (usar clientes fictícios na gravação).
- 2:00 — Colar o prompt + os dados de 4-5 clientes de exemplo.
- 2:50 — Ler a saída ao vivo: a tabela ranqueada, os critérios, o playbook por faixa e a lista de quem ligar hoje.
- 4:30 — Fecho: o resultado esperado + "se quiser o score puxando pagamento e engajamento sozinho do seu sistema, me chama" (contato).

## Erros comuns
- Misturar opinião com dado: o score é mais útil quando os critérios são factuais (atrasou ou não, respondeu ou não). Guarde a interpretação pra leitura do resultado.
- Preencher um critério no chute: se não sabe, deixe em branco. O [VERIFICAR] é honesto e evita um score falso.
- Tratar o score como verdade absoluta: é priorização por sinais, não previsão estatística. Use pra decidir quem olhar primeiro, não pra cravar quem vai sair.
- Rodar uma vez e parar: o valor está na recorrência — o cliente que era risco médio pode virar alto na semana seguinte.
