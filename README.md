# 🐉 Vila RPG Imersiva VR

> Um protótipo de fantasia medieval interativa construído na engine Unity

**Autor:** Armando José Freire de Melo

---

## ✦ Sobre o Projeto

Este projeto consiste em um **ambiente virtual inspirado em jogos de RPG e fantasia medieval**, desenvolvido na Unity. Foi criada uma vila explorável com casas, ruas e criaturas temáticas — incluindo um dragão gigante e uma personagem vampira animada.

O usuário controla um personagem em **terceira pessoa**, podendo caminhar pelo cenário, observar os habitantes da vila e explorar o ambiente virtual em busca de imersão narrativa.

## ✦ Stack Técnica

| Item | Detalhe |
|:---|:---|
| **Engine** | Unity (compatível com XR) |
| **Linguagem** | C# |
| **Plataforma de teste** | Windows — Unity Editor |
| **Plataforma preparada** | Android / Meta Quest |
| **XR Framework** | XR Plugin Management + OpenXR |
| **Input System** | Both (Old + New) |

## ✦ Contexto e Objetivos

A proposta é representar como experiências de **RPG narrativo podem evoluir dentro do Metaverso**, oferecendo maior imersão aos jogadores.

Em vez de apenas imaginar cenários ou utilizar chamadas de voz, os participantes poderiam explorar cidades virtuais, interagir com personagens e vivenciar campanhas em ambientes digitais.

A ideia central parte de um princípio simples: **transportar o RPG tradicional de mesa para um espaço virtual imersivo**, onde os jogadores não apenas imaginam a cena, mas passam a vivê-la dentro do espaço digital.

### Da mesa ao mundo virtual

Em vez de depender somente de chamadas por voz, texto ou encontros presenciais difíceis de organizar, os participantes poderiam entrar em tavernas, castelos, cidades ou cenários sombrios e interagir diretamente com o ambiente, objetos e personagens.

Mestres de jogo (*Game Masters*) também poderiam conduzir sessões de forma mais dinâmica, criando eventos narrativos em tempo real, especialmente em campanhas centradas em interpretação como *Vampiro: A Máscara* e outros sistemas narrativos.

---

## ✦ Funcionalidades

### 🐲 Dragão Animado

O asset do dragão já possuía animações prontas, utilizadas no projeto através de comandos de teclado:

| Tecla | Ação |
|:---:|:---|
| `W` | Caminhada |
| `Q` | Postura agressiva |
| `E` | Alerta |
| `R` | Posição de combate |
| `T` | Mordida |
| `Y` | Sopro de fogo |
| `U` | Voo para frente |
| `I` | Ataque aéreo |
| `O` | Voo parado |
| `A` | Pouso |
| `P` | Decolagem |
| `D` | Derrota |

> **Decisão criativa:** o tamanho do dragão foi aumentado em relação ao asset original para transmitir sensação de ameaça e grandiosidade dentro da narrativa.

### 🩸 Personagem Vampira

A personagem vampira importada já possuía **animação automática contínua**, característica aproveitada para tornar o ambiente mais vivo e dinâmico — fazendo a vila respirar por conta própria, mesmo sem ação direta do jogador.

### 🎲 Interação Criada — Dado D20

Foi desenvolvido um **dado D20 clicável** no cenário. Ao clicar no objeto, o sistema realiza uma rolagem virtual aleatória entre 1 e 20, exibindo o resultado no Console da Unity, simulando a mecânica clássica de um dado físico de RPG.

```csharp
int resultado = Random.Range(1, 21);
Debug.Log("D20 rolado: " + resultado);
```

---

## ✦ Como Executar

1. Clone este repositório:
   ```bash
   git clone https://github.com/armanfm/RPG-VR.git
   ```
2. Abra o projeto no Unity (versão compatível com XR)
3. Verifique a configuração de Input em:
   `Edit → Project Settings → Player → Configuration → Active Input Handling = Both`
4. Abra a cena principal em `Assets/Scenes/`
5. Pressione **Play** no Editor

### Controles do Personagem

- **W A S D** — movimentação do personagem em terceira pessoa
- **Mouse** — rotação da câmera
- **Click** — interagir com o D20
- **Teclas de comando** — controlar o dragão (ver tabela acima)

---

## ✦ Processo de Criação e Dificuldades

O desenvolvimento seguiu uma rota orgânica: primeiro a **composição da cena**, depois a **integração dos personagens**, e por fim os **ajustes finos de câmera e input**.

### Matérias-primas

Foram utilizados **assets 3D gratuitos** importados para compor a cena — vila, dragão, vampira e elementos ambientais. Sobre esses assets, foram realizados ajustes de escala, posicionamento, movimentação do personagem jogável e personalização visual de alguns elementos.

### Principais desafios

- **Organização da cena** — harmonizar múltiplos assets de origens diferentes para que parecessem pertencer ao mesmo universo visual
- **Câmera em terceira pessoa** — calibrar o comportamento da câmera para acompanhar o personagem sem atravessar paredes
- **Integração dos personagens** — garantir que dragão, vampira e jogador convivessem na cena sem conflitos de animação ou escala
- **Compatibilidade do Input System** — o desafio técnico mais delicado do projeto

### ⚠ A solução do Input — "Both"

Para que os **comandos de teclado do dragão** funcionassem ao mesmo tempo que a **interação por clique no D20**, foi necessário alterar a configuração de **Input Handling** da Unity para a opção **Both** — permitindo compatibilidade entre o sistema antigo e o novo Input System.

```
Edit → Project Settings → Player → Configuration → Active Input Handling = Both
```

Sem essa configuração, era preciso escolher entre uma coisa ou outra: ou os comandos do dragão funcionavam, ou o clique no dado funcionava. Com `Both`, ambos passam a coexistir sem conflito.

---

## ✦ Visão Expandida

A proposta deste projeto vai **além da entrega técnica**: ela enxerga o RPG como um espaço social vivo dentro do Metaverso.

Mestres conduziriam sessões de forma mais dinâmica, criando eventos narrativos em tempo real. Sistemas centrados em diálogo e decisão — como *Vampiro: A Máscara* — ganhariam um palco à altura. E o mercado de RPG online, já em crescimento, encontraria uma nova forma de existir: **imersiva, visual e emocionalmente densa**.

> *Em resumo: unir narrativa, interpretação social e presença virtual, transformando o RPG em uma experiência próxima de viver um filme interativo — onde cada espaço pode ser explorado, e cada ação ganha peso real dentro da cena.*

---

## ✦ Estrutura do Projeto

```
RPG-VR/
├── Assets/
│   ├── Scenes/
│   ├── Scripts/
│   ├── Prefabs/
│   └── ...
├── Packages/
├── ProjectSettings/
└── README.md
```

---

<div align="center">

**Armando Freire**

[github.com/armanfm](https://github.com/armanfm)

</div>
