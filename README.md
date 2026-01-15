# ⚽ Penalty Shootout 1v1 Online

Um jogo multiplayer rápido e divertido de pênaltis desenvolvido em Unity, onde dois jogadores se enfrentam em disputas emocionantes de apenas 2 minutos!

---

## 🎮 Sobre o Jogo

**Penalty Shootout 1v1 Online** é um jogo multiplayer competitivo onde dois jogadores se enfrentam em uma disputa de pênaltis. Cada jogador alterna entre chutar e defender, escolhendo entre 5 posições diferentes do gol. A mecânica é simples mas estratégica: ambos escolhem simultaneamente em apenas 3 segundos!

### ✨ Características Principais

- 🌐 **Multiplayer Online** - Jogue contra adversários do mundo todo
- ⚡ **Partidas Rápidas** - Cada jogo dura aproximadamente 2 minutos
- 🎭 **Animações Diversas** - Chutes, defesas, comemorações épicas (Siuuu, aviãozinho, danças)
- 🌍 **Cenários Únicos** - Jogue em locais icônicos de vários países
- 🎯 **Gameplay Estratégico** - Antecipe o movimento do adversário!

---

## 🎯 Como Jogar

### Mecânica do Jogo

1. **Dois jogadores online** se conectam para uma partida
2. Um jogador **chuta** enquanto o outro **defende** (goleiro)
3. Cada jogador tem **5 opções** para escolher:
   - ① Canto superior esquerdo
   - ② Meio em cima (centro superior)
   - ③ Canto superior direito
   - ④ Canto inferior esquerdo
   - ⑤ Canto inferior direito

4. **Timer de 3 segundos** - Ambos escolhem simultaneamente
5. **Resultado:**
   - 🧤 **Mesma escolha** = Defesa!
   - ⚽ **Escolhas diferentes** = Gol!

6. Cada jogador chuta **5 vezes** (alternando entre batedor e goleiro)
7. **Quem fizer mais gols vence!**

---

## 🌍 Cenários

Jogue em locais icônicos ao redor do mundo (não estádios profissionais):

- 🇧🇷 **Brasil** - Praia de Copacabana / Várzea
- 🇦🇷 **Argentina** - Bairro de Buenos Aires
- 🇯🇵 **Japão** - Templo com cerejeiras
- 🇮🇹 **Itália** - Praça de Roma com Coliseu ao fundo
- 🇫🇷 **França** - Aos pés da Torre Eiffel
- 🇬🇧 **Inglaterra** - Parque em Londres (com chuva)
- 🇪🇬 **Egito** - Pirâmides no horizonte
- 🇺🇸 **EUA** - Quadra de bairro em NYC
- 🇦🇺 **Austrália** - Outback com cangurus
- 🇿🇦 **África do Sul** - Savana com animais selvagens
- E muitos mais...

---

## 🛠️ Tecnologias Utilizadas

- **Engine:** Unity 2022.3 LTS ou superior
- **Linguagem:** C#
- **Multiplayer:** Photon PUN 2 (Photon Unity Networking 2)
- **Animações:** Mixamo (animações de personagens)
- **Assets:** Unity Asset Store (cenários, modelos 3D, efeitos)
- **Controle de Versão:** Git & GitHub

---

## 🚀 Como Rodar o Projeto

### Pré-requisitos

