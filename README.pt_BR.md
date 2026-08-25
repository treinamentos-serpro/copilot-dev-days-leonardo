<!-- l10n-sync: source-file="README.md" -->
<div align="center">

# 🎱 Soc Ops

**Um workshop prático de GitHub Copilot Agent disfarçado de jogo de Social Bingo.**

_Construa algo real. Publique com IA. Aprenda na prática._

[![Iniciar o Lab](https://img.shields.io/badge/▶%20Iniciar%20o%20Lab-brightgreen?style=for-the-badge)](workshop/pt_BR/GUIDE.md)
[![Java 21](https://img.shields.io/badge/Java-21-orange?style=flat-square)](https://adoptium.net/)
[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.4.2-6DB33F?style=flat-square)](https://spring.io/projects/spring-boot)

</div>

---

## O que é isso?

**Soc Ops** é um aplicativo de Social Bingo para encontros presenciais onde os participantes encontram pessoas que correspondem a perguntas divertidas — quem fizer 5 em linha primeiro ganha!

Mas o jogo de verdade acontece no seu editor.

Em ~1 hora, você usará o **GitHub Copilot Agent Mode** para evoluir este app — redesenhando a UI, inventando temas de quiz personalizados e entregando novas funcionalidades com fluxos TDD multi-agente.

---

## 🎯 O que você vai construir & aprender

| # | Habilidade | O que você vai fazer |
|---|------------|----------------------|
| 🏗️ | **Engenharia de Contexto** | Ensine o Copilot sobre sua base de código |
| 🎨 | **Desenvolvimento Design-First** | Redesenhe a UI com temas criativos |
| 🤖 | **Agentes Personalizados** | Crie um agente quiz master para novos icebreakers |
| 🔁 | **TDD Multi-Agente** | Desenvolva features com fluxos red/green/refactor |

---

## 📚 Guia do Lab

| Parte | Título | Duração |
|-------|--------|---------|
| [**00**](workshop/pt_BR/00-overview.md) | Visão Geral & Lista Rápida | — |
| [**01**](workshop/pt_BR/01-setup.md) | Configuração & Engenharia de Contexto | 15 min |
| [**02**](workshop/pt_BR/02-design.md) | Frontend Design-First | 15 min |
| [**03**](workshop/pt_BR/03-quiz-master.md) | Quiz Master Personalizado | 10 min |
| [**04**](workshop/pt_BR/04-multi-agent.md) | Desenvolvimento Multi-Agente | 20 min |

> 💡 **Dica:** Use o DevContainer para um ambiente sem configuração. Os guias também estão na pasta [`workshop/pt_BR/`](workshop/pt_BR/) para leitura offline.

---

## 🚀 Início Rápido

**Pré-requisitos:** [Java 21 JDK](https://adoptium.net/) · [Apache Maven 3.9+](https://maven.apache.org/)

```bash
cd socops
./mvnw spring-boot:run
# Abra http://localhost:8080
```

```bash
# Build
./mvnw clean package

# Testes
./mvnw test
```

O deploy é feito automaticamente no GitHub Pages ao fazer push para `main`.
