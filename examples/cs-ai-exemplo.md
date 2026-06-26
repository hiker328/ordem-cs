# Prova — CS AI — Resumo da Carteira + Risco de Churn

> Exemplo com dados FICTÍCIOS. Mostra o tipo de saída que a solução gera a partir de trechos de conversa.

## Input de exemplo (colado)
```
Contexto: carteira de 3 clientes de retainer mensal. Entrego gestão de tráfego.

=== Cliente: Padaria do João (ticket R$ 2.500/mês, 8 meses de casa) ===
WhatsApp:
João: "Cara, o movimento da loja explodiu esse mês, valeu demais!"
João: "Tenho um amigo que tem uma pizzaria, posso passar seu contato?"
Histórico: entregas em dia, paga sempre antes do vencimento.

=== Cliente: Studio Bella (ticket R$ 1.800/mês, 5 meses) ===
WhatsApp:
Bella: "Oi, e o relatório de outubro?" (dia 3)
Bella: "Oi? Ainda esperando o relatório." (dia 6)
Bella: "Tá complicado isso, é a segunda vez que atrasa."
Histórico: relatório atrasou 2 vezes seguidas. Pagamento em dia.

=== Cliente: Auto Center Z (ticket R$ 3.200/mês, 11 meses) ===
WhatsApp:
(sumido há 18 dias, antes respondia no mesmo dia)
Você: "Oi, fechamos a campanha nova?" — sem resposta há 4 dias.
Histórico: fatura de novembro vencida há 9 dias. Antes, sempre pontual.
```

## Output esperado (trecho)
```
1. RESUMO EXECUTIVO DA CARTEIRA
Carteira de 3 clientes: 1 satisfeito, 1 em risco, 1 em alerta de churn alto. O movimento
mais urgente é o Auto Center Z (silêncio + fatura vencida = padrão clássico de pré-cancelamento).
Studio Bella ainda é recuperável, mas o atraso recorrente está corroendo a confiança. Padaria
do João é a oportunidade do mês: cliente promotor, abriu a porta pra uma indicação.

2. CLIENTES SATISFEITOS
Padaria do João — sinais positivos: elogio espontâneo ("explodiu esse mês") e oferta de
indicação não solicitada. Oportunidade: aceitar a indicação hoje e propor um case de sucesso.

3. CLIENTES EM RISCO
Studio Bella — sinal: reclamação explícita por atraso recorrente do relatório ("segunda vez
que atrasa"). Evidência: 3 cobranças em 3 dias + histórico de 2 atrasos. Tom esfriou. Risco real.

4. ALERTAS DE CHURN
Auto Center Z — gatilho: silêncio de 18 dias (era responsivo) + fatura vencida há 9 dias +
não respondeu sobre a campanha nova. Nível: ALTO. Janela: agir HOJE.

5. PRÓXIMAS AÇÕES PRIORIZADAS POR CLIENTE
Auto Center Z | P1 hoje | Ligar (não mandar texto) | "Senti que sumimos, quero entender
   como você está — e resolver a fatura junto." | Silêncio + inadimplência = churn iminente.
Studio Bella | P1 hoje | Mandar áudio + entregar o relatório atrasado | "O atraso foi falha
   minha, já corrigi e ó aqui o de outubro." | Recuperar confiança antes que vire cancelamento.
Padaria do João | P2 | Responder a indicação | "Manda sim o contato, e topo gravar um
   depoimento rápido com você." | Capitalizar o cliente promotor.
```

## Por que funciona
A classificação sai dos próprios trechos colados (não há achismo): elogio e oferta de indicação são lidos como sinal positivo; cobrança repetida e tom frio como risco; silêncio prolongado somado a fatura vencida como alerta de churn alto. Onde a evidência for fraca, a solução marca [SINAL FRACO] em vez de inventar sentimento — e a ação mais urgente (ligar pro cliente que pode cancelar hoje) vem priorizada no topo.
