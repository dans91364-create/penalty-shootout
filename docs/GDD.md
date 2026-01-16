# 📋 Game Design Document (GDD)
# Penalty Shootout 1v1 Online

**Versão:** 1.0  
**Data:** Janeiro 2026  
**Autor:** Dans91364  
**Engine:** Unity 2022.3 LTS  

---

## 1. Visão Geral do Jogo

### 1.1 Conceito
**Penalty Shootout 1v1 Online** é um jogo multiplayer competitivo de pênaltis onde dois jogadores se enfrentam em disputas rápidas e estratégicas. O jogo combina simplicidade mecânica com profundidade estratégica, permitindo partidas intensas de aproximadamente 2 minutos.

### 1.2 Gênero
- Esporte
- Multiplayer Online
- Casual/Competitivo
- Estratégia em Tempo Real

### 1.3 Plataformas-Alvo
- PC (Windows)
- WebGL (navegador)
- Possível expansão futura: Mobile (iOS/Android)

### 1.4 Público-Alvo
- Idade: 10+ anos
- Jogadores casuais que buscam partidas rápidas
- Fãs de futebol
- Jogadores competitivos que gostam de jogos de estratégia simples

### 1.5 Experiência Desejada
- **Rápido:** Partidas de 2 minutos
- **Tenso:** Decisões simultâneas criam suspense
- **Estratégico:** Antecipar o adversário
- **Divertido:** Animações e comemorações variadas
- **Imersivo:** Cenários únicos do mundo todo

---

## 2. Mecânicas de Gameplay

### 2.1 Mecânica Principal

#### Fluxo de Jogo
1. **Matchmaking:** Dois jogadores são conectados
2. **Preparação:** Cada jogador vê o cenário e se prepara
3. **Rodada de Pênalti:**
   - Um jogador é o **Batedor**
   - Outro jogador é o **Goleiro**
   - Ambos veem uma interface com 5 opções
   - Timer de 3 segundos começa
   - Ambos escolhem simultaneamente (clique em botão)
   - Animação é executada
   - Resultado: Gol ou Defesa
   - Pontuação é atualizada

4. **Alternância:** Papéis são invertidos para a próxima rodada
5. **Repetição:** Processo se repete até cada jogador ter chutado 5 vezes
6. **Resultado Final:** Jogador com mais gols vence

#### Posições de Escolha
```
┌─────────────────────┐
│  ①      ②      ③   │  ← Superior
│                     │
│  ④             ⑤   │  ← Inferior
└─────────────────────┘
```

- **①** Canto superior esquerdo
- **②** Centro superior (meio em cima)
- **③** Canto superior direito
- **④** Canto inferior esquerdo
- **⑤** Canto inferior direito

#### Lógica de Resultado
```
SE (escolha_batedor == escolha_goleiro):
    RESULTADO = DEFESA
    goleiro_ganha_ponto_de_defesa (opcional)
SENÃO:
    RESULTADO = GOL
    batedor_ganha_ponto
```

### 2.2 Sistema de Pontuação

#### Pontuação Base
- **Gol marcado:** +1 ponto
- **Defesa realizada:** 0 pontos (mas conta estatística)

#### Vitória
- Após 5 chutes por jogador (10 pênaltis total):
  - Jogador com **mais gols** vence
  - Em caso de empate: **Morte Súbita** (rodadas extras até desempate)

### 2.3 Timer e Pressão
- **3 segundos** para ambos escolherem
- Se um jogador não escolher a tempo:
  - **Batedor:** Chute automático no centro (posição ②)
  - **Goleiro:** Defesa automática no centro (posição ②)
- Barra de progresso visual mostra o tempo restante

### 2.4 Sistema de Turnos
```
Rodada 1: Jogador A bate, Jogador B defende
Rodada 2: Jogador B bate, Jogador A defende
Rodada 3: Jogador A bate, Jogador B defende
Rodada 4: Jogador B bate, Jogador A defende
Rodada 5: Jogador A bate, Jogador B defende
Rodada 6: Jogador B bate, Jogador A defende
Rodada 7: Jogador A bate, Jogador B defende
Rodada 8: Jogador B bate, Jogador A defende
Rodada 9: Jogador A bate, Jogador B defende
Rodada 10: Jogador B bate, Jogador A defende
```

