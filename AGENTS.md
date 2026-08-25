# Soc Ops Agent Guidelines

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

## Documentation and Deployment

- Keep docs linked (not duplicated). Start with [README.md](README.md) and [workshop/GUIDE.md](workshop/GUIDE.md).
- Deployment/build checks for docs + Spring Boot packaging are in [.github/workflows/deploy.yml](.github/workflows/deploy.yml).