- Unity 2022.3 LTS ou superior
- Git
- Conta no Photon (para multiplayer) - [photonengine.com](https://www.photonengine.com/)

### Passos para Instalação

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/dans91364-create/penalty-shootout.git
   cd penalty-shootout
   ```

2. **Abra o projeto no Unity Hub:**
   - Abra o Unity Hub
   - Clique em "Add" (Adicionar)
   - Selecione a pasta do projeto clonado
   - Abra o projeto com a versão Unity 2022.3 LTS ou superior

3. **Configure o Photon PUN 2:**
   - Crie uma conta gratuita em [photonengine.com](https://www.photonengine.com/)
   - Crie um novo aplicativo PUN
   - Copie o App ID
   - No Unity, vá em `Window > Photon Unity Networking > PUN Wizard`
   - Cole seu App ID

4. **Importe os Assets necessários:**
   - Consulte o arquivo `docs/ASSETS.md` para a lista completa de assets
   - Baixe e importe os assets do Asset Store e Mixamo

5. **Execute o projeto:**
   - Abra a cena principal em `Assets/Scenes/MainMenu.unity`
   - Clique no botão Play no Unity Editor

---

## 📁 Estrutura do Projeto

```
penalty-shootout/
├── Assets/
│   ├── Animations/          # Animações de personagens e objetos
│   ├── Audio/               # Música e efeitos sonoros
│   ├── Materials/           # Materiais e texturas
│   ├── Models/              # Modelos 3D
│   ├── Prefabs/             # Prefabs reutilizáveis
│   ├── Scenes/              # Cenas do jogo
│   ├── Scripts/             # Scripts C#
│   ├── UI/                  # Elementos de interface
│   └── Resources/           # Recursos carregados dinamicamente
├── Packages/                # Pacotes do Unity
├── ProjectSettings/         # Configurações do projeto
├── docs/                    # Documentação
│   ├── GDD.md              # Game Design Document
│   └── ASSETS.md           # Lista de assets necessários
├── .gitignore              # Arquivos ignorados pelo Git
└── README.md               # Este arquivo
```

---

## 📚 Documentação

- **[Game Design Document (GDD)](docs/GDD.md)** - Especificações completas do jogo
- **[Lista de Assets](docs/ASSETS.md)** - Assets necessários e onde encontrá-los

---

## 🗺️ Roadmap

### Fase 1: Configuração Inicial ✅
- [x] Criar estrutura do repositório
- [x] Documentação inicial (README, GDD, ASSETS)
- [x] Configurar .gitignore para Unity

### Fase 2: Protótipo Base 🔄
- [ ] Configurar projeto Unity
- [ ] Implementar mecânica básica de escolha (UI com 5 botões)
- [ ] Implementar lógica de gol vs defesa
- [ ] Sistema de pontuação simples
- [ ] Timer de 3 segundos

### Fase 3: Multiplayer 🔜
- [ ] Integrar Photon PUN 2
- [ ] Sistema de matchmaking
- [ ] Sincronização de escolhas entre jogadores
- [ ] Sistema de turnos (alternar batedor/goleiro)

### Fase 4: Visual e Animações 🔜
- [ ] Importar modelos 3D (jogador, goleiro, bola, gol)
- [ ] Implementar animações de chute
- [ ] Implementar animações de defesa
- [ ] Criar cenário básico

### Fase 5: Polimento 🔜
- [ ] Adicionar comemorações variadas
- [ ] Múltiplos cenários de países
- [ ] Sistema de som e música
- [ ] Menu principal e UI completa
- [ ] Tela de resultado da partida

### Fase 6: Lançamento 🔜
- [ ] Testes multiplayer extensivos
- [ ] Otimização de performance
- [ ] Build para plataformas (PC, WebGL)
- [ ] Deploy e publicação

---

## 🤝 Como Contribuir

1. Fork o projeto
2. Crie uma branch para sua feature (`git checkout -b feature/MinhaFeature`)
3. Commit suas mudanças (`git commit -m 'Adiciona MinhaFeature'`)
4. Push para a branch (`git push origin feature/MinhaFeature`)
5. Abra um Pull Request

---

## 📝 Licença

Este projeto está sob a licença MIT. Veja o arquivo `LICENSE` para mais detalhes.

---

## 👥 Autores

- **Dans91364** - Criador e desenvolvedor principal

---

## 🙏 Agradecimentos

- Mixamo - Animações de personagens
- Unity Asset Store - Assets e recursos
- Photon - Solução de multiplayer
- Comunidade Unity Brasil

---

**Divirta-se jogando Penalty Shootout! ⚽🎮**