---

## 3. Animações e Feedback Visual

### 3.1 Animações de Chute
- **Corrida:** Jogador corre em direção à bola
- **Chute para cada posição:**
  - Chute alto esquerdo (com efeito)
  - Chute alto centro
  - Chute alto direito (com efeito)
  - Chute rasteiro esquerdo
  - Chute rasteiro direito

### 3.2 Animações de Defesa
- **Posição inicial:** Goleiro preparado
- **Pulo para cada posição:**
  - Mergulho alto esquerdo
  - Pulo para cima (centro)
  - Mergulho alto direito
  - Mergulho baixo esquerdo
  - Mergulho baixo direito

### 3.3 Animações de Resultado

#### Em caso de GOL ⚽
- **Batedor:**
  - Siuuu (comemoração CR7)
  - Aviãozinho
  - Dança da vitória
  - Soco no ar
  - Camisa na cabeça
- **Goleiro:**
  - Decepção (mãos na cabeça)
  - Soco no chão
  - Olhar para o céu

#### Em caso de DEFESA 🧤
- **Batedor:**
  - Frustração (mãos na cabeça)
  - Chute no chão
  - Olhar para baixo
- **Goleiro:**
  - Comemoração épica
  - Soco no ar
  - Gritar de alegria
  - Provocação (gesto de "não passou")

### 3.4 Efeitos Visuais (VFX)
- Rastro da bola
- Partículas quando a bola bate na rede
- Partículas quando o goleiro defende
- Slow motion em momentos cruciais (rodada 5)
- Replay rápido (opcional)

### 3.5 Camera
- **Durante escolha:** Vista de cima da área
- **Durante execução:** Camera dinâmica que segue a ação
- **Durante comemoração:** Close no jogador comemorando
- **Placar:** Camera fixa mostrando o placar

---

## 4. Interface do Usuário (UI)

### 4.1 Menu Principal
```
┌─────────────────────────────┐
│   PENALTY SHOOTOUT 1V1      │
│                             │
│   [  JOGAR ONLINE  ]       │
│   [  COMO JOGAR    ]       │
│   [  CONFIGURAÇÕES ]       │
│   [  CRÉDITOS      ]       │
│   [  SAIR          ]       │
└─────────────────────────────┘
```

### 4.2 Tela de Matchmaking
```
┌─────────────────────────────┐
│   Procurando Oponente...    │
│                             │
│        [  ⚽  ]             │
│      Aguarde...             │
│                             │
│   [  CANCELAR  ]           │
└─────────────────────────────┘
```

### 4.3 Interface de Jogo (Durante Pênalti)

#### Visão do Batedor
```
┌─────────────────────────────┐
│  VOCÊ: 2  |  OPONENTE: 1   │
│  Rodada 5 de 10             │
├─────────────────────────────┤
│                             │
│   ESCOLHA ONDE CHUTAR:      │
│   ⏱️  3s                    │
│                             │
│   [①]  [②]  [③]            │
│        [④]  [⑤]            │
└─────────────────────────────┘
```

#### Visão do Goleiro
```
┌─────────────────────────────┐
│  VOCÊ: 1  |  OPONENTE: 2   │
│  Rodada 5 de 10             │
├─────────────────────────────┤
│                             │
│   ESCOLHA ONDE DEFENDER:    │
│   ⏱️  3s                    │
│                             │
│   [①]  [②]  [③]            │
│        [④]  [⑤]            │
└─────────────────────────────┘
```

### 4.4 Tela de Resultado
```
┌─────────────────────────────┐
│      VOCÊ VENCEU! 🏆        │
│                             │
│      VOCÊ    4 x 2   OPO    │
│                             │
│   Gols: 4                   │
│   Defesas: 1                │
│   Precisão: 80%             │
│                             │
│   [  JOGAR NOVAMENTE  ]    │
│   [  MENU PRINCIPAL   ]    │
└─────────────────────────────┘
```

