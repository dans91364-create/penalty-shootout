# 📦 Lista de Assets Necessários

Este documento lista todos os assets necessários para o desenvolvimento do **Penalty Shootout 1v1 Online**, incluindo onde encontrá-los e sugestões específicas.

---

## 🎯 Categorias de Assets

1. [Personagens e Animações](#-personagens-e-animações)
2. [Modelos 3D](#-modelos-3d)
3. [Cenários](#-cenários)
4. [UI e Interface](#-ui-e-interface)
5. [Audio](#-audio)
6. [Efeitos Visuais (VFX)](#-efeitos-visuais-vfx)
7. [Packages e Plugins](#-packages-e-plugins)

---

## 🏃 Personagens e Animações

### Modelos de Personagens
**Fonte:** Mixamo / Unity Asset Store

#### Jogador (Batedor)
- **Modelo:** Humanoid rigged character
- **Sugestões:**
  - Mixamo: "X Bot" (gratuito) ou "Y Bot"
  - Asset Store: "Cartoon Soccer Player" ou similares

#### Goleiro
- **Modelo:** Mesmo modelo do jogador, mas com uniforme diferente
- **Variação:** Luvas de goleiro (pode ser material diferente)

### Animações - Mixamo (Gratuito)

#### Animações do Batedor
- [ ] **Idle** - Parado esperando
- [ ] **Walk/Run** - Corrida em direção à bola
- [ ] **Kick** - Chute (várias variações):
  - Kick (normal)
  - Right Foot Kick
  - Standing Kick
- [ ] **Celebrações (Gol):**
  - Victory Idle
  - Celebration (dance)
  - Raising Arms
  - Running (comemoração correndo)
  - Fist Pump
  - "Siuuu" - usar Jump ou outra animação criativa
  - Airplane (ou criar custom)
- [ ] **Frustração (Errou):**
  - Defeat
  - Sad Idle
  - Hands on Head
  - Frustrated

#### Animações do Goleiro
- [ ] **Goalkeeper Idle** - Posição inicial
- [ ] **Diving Saves** (mergulhos):
  - Dive Left
  - Dive Right  
  - Jump (para cima)
  - Dive Low Left
  - Dive Low Right
- [ ] **Catch** - Pegar a bola
- [ ] **Celebrações (Defesa):**
  - Victory
  - Fist Pump
  - Roar/Scream
- [ ] **Frustração (Levou Gol):**
  - Defeat
  - Hands on Head
  - Sitting Disappointed

**Link:** [mixamo.com](https://www.mixamo.com/)  
**Notas:**
- Criar conta Adobe (gratuito)
- Baixar com o modelo "X Bot" ou "Y Bot"
- Formato FBX para Unity
- Configurar como Humanoid no Unity

---

## 🎨 Modelos 3D

### Bola de Futebol
**Fontes:** Unity Asset Store / Free3D / CGTrader

**Sugestões:**
- [ ] **Simple Soccer Ball** (Asset Store - gratuito)
- [ ] **Sports Balls Pack** (Asset Store)
- [ ] Criar simples: Esfera com textura UV de bola

**Especificações:**
- Poly count: 500-2000 (low poly)
- Textura: 512x512 ou 1024x1024
- Normal map para detalhes
- Rigidbody com física

### Gol/Trave
**Fontes:** Asset Store / Sketchfab

**Sugestões:**
- [ ] **Soccer Goal** (Asset Store)
- [ ] **Football/Soccer Pack** (Asset Store)
- [ ] Criar no Blender (simples, retangular)

**Especificações:**
- Postes metálicos (material PBR)
- Rede com textura transparente
- Poly count: 1000-5000
- Dimensões FIFA padrão (escala proporcional)

### Marca de Pênalti
- [ ] Simples: Plane com textura/decal
- [ ] Linha branca pintada no chão

---

## 🌍 Cenários

### Assets de Cenários - Unity Asset Store

#### 🇧🇷 Brasil - Praia de Copacabana
**Sugestões:**
- [ ] **Beach Environment** (Asset Store)
- [ ] **Tropical Beach Pack**
- [ ] **Low Poly Beach**

**Elementos necessários:**
- Areia (terreno ou plane)
- Mar (water shader)
- Prédios ao fundo (low poly buildings)
- Calçadão (textura ou modelo)
- Palmeiras

#### 🇦🇷 Argentina - Bairro
**Sugestões:**
- [ ] **Urban City Pack**
- [ ] **Street Environment**
- [ ] **Favela/Slum Pack** (adaptar)

**Elementos necessários:**
- Casas coloridas
- Rua de paralelepípedos (textura)
- Muros, portões
- Iluminação de rua

#### 🇯🇵 Japão - Templo
**Sugestões:**
- [ ] **Japanese Temple Pack**
- [ ] **Asian Architecture Set**
- [ ] **Cherry Blossom Trees**

**Elementos necessários:**
- Templo (modelo)
- Árvores de cerejeira
- Lanternas japonesas
- Chão de pedra
- Partículas de pétalas caindo

#### 🇮🇹 Itália - Roma
**Sugestões:**
- [ ] **Rome City Pack**
- [ ] **Ancient Ruins**
- [ ] **Colosseum Model**

**Elementos necessários:**
- Coliseu (baixo poly ao fundo)
- Praça de pedra
- Fontes
- Ruínas romanas

#### 🇫🇷 França - Torre Eiffel
**Sugestões:**
- [ ] **Paris Pack**
- [ ] **Eiffel Tower Model**
- [ ] **European City**

**Elementos necessários:**
- Torre Eiffel (modelo simples)
- Gramado
- Árvores europeias
- Sky com nuvens

#### 🇬🇧 Inglaterra - Parque Londres
**Sugestões:**
- [ ] **London Park Pack**
- [ ] **Rainy Weather System**
- [ ] **UK Architecture**

**Elementos necessários:**
- Árvores de parque
- Grama molhada (shader)
- Big Ben ao fundo (opcional)
- Rain particles
- Fog/névoa

#### 🇪🇬 Egito - Pirâmides
**Sugestões:**
- [ ] **Desert Pack**
- [ ] **Egyptian Pyramids**
- [ ] **Sand Dunes**

**Elementos necessários:**
- Pirâmides (low poly)
- Terreno de areia
- Palmeiras de deserto
- Camelo (modelo simples)
- Skybox de deserto

#### 🇺🇸 EUA - NYC
**Sugestões:**
- [ ] **New York City Pack**
- [ ] **Urban Basketball Court**
- [ ] **Graffiti Pack**

**Elementos necessários:**
- Prédios altos (skyline)
- Cerca de alambrado
- Grafites em muros
- Iluminação noturna
- Asfalto urbano

#### 🇦🇺 Austrália - Outback
**Sugestões:**
- [ ] **Outback Environment**
- [ ] **Desert Wildlife Pack**
- [ ] **Australian Animals**

**Elementos necessários:**
- Terra vermelha (terreno)
- Arbustos
- Canguru (modelo)
- Rochas
- Céu aberto

#### 🇿🇦 África do Sul - Savana
**Sugestões:**
- [ ] **African Savanna Pack**
- [ ] **Safari Animals**
- [ ] **Acacia Trees**

**Elementos necessários:**
- Árvores de acácia
- Gramado de savana
- Animais (girafa, zebra) ao fundo
- Montanhas distantes
- Pôr do sol africano (skybox)

### Skyboxes
**Sugestões:**
- [ ] **AllSky - 200+ Sky / Skybox Set** (Asset Store)
- [ ] **Free Skyboxes** (Asset Store)
- [ ] **HDRI Haven** (gratuito, converter para cubemap)

**Necessários:**
- Dia claro
- Pôr do sol
- Noite
- Nublado/chuvoso
- Deserto
- Tropical

### Iluminação
- [ ] **Directional Light** (sol)
- [ ] **Post Processing Stack** (Asset Store - gratuito)
- [ ] **Light Shafts** (opcional)

---

## 🖼️ UI e Interface

### Ícones e Botões
**Fontes:** Kenney Assets / Flaticon / Font Awesome

**Necessários:**
- [ ] Botão padrão (normal, hover, pressed)
- [ ] Ícone de timer/relógio
- [ ] Ícone de gol (bola)
- [ ] Ícone de defesa (luvas)
- [ ] Ícone de configurações (engrenagem)
- [ ] Ícone de som on/off
- [ ] Números grandes (placar)
- [ ] Setas (← → ↑ ↓)

**Sugestões:**
- [ ] **Kenney UI Pack** (kenney.nl - gratuito)
- [ ] **Game GUI Pack** (Asset Store)
- [ ] **Sport UI Kit** (Asset Store)

### Fontes
**Fontes:** Google Fonts / DaFont

**Sugestões:**
- [ ] **Bebas Neue** - Placar e títulos
- [ ] **Roboto** - Textos gerais
- [ ] **Bangers** - Títulos divertidos
- [ ] **Anton** - Números grandes

**Link:** [fonts.google.com](https://fonts.google.com/)

### Telas/Painéis
- [ ] Background menu (gradient ou imagem)
- [ ] Panel de escolha (semi-transparente)
- [ ] Barra de timer (progress bar)
- [ ] Placar (scoreboard)
- [ ] Tela de resultado (victory/defeat)

---

## 🔊 Audio

### Música (Background)
**Fontes:** Incompetech / FreePD / Bensound / Asset Store

**Necessários:**
- [ ] **Menu Principal** - Energética e esportiva
  - Sugestão: "Wallpaper" (Incompetech)
- [ ] **Durante Jogo** - Tensa/suspense
  - Sugestão: "Cipher" (Incompetech)
- [ ] **Vitória** - Triunfante
  - Sugestão: "Fanfare" style
- [ ] **Derrota** - Melancólica/suave

**Links:**
- [incompetech.com](https://incompetech.com/music/) (gratuito com atribuição)
- [freepd.com](https://freepd.com/)
- [bensound.com](https://www.bensound.com/)

### Efeitos Sonoros (SFX)
**Fontes:** Freesound.org / Zapsplat / Asset Store

#### UI
- [ ] Clique em botão
- [ ] Hover
- [ ] Timer tick-tock
- [ ] Matchmaking "ding"

#### Gameplay
- [ ] Apito de árbitro
- [ ] Passos na grama
- [ ] Passos na areia
- [ ] Chute na bola (impacto)
- [ ] Bola na rede (gol)
- [ ] Bola nas mãos (defesa)
- [ ] Bola na trave (ping)

#### Multidão/Torcida
- [ ] Torcida geral (loop)
- [ ] Reação a gol (celebração)
- [ ] Reação a defesa (oooh)
- [ ] Suspense (antes do chute)

#### Vocalizações
- [ ] Grito de comemoração (masculino)
- [ ] Grito de frustração
- [ ] "Yes!" / "No!"

**Links:**
- [freesound.org](https://freesound.org/) (gratuito)
- [zapsplat.com](https://www.zapsplat.com/) (gratuito)
- **Sport Sound Effects Pack** (Asset Store)

---

## ✨ Efeitos Visuais (VFX)

### Partículas
**Fonte:** Unity Particle System / Asset Store

**Necessários:**
- [ ] **Rastro da bola** (Trail Renderer)
- [ ] **Impacto da bola na rede** (partículas brancas)
- [ ] **Defesa do goleiro** (partículas ao redor das mãos)
- [ ] **Poeira ao chutar** (em cenários de areia/terra)
- [ ] **Pétalas caindo** (Japão)
- [ ] **Chuva** (Inglaterra)
- [ ] **Faíscas de comemoração** (opcional)

**Sugestões:**
- [ ] **Cartoon FX Pack** (Asset Store)
- [ ] **Particle Effect Pack** (Asset Store - gratuito)
- [ ] Criar custom com Unity Particle System

### Shaders e Materiais
- [ ] Water shader (mar, fontes)
- [ ] Grass shader (grama realista)
- [ ] Sand shader (areia)
- [ ] Metal PBR (traves do gol)
- [ ] Cloth/Net (rede do gol)

**Sugestões:**
- [ ] **Standard Assets** (Unity)
- [ ] **Shader Graph** (criar custom)
- [ ] **Low Poly Shaders Pack** (Asset Store)

---

## 🔌 Packages e Plugins

### Essenciais

#### Photon PUN 2 (Multiplayer)
- **Nome:** Photon PUN 2 - FREE
- **Fonte:** Asset Store
- **Link:** [assetstore.unity.com/packages/tools/network/pun-2-free-119922](https://assetstore.unity.com/packages/tools/network/pun-2-free-119922)
- **Custo:** Gratuito (até 20 CCU)
- **Versão:** 2.x latest

#### Post Processing
- **Nome:** Post Processing Stack v2
- **Fonte:** Package Manager (Unity)
- **Uso:** Bloom, Color Grading, Vignette, Motion Blur

#### TextMesh Pro
- **Nome:** TextMesh Pro
- **Fonte:** Package Manager (Unity - incluído)
- **Uso:** UI text de alta qualidade

### Recomendados

#### DOTween (Animações UI)
- **Nome:** DOTween (HOTween v2)
- **Fonte:** Asset Store
- **Link:** [assetstore.unity.com/packages/tools/animation/dotween-hotween-v2-27676](https://assetstore.unity.com/packages/tools/animation/dotween-hotween-v2-27676)
- **Custo:** Gratuito
- **Uso:** Animações smooth de UI

#### Cinemachine
- **Nome:** Cinemachine
- **Fonte:** Package Manager (Unity)
- **Uso:** Sistema de câmera dinâmica

#### ProBuilder (Opcional)
- **Nome:** ProBuilder
- **Fonte:** Package Manager (Unity)
- **Uso:** Criar modelos 3D simples in-engine

---

## 📥 Ordem de Download/Importação

### Semana 1: Setup Básico
1. ✅ Photon PUN 2
2. ✅ Post Processing
3. ✅ TextMesh Pro
4. ✅ DOTween

### Semana 2: Personagens
5. Baixar personagens do Mixamo (X Bot)
6. Baixar animações de chute do Mixamo
7. Baixar animações de goleiro do Mixamo
8. Baixar celebrações do Mixamo

### Semana 3: Modelos Básicos
9. Bola de futebol
10. Gol/trave
11. UI Pack (Kenney)

### Semana 4+: Cenários
12. 1-2 cenários por vez (começar com Brasil)
13. Skyboxes
14. Props e decorações

### Semana 6+: Audio
15. Música (4 tracks)
16. SFX de gameplay
17. SFX de UI
18. Torcida/ambiente

### Semana 7+: VFX
19. Particle packs
20. Shaders especiais
21. Post-processing presets

---

## 💰 Custo Estimado

### Gratuito (Total: $0)
- Mixamo (animações)
- Photon PUN 2 (até 20 jogadores simultâneos)
- Unity Packages (TextMesh Pro, Post Processing, Cinemachine)
- Kenney Assets (UI)
- Freesound.org / Incompetech (audio)
- Models básicos (criar ou gratuitos)

### Baixo Custo (Opcional: $50-150)
- Asset Store: Cenários de qualidade ($10-30 cada)
- Asset Store: Particle packs ($5-15)
- Asset Store: Audio packs ($10-30)
- Modelos premium de personagens ($20-40)

### Médio Custo (Opcional: $200-500)
- Coleções completas de cenários
- Audio profissional
- Animações custom (contratar)

**Recomendação:** Começar 100% gratuito, investir depois conforme necessidade.

---

## 🔗 Links Úteis

### Sites de Assets Gratuitos
- **Mixamo:** [mixamo.com](https://www.mixamo.com/) - Animações
- **Kenney Assets:** [kenney.nl](https://kenney.nl/) - UI, modelos, audio
- **Freesound:** [freesound.org](https://freesound.org/) - SFX
- **Incompetech:** [incompetech.com](https://incompetech.com/) - Música
- **Sketchfab:** [sketchfab.com](https://sketchfab.com/) - Modelos 3D (filtrar CC0)
- **Poly Haven:** [polyhaven.com](https://polyhaven.com/) - HDRIs, texturas
- **Google Fonts:** [fonts.google.com](https://fonts.google.com/) - Fontes

### Unity Asset Store
- **Asset Store:** [assetstore.unity.com](https://assetstore.unity.com/)
- Filtrar por "Free" para assets gratuitos
- Aproveitar promoções (Weekly Sale)

### Tutoriais de Importação
- YouTube: "How to import Mixamo to Unity"
- YouTube: "Unity Photon PUN 2 setup tutorial"
- Unity Learn: [learn.unity.com](https://learn.unity.com/)

---

## ✅ Checklist de Assets

Use esta checklist para acompanhar o progresso:

### Personagens
- [ ] Modelo do jogador
- [ ] 5+ animações de chute
- [ ] 5+ animações de goleiro
- [ ] 3+ celebrações
- [ ] 2+ frustrações

### Modelos 3D
- [ ] Bola de futebol
- [ ] Gol com rede
- [ ] Marca de pênalti

### Cenários (mínimo 3 para MVP)
- [ ] Brasil - Praia
- [ ] Japão - Templo
- [ ] Egito - Pirâmides
- [ ] (Expandir conforme desenvolvimento)

### UI
- [ ] Botões
- [ ] Ícones
- [ ] Fontes (2)
- [ ] Backgrounds

### Audio
- [ ] 2 músicas (menu + jogo)
- [ ] 10+ SFX essenciais
- [ ] Torcida ambiente

### VFX
- [ ] Trail da bola
- [ ] Impactos
- [ ] 1 pack de partículas

### Plugins
- [ ] Photon PUN 2
- [ ] Post Processing
- [ ] TextMesh Pro
- [ ] DOTween

---

**Documento será atualizado conforme novos assets forem identificados**

**Última atualização:** Janeiro 2026
