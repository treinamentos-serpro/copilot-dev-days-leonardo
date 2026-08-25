<!-- l10n-sync: source-file="README.md" -->
<div align="center">

# 🎱 Soc Ops

**Un workshop práctico de GitHub Copilot Agent disfrazado de juego de Social Bingo.**

_Construye algo real. Publícalo con IA. Aprende haciendo._

[![Iniciar el Lab](https://img.shields.io/badge/▶%20Iniciar%20el%20Lab-brightgreen?style=for-the-badge)](workshop/es/GUIDE.md)
[![Java 21](https://img.shields.io/badge/Java-21-orange?style=flat-square)](https://adoptium.net/)
[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.4.2-6DB33F?style=flat-square)](https://spring.io/projects/spring-boot)

</div>

---

## ¿Qué es esto?

**Soc Ops** es una app de Social Bingo para encuentros presenciales donde los participantes encuentran personas que coinciden con preguntas divertidas — ¡el primero en conseguir 5 en línea gana!

Pero el verdadero juego ocurre en tu editor.

En ~1 hora, usarás el **GitHub Copilot Agent Mode** para evolucionar esta app — rediseñando la UI, inventando temas de quiz personalizados y entregando nuevas funcionalidades con flujos TDD multi-agente.

---

## 🎯 Qué vas a construir y aprender

| # | Habilidad | Qué vas a hacer |
|---|-----------|-----------------|
| 🏗️ | **Ingeniería de Contexto** | Enseña a Copilot sobre tu base de código |
| 🎨 | **Desarrollo Design-First** | Rediseña la UI con temas creativos |
| 🤖 | **Agentes Personalizados** | Crea un agente quiz master para nuevos icebreakers |
| 🔁 | **TDD Multi-Agente** | Desarrolla features con flujos red/green/refactor |

---

## 📚 Guía del Lab

| Parte | Título | Duración |
|-------|--------|----------|
| [**00**](workshop/es/00-overview.md) | Descripción General y Lista de Verificación | — |
| [**01**](workshop/es/01-setup.md) | Configuración e Ingeniería de Contexto | 15 min |
| [**02**](workshop/es/02-design.md) | Desarrollo Frontend Orientado al Diseño | 15 min |
| [**03**](workshop/es/03-quiz-master.md) | Quiz Master Personalizado | 10 min |
| [**04**](workshop/es/04-multi-agent.md) | Desarrollo Multi-Agente | 20 min |

> 💡 **Consejo:** Usa el DevContainer para un entorno sin configuración. Las guías también están en la carpeta [`workshop/es/`](workshop/es/) para lectura sin conexión.

---

## 🚀 Inicio Rápido

**Requisitos previos:** [Java 21 JDK](https://adoptium.net/) · [Apache Maven 3.9+](https://maven.apache.org/)

```bash
cd socops
./mvnw spring-boot:run
# Abre http://localhost:8080
```

```bash
# Compilar
./mvnw clean package

# Pruebas
./mvnw test
```

Se despliega automáticamente a GitHub Pages con cada push a `main`.