---

## 5. Cenários e Ambientação

### 5.1 Lista de Cenários

#### 🇧🇷 Brasil - Praia de Copacabana
- **Descrição:** Gol montado na areia com a praia ao fundo
- **Elementos:** Mar, prédios, calçadão, sol, pessoas
- **Clima:** Ensolarado, tropical

#### 🇦🇷 Argentina - Bairro de Buenos Aires
- **Descrição:** Gol em rua de bairro (potrero)
- **Elementos:** Casas coloridas, rua de paralelepípedos
- **Clima:** Tarde nublada

#### 🇯🇵 Japão - Templo com Cerejeiras
- **Descrição:** Gol em jardim de templo
- **Elementos:** Cerejeiras em flor, templo ao fundo, lanternas
- **Clima:** Primavera, pétalas caindo

#### 🇮🇹 Itália - Praça de Roma
- **Descrição:** Gol em praça com Coliseu ao fundo
- **Elementos:** Coliseu, fontes, pedras antigas
- **Clima:** Pôr do sol dourado

#### 🇫🇷 França - Torre Eiffel
- **Descrição:** Gol aos pés da Torre Eiffel
- **Elementos:** Torre Eiffel, gramado, turistas ao fundo
- **Clima:** Dia claro

#### 🇬🇧 Inglaterra - Parque em Londres
- **Descrição:** Gol em parque urbano
- **Elementos:** Árvores, Big Ben ao longe, grama molhada
- **Clima:** Chuva leve, nublado

#### 🇪🇬 Egito - Pirâmides
- **Descrição:** Gol no deserto com pirâmides
- **Elementos:** Pirâmides, areia, camelo ao fundo
- **Clima:** Pôr do sol no deserto

#### 🇺🇸 EUA - Quadra de NYC
- **Descrição:** Gol em quadra de bairro
- **Elementos:** Prédios altos, grafite, cerca de alambrado
- **Clima:** Noite com luzes da cidade

#### 🇦🇺 Austrália - Outback
- **Descrição:** Gol no outback australiano
- **Elementos:** Terra vermelha, cangurus, arbustos
- **Clima:** Dia ensolarado

#### 🇿🇦 África do Sul - Savana
- **Descrição:** Gol na savana africana
- **Elementos:** Árvores de acácia, animais (girafas, zebras)
- **Clima:** Pôr do sol alaranjado

### 5.2 Elementos Comuns
Todos os cenários devem ter:
- **Gol padrão** (mesma proporção)
- **Marca de pênalti**
- **Iluminação adequada** para visibilidade
- **Público/Espectadores** (opcional, ao fundo)
- **Variação dia/noite** (futuro)

---

## 6. Audio Design

### 6.1 Música
- **Menu Principal:** Música animada e esportiva
- **Durante o jogo:** Música de fundo tensa/suspense
- **Vitória:** Música triunfante
- **Derrota:** Música melancólica

### 6.2 Efeitos Sonoros (SFX)

#### Interface
- Clique em botão
- Hover sobre botão
- Timer tick-tock
- Encontrou oponente

#### Gameplay
- **Apito do árbitro** (início de rodada)
- **Corrida** (passos na grama/areia)
- **Chute na bola** (som de impacto)
- **Bola na rede** (gol)
- **Bola nas mãos do goleiro** (defesa)
- **Torcida** (reações variadas)

#### Comemorações
- **Gritos de comemoração**
- **Gritos de frustração**
- **Torcida celebrando/lamentando**

---

## 7. Sistemas Técnicos

### 7.1 Networking (Photon PUN 2)

#### Matchmaking
- Sistema de sala automática
- Busca por jogadores disponíveis
- Timeout de 30 segundos

#### Sincronização
- **Escolhas:** Enviadas via RPC quando ambos escolherem
- **Timer:** Sincronizado entre clientes
- **Pontuação:** Atualizada no Master Client
- **Animações:** Disparadas simultaneamente

