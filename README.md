🌐 [Português (BR)](README.pt_BR.md) | [Español](README.es.md)

<div align="center">

# 🎱 Soc Ops

**A hands-on GitHub Copilot Agent workshop disguised as a Social Bingo game.**

_Build something real. Ship it with AI. Learn by doing._

[![Start the Lab](https://img.shields.io/badge/▶%20Start%20the%20Lab-brightgreen?style=for-the-badge)](workshop/GUIDE.md)
[![Java 21](https://img.shields.io/badge/Java-21-orange?style=flat-square)](https://adoptium.net/)
[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.4.2-6DB33F?style=flat-square)](https://spring.io/projects/spring-boot)

</div>

---

## What is this?

**Soc Ops** is an in-person Social Bingo app where participants find people who match fun icebreaker prompts and mark them off — first to get 5 in a row wins!

But the real game happens in your editor.

Over ~1 hour, you'll use **GitHub Copilot Agent Mode** to evolve this app from a plain starting point into something polished — redesigning the UI, inventing custom quiz themes, and shipping new features using multi-agent TDD workflows.

---

## 🎯 What You'll Build & Learn

| # | Skill | What you'll do |
|---|-------|----------------|
| 🏗️ | **Context Engineering** | Teach Copilot about your codebase with instruction files |
| 🎨 | **Design-First Development** | Redesign the UI with creative AI-driven themes |
| 🤖 | **Custom Agents** | Create a quiz master agent that invents new icebreakers |
| 🔁 | **Multi-Agent TDD** | Build features with red/green/refactor agent workflows |

---

## 📚 Lab Guide

| Part | Title | Time |
|------|-------|------|
| [**00**](workshop/00-overview.md) | Overview & Checklist | — |
| [**01**](workshop/01-setup.md) | Setup & Context Engineering | 15 min |
| [**02**](workshop/02-design.md) | Design-First Frontend | 15 min |
| [**03**](workshop/03-quiz-master.md) | Custom Quiz Master | 10 min |
| [**04**](workshop/04-multi-agent.md) | Multi-Agent Development | 20 min |

> 💡 **Tip:** Use the DevContainer for a zero-setup environment. Lab guides are also in the [`workshop/`](workshop/) folder for offline reading.

---

## 🚀 Quick Start

**Prerequisites:** [Java 21 JDK](https://adoptium.net/) · [Apache Maven 3.9+](https://maven.apache.org/)

```bash
cd socops
./mvnw spring-boot:run
# Open http://localhost:8080
```

```bash
# Build
./mvnw clean package

# Test
./mvnw test
```

Deploys automatically to GitHub Pages on push to `main`.
