# FICHA DE DECISÕES · War Room FiapBank (CP6 · 3 aulas)

> Este arquivo é o **README.md do repositório do grupo** (`cp6-warroom-gambiarra`).
> Vale **5,0 pontos** (rodadas 0,5 · relâmpagos 0,3), e a nota é pela
> **justificativa**, não pela letra. Preencham após cada aula e commitem até
> **23h59 do mesmo dia** (regras completas na seção 5 do enunciado).
>
> **Os incidentes da madrugada são revelados só em aula.** O título de cada registro
> será **ditado pelo professor na hora**; ninguém se antecipe.

**Grupo (nome da equipe plantonista):** Gambiarra

**Turma:** CCPX **Repo:** `cp6-warroom-gambiarra`

**Integrantes (nome + RM):**

| Nome | RM |
|---|---|
| Enzo Cerneviva | 563480 |
| Matheus Lara | 564049 |
| Victor Hugo | 564633 |
| | |
| | |

---

## 📁 Dossiê técnico do FiapBank (MVP em produção)

**Stack:** Java 17 + Spring Boot + Spring Data JPA + Oracle. API com endpoints em
`/api/contas` e `/api/transferencias` (cenário visto desde a Aula 13).

**Contrato e regras de negócio que o banco prometeu aos clientes e aos reguladores:**

| Regra | Como deve ser |
|---|---|
| Transferência **PIX** | taxa **R$ 0,00** |
| Transferência **TED** | taxa fixa **R$ 5,00** |
| Saldo | **nunca fica negativo**: transferência/saque sem saldo é recusado com erro claro |
| Número de conta | **sequencial e único** (1001, 1002, 1003...), gerado pelo sistema |
| Extrato de transferência | grava **quem pagou** e **quem recebeu**, na ordem certa |
| CPF | **dado sensível**: nunca aparece nas respostas da API |
| Consultas ao banco | sempre parametrizadas, e cada operação **usa e libera** a conexão |
| Suíte de testes | roda antes de todo deploy; **verde** é pré-requisito pra subir |

**Como escrever a justificativa:** nomeie o **mecanismo técnico** em jogo (o
conceito das Aulas 11 a 15 que explica o incidente) e o **trade-off** (velocidade ×
segurança × faturamento × dívida). "Porque é mais seguro" não é justificativa.

---

# 📝 REGISTRO DE DECISÕES

> A cada incidente, o professor dita o título (ex.: "Rodada 1"). **Copiem o modelo
> abaixo, colem no fim desta seção** e preencham com o rascunho feito em aula, junto
> com o **placar do grupo** após a consequência. Commitem 1 commit por rodada até
> 23h59 do dia.
>
> **Eventos relâmpago:** registrem apenas se o grupo for **afetado** (o professor
> chama quem for; não ser chamado é bom sinal).

**Modelo (copiar para cada decisão):**

```
## <título ditado pelo professor>

**Tipo:** ( rodada / relâmpago ) · **Voto:** ( A / B / C / D )

**Justificativa:**

<2 a 3 linhas: mecanismo técnico + trade-off>

**Placar do grupo após esta decisão:** 🔥 __ · 💰 R$ __ mil · 🧹 __
```

*(as decisões entram aqui, na ordem em que a madrugada as trouxer; placar inicial:
🔥 7 · 💰 0 · 🧹 2)*

## Rodada 1

**Tipo:** rodada · **Voto:** D

**Justificativa:**

Voltar ao código da terça (rollback), pois o problema só apareceu na quinta-feira, o que significa que antes estava funcionando. Com o tempo curto, não garantiríamos conseguir corrigir o problema.

**Placar do grupo após esta decisão:** 🔥 7 · 💰 R$ 15 mil · 🧹 3

---

## Rodada 1 Relâmpago

**Tipo:** relâmpago · **Voto:** B

**Justificativa:**

Escolhemos o findByTitular por ter a query já construída.

**Placar do grupo após esta decisão:** 🔥 7 · 💰 R$ 15 mil · 🧹 2

---

## Rodada 3

**Tipo:** rodada · **Voto:** D

**Justificativa:**

De acordo com o contrato, o número da conta deve ser sequencial e gerado pelo sistema.

**Placar do grupo após esta decisão:** 🔥 7 · 💰 R$ 25 mil · 🧹 2

---

## 🔎 O caminho do MEU grupo (preencher na 3ª aula, quando o mapa for revelado)

Uma linha por decisão registrada acima (usem os títulos ditados em aula):

| # | Decisão | Nossa letra | Consequência que ELA teria tido |
|---|---|---|---|
| | | | |
| | | | |
| | | | |

*(adicionem linhas conforme as decisões da madrugada)*

---

# 📋 PÓS-MORTEM · relatório de incidente (montar em sala na 3ª aula)

> Rascunho em aula e commit final `pos-mortem:` até 23h59 do dia da 3ª aula.

## 1. Linha do tempo da madrugada

_______________________________________________________________________________________

_______________________________________________________________________________________

_______________________________________________________________________________________

## 2. Causa raiz de 2 incidentes (aula + mecanismo técnico)

**Incidente 1:** _______________________________________________

Aula/mecanismo:

_______________________________________________________________________________________

**Incidente 2:** _______________________________________________

Aula/mecanismo:

_______________________________________________________________________________________

## 3. O que faríamos diferente (2 rodadas + por quê)

_______________________________________________________________________________________

_______________________________________________________________________________________

## 4. A maior lição da equipe

_______________________________________________________________________________________