#### Desconexão
- Se um jogador desconectar:
  - Aguardar 10 segundos
  - Se não reconectar: Vitória automática para o oponente

### 7.2 Arquitetura do Código

#### Namespaces/Pastas
```
Scripts/
├── Core/
│   ├── GameManager.cs
│   └── SceneController.cs
├── Gameplay/
│   ├── PenaltyController.cs
│   ├── PlayerChoice.cs
│   ├── ScoreManager.cs
│   └── TimerController.cs
├── Network/
│   ├── PhotonLobby.cs
│   ├── PhotonRoom.cs
│   └── NetworkSync.cs
├── UI/
│   ├── MainMenuUI.cs
│   ├── GameplayUI.cs
│   ├── ResultUI.cs
│   └── ChoiceButtonHandler.cs
├── Animation/
│   ├── PlayerAnimator.cs
│   ├── GoalkeeperAnimator.cs
│   └── CameraController.cs
└── Audio/
    ├── AudioManager.cs
    └── SFXController.cs
```

#### Principais Classes

**GameManager.cs**
- Singleton
- Gerencia estado global do jogo
- Controla fluxo de telas

**PenaltyController.cs**
- Controla lógica de uma rodada de pênalti
- Recebe escolhas dos jogadores
- Calcula resultado (gol ou defesa)
- Dispara animações

**PlayerChoice.cs**
- Enum com as 5 posições
- Métodos de comparação

**ScoreManager.cs**
- Armazena pontuação de ambos jogadores
- Determina vencedor
- Estatísticas (gols, defesas, precisão)

**TimerController.cs**
- Conta 3 segundos
- Dispara evento quando tempo acaba
- UI de progresso

**NetworkSync.cs**
- RPCs para sincronizar escolhas
- Sincronizar pontuação
- Sincronizar estado do jogo

### 7.3 Estados do Jogo
```
MENU_PRINCIPAL
    ↓
MATCHMAKING
    ↓
PREPARANDO_PARTIDA
    ↓
ESPERANDO_ESCOLHA (Timer 3s)
    ↓
EXECUTANDO_PENALTI (Animação)
    ↓
MOSTRANDO_RESULTADO (2s)
    ↓
(Se não acabou) → ESPERANDO_ESCOLHA
(Se acabou) → TELA_RESULTADO_FINAL
```

---

## 8. Arte e Estilo Visual

### 8.1 Estilo Artístico
- **Low Poly / Semi-Realista**
- Cores vibrantes
- Iluminação dinâmica
- Foco em performance

### 8.2 Personagens
- Modelos 3D humanoides
- Customizável (futuro): cor de uniforme, número
- Animações fluidas do Mixamo

### 8.3 Bola
- Modelo 3D de bola de futebol padrão
- Material com normal map para detalhes
- Trail renderer para rastro

### 8.4 Gol
- Modelo padrão para todos os cenários
- Rede com física (Cloth ou simulada)
- Postes com material metálico

---

## 9. Progressão e Retenção (Futuro)

### 9.1 Sistema de Nível (Fase Futura)
- XP por partida jogada
- XP bônus por vitórias
- Níveis desbloqueiam:
  - Novos cenários
  - Novas comemorações
  - Customizações

### 9.2 Conquistas (Fase Futura)
- "Primeira Vitória"
- "5 Vitórias Seguidas"
- "Defesa Impossível" (defender todas as 5)
- "Artilheiro" (marcar todas as 5)
- "Viajante" (jogar em todos os cenários)

### 9.3 Ranking (Fase Futura)
- Leaderboard global
- Pontuação ELO
- Temporadas mensais

---

## 10. Plano de Desenvolvimento

### Fase 1: Protótipo Base (2-3 semanas)
**Objetivo:** Mecânica jogável offline

- [ ] Setup do projeto Unity
- [ ] UI básica com 5 botões
- [ ] Timer de 3 segundos
- [ ] Lógica de gol vs defesa
- [ ] Sistema de pontuação
- [ ] Feedback visual básico (texto)
- [ ] 1 cenário simples

