# Soc Ops Copilot Instructions

## Mandatory Development Checklist

Run from `socops/` before considering a task done:

- [ ] Lint (if configured)
- [ ] Build: `./mvnw clean package`
- [ ] Test: `./mvnw test`

## Project Shape

- Java 21 + Spring Boot 3.4.2 social bingo app.
- Backend: `socops/src/main/java/com/socops` (`web` controllers, `service/BoardAssembler` game logic, `model` API records).
- UI game: `socops/src/main/resources/templates/game.html` (Thymeleaf + inline JS). Keep browser and backend game rules aligned.
- Styles: `socops/src/main/resources/static/css/app.css` custom utilities (no Tailwind).
- Workshop/presentation lives in `workshop/` and `docs/`, separate from runtime app.

## Build and Test

Run from `socops/` with Maven wrapper:

```bash
./mvnw test
./mvnw clean package
./mvnw spring-boot:run
```

App default port: `8080`. Automated tests currently emphasize `BoardAssembler`; validate controller/browser/JS/accessibility changes manually when relevant.

## Implementation Conventions

- Preserve project style: Java records, `var` when clearer, immutable outputs, pure static helpers in `BoardAssembler`, JUnit 5 with descriptive `@DisplayName`.
- Preserve board contract unless explicitly changed: 5x5 grid, 25 cells, free center at index 12 selected.
- Keep API and UI behavior in sync for generation, selection, and win detection.
- Add/update focused backend tests in `socops/src/test/java` for rule changes.
- Follow [.github/instructions/css-utilities.instructions.md](.github/instructions/css-utilities.instructions.md) and, for UI redesign, [.github/instructions/frontend-design.instructions.md](.github/instructions/frontend-design.instructions.md).
- Keep icebreaker prompts inclusive and low-risk; prefer [quiz master agent](.github/agents/quiz-master.agent.md). Use TDD agents when doing TDD workflows.

## Design Guide

### Goal

Treat the interface as a polished product, not a default template. The app should feel intentional, coherent, and visually distinctive for an in-person social game.

### Styling Rules

- Use the existing utility-first CSS approach in `socops/src/main/resources/static/css/app.css` instead of introducing a new framework.
- Prefer a cohesive visual theme with a clear primary palette, supporting neutrals, and a single strong accent color.
- Keep contrast high for readability, especially in dark mode and for text inside tiles and action buttons.
- Maintain consistent spacing, borders, and shadows across the lobby, board, header, and modal states.
- Respect the minimal, browser-friendly runtime stack: HTML, CSS utilities, and inline JavaScript.

### Theme Direction

- Dark-mode themes are preferred for modern game interfaces, with layered gradients and subtle glow accents.
- Pick a dominant mood and commit to it: for example, midnight gaming, premium glass, or cyberpunk neon.
- Avoid generic “AI default” styling: no bland white cards, overused purple-white gradients, or repetitive neutral palettes.
- Use strong typography and restrained motion to create polish without becoming noisy.

### UI Expectations

- Keep the lobby clear and welcoming, with a strong call-to-action.
- Preserve the 5x5 board layout and game interactions while improving visual hierarchy.
- Make selected cells and winning lines visually obvious without breaking accessibility.
- Keep the victory modal and banner noticeable but not distracting.
- Ensure hover, tap, and focus states are visually consistent and accessible.

### Implementation Pattern

- Update shared utility classes before adding page-specific overrides.
- Keep CSS specificity low and avoid scattered one-off styles when a utility can be reused.
- Review the game page and CSS together so the markup and the styling stay in sync.
- When changing the design, validate both the gameplay logic and the front-end behavior manually.

## Documentation and Deployment

- Keep docs linked (not duplicated). Start with [README.md](README.md) and [workshop/GUIDE.md](workshop/GUIDE.md).
- Deployment/build checks for docs + Spring Boot packaging are in [.github/workflows/deploy.yml](.github/workflows/deploy.yml).
