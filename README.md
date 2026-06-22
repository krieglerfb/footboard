# ⚽ Footboard Card Game

Jogo tático de futebol para 2 jogadores que combina tabuleiro com cartas estratégicas.

🎮 **[Jogar agora](https://krieglerfb.github.io/footboard/)**

---

## Modos de Jogo

- **Criar Sala** — gera um código para compartilhar com o adversário (online)
- **Entrar em Sala** — digite o código recebido para jogar online
- **Jogar Offline** — dois jogadores no mesmo dispositivo

---

## Preparação

### 1. Escolha seu Time
Selecione um time na tela inicial (seleções ou clubes). Cada time inclui elenco completo e um deck de 30 cartas.

### 2. Posicione seus Jogadores
Na tela de posicionamento, clique em um jogador da lista e depois em uma casa válida do campo (destacada em verde). Use **Auto-posicionar** para posicionar automaticamente conforme a formação do time.

O goleiro deve ocupar obrigatoriamente a casa GOL.

---

## O Campo

O campo tem **10 linhas × 5 colunas**. Linhas 0 e 9 são as casas do goleiro (GOL). As linhas 1–8 são o campo de jogo.

```
Linha 0:  —  | —  | GOL | —  | —    ← Goleiro adversário
Linha 1:  LD | ZAG| ZAG |ZAG | LE
Linha 2:  MD | VOL| VOL |VOL | ME
Linha 3:  MD | MA |  MA | MA | ME
Linha 4:  PD | SA |  CV | SA | PE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━    ← Meio de campo
Linha 5:  PE | SA |  CV | SA | PD
Linha 6:  ME | MA |  MA | MA | MD
Linha 7:  ME | VOL| VOL |VOL | MD
Linha 8:  LE | ZAG| ZAG |ZAG | LD
Linha 9:  —  | —  | GOL | —  | —    ← Seu goleiro
```

Time 1 começa nas linhas 0–4 e ataca em direção às linhas mais altas.  
Time 2 começa nas linhas 5–9 e ataca em direção às linhas mais baixas.

### Zonas de Chute

Calculadas em relação ao gol adversário:

- **Z1** — linha ZAG adversária, colunas 1, 2 e 3 (centro)
- **Z2** — linha ZAG adversária colunas 0 e 4 (laterais) + linha VOL adversária colunas 1, 2 e 3
- **Z3** — linha MA adversária colunas 1, 2 e 3 + linha VOL colunas 0 e 4

---

## Estrutura do Turno

### Fase 1 — Início
- O jogador **com a bola** recebe **2 Ações**
- O jogador **sem a bola** recebe **3 Ações**
- Ações reservadas do turno anterior são somadas ao total
- Compra-se **1 carta** do deck

### Fase 2 — Ações
Gaste ações para mover jogadores, passar, chutar ou jogar cartas.  
Ações não usadas ficam **reservadas** para o próximo turno (sem limite de acúmulo).

### Fase 3 — Encerramento
Clique **Encerrar** para passar o turno. Descarte cartas até ficar com no máximo 3 na mão.

---

## Ações Disponíveis

| Ação | Custo | Detalhe |
|------|-------|---------|
| Mover | 1 | 1 casa ortogonal (cima, baixo, esquerda, direita) |
| Passe Curto | 1 | Ortogonal, alcance 1 casa |
| Passe Longo | 2 | Ortogonal, alcance até 2 casas |
| Cruzamento | 3 | Qualquer direção, soma de dr+dc ≤ 4 |
| Chute Z1 | 1 | +1 no dado do atacante |
| Chute Z2 | 2 | Sem modificador |
| Chute Z3 | 3 | −1 no dado do atacante |
| Desarme | 1 | Na mesma casa ou adjacente (com Antecipação!) |

> O goleiro na casa GOL tem alcance de passe ampliado (até 4 casas ortogonais).

---

## Resolução do Chute

1. Atacante rola 1d6 e aplica bônus/penalidades de habilidades
2. Goleiro rola 1d6 e aplica seus bônus
3. **Atacante ≥ Goleiro** → GOL
4. **Goleiro > Atacante** → Defesa — goleiro fica com a bola

**Goleiro fora da casa GOL** → gol automático.

---

## Ocupação de Casas

- Máximo de **2 jogadores por casa**, de qualquer time
- **Velocista!** e **Cabeceador Nato!** ignoram esse limite
- **Marcador Implacável!** pode entrar em casa com 1 adversário (ficando 2 na mesma casa)

---

## Regras Especiais

### Goleiro
- Move-se e passa como qualquer jogador
- Só defende chutes se estiver na casa GOL
- Ao encerrar o turno **com a bola**, é obrigado a passar (Passe Curto ou Longo)

### Após o Gol
- Ambos os times se reposicionam livremente
- A bola vai para o **CV do time que sofreu o gol**
- Cada jogador escolhe: **completar a mão até 3 cartas** ou **descartar tudo e comprar 3**
- Ações reservadas são zeradas

### Intervalo (turno 16)
- Ambos os times podem fazer **1 substituição gratuita**
- Mesma escolha de cartas que após gol
- O time que não iniciou o primeiro tempo começa o segundo

### Substituições
- Máximo de **3 por time** por partida
- Ocorrem no intervalo, após gol ou via Paralisação

---

## Cartas

### Tipos
- **c** (carta de ação) — jogada gastando ações, efeito imediato
- **a** (aura) — permanece em campo; efeito contínuo até ser sacrificada ou removida
- **i** (instante/reativo) — fica na mão; dispara automaticamente quando o gatilho ocorre

### Cartas Disponíveis

| Carta | Custo | Tipo | Efeito |
|-------|-------|------|--------|
| Acréscimo | 1 | c | +2 Ações imediatas |
| Assistência | 2 | c | Próximo passe invulnerável; receptor ganha +3 no dado de chute e +1 Ação de Chute |
| Assistência Médica | 1 | c | Remove Lesão do aliado alvo (se houver) e concede +1 Ação de Movimento |
| Bote Certo | 0 | i | Gatilho: adversário com a bola entra ou passa pela sua casa → rouba a bola e encerra o turno |
| Capitão | 2 | a | Aura (1 por time): ao fim do turno com a bola, jogadores adjacentes ao portador movem 1 casa de graça |
| Cavar Falta | — | c | Encerra o turno; adversário perde 1 ação no próximo turno |
| Cometer Falta | — | c | Recupera a bola; adversário recebe escanteio/falta |
| Contra-Ataque | 2 | c | Portador move verticalmente até a próxima casa com um adversário |
| Efeito Inesperado | 1 | c | Próximo chute na Z3 recebe +3 no dado |
| Fazer Cera | 1 | c | +2 Ações; ambos os times pulam 1 turno. Um aliado aleatório rola d6: ≤2 → Cartão Amarelo |
| Gol de Placa | 1 | c | Portador ganha Driblador!, Velocista! e Finalizador 1! até o fim do turno |
| Jogada Ensaiada | 1 | c | +1 Ação de Passe e +1 Ação de Chute específicas ao portador |
| Jogo da Vida | 2 | a | Aura: a cada turno com a bola, +1 ação vinculada. Se marcar gol, a aura é sacrificada |
| Lesão | 2 | a | Aura adversária: jogador alvo no perímetro tem +1 custo em todos os movimentos |
| Marcação sob Pressão | 2 | c | Sem posse: todos os seus jogadores de linha avançam 1 casa (bloqueados apenas se houver 2+ no destino) |
| No Auge | 1 | a | Aura: quando o portador fosse perder a bola, pode sacrificar a aura e mantê-la |
| No Grito | 0 | i | Gatilho: você marca gol → próximo turno +2 Ações de Movimento |
| Provocação | 0 | i | Gatilho: adversário declara chute → −2 no dado do atacante |
| Rebote | 0 | i | Gatilho: chute falhou e defesa ≤ 3 → próximo chute sem custo de ação |
| Reposição Rápida | 0 | i | Gatilho: goleiro defende → próximo turno +1 Passe Longo e +1 Movimento grátis |
| Tiki-taka | 1 | c | Com 2+ passes curtos realizados no turno: compre 2 cartas sem descartar no encerramento |
| Vantagem Defensiva | 1 | c | Com maioria de jogadores no perímetro do portador adversário: seu jogador fica com a bola |
| Vantagem Numérica | 1 | c | Com posse na zona ofensiva e maioria: compre 2 cartas e receba 2 Ações extras. Sem descarte no encerramento |
| Virada | 0 | i | Gatilho: gol de empate → próximo turno +2 Ações de Passe Longo |

---

## Keywords (Habilidades dos Jogadores)

### Movimento
| Keyword | Efeito |
|---------|--------|
| Driblador! | 1 movimento grátis por turno quando **com a bola** |
| Driblador Ofensivo! | Movimento ofensivo grátis quando com a bola |
| Incansável! | 1 movimento grátis por turno quando o time **não** tem a bola |
| Deslize Lateral! | 1 movimento ortogonal grátis quando em coluna lateral (col 0 ou 4) |
| Velocista! | Ignora o limite de 2 jogadores por casa ao se mover |
| Lento! | Todo movimento custa +1 Ação |

### Passes
| Keyword | Efeito |
|---------|--------|
| Lançador! | Passe Longo tem alcance +1 (até 3 casas) |
| Clássico 10! | Ao encerrar o turno com a bola: ganha 1 ação vinculada no próximo turno |

### Finalização
| Keyword | Efeito |
|---------|--------|
| Finalizador 1! | +1 no dado de chute **apenas na Z1** |
| Finalizador 2! | +2 no dado de chute **apenas na Z1** |
| Chute Longo 1! | +1 no dado de chute em Z2 e Z3 |
| Chute Longo 2! | +2 no dado de chute em Z2 e Z3 |
| Chute de Primeira! | Chute custa −1 Ação (mínimo 0) |
| Cabeceador Nato! | Ignora limite de 2/casa na Z1 adversária; cruzamentos para ele custam −1 |
| Especialista em Pênalti! | Se tirar 6 no dado, gol garantido na cobrança |

### Defesa
| Keyword | Efeito |
|---------|--------|
| Antecipação! | Pode desarmar jogadores em casas **ortogonalmente adjacentes** |
| Carrinho! | Após desarme, empurra o adversário 1 casa |
| Líbero! | Após desarme, ganha 1 movimento grátis |
| Lateral Implacável! | A cada desarme bem-sucedido: +1 Ação |
| Marcador Implacável! | Pode entrar na casa de 1 adversário (compartilhando a casa) |
| Paredão! | Adversários não podem entrar com a bola na sua casa |
| Saltador! | Intercepta passes longos que passam pela sua casa |

### Goleiro
| Keyword | Efeito |
|---------|--------|
| Reflexo 1! | +1 no dado de defesa (apenas se for o único adversário na Z1) |
| Reflexo 2! | +2 no dado de defesa (mesmo condição do Reflexo 1!) |
| Reflexo Geral! | +1 no dado de defesa em qualquer zona, sem condição |
| Pegador de Pênalti! | Defende pênalti também quando dado do goleiro = dado do cobrador − 1 |
| Provocador! | Se tirar 6 no dado de defesa, anula o chute |

---

## Pênaltis

Em caso de empate ao fim dos turnos regulares:

1. Cada time realiza **5 cobranças** alternadas
2. Atacante rola 1d6 (Especialista em Pênalti! garante gol com dado 6)
3. Goleiro rola 1d6 (Pegador de Pênalti! defende também com empate −1)
4. **Atacante ≥ Goleiro** → GOL; caso contrário → Defesa
5. Em novo empate após 5x5, **morte súbita** (1 cobrança por vez)

---

## Créditos

Criado por **Bruno Kriegler**  
Desenvolvido com [Claude](https://claude.ai) (Anthropic)
