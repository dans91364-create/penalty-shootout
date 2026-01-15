# ⚽ Penalty Shootout - Game Design Document

> Nome temporário: Penalty Shootout
> Status: Em desenvolvimento
> Documento criado: 2026-01-15

---

## 📖 Índice

1. [Visão Geral](#-visão-geral)
2. [Gameplay](#-gameplay)
3. [Cenário - Praia](#-cenário---praia)
4. [Sistema de Eventos](#-sistema-de-eventos)
5. [Eventos por Placar](#-eventos-por-placar)
6. [Eventos por Sequência](#-eventos-por-sequência)
7. [Sistema de Medalhas](#-sistema-de-medalhas)
8. [Personagens](#-personagens)
9. [Combos Secretos](#-combos-secretos)
10. [Sistema Anti-Rage Quit](#-sistema-anti-rage-quit)
11. [Assets](#-assets)

---

## 🎮 Visão Geral

### O que é?
Jogo de pênaltis estilo cartoon com eventos aleatórios que dão vida ao cenário.

### Origem
- Jogo já existiu (centenas de jogadores)
- Era apenas: tela verde + quadrado + bola
- Foi desligado há vários anos
- Esta versão: visual INCRÍVEL + eventos + medalhas

### Diferencial
| Antes | Agora |
|-------|-------|
| 🟩 Tela verde | 🏖️ Praia linda |
| ⬜ Quadrado | 🥅 Trave real |
| ⚪ Bola simples | ⚽ Bola cartoon |
| 😐 Sem graça | 🎲 Eventos, vida, surpresas |

---

## 🎯 Gameplay

### Mecânica Base
- 5 cobranças de pênalti
- Simples e acessível
- 1 partida = ~2 minutos

### Posições de Chute/Defesa
```
┌─────────────────────────┐
│                         │
│    ↖️      ⬆️      ↗️    │
│                         │
│    ↙️            ↘️     │
│                         │
└─────────────────────────┘
```
- 5 posições: 4 cantos + centro

### Modos
| Modo | Descrição |
|------|-----------|
| ⚽ Batedor | Você chuta |
| 🧤 Goleiro | Você defende |
| 🔄 Alternado | Troca a cada cobrança |

---

## 🏖️ Cenário - Praia

### Elementos Visuais

| Camada | Elementos |
|--------|-----------|
| 🌅 **Fundo (Skybox)** | Céu, sol, nuvens |
| 🌊 **Mar** | Ondas animadas |
| 🏖️ **Areia** | Textura de praia |
| 🌴 **Vegetação** | Palmeiras (balançam com vento) |
| 🥅 **Campo** | Trave, área do gol |
| 👤 **Personagens** | Batedor, goleiro |

### Asset Pack
- **Creative Characters** (Unity Asset Store)
- Estilo: Cartoon/Low Poly
- Consistente para todos os elementos

---

## 🎲 Sistema de Eventos

### Filosofia
```
MUITOS eventos possíveis... 
Mas só 1-2 por partida!

= VARIEDADE, não poluição
= Cada partida DIFERENTE
```

### Tabela de Raridade

| Cor | Raridade | % Chance | % Jogadores veem |
|-----|----------|----------|------------------|
| ⚪ | Comum | 70% | 100% |
| 🟢 | Incomum | 20% | 80% |
| 🔵 | Raro | 8% | 40% |
| 🟣 | Épico | 1.5% | 15% |
| 🟡 | Lendário | 0.4% | 5% |
| 💎 | Mítico | 0.1% | 1% |
| ⚫ | IMPOSSÍVEL | 0.01% | 0.1% |

### Eventos Aleatórios - Praia

#### ⚪ Comuns (70%)
| Evento | Descrição |
|--------|-----------|
| 🐕 Cachorro | Corre atrás de bola |
| 🐈 Gato | Anda e deita |
| 👧👦 Crianças | Brincam no fundo |
| 🦀 Caranguejo | Anda de lado |
| 🐦 Passarinho | Voa, pousa na trave |
| 🏃 Corredor | Pessoa correndo |
| 🐚 Concha | Aparece na areia |

#### 🟢 Incomuns (20%)
| Evento | Descrição |
|--------|-----------|
| 🏐 Vôlei | Jogo ao fundo |
| 🏄 Surfista | No mar |
| 🎈 Balão | Voa passando |
| 🪁 Pipa | No céu |
| 🐬 Golfinho | Pula no mar |
| 🚤 Lancha | Passa ao fundo |
| 📸 Turista | Tira foto |
| 🍦 Sorveteiro | Carrinho passa |

#### 🔵 Raros (8%)
| Evento | Descrição |
|--------|-----------|
| ✈️ Avião | Com faixa |
| 🚁 Helicóptero | Passa filmando |
| 🪂 Paraquedista | Cai do céu |
| 🦈 Tubarão | Barbatana no mar |
| 🐋 Baleia | Esguicho ao longe |
| ⛵ Veleiro | Navega bonito |
| 🎆 Fogos | No céu |
| 🌅 Pôr do Sol | Céu muda de cor |

#### 🟣 Épicos (1.5%)
| Evento | Descrição |
|--------|-----------|
| 🛸 OVNI | Passa rápido |
| 🦖 Dinossauro | WTF?! |
| 🧜‍♀️ Sereia | No mar |
| 🎅 Papai Noel | Fora de época |
| 🐰 Coelho Páscoa | Fora de época |
| 🎃 Fantasma | Fora de Halloween |

#### 🟡 Lendários (0.4%)
| Evento | Descrição |
|--------|-----------|
| 🐉 Dragão | Voa no céu |
| 💥 Meteoro | Cai ao longe |
| 🦸 Super-herói | Voa passando |
| 👽 Alien | Aparece e some |
| 🦑 Kraken | Tentáculo no mar |
| 🏴‍☠️ Navio Pirata | No horizonte |

---

## 📊 Eventos por Placar

### Ganhando (Eventos positivos)

| Placar | Evento |
|--------|--------|
| 2x0 | 🎉 Fogos leves |
| 3x0 | 🌈 Arco-íris |
| 4x0 | 👑 Coroa aparece |
| 5x0 | 🐉 DRAGÃO + evento especial |

### Empatando (Tensão)

| Placar | Evento |
|--------|--------|
| 1x1 | 🎈 Leve tensão |
| 2x2 | 🌤️ Nuvem aparece |
| 3x3 | ⛅ Céu muda |
| 4x4 | ⚡🌩️ TENSÃO MÁXIMA (raio, trovão, silêncio) |

### Perdendo (Motivação/Tristeza)

| Placar | Evento |
|--------|--------|
| 0x2 | 😅 Cachorro anima |
| 0x3 | 🌧️ Chuvinha |
| 0x4 | 🌈 Arco-íris de esperança |

---

## 🔥 Eventos por Sequência

### Sistema de Histórico
```
Sequências contam ENTRE PARTIDAS!

PARTIDA 1: ⚽⚽⚽⚽⚽ (5 gols)
PARTIDA 2: ⚽⚽⚽... 

3º gol da partida 2 = 8 GOLS SEGUIDOS TOTAL!
```

### Gols Consecutivos

| Sequência | Raridade | Evento EXCLUSIVO |
|-----------|----------|------------------|
| ⚽ x5 | 🟢 Incomum | 🔥 Bola pega fogo |
| ⚽ x10 | 🔵 Raro | ☄️ Cometa passa no céu |
| ⚽ x15 | 🟣 Épico | 🦅 Águia dourada voa |
| ⚽ x20 | 🟡 Lendário | 🐉 Dragão de FOGO |
| ⚽ x25 | 💎 Mítico | 🌋 Vulcão explode ao longe |
| ⚽ x30 | 💎 Mítico | 🌠 Chuva de meteoros |
| ⚽ x50 | ⚫ IMPOSSÍVEL | 🌌 Buraco negro abre no céu |
| ⚽ x100 | ⚫ IMPOSSÍVEL | 💥 BIG BANG |

### Defesas Consecutivas

| Sequência | Raridade | Evento EXCLUSIVO |
|-----------|----------|------------------|
| 🧤 x5 | 🟢 Incomum | 🧱 Muro aparece atrás |
| 🧤 x10 | 🔵 Raro | 🏰 Castelo surge |
| 🧤 x15 | 🟣 Épico | ❄️ Nevasca congela tudo |
| 🧤 x20 | 🟡 Lendário | 🐉 Dragão de GELO |
| 🧤 x25 | 💎 Mítico | 🌊 Tsunami gigante no fundo |
| 🧤 x30 | 💎 Mítico | 🛡️ Escudo dos deuses |
| 🧤 x50 | ⚫ IMPOSSÍVEL | 🕳️ Buraco negro SUGA as bolas |
| 🧤 x100 | ⚫ IMPOSSÍVEL | ⏱️ Tempo PARA |

### Vitórias Consecutivas

| Sequência | Raridade | Evento EXCLUSIVO |
|-----------|----------|------------------|
| 🏆 x3 | 🟢 Incomum | 🎉 Fogos de artifício |
| 🏆 x5 | 🔵 Raro | 🎺 Trombetas reais |
| 🏆 x10 | 🟣 Épico | 👑 Coroa desce do céu |
| 🏆 x15 | 🟡 Lendário | 🦁 Leão ruge ao fundo |
| 🏆 x20 | 💎 Mítico | 🏛️ Estátua sua aparece |
| 🏆 x25 | 💎 Mítico | ⚔️ Exército marcha ao fundo |
| 🏆 x50 | ⚫ IMPOSSÍVEL | 🌌 Constelação com seu nome |
| 🏆 x100 | ⚫ IMPOSSÍVEL | 🪐 Planeta novo surge no céu |

---

## 🏅 Sistema de Medalhas

### Medalhas vão pro PERFIL do jogador
```
┌─────────────────────────────────────┐
│                                     │
│  👤 @NomeDoJogador                  │
│                                     │
│  🏅 Medalhas: 🐉 🌋 👑              │
│                                     │
│  ⚽ Gols: 1.247                     │
│  🧤 Defesas: 834                    │
│  🏆 Vitórias: 523                   │
│                                     │
│  🔥 RECORDES:                       │
│  ⚽ Maior sequência gols: 23        │
│  🧤 Maior sequência defesas: 18    │
│  🏆 Maior sequência vitórias: 12   │
│                                     │
└─────────────────────────────────────┘
```
### Medalhas de Gols

| Medalha | Nome | Requisito | % tem |
|---------|------|-----------|-------|
| 🔥 | "Fogo" | 5 gols seguidos | 60% |
| ☄️ | "Cometa" | 10 gols seguidos | 25% |
| 🦅 | "Águia Dourada" | 15 gols seguidos | 8% |
| 🐉 | "Dragão de Fogo" | 20 gols seguidos | 2% |
| 🌋 | "Vulcão" | 25 gols seguidos | 0.5% |
| 🌠 | "Meteoros" | 30 gols seguidos | 0.1% |
| 🌌 | "Buraco Negro" | 50 gols seguidos | 0.01% |
| 💥 | "Big Bang" | 100 gols seguidos | 0.001% |

### Medalhas de Defesas

| Medalha | Nome | Requisito | % tem |
|---------|------|-----------|-------|
| 🧱 | "Muro" | 5 defesas seguidas | 55% |
| 🏰 | "Castelo" | 10 defesas seguidas | 20% |
| ❄️ | "Nevasca" | 15 defesas seguidas | 6% |
| 🐉 | "Dragão de Gelo" | 20 defesas seguidas | 1.5% |
| 🌊 | "Tsunami" | 25 defesas seguidas | 0.4% |
| 🛡️ | "Escudo dos Deuses" | 30 defesas seguidas | 0.08% |
| 🕳️ | "Buraco Negro" | 50 defesas seguidas | 0.005% |
| ⏱️ | "Tempo Parou" | 100 defesas seguidas | 0.0005% |

### Medalhas de Vitórias

| Medalha | Nome | Requisito | % tem |
|---------|------|-----------|-------|
| 🎉 | "Festeiro" | 3 vitórias seguidas | 70% |
| 🎺 | "Real" | 5 vitórias seguidas | 45% |
| 👑 | "Rei" | 10 vitórias seguidas | 15% |
| 🦁 | "Leão" | 15 vitórias seguidas | 4% |
| 🏛️ | "Estátua" | 20 vitórias seguidas | 1% |
| ⚔️ | "Exército" | 25 vitórias seguidas | 0.3% |
| 🌌 | "Constelação" | 50 vitórias seguidas | 0.02% |
| 🪐 | "Planeta" | 100 vitórias seguidas | 0.002% |

---

## 👤 Personagens

### Filosofia
```
Não é só "jogador de futebol"... 
É QUALQUER UM que quer bater pênalti!

Alien vs Pirata? PODE!
Padeiro vs Dinossauro? PODE!
```

### Lista de Personagens

#### 👔 Profissões
| Personagem | Visual |
|------------|--------|
| 👨‍🍳 Chef/Padeiro | Chapéu de cozinheiro, avental |
| 👨‍🚒 Bombeiro | Capacete, roupa amarela |
| 👨‍⚕️ Médico | Jaleco branco |
| 👷 Pedreiro | Capacete, colete |
| 👨‍🌾 Fazendeiro | Chapéu de palha |
| 👨‍🎤 Rockeiro | Moicano, guitarra |
| 👨‍🚀 Astronauta | Roupa espacial |
| 🧑‍✈️ Piloto | Óculos aviador |

#### ⚔️ Históricos/Fantasia
| Personagem | Visual |
|------------|--------|
| 🏴‍☠️ Pirata | Tapa-olho, chapéu |
| ⚔️ Cavaleiro | Armadura, espada |
| 🧙 Mago | Cajado, chapéu pontudo |
| 🥷 Ninja | Roupa preta, máscara |
| 🤴 Rei/Rainha | Coroa, manto |
| 🧛 Vampiro | Capa, dentes |
| 🧟 Zumbi | Rasgado, verde |
| 🦹 Super-herói | Capa, máscara |

#### 👽 Criaturas
| Personagem | Visual |
|------------|--------|
| 👽 Alien | Verde, cabeção |
| 🤖 Robô | Metal, olhos LED |
| 💀 Esqueleto | Só ossos |
| 🎃 Abóbora | Cabeça de abóbora |
| 👻 Fantasma | Transparente |
| 🐲 Dragão | Escamas, asas pequenas |
| 🦖 Dinossauro | T-Rex fofinho |

#### 🎉 Cultura Pop
| Personagem | Visual |
|------------|--------|
| 🕺 Discoteca | Roupa anos 70, afro |
| 🎸 Punk | Moicano colorido |
| 🏄 Surfista | Bermudão, cabelo loiro |
| 🎅 Papai Noel | Barba, roupa vermelha |
| 🤡 Palhaço | Nariz vermelho |

### Como Desbloquear

| Tipo | Como |
|------|------|
| ⚪ Comuns | Começa com alguns |
| 🟢 Incomuns | Joga X partidas |
| 🔵 Raros | Conquistas específicas |
| 🟣 Épicos | Medalhas difíceis |
| 🟡 Lendários | Sequências insanas |
| 🎃 Eventos | Datas especiais |
| 💎 Secretos | Descobrir! |

---

## 🔓 Combos Secretos

### Sistema
```
PERSONAGEM + CENÁRIO = Eventos SECRETOS!

Combinação CERTA = SEGREDO desbloqueado!
```

### Pirata + Praia

| Resultado | Gols | Def | Eventos | Raridade |
|-----------|------|-----|---------|----------|
| Ganhou | - | - | 🏴‍☠️ Navio | ⚪ |
| 2x0 | 2 | 5 | 🏴‍☠️ + ☠️💀 Fantasma | 🔵 Raro |
| 4x0 | 4 | - | 🏴‍☠️ + ⚔️ Espadas | 🟣 Épico |
| 5x0 (gols) | 5 | 0-4 | 🏴‍☠️ + 💰 Ouro | 🟡 Lendário |
| 5x0 (def) | 0-4 | 5 | 🏴‍☠️ + 🦑 Kraken | 🟡 Lendário |
| **5x0 PERFEITO** | **5** | **5** | 🏴‍☠️💰🦑👑 **TUDO!** | 💎 **IMPOSSÍVEL** |

### Surfista + Praia

| Resultado | Eventos |
|-----------|---------|
| Ganhou | 🌊 Onda grande |
| 5x0 gols | 🌊 + 🐬 Golfinhos saltam |
| 5x0 defesas | 🌊 + 🌊🌊 TSUNAMI |
| 2x0 | 🌊 + 🐋 Baleia (RARO!) |
| 5x0 PERFEITO | 🌊🐬🌊🌊🐋👑 TUDO! |

### Alien + Praia

| Resultado | Eventos |
|-----------|---------|
| Ganhou | 🛸 OVNI passa |
| 5x0 gols | 🛸 + ⚡ Raio abduz bola |
| 5x0 defesas | 🛸 + 🛸🛸🛸 INVASÃO |
| 2x0 | 🛸 + 🌌 Portal abre (RARO!) |
| 5x0 PERFEITO | 🛸⚡🛸🛸🛸🌌👑 TUDO! |

### Todos os Combos (5x0 PERFEITO)

| Personagem | Cenário | Evento IMPOSSÍVEL |
|------------|---------|-------------------|
| 🏴‍☠️ Pirata | 🏖️ Praia | 👑💀 Rei dos Piratas |
| 🏄 Surfista | 🏖️ Praia | 🌊👑 Deus do Mar |
| 👽 Alien | 🏖️ Praia | 🌌👑 Imperador Galáctico |
| 🧙 Mago | 🏖️ Praia | ✨👑 Arquimago Supremo |
| 🦖 Dino | 🏖️ Praia | 🦖👑 Rei dos Dinossauros |
| 🤖 Robô | 🏖️ Praia | 🤖👑 Skynet Ativada |
| 🧛 Vampiro | 🏖️ Praia | 🧛👑 Conde Drácula |
| 🥷 Ninja | 🏖️ Praia | 🥷👑 Mestre das Sombras |

### O que é 5x0 PERFEITO?
```
5x0 PERFEITO:
⚽ Você fez 5 gols (TODOS!)
🧤 Você defendeu 5 (TODOS!)

= 10/10 ACERTOS
= SUPER MEGA RARO! 💎💎💎
```

---

## 🛡️ Sistema Anti-Rage Quit

### O Problema
```
Placar: 4 x 0

Jogador perdendo: "Vou tomar 5x0..."
Jogador perdendo: "Ele vai ganhar evento RARO..."
Jogador perdendo: "NÃO VOU DAR ESSA MORAL!"

*desconecta*

💀 Jogador ganhando: "CADÊ MEU EVENTO?!" 😭
```

### Solução

#### Punição pra quem SAI
| Punição | Descrição |
|---------|-----------|
| ⏱️ Timeout | Não pode jogar por 5-10 min |
| 📉 Perde pontos | -50 pontos ranking |
| 💀 Conta derrota | 0x5 no histórico |
| 🚫 Streak quebra | Perde sequência |
| 🐔 +1 abandono | Visível no perfil |

#### Recompensa pra quem FICA
| Recompensa | Descrição |
|------------|-----------|
| ✅ Vitória completa | Conta como 5x0 |
| 🎲 Eventos | Desbloqueiam normalmente |
| 🎁 Bônus | +50 moedas extras |
| 🐔 Evento engraçado | Galinha passa 😂 |

### Eventos de W.O.

| Evento | Descrição |
|--------|-----------|
| 🏃💨 "Fugiu!" | Adversário some correndo |
| 🐔 Galinha | Galinha passa cacareando |
| 👻 Fantasma | Adversário vira fantasma |
| 🚪 Porta | Porta aparece, ele entra |
| 💨 Poeira | Só poeira onde ele estava |

### Sistema de Reputação
```
PERFIL DO JOGADOR:

👤 @NomeDoJogador

⚽ Vitórias: 50
💀 Derrotas: 30
🐔 Abandonos: 15  ← TODO MUNDO VÊ!

🏅 Medalhas: 🐔🐔🐔 (vergonha)
```

---

## 🎨 Assets

### Asset Pack Principal
- **Nome:** Creative Characters
- **Fonte:** Unity Asset Store
- **Estilo:** Cartoon/Low Poly
- **Uso:** Personagens, cenário, objetos

### Elementos do Cenário Praia
| Elemento | Asset |
|----------|-------|
| 🌴 Palmeiras | Creative Characters |
| 🏖️ Areia | Creative Characters |
| 🌊 Mar | Creative Characters |
| 🥅 Trave | Creative Characters |
| ⚽ Bola | Creative Characters |
| 👤 Personagens | Creative Characters |
| 🐕🐈🦀 Animais | Creative Characters |

---

## 📅 Próximos Passos

- [ ] Implementar cenário base da praia
- [ ] Sistema de eventos aleatórios
- [ ] Sistema de sequências entre partidas
- [ ] Sistema de medalhas e perfil
- [ ] Personagens e skins
- [ ] Combos secretos
- [ ] Sistema anti-rage quit
- [ ] Sons e música

---

> Documento vivo - será atualizado conforme o desenvolvimento