### Fase 2: Multiplayer (2 semanas)
**Objetivo:** Dois jogadores online

- [ ] Integrar Photon PUN 2
- [ ] Sistema de matchmaking
- [ ] Sincronização de escolhas
- [ ] Sincronização de pontuação
- [ ] Sistema de turnos
- [ ] Tratamento de desconexão

### Fase 3: Animações e Visuais (3 semanas)
**Objetivo:** Jogo visualmente atraente

- [ ] Importar modelos 3D (jogador, goleiro, bola)
- [ ] Implementar animações de chute (Mixamo)
- [ ] Implementar animações de defesa
- [ ] Implementar comemorações variadas
- [ ] Sistema de câmera dinâmica
- [ ] Efeitos visuais (partículas, trails)

### Fase 4: Cenários (2 semanas)
**Objetivo:** 5-10 cenários únicos

- [ ] Criar/importar 10 cenários temáticos
- [ ] Iluminação e atmosfera de cada cenário
- [ ] Sistema de seleção aleatória de cenário

### Fase 5: Audio (1 semana)
**Objetivo:** Imersão sonora

- [ ] Implementar AudioManager
- [ ] Música de menu e gameplay
- [ ] SFX de gameplay
- [ ] SFX de UI

### Fase 6: Polimento (2 semanas)
**Objetivo:** Jogo completo e estável

- [ ] UI/UX refinada
- [ ] Balanceamento
- [ ] Correção de bugs
- [ ] Otimização de performance
- [ ] Testes multiplayer extensivos

### Fase 7: Build e Deploy (1 semana)
**Objetivo:** Publicar o jogo

- [ ] Build para Windows
- [ ] Build para WebGL
- [ ] Testes finais
- [ ] Deploy em plataforma (itch.io, etc)

**Tempo Total Estimado:** 13-15 semanas

---

## 11. Métricas de Sucesso

### KPIs Técnicos
- **Latência:** < 100ms em partidas
- **FPS:** 60 FPS estável
- **Taxa de Matchmaking:** < 30 segundos
- **Taxa de Conclusão:** > 80% das partidas finalizadas

### KPIs de Engajamento (Futuro)
- Retenção D1, D7, D30
- Média de partidas por sessão
- Tempo médio de sessão

---

## 12. Riscos e Mitigações

| Risco | Impacto | Probabilidade | Mitigação |
|-------|---------|---------------|-----------|
| Latência alta | Alto | Média | Otimizar sincronização, servidores regionais |
| Bugs de sincronização | Alto | Alta | Testes extensivos, código robusto |
| Falta de jogadores | Médio | Média | Marketing, bot offline (futuro) |
| Assets de baixa qualidade | Médio | Baixa | Curadoria cuidadosa do Asset Store |
| Animações quebradas | Médio | Média | Testar todas animações, fallbacks |

---

## 13. Referências e Inspirações

### Jogos Similares
- **8 Ball Pool** (Miniclip) - Mecânica de escolha simultânea
- **Head Ball 2** - Futebol arcade online
- **Penalty Shooters** (web) - Simplicidade e rapidez

### Estilo Visual
- **Rocket League** - Visual vibrante e arcade
- **Fall Guys** - Cores e diversão
- **FIFA Street** - Cenários urbanos

---

## 14. Glossário

- **RPC:** Remote Procedure Call (chamada de procedimento remoto)
- **PUN:** Photon Unity Networking
- **Mixamo:** Plataforma de animações 3D da Adobe
- **Asset Store:** Loja de assets do Unity
- **Low Poly:** Estilo visual com poucos polígonos
- **Trail Renderer:** Componente Unity para rastros
- **VFX:** Visual Effects (efeitos visuais)
- **SFX:** Sound Effects (efeitos sonoros)

---

**Documento vivo - Será atualizado conforme o desenvolvimento progride**

**Última atualização:** Janeiro 2026  
**Versão:** 1.0
