# 🌑 Anahí (Projeto 3F)

*Action Metroidvania / RPG em Pixel Art 2D de Folclore, Flora e Fauna do Brasil*

**Projeto Integrador I — Análise e Desenvolvimento de Sistemas (ADS) 🚀**

**Ipê Arc Studio · Versão 3.0 · 2026**

---

## 📂 Estrutura do Repositório

```text
📦 Anahi-Projeto3F
 ┣ 📂 docs/
 ┃ ┣ 📜 DAN  — Documento de Análise de Negócio
 ┃ ┣ 📜 DDR  — Documento de Definição de Requisitos
 ┃ ┣ 📜 DAA  — Documento de Arquitetura e Diagramas
 ┃ ┣ 📜 Estética de Personagens
 ┃ ┗ 📜 Wireframes
 ┣ 📂 src/
 ┗ 📂 data/
```

---

## 📖 Sobre o Projeto

Identificamos uma lacuna significativa na forma como a História do Brasil e o nosso folclore são representados no mercado de jogos. Atualmente, essas temáticas costumam ser abordadas de maneira infantilizada, superficial ou estereotipada, o que quebra a imersão e afasta o público de jogadores mais assíduos.

O **Anahí (Projeto 3F — Folclore · Flora · Fauna)** nasce para quebrar esse estigma. Nosso objetivo é criar um **Action Metroidvania / Action RPG 2D em Pixel Art**, com atmosfera madura, no qual a fauna, a flora e as lendas brasileiras são tratadas com profundidade simbólica e mitológica. O jogador explora biomas interconectados, enfrenta entidades folclóricas em **combate action em tempo real** e constrói, ao longo da jornada, um **Codex Cultural** consultável.

O jogo é uma aplicação **desktop standalone**, single-player, com **persistência local em arquivo** (sem servidor).

---

## 💡 Nossas Motivações

