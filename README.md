# ⚽ Footboard Card Game

Jogo tático de futebol para 2 jogadores que combina tabuleiro com cartas estratégicas.

🎮 **[Jogar agora](https://krieglerfb.github.io/footboard/)**

---

## Como Jogar

### Modos
- **Criar Sala** — gera um código de 8 caracteres (ex: `FCG-K7QR`) para compartilhar com seu amigo
- **Entrar em Sala** — digite o código recebido e escolha seu time
- **Jogar Offline** — dois jogadores no mesmo computador

---

## Preparação

### 1. Monte seu Deck
Cada jogador monta um deck de **exatamente 30 cartas**, com no máximo **3 cópias** de uma mesma carta.

Use o botão **Auto-preencher** para montar automaticamente, ou selecione manualmente pelo pool de cartas disponíveis. Confirme quando atingir 30.

### 2. Escolha sua Formação
Cada time escolhe uma formação tática. As formações disponíveis são:

| Formação | Estilo |
|----------|--------|
| 4-3-3 | Posse + Equilibrada |
| 4-4-2 | Clássico |
| 3-5-2 | Contra-ataque |
| 5-3-2 | Defesa Sólida |
| 4-2-3-1 | Jogador Alvo |

### 3. Posicione seus Jogadores
Selecione um jogador da lista e clique na casa válida (destacada em verde) no campo. Use **Auto-posicionar** para colocar todos automaticamente conforme a formação.

---

## Estrutura do Turno

Cada jogador tem **30 turnos** por tempo (15 + 15). O jogo tem 2 tempos.

### Fase 1 — Preparação
- **Com a bola:** compra 1 carta + recebe 2 Ações
- **Sem a bola:** compra 1 carta + recebe 3 Ações

### Fase 2 — Ações
Gaste suas Ações para mover, passar, chutar ou jogar cartas.  
Ações não usadas são **reservadas** para turnos futuros (sem limite).

### Fase 3 — Encerramento
Descarte cartas até ficar com no máximo 3 na mão.

---

## Ações Básicas

| Ação | Custo | Descrição |
|------|-------|-----------|
| Mover | 1 | Move 1 casa (vertical ou horizontal) |
| Passe Curto | 1 | Para jogador adjacente |
| Passe Longo | 2 | Até 2 casas ou 1 diagonal |
| Desarme | 1 | Recupera a bola na mesma casa |
| Chute Z1 | 1 | +1 no dado |
| Chute Z2 | 2 | +0 no dado |
| Chute Z3 | 3 | −1 no dado |
| Cometer Falta | 5 | Encerra o turno imediatamente |

---

## Zonas do Campo

O campo é dividido em **8 linhas × 5 colunas**, com 2 casas GOL especiais (só acessíveis pelo goleiro).

```
        [  GOL  ]          ← Casa do goleiro adversário

 LD  | ZAG | ZAG | ZAG | LE   ← Z2 / Z1 / Z1 / Z1 / Z2
 MD  | VOL | VOL | VOL | ME   ← Z3 / Z2 / Z2 / Z2 / Z3
 MD  | MEI | MEI | MEI | ME   ←  — / Z3 / Z3 / Z3 /  —
 PD  |  SA |  CV |  SA | PE   ← Linha de ataque (CV = saída de bola)
─────────────────────────────  ← Meio de campo
 PE  |  SA |  CV |  SA | PD
 ME  | MEI | MEI | MEI | MD
 ME  | VOL | VOL | VOL | MD
 LE  | ZAG | ZAG | ZAG | LD

        [  GOL  ]          ← Sua casa do goleiro
```

**Zonas de Chute** (do ponto de vista de quem ataca):
- **Z1** — linha ZAG adversária (colunas centrais)
- **Z2** — linha VOL/LD/LE adversária; e colunas laterais da linha ZAG
- **Z3** — linha MEI adversária (colunas centrais); e colunas laterais da linha VOL

---

## Chute ao Gol

1. Role 1d6 e aplique o modificador da zona
2. Goleiro rola 1d6
3. Se **atacante ≥ goleiro** → GOL
4. Se **goleiro > atacante** → defesa, goleiro fica com a bola

**Goleiro fora da casa GOL** → gol automático.

---

## Regras Especiais

### Goleiro
- Move-se como qualquer jogador
- Só defende chutes se estiver na casa GOL
- Ao fim do turno com a bola, **é obrigado a passar**
- Se não tiver ações, o adversário recebe ações equivalentes ao custo do passe

### Dois jogadores na mesma casa
- Máximo de 2 jogadores por casa (de qualquer time)
- Se ao fim do turno **2 aliados** tiverem a bola, o adversário recebe +1 ação no próximo turno

### Após o Gol
- Ambos os times se reposicionam conforme a formação ativa
- A bola vai para o CV do time que sofreu o gol
- Cada jogador escolhe: manter cartas (completar até 3) ou descartar tudo e comprar 3
- Ações reservadas são zeradas

### Intervalo (fim do turno 15)
- Times podem fazer substituições
- Mesma escolha de cartas que após gol
- O time que **não** iniciou o primeiro tempo começa o segundo

### Substituições
- Máximo de 3 por time por partida
- Ocorrem após gol, no intervalo ou via carta especial

---

## Keywords (Habilidades dos Jogadores)

### Gerais
| Keyword | Efeito |
|---------|--------|
| Clássico 10! | Se reservar ação com a bola, ganha 1 ação vinculada no próximo turno |
| Driblador! | 1 movimento grátis por turno quando com a bola |
| Incansável! | 1 movimento grátis quando o time está sem a bola |
| Deslize Lateral! | 1 movimento vertical grátis quando em casa lateral |
| Lançador! | +1 alcance em Passes Longos |
| Velocista! | Pode entrar em casas com 2 jogadores |
| Lento! | Movimentação custa +1 ação |

### Ofensivas
| Keyword | Efeito |
|---------|--------|
| Finalizador 1! | +1 no dado de chute na Z1 |
| Finalizador 2! | +2 no dado de chute na Z1 |
| Chute Longo! | +1 no dado de chute nas Z2 e Z3 |
| Chute de Primeira! | Reduz custo de chute em −1 |
| Cabeceador! | Pode entrar na Z1 mesmo com 2 jogadores; cruzamentos custam −1 |

### Defensivas
| Keyword | Efeito |
|---------|--------|
| Antecipação! | Pode desarmar jogadores em casas adjacentes |
| Carrinho! | Após desarme, empurra adversário 1 casa |
| Líbero! | Após desarme, ganha 1 movimento grátis |
| Marcador Implacável! | Segue adversário com a bola sem custo |
| Paredão! | Adversários não podem entrar com a bola na sua casa |
| Saltador! | Intercepta passes longos que passam pela sua casa |

### Goleiro
| Keyword | Efeito |
|---------|--------|
| Pegador de Pênalti! | Defende também se o dado for 1 abaixo do cobrador |
| Provocador! | Se tirar 6 na defesa, anula o chute |
| Reflexo 1! | +1 na defesa se for o único adversário na Z1 |

---

## Elencos Disponíveis

### 🇧🇷 Time Brasil
| Jogador | Posição | Habilidades |
|---------|---------|-------------|
| Taffarel | GOL | Peg.Pên.!, Provocador! |
| Roberto C. | LE | Lançador!, Cruzar!, DeslizLat.! |
| Aldair | ZAG | Paredão! |
| Mauro S. | ZAG | Antecipação!, Marc.Impl.! |
| Marcio S. | ZAG | Paredão! |
| Cafu | LD | Incansável!, DeslizLat.! |
| Makelele | VOL | Antecipação!, Carrinho! |
| Dunga | VOL | Lançador!, Carrinho! |
| Zico | MEI | Clássico10!, Driblador! |
| Romário | SA | Fin.1!, Chute1ª!, Velocista! |
| Pelé | CV | Velocista!, Fin.2!, Driblador! |

### 🇮🇹 Time Itália
| Jogador | Posição | Habilidades |
|---------|---------|-------------|
| Buffon | GOL | Peg.Pên.!, Provocador!, Reflexo1! |
| Grosso | LE | DeslizLat.!, Cobrador! |
| Cannavaro | ZAG | Paredão!, Antecipação! |
| Nesta | ZAG | Saltador!, Marc.Impl.! |
| Maldini | ZAG | Líbero!, Carrinho! |
| Zambrotta | LD | Incansável!, DeslizLat.! |
| Gattuso | VOL | Carrinho!, Antecipação!, Lento! |
| Pirlo | VOL | Lançador!, Clássico10!, Cobrador! |
| Totti | MEI | Clássico10!, Driblador! |
| Del Piero | SA | Fin.1!, Especialista! |
| Inzaghi | CV | Chute1ª!, Fin.1!, Cabeceador! |

---

## Pênaltis

Em caso de empate ao fim das 30 rodadas:
1. Cada time realiza 5 cobranças alternadas
2. Cobrador rola 1d6 — se tirar **1**, bola fica com o goleiro
3. Goleiro rola 1d6 — se **igual** ao cobrador, defende; se **diferente**, gol
4. Em novo empate, morte súbita (1 cobrança por vez)

---

## Créditos

Criado por **Bruno Kriegler**  
Desenvolvido com [Claude](https://claude.ai) (Anthropic)
