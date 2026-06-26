# A Ordem — Customer Success (Skills)

> Grupo de **Agent Skills** (formato `SKILL.md`) para Claude Code / Cursor, focado em
> **retenção e relacionamento com clientes** de agência. Microsoluções plug-and-play
> (paste-based, sem credencial).
> Feito pela **A Ordem**.

---

## O que é

Skills de CS dentro do seu agente: leem o que está acontecendo na carteira e ajudam a
**ver o churn chegando** e agir antes. Você cola as conversas/situação dos clientes e o
agente devolve diagnóstico e próximos passos — sem conectar token.

## Por que existe

Na agência, churn quase sempre dá sinal antes — mas ninguém tem tempo de ler a
carteira inteira toda semana. Estas skills transformam as conversas e o histórico em
um **raio-x de risco**, no mesmo padrão, para a agência agir antes de perder o cliente.

## Pra quem é

- **Agências** que querem reter cliente e parar de "achar" como cada conta está.
- **CS / gestores de conta** que precisam de um raio-x rápido e consistente da carteira.

## As skills

| Skill | O que faz |
|-------|-----------|
| **cs-ai** | Raio-x da carteira: classifica satisfação, aponta **risco de churn** (com motivo e janela de ação) e o que fazer com cada cliente |

Cada skill traz, além do `SKILL.md`: `references/` (como-aplicar, prova, resultado,
setup-credenciais) e `card.html` (card de vitrine A Ordem).

> Este grupo vai crescer — novas microsoluções de CS (ex.: onboarding de cliente, QBR,
> playbook de retenção) entram aqui.

## Início rápido

```bash
git clone https://github.com/<voce>/ordem-cs.git
cd ordem-cs
claude
> faz um raio-x da minha carteira (colo as conversas/situação)
```

As skills em `.claude/skills/` são detectadas ao rodar o agente na pasta. Para usar em
qualquer projeto, copie `.claude/skills/*` para `~/.claude/skills/` (Claude Code) ou
`~/.cursor/skills/` (Cursor).

## Credenciais

**Nenhuma.** Paste-based: você cola os dados da carteira. Nada conecta, nada pede token.

## O que isso NÃO é

- Não conecta no seu CRM nem pede token — é paste-based (você cola os dados da carteira).
- Não substitui o CS — entrega diagnóstico e prioridade; a conversa com o cliente é sua.
- Não inventa status — a classificação sai dos sinais reais, não de achismo.

## Feito pela A Ordem

Criado e mantido pela **A Ordem**. Skills feitas para agências de marketing/tráfego.
Licença MIT (ver `LICENSE`).