* **Valorização Cultural Madura:** elevar o folclore brasileiro ao patamar de alta fantasia e terror, mostrando que criaturas como Cuca, Corpo Seco e Saci possuem enorme potencial para narrativas maduras e desafiadoras, apresentadas de forma **não infantilizada**.
* **Aprendizagem Ativa (*Show, don't tell*):** combater o consumo passivo de conteúdo, contando a história pelo cenário e pela exploração, recompensando a curiosidade do jogador.
* **Engajamento e Retenção:** entregar uma experiência recompensadora, com progressão de habilidades e um registro cultural consultável que favorece a revisitação do conteúdo.

---

## 🎯 Objetivos e Roadmap

- [ ] **Direção de Arte e Atmosfera:** consolidar a identidade visual em *Pixel Art 2D*, com paleta e design de som focados no clima noturno e de sobrevivência.
- [ ] **Design Narrativo Ambiental:** história contada pelo cenário, com pistas, ruínas e diálogos culturais que geram entradas no Codex.
- [ ] **Combate Action em Tempo Real:** implementar e balancear ataque leve, ataque pesado, esquiva, habilidades com *cooldown* e *stamina* — sem combate por turno.
- [ ] **Design de Criaturas Folclóricas:** traduzir entidades do folclore para mecânicas, comportamentos e *bosses*.
- [ ] **Exploração de Biomas:** ambientar o jogo em **dois biomas brasileiros — Mata Atlântica e Caatinga**.

---

## ⚙️ Funcionalidades (EAS — F1 a F13)

As 13 funcionalidades estão organizadas pelas etapas do Sistema de Informação: **Entrada**, **Processamento** e **Saída**.

**🟢 Entrada**
* **F1 — Menu Principal e Navegação Inicial**
* **F2 — Criação de Personagem** (nome e *classType*)
* **F3 — Gerenciamento de Jornadas** (até 3 *slots* salvos)
* **F4 — Configurações do Sistema**

**🟡 Processamento (gameplay ativo)**
* **F5 — Exploração de Biomas** (Mata Atlântica e Caatinga)
* **F6 — Combate Action contra Entidades do Folclore**
* **F7 — Sistema de Diálogos Culturais**
* **F8 — Habilidades Action Metroidvania**
* **F9 — Coleta de Itens Culturais**

**🔵 Saída**
* **F10 — Progressão de Personagem e Recompensas**
* **F11 — Codex Cultural Consultável**
* **F12 — Salvamento e Persistência de Progresso**
* **F13 — Painel de Resultados Educacionais** (acesso restrito à Professora)

---

## 🧍 Personagens

* **Anahí** — protagonista, indígena Tupi com forte conexão com a natureza. Após a invasão de sua aldeia por tropas portuguesas, parte em jornada para buscar a ajuda das entidades da mata. Caçadora ágil, usa **arco e flecha, tacapé** e pinturas rituais de **jenipapo** (luto) e **urucum** (vingança).
* **Cuca** — entidade de origem ibérica, bruxa do manguezal que se transforma em um **jacaré-açu**.
* **Saci Pererê** — entidade folclórica *(em desenvolvimento)*.
* **Corpo Seco** — entidade folclórica *(em desenvolvimento)*.

---

## 🏗️ Arquitetura

Arquitetura **em camadas** (*layered architecture*), na qual cada camada depende apenas da imediatamente inferior:

* **Apresentação (UI / HUD)** — telas e HUD (F1–F4, F11, F13).
* **Controle (Game Loop)** — `GameManager`, `InputManager`, controladores de Exploração, Combate, Diálogo, Progressão, Codex e Relatórios (UC01–UC13).
* **Domínio (Modelo + Regras)** — entidades de jogo e o **Motor de Regras de Negócio** (RN1–RN13).
* **Serviços / Infraestrutura** — `SaveManager`, `PersistenceService`, `AudioManager`, `AssetLoader`, `ExportService`, `ContentRepository`.
* **Dados — Disco Local** — *slots* de jornada (1–3), configuração, base do Codex e relatórios exportados.

---

## 🎨 Protótipo e Wireframes

Telas mapeadas (ver documento de **Wireframes**):

* Tela de Início / Título
* Tela de Menu
* Tela de Configurações
* Tela de Nova Jornada (seleção de classe e dificuldade)
* Tela de Continuar Jornada (*slots* de save)
* Tela de Jogo (HUD)
* Tela de Mapa

---

## 📋 Product Backlog (Sprint 1)

| Rank | Prioridade | Resumo | User Story | Sprint | Status |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | Alta | Documentação e Escopo | Como membro da equipe, quero finalizar o DAN e o DDR para garantir que o escopo está definido e alinhado. | 1 | Finalizado |
| 2 | Alta | Configuração do Repositório | Como desenvolvedor, quero configurar o repositório base e o motor de jogo para iniciar o versionamento. | 1 | Em progresso |
| 3 | Alta | Prototipação de Movimentação | Como jogador, quero andar, pular e interagir para testar a fluidez da movimentação. | 1 | A Fazer |
| 4 | Alta | Concept Art e Identidade | Como artista, quero definir paleta e esboços em Pixel Art para a atmosfera do bioma inicial. | 1 | Em progresso |
| 5 | Média | Esboço da Interface (HUD) | Como jogador, quero uma HUD minimalista (vida e energia) para focar na ação. | 1 | A Fazer |
| 6 | Média | Combate Action Básico | Como jogador, quero uma mecânica de ataque simples para validar a resposta e a tática do combate. | 1 | A Fazer |

---

## 👥 Equipe e Papéis

| Nome | Papel / Função | Contato |
| :--- | :--- | :--- |
| **João Pedro** | PO (*Product Owner*) | joao.naves@sempreceub.com |
| **Rodrigo Seabra** | SM (*Scrum Master*) | rodrigo.adrw@sempreceub.com |
| **Raphael Salvini** | Dev Team | raphael.henriques@sempreceub.com |
| **Luis Eduardo** | AD / DBA | luis.eduardof@sempreceub.com |
| **Vitor Camargo** | Arquiteto de Software | vitor.co@sempreceub.com |

---

## 📚 Referências

* **Folclore e Mitologia:** Câmara Cascudo, *Dicionário do Folclore Brasileiro* (1954).
* **Cultura Indígena / Pintura Corporal:** FUNAI — *Tradição: o arco e flecha na cultura das populações indígenas*; *Pinturas corporais indígenas carregam marcas de identidade cultural*. GALLOIS, D. T. (org.), *Kusiwa: pintura corporal e arte gráfica Wajãpi* (Museu do Índio/FUNAI, 2002).
* **Referências de Gameplay:** *Hollow Knight* (movimentação e narrativa ambiental), *Blasphemous* (tom maduro e combate).
* **Motor Gráfico:** Unity.
