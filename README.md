# A Ordem — Customer Success (Skills)

> Grupo de **Agent Skills** (formato `SKILL.md`) para Claude Code / Cursor, focado em
> **retenção e relacionamento com clientes** de agência. Microsoluções plug-and-play
> (paste-based, sem credencial).
> Feito pela **A Ordem**.

---

## O que é

Skills de CS dentro do seu agente: leem o que está acontecendo na carteira e ajudam a
**ver o churn chegando**, estruturar o onboarding e provar valor na renovação. Você
cola as conversas/situação dos clientes e o agente devolve diagnóstico, prioridade e
próximos passos — sem conectar token.

## Por que existe

Na agência, churn quase sempre dá sinal antes — mas ninguém tem tempo de ler a carteira
inteira toda semana, nem de montar onboarding e QBR do zero. Estas skills transformam
conversas e histórico em **ação de retenção**, sempre no mesmo padrão, pra agência agir
antes de perder o cliente.

## Pra quem é

- **Agências** que querem reter cliente e parar de "achar" como cada conta está.
- **CS / gestores de conta** que precisam de raio-x, onboarding e QBR rápidos e consistentes.

## Como o conjunto é organizado

Cada skill segue o mesmo padrão (*progressive disclosure*):

```
SKILL.md         →  o agente lê primeiro: papel, inputs e regras.
references/*.md  →  como aplicar, prova (exemplo) e resultado esperado.
card.html        →  card de apresentação da microsolução (visual A Ordem).
```

Princípio: **a classificação sai dos sinais reais, não de achismo** — e o que falta
vira [VERIFICAR], nunca número inventado.

## As skills

| Skill | O que faz |
|-------|-----------|
| **cs-ai** | Raio-x da carteira: classifica satisfação e aponta **risco de churn** (com motivo e janela de ação) |
| **churn-radar** | **Score de risco** por cliente (critérios + pesos transparentes) + playbook de retenção por faixa |
| **onboarding-cliente** | Plano dos **primeiros 30 dias**: kickoff, marcos por semana, acessos, quick win |
| **qbr-relatorio** | **QBR** trimestral pronto pra apresentar: resultados vs meta, entregas, plano e renovação |

Cada skill traz, além do `SKILL.md`: `references/` (como-aplicar, prova, resultado,
setup-credenciais) e `card.html`.

## Início rápido

```bash
git clone https://github.com/hiker328/ordem-cs.git
cd ordem-cs
claude
> faz um raio-x da minha carteira (colo as conversas/situação)
```

Rodando o `claude` dentro da pasta, as skills em `.claude/skills/` são detectadas. Para
usar em qualquer projeto, copie `.claude/skills/*` para `~/.claude/skills/` (Claude
Code) ou `~/.cursor/skills/` (Cursor).

## Credenciais

**Nenhuma.** Paste-based: você cola os dados da carteira. Nada conecta, nada pede token.

## Exemplos

Um exemplo (input fictício → output) por skill em [`examples/`](examples/).

## O que você precisa pra rodar

- **Claude Code** (ou Cursor) — as skills são `SKILL.md`.
- Os seus **dados da carteira** (conversas, situação, resultados colados).

## Estrutura do repositório

```
ordem-cs/
├── README.md · LICENSE · .gitignore
├── examples/                 # 1 exemplo por skill (input → output)
└── .claude/skills/
    ├── cs-ai/                (SKILL.md + references/ + card.html)
    ├── churn-radar/
    ├── onboarding-cliente/
    └── qbr-relatorio/
```

## Roadmap

| Versão | Conteúdo |
|--------|----------|
| v1 (atual) | 4 skills paste-based de Customer Success |
| Próximas | playbook de upsell · pesquisa de satisfação (NPS) · health score recorrente |

## O que isso NÃO é

- Não conecta no seu CRM nem pede token — é paste-based (você cola os dados da carteira).
- Não substitui o CS — entrega diagnóstico e prioridade; a conversa com o cliente é sua.
- Não inventa status — a classificação sai dos sinais reais, não de achismo.

## Feito pela A Ordem

Criado e mantido pela **A Ordem**. Skills feitas para agências de marketing/tráfego.
Licença MIT (ver `LICENSE`).
