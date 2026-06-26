# Prova — Churn Radar — Score de Risco de Churn + Playbook por Faixa

> Exemplo com dados FICTÍCIOS. Mostra o tipo de saída que a solução gera a partir dos critérios colados.

## Input de exemplo (colado)
```
Carteira de tráfego, 4 clientes. Quero peso maior pra pagamento e engajamento.

- Ótica Vê Bem — paga em dia, responde no mesmo dia, resultado dentro do combinado, tom caloroso,
  9 meses de casa, R$ 2.500/mês.
- Restaurante Maré — fatura atrasada há 12 dias, sumido há 2 semanas, resultado abaixo do combinado,
  última conversa foi reclamação, 5 meses de casa, R$ 3.000/mês.
- Academia Pulse — paga em dia, responde devagar, resultado dentro do combinado, tom neutro,
  3 meses de casa, R$ 1.800/mês.
- Imobiliária Lar — paga em dia mas pediu "reavaliar o investimento", engajada, resultado um pouco
  abaixo, tom ainda ok, 14 meses de casa, R$ 4.000/mês.
```

## Output esperado (trecho)
```
1. CRITÉRIOS E PESOS USADOS
Critérios: Pagamento (peso 2), Engajamento (peso 2), Resultado vs combinado (peso 1),
Relacionamento/tom (peso 1), Tempo de casa (peso 1). Cada critério pontua 0 (ok) a 2 (crítico);
score = soma ponderada. Faixas: Alto (sinal crítico em pagamento OU engajamento, ou score alto),
Médio (sinais moderados), Baixo (estável). Isto é priorização por sinais, não modelo estatístico.

2. TABELA DE RISCO RANQUEADA
Cliente          | Risco | Score | Pagto | Engaj | Result | Relac | Tempo | Motivo principal
Restaurante Maré | Alto  |  alto | atras | sumido| abaixo | recl. | 5m    | Inadimplência + silêncio + reclamação
Imobiliária Lar  | Médio |  méd  | em dia| ativo | abaixo | ok    | 14m   | Pediu reavaliar investimento
Academia Pulse   | Médio |  baixo| em dia| lento | ok     | neutro| 3m    | Engajamento frio + casa recente
Ótica Vê Bem     | Baixo |  baixo| em dia| rápido| ok     | caloro| 9m    | Cliente saudável e promotor

3. DETALHE POR CLIENTE EM RISCO (ALTO E MÉDIO)
Restaurante Maré (Alto) — motivo: fatura vencida há 12 dias + sumiço de 2 semanas + última
conversa foi reclamação. Em jogo: R$ 3.000/mês, 5 meses de casa. Ação: você liga HOJE (não texto),
ouve a reclamação, resolve a fatura junto e mostra um plano de virada do resultado.
Imobiliária Lar (Médio) — motivo: pediu "reavaliar o investimento" e resultado ficou abaixo,
apesar de pagar em dia e seguir engajada. Em jogo: R$ 4.000/mês, 14 meses (cliente antigo e de
ticket alto). Ação: agendar reunião esta semana pra remontar o plano e mostrar o valor acumulado.
[VERIFICAR] o que motivou o pedido de reavaliar (orçamento? expectativa?).

4. PLAYBOOK DE RETENÇÃO POR FAIXA
Alto — recuperação imediata: ligação (não texto) em até 24h, resolver a dor concreta (pagamento/
entrega), plano de virada por escrito, follow-up em 48h. Tom: humilde e resolutivo.
Médio — reforço e prevenção: reunião de valor esta semana, remontar plano, antecipar o resultado.
Tom: consultivo. Cadência: acompanhar de perto por 2-3 semanas.
Baixo — manutenção e expansão: manter cadência normal, pedir indicação/depoimento, oferecer escopo
extra quando fizer sentido. Tom: caloroso.

5. QUEM CONTATAR HOJE x ESTA SEMANA
Hoje: Restaurante Maré — ligar, ouvir a reclamação e resolver a fatura.
Esta semana: Imobiliária Lar — reunião de valor; Academia Pulse — checagem de engajamento.

6. VERIFICAR
- Imobiliária Lar: confirmar o que motivou o pedido de reavaliar — muda a abordagem.
- Academia Pulse: engajamento lento com 3 meses de casa pode ser estilo do cliente; confirmar.
- Nenhum critério ficou totalmente em branco neste exemplo.
```

## Por que funciona
O score sai dos critérios colados e mostra como cada cliente pontuou em cada um — nada de caixa-preta. O Restaurante Maré sobe pro topo porque acumula os dois sinais mais fortes (inadimplência + silêncio), respeitando o peso que o usuário pediu; a Imobiliária Lar, mesmo pagando em dia, entra como médio pelo pedido de "reavaliar". Onde falta dado pra explicar um sinal, a solução marca [VERIFICAR] em vez de inventar, e a lista "Hoje x Esta semana" transforma o score em ação priorizada.
