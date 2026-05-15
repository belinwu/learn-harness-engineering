<p align="center">
  <a href="./README.md"><img alt="English" src="https://img.shields.io/badge/EN-English-blue?style=flat-square"></a>
  <a href="./README-CN.md"><img alt="简体中文" src="https://img.shields.io/badge/ZH-简体中文-red?style=flat-square"></a>
  <a href="./README-ZH-TW.md"><img alt="繁體中文" src="https://img.shields.io/badge/ZH--TW-繁體中文-orange?style=flat-square"></a>
  <a href="./README-JA.md"><img alt="日本語" src="https://img.shields.io/badge/JA-日本語-green?style=flat-square"></a>
  <a href="./README-KO.md"><img alt="한국어" src="https://img.shields.io/badge/KO-한국어-blueviolet?style=flat-square"></a>
  <a href="./README-ES.md"><img alt="Español" src="https://img.shields.io/badge/ES-Español-yellow?style=flat-square"></a>
  <a href="./README-FR.md"><img alt="Français" src="https://img.shields.io/badge/FR-Français-007EC6?style=flat-square"></a>
  <a href="./README-RU.md"><img alt="Русский" src="https://img.shields.io/badge/RU-Русский-informational?style=flat-square"></a>
  <a href="./README-DE.md"><img alt="Deutsch" src="https://img.shields.io/badge/DE-Deutsch-2EA043?style=flat-square"></a>
  <a href="./README-AR.md"><img alt="العربية" src="https://img.shields.io/badge/AR-العربية-success?style=flat-square"></a>
  <a href="./README-VI.md"><img alt="Tiếng Việt" src="https://img.shields.io/badge/VI-Tiếng_Việt-cc6699?style=flat-square"></a>
  <a href="./README-UZ.md"><img alt="Oʻzbekcha" src="https://img.shields.io/badge/UZ-Oʻzbekcha-1A8BBA?style=flat-square"></a>
</p>

# Learn Harness Engineering

> **Проектный курс о построении окружений, управлении состоянием, верификации и механизмах контроля, которые делают KI-Coding-агентов надёжными.**

Learn Harness Engineering — курс, посвящённый инженерии AI-агентов для кодинга. Мы глубоко изучили и обобщили самые передовые теории и практики Harness Engineering в индустрии. Наши основные источники:

- [OpenAI: Harness engineering: leveraging Codex in an agent-first world](https://openai.com/index/harness-engineering/)
- [Anthropic: Effective harnesses for long-running agents](https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents)
- [Anthropic: Harness design for long-running application development](https://www.anthropic.com/engineering/harness-design-long-running-apps)
- [Awesome Harness Engineering](https://github.com/walkinglabs/awesome-harness-engineering)

> **Быстрый старт?** Skill [`skills/harness-creator/`](../../skills/) поможет вам за считанные минуты создать готовое к продакшену harness (AGENTS.md, feature-списки, init.sh, верификационные workflow) для вашего собственного проекта.

---

## Содержание

- [Визуальная подборка](#визуальная-подборка)
- [Модель умна, harness делает её надёжной](#модель-умна-harness-делает-её-надёжной)
- [Быстрый старт: улучшите своего агента уже сегодня](#быстрый-старт-улучшите-своего-агента-уже-сегодня)
- [Итоговый проект: настоящее приложение](#итоговый-проект-настоящее-приложение)
- [Путь обучения](#путь-обучения)
- [Учебная программа](#учебная-программа)
- [Skills](#skills)
- [Другие курсы](#другие-курсы)

---

## Визуальная подборка

### Главная страница курса
> Обзор курса и введение в ключевые философии, формирующие чёткий путь для старта.

![Предпросмотр главной страницы курса](../../docs/public/screenshots/readme/zh-home.png)

### Иммерсивные лекции
> Глубокое погружение в реальные проблемы и практические проекты (например, Проект 01) для иммерсивного обучения.

![Предпросмотр лекций курса](../../docs/public/screenshots/readme/zh-lecture-01.png)

### Библиотека шаблонов
> Шаблоны и эталонные конфигурации, созданные для решения распространённых проблем при разработке многоходовых KI-агентов, таких как потеря контекста и преждевременное завершение задач.

![Предпросмотр библиотеки шаблонов](../../docs/public/screenshots/readme/zh-resources.png)

## PDF-учебники курса

Репозиторий теперь содержит pipeline для генерации PDF-версий учебных материалов.

- Запустите `npm run pdf:build`, чтобы сгенерировать PDF на английском и китайском языках локально.
- Готовые файлы помещаются в `artifacts/pdfs/`.
- Запустите `npm run screenshots:readme`, если хотите обновить скриншоты для README.
- GitHub Actions workflow [`release-course-pdfs.yml`](../../.github/workflows/release-course-pdfs.yml) может создать PDF и опубликовать их в GitHub Releases.

---

## Модель умна, harness делает её надёжной

Существует суровая правда, которую большинство людей познаёт на собственном опыте: **самая мощная модель в мире всё равно провалит реальную инженерную задачу, если вы не построите для неё подходящее окружение.**

Вы, вероятно, сталкивались с этим сами. Вы даёте Claude или GPT задачу в своём репозитории. Всё начинается хорошо — агент читает файлы, пишет код, выглядит продуктивно. Затем что-то идёт не так. Он пропускает шаг. Ломает тест. Говорит «готово", но на самом деле ничего не работает. Вы тратите больше времени на исправление, чем если бы сделали всё сами.

Это не проблема модели. Это проблема harness.

Доказательства однозначны. Anthropic провёл контролируемый эксперимент: та же модель (Opus 4.5), тот же промпт («постройте 2D-ретро-игровой редактор"). Без harness агент потратил 9 $ за 20 минут и создал что-то неработающее. С полным harness (планировщик + генератор + оценщик) он потратил 200 $ за 6 часов и создал игру, в которую можно реально играть. Модель не изменилась. Изменился harness.

OpenAI сообщает то же самое с Codex: в хорошо подготовленном репозитории та же модель переходит от «ненадёжной" к «надёжной". Не маргинальное улучшение — качественный скачок.

**Этот курс научит вас, как построить такое окружение.**

```text
                    THE HARNESS PATTERN
                    ====================

    You --> give task --> Agent reads harness files --> Agent executes
                                                        |
                                              harness governs every step:
                                              |
                                              +--> Instructions: what to do, in what order
                                              +--> Scope:       one feature at a time, no overreach
                                              +--> State:       progress log, feature list, git history
                                              +--> Verification: tests, lint, type-check, smoke runs
                                              +--> Lifecycle:   init at start, clean state at end
                                              |
                                              v
                                         Agent stops only when
                                         verification passes
```

---

## Что на самом деле означает Harness Engineering

Harness Engineering — это построение полноценной рабочей среды вокруг модели, чтобы она давала надёжные результаты. Речь не о том, чтобы писать лучшие промпты. Речь о проектировании системы, в которой модель работает.

Harness состоит из пяти подсистем:

```text
    ┌─────────────────────────────────────────────────────────────────┐
    │                        THE HARNESS                              │
    │                                                                 │
    │   ┌──────────────┐  ┌──────────────┐  ┌──────────────────────┐ │
    │   │ Instructions  │  │    State     │  │   Verification       │ │
    │   │              │  │              │  │                      │ │
    │   │ AGENTS.md    │  │ progress.md  │  │ tests + lint         │ │
    │   │ CLAUDE.md    │  │ feature_list │  │ type-check           │ │
    │   │ feature_list │  │ git log      │  │ smoke runs           │ │
    │   │ docs/        │  │ session hand │  │ e2e pipeline         │ │
    │   └──────────────┘  └──────────────┘  └──────────────────────┘ │
    │                                                                 │
    │   ┌──────────────┐  ┌──────────────────────────────────────┐   │
    │   │    Scope     │  │         Session Lifecycle             │   │
    │   │              │  │                                      │   │
    │   │ one feature  │  │ init.sh at start                     │   │
    │   │ at a time   │  │ clean-state checklist at end          │   │
    │   │ definition   │  │ handoff note for next session        │   │
    │   │ of done      │  │ commit only when safe to resume      │   │
    │   └──────────────┘  └──────────────────────────────────────┘   │
    │                                                                 │
    └─────────────────────────────────────────────────────────────────┘

    The MODEL decides what code to write.
    The HARNESS governs when, where, and how it writes it.
    The harness doesn't make the model smarter.
    It makes the model's output reliable.
```

Каждая подсистема выполняет свою задачу:

- **Instructions** — указывают агенту, что делать, в каком порядке и что прочитать перед началом. Не один гигантский файл, а структура прогрессивного раскрытия, по которой агент навигирует по мере необходимости.
- **State** — отслеживает, что сделано, что в работе и что предстоит дальше. Сохраняется на диске, чтобы следующая сессия продолжала точно с того места, где остановилась предыдущая.
- **Verification** — только существующий набор тестов считается доказательством. Агент не может сообщить об успехе без исполняемого подтверждения.
- **Scope** — ограничивает агента одной фичей за раз. Никаких превышений полномочий. Никакого полуготового завершения трёх вещей. Никакой переписки feature-списка, чтобы скрыть незавершённую работу.
- **Session Lifecycle** — инициализация в начале. Очистка в конце. Оставление чистого пути перезапуска для следующей сессии.

---

## Почему существует этот курс

Вопрос не в том, «могут ли модели писать код?" Могут. Вопрос в том: **могут ли они надёжно выполнять реальные инженерные задачи в реальных репозиториях на протяжении нескольких сессий без постоянного человеческого контроля?**

На данный момент ответ: нет без harness.

```text
    WITHOUT HARNESS                          WITH HARNESS
    ==============                          ============

    Session 1: agent writes code            Session 1: agent reads instructions
              agent breaks tests                      agent runs init.sh
              agent says "done"                       agent works on one feature
              you fix it manually                     agent verifies before claiming done
                                                       agent updates progress log

    Session 2: agent starts fresh                    agent commits clean state
              agent has no memory
              of what happened before         Session 2: agent reads progress log
              agent re-does work                       agent picks up exactly where it left off
              or does something else entirely          agent continues the unfinished feature
              you fix it again                         you review, not rescue

    Result: you spend more time                  Result: agent does the work,
            cleaning up than if you                      you verify the result
            did it yourself
```

Вопросы, которые действительно волнуют этот курс:

- Какие дизайны harness повышают процент завершения задач?
- Какие дизайны сокращают переделки и ложные завершения?
- Какие механизмы поддерживают продвижение длительных задач?
- Какие структуры сохраняют поддерживаемость системы после множества запусков агента?

---

## Учебная программа и документация

Полные материалы курса доступны на **[сайте документации](https://walkinglabs.github.io/learn-harness-engineering/)**.

Программа разделена на три части:

1. **Лекции**: 12 концептуальных блоков, объясняющих теорию Harness Engineering.
2. **Проекты**: 6 практических проектов, в которых вы строите агентскую рабочую среду с нуля.
3. **Библиотека шаблонов**: готовые к копированию шаблоны (`AGENTS.md`, `feature_list.json`, `init.sh` и др.), которые вы можете использовать в своих репозиториях уже сегодня.

---

## Быстрый старт: улучшите своего агента уже сегодня

Вам не нужно читать все 12 лекций, чтобы получить пользу. Если вы уже используете coding-агента в реальном проекте, вы можете улучшить его прямо сейчас.

Идея проста: вместо того чтобы писать только промпты, дайте своему агенту набор структурированных файлов, определяющих, что нужно сделать, что уже сделано и как проверить результат. Эти файлы находятся в вашем репозитории, поэтому каждая сессия стартует из одного и того же состояния.

```text
    YOUR PROJECT ROOT
    ├── AGENTS.md              <-- операционное руководство агента
    ├── CLAUDE.md              <-- (альтернатива, если вы используете Claude Code)
    ├── init.sh                <-- выполняет install + verify + start
    ├── feature_list.json      <-- какие фичи существуют, какие выполнены
    ├── claude-progress.md     <-- что произошло в каждой сессии
    └── src/                   <-- ваш фактический код
```

Скачайте стартовые шаблоны из [библиотеки шаблонов](https://walkinglabs.github.io/learn-harness-engineering/ru/resources/) и добавьте их в свой проект. Вот и всё. Четыре файла — и ваши агентские сессии уже станут значительно стабильнее, чем с одними промптами.

---

## Итоговый проект: настоящее приложение

Все шесть проектов курса вращаются вокруг одного продукта: **десктопного приложения для персонального управления знаниями на базе Electron.**

```text
    ┌─────────────────────────────────────────────────────┐
    │               Knowledge Base Desktop App            │
    │                                                     │
    │  ┌──────────────┐  ┌──────────────────────────────┐│
    │  │ Document List │  │       Q&A Panel              ││
    │  │              │  │                              ││
    │  │ doc-001.md   │  │  Q: What is harness eng?    ││
    │  │ doc-002.md   │  │  A: The environment built    ││
    │  │ doc-003.md   │  │     around an agent model... ││
    │  │ ...          │  │     [citation: doc-002.md]   ││
    │  └──────────────┘  └──────────────────────────────┘│
    │                                                     │
    │  ┌─────────────────────────────────────────────────┐│
    │  │ Status Bar: 42 docs | 38 indexed | last sync 3m ││
    │  └─────────────────────────────────────────────────┘│
    └─────────────────────────────────────────────────────┘

    Core features:
    ├── Import local documents
    ├── Manage a document library
    ├── Process and index documents
    ├── Run AI-powered Q&A over imported content
    └── Return grounded answers with citations
```

Этот проект выбран потому, что он сочетает высокую практическую пользу, достаточную реальную продуктовую сложность и хороший сценарий для наблюдения улучшений harness (до/после).

Каждый курсовой проект (starter/solution) — это полная копия этого Electron-приложения на соответствующей стадии развития. Starter для P(N+1) получается из solution для P(N) — приложение эволюционирует вместе с ростом ваших навыков harness.

---

## Путь обучения

Курс рассчитан на последовательное прохождение. Каждая фаза строится на предыдущей.

```text
    Phase 1: SEE THE PROBLEM              Phase 2: STRUCTURE THE REPO
    ========================              ==========================

    L01  Strong models ≠ reliable         L03  Repository as single
         execution                              source of truth
    L02  What harness actually means
                                       L04  Split instructions across
         |                                   files, not one giant file
         v
    P01  Prompt-only vs.                       |
         rules-first comparison                v
                                               P02  Agent-readable workspace


    Phase 3: CONNECT SESSIONS             Phase 4: FEEDBACK & SCOPE
    ==========================           =========================

    L05  Keep context alive               L07  Draw clear task boundaries
         across sessions
                                       L08  Feature lists as harness
    L06  Initialize before every               primitives
         agent session
                                               |
         |                                     v
         v                                     P04  Runtime feedback to
    P03  Multi-session continuity                   correct agent behavior


    Phase 5: VERIFICATION                 Phase 6: PUT IT ALL TOGETHER
    =====================                 ============================

    L09  Stop agents from                 L11  Make agent's runtime
         declaring victory early               observable

    L10  Full-pipeline run =              L12  Clean handoff at end of
         real verification                      every session

         |                                     |
         v                                     v
    P05  Agent verifies its own work       P06  Build a complete harness
                                               (capstone project)
```

Каждая фаза занимает примерно неделю при обучении параллельно с основной работой. Если двигаться быстрее, фазы 1–3 можно пройти за длинные выходные.

---

## Учебная программа

### Лекции — 12 концептуальных блоков, каждый отвечает на один ключевой вопрос

*Читайте полный текст каждой лекции на [сайте документации](https://walkinglabs.github.io/learn-harness-engineering/).*

| Занятие | Вопрос | Ключевая идея |
|---------|--------|---------------|
| [L01](../../docs/lectures/lecture-01-why-capable-agents-still-fail/index.md) | Почему сильные модели всё равно ошибаются на реальных задачах? | Разрыв между бенчмарками и реальным инжинирингом |
| [L02](../../docs/lectures/lecture-02-what-a-harness-actually-is/index.md) | Что на самом деле означает «harness"? | Пять подсистем: Instructions, State, Verification, Scope, Lifecycle |
| [L03](../../docs/lectures/lecture-03-why-the-repository-must-become-the-system-of-record/index.md) | Почему репозиторий должен быть единственным источником истины? | Если агент не может это увидеть — этого не существует |
| [L04](../../docs/lectures/lecture-04-why-one-giant-instruction-file-fails/index.md) | Почему одна гигантская инструкция обречена на провал? | Прогрессивное раскрытие: дать карту, а не энциклопедию |
| [L05](../../docs/lectures/lecture-05-why-long-running-tasks-lose-continuity/index.md) | Почему длительные задачи теряют связность? | Сохранять прогресс на диске; продолжать с того места, где остановились |
| [L06](../../docs/lectures/lecture-06-why-initialization-needs-its-own-phase/index.md) | Почему инициализация требует отдельной фазы? | Проверить работоспособность окружения до того, как агент начнёт работу |
| [L07](../../docs/lectures/lecture-07-why-agents-overreach-and-under-finish/index.md) | Почему агенты выходят за рамки и не доделывают? | Одна фича за раз; явное определение «готово" |
| [L08](../../docs/lectures/lecture-08-why-feature-lists-are-harness-primitives/index.md) | Почему feature-списки — это примитивы harness? | Машинно-читаемые границы scope, которые агент не может проигнорировать |
| [L09](../../docs/lectures/lecture-09-why-agents-declare-victory-too-early/index.md) | Почему агенты объявляют успех слишком рано? | Пробелы в верификации: доверие ≠ корректность |
| [L10](../../docs/lectures/lecture-10-why-end-to-end-testing-changes-results/index.md) | Почему end-to-end-тестирование меняет результаты? | Только полный прогон pipeline считается настоящей верификацией |
| [L11](../../docs/lectures/lecture-11-why-observability-belongs-inside-the-harness/index.md) | Почему observability должна быть внутри harness? | Если вы не видите, что сделал агент, вы не сможете починить то, что он сломал |
| [L12](../../docs/lectures/lecture-12-why-every-session-must-leave-a-clean-state/index.md) | Почему каждая сессия должна оставлять чистое состояние? | Успех следующей сессии зависит от уборки в этой |

### Проекты — 6 практических проектов, применяющих методы лекций к одному и тому же Electron-приложению

| Проект | Что вы делаете | Механизм harness |
|---------|----------------|-------------------|
| [P01](../../docs/projects/project-01-baseline-vs-minimal-harness/index.md) | Выполнить одну задачу дважды: только промпт vs. на основе правил | Минимальный harness: AGENTS.md + init.sh + feature_list.json |
| [P02](../../docs/projects/project-02-agent-readable-workspace/index.md) | Реструктурировать репозиторий для чтения агентом | Агентно-читаемое рабочее пространство + постоянные файлы состояния |
| [P03](../../docs/projects/project-03-multi-session-continuity/index.md) | Позволить агенту продолжить с того места, где он остановился | Протокол прогресса + передача сессии + мультисессионная связность |
| [P04](../../docs/projects/project-04-incremental-indexing/index.md) | Не дать агенту сделать слишком много или слишком мало | Runtime-обратная связь + контроль scope + инкрементальное индексирование |
| [P05](../../docs/projects/project-05-grounded-qa-verification/index.md) | Заставить агента верифицировать собственную работу | Самоверификация + обоснованный Q&A + завершение на основе свидетельств |
| [P06](../../docs/projects/project-06-runtime-observability-and-debugging/index.md) | Построить полный harness с нуля (итоговый проект) | Полный harness: все механизмы + observability + абляционное исследование |

```text
    PROJECT EVOLUTION
    =================

    P01  Prompt-only vs. rules-first       You see the problem
     |
     v
    P02  Agent-readable workspace           You restructure the repo
     |
     v
    P03  Multi-session continuity           You connect sessions
     |
     v
    P04  Runtime feedback & scope           You add feedback loops
     |
     v
    P05  Self-verification                  You make the agent check itself
     |
     v
    P06  Complete harness (capstone)        You build the full system

    Each project's solution becomes the next project's starter.
    The app evolves. Your harness skills grow with it.
```

### Библиотека шаблонов

- [English](https://walkinglabs.github.io/learn-harness-engineering/en/resources/) — templates, checklists, and method references
- [简体中文](https://walkinglabs.github.io/learn-harness-engineering/zh/resources/) — 中文模板、清单和方法参考
- [繁體中文](https://walkinglabs.github.io/learn-harness-engineering/zh-TW/resources/) — 繁體中文範本、清單和方法參考
- [日本語](https://walkinglabs.github.io/learn-harness-engineering/ja/resources/) — テンプレート、チェックリスト、方法リファレンス
- [한국어](https://walkinglabs.github.io/learn-harness-engineering/ko/resources/) — 템플릿, 체크리스트, 방법 참고 자료
- [Español](https://walkinglabs.github.io/learn-harness-engineering/es/resources/) — plantillas, listas de verificación y referencias
- [Français](https://walkinglabs.github.io/learn-harness-engineering/fr/resources/) — modèles, listes de contrôle et références
- [Русский](https://walkinglabs.github.io/learn-harness-engineering/ru/resources/) — шаблоны, чек-листы и справочники
- [Deutsch](https://walkinglabs.github.io/learn-harness-engineering/de/resources/) — Vorlagen, Checklisten und Referenzen
- [العربية](https://walkinglabs.github.io/learn-harness-engineering/ar/resources/) — قوالب، قوائم تحقق ومراجع
- [Tiếng Việt](https://walkinglabs.github.io/learn-harness-engineering/vi/resources/) — mẫu, danh sách kiểm tra và tài liệu tham khảo
- [Oʻzbekcha](https://walkinglabs.github.io/learn-harness-engineering/uz/resources/) — andozalar, tekshiruv roʻyxatlari va maʼlumotnomalar

---

## Жизненный цикл агентской сессии

Одна из ключевых идей этого курса: **сессия агента должна следовать структурированному жизненному циклу, а не быть свободным плаванием.** Вот как это выглядит:

```text
    AGENT SESSION LIFECYCLE
    ======================

    ┌──────────────────────────────────────────────────────────────────┐
    │  START                                                          │
    │                                                                  │
    │  1. Agent reads AGENTS.md / CLAUDE.md                           │
    │  2. Agent runs init.sh (install, verify, health check)          │
    │  3. Agent reads claude-progress.md (what happened last time)    │
    │  4. Agent reads feature_list.json (what's done, what's next)    │
    │  5. Agent checks git log (recent changes)                       │
    │                                                                  │
    │  SELECT                                                          │
    │                                                                  │
    │  6. Agent picks exactly ONE unfinished feature                   │
    │  7. Agent works only on that feature                             │
    │                                                                  │
    │  EXECUTE                                                         │
    │                                                                  │
    │  8. Agent implements the feature                                 │
    │  9. Agent runs verification (tests, lint, type-check)           │
    │  10. If verification fails: fix and re-run                      │
    │  11. If verification passes: record evidence                    │
    │                                                                  │
    │  WRAP UP                                                         │
    │                                                                  │
    │  12. Agent updates claude-progress.md                           │
    │  13. Agent updates feature_list.json                            │
    │  14. Agent records what's still broken or unverified            │
    │  15. Agent commits (only when safe to resume)                   │
    │  16. Agent leaves clean restart path for next session           │
    │                                                                  │
    └──────────────────────────────────────────────────────────────────┘

    The harness governs every transition in this lifecycle.
    The model decides what code to write at each step.
    Without the harness, step 9 becomes "agent says it looks fine."
    With the harness, step 9 is "tests pass, lint is clean, types check."
```

---

## Для кого этот курс

Этот курс предназначен для:

- Разработчиков, уже использующих coding-агентов и желающих большей стабильности и качества
- Исследователей и разработчиков, стремящихся получить систематическое понимание дизайна harness
- Технических лидеров, желающих понять, как дизайн окружения влияет на производительность агентов

Этот курс НЕ предназначен для:

- Тех, кто ищет введение в KI без программирования
- Тех, кому интересны только промпты без планов реальной реализации
- Обучающихся, не готовых доверить агентам работу в реальных репозиториях

---

## Необходимые инструменты

Это курс, в котором вы реально запускаете coding-агентов.

Вам понадобится как минимум один из следующих инструментов:

- Claude Code
- Codex
- Другой IDE- или CLI-coding-агент с поддержкой редактирования файлов, выполнения команд и многошаговых задач

Курс предполагает, что вы умеете:

- Открыть локальный репозиторий
- Разрешить агенту редактировать файлы
- Разрешить агенту выполнять команды
- Проверять вывод и перезапускать задачи

Если у вас нет такого инструмента, вы сможете читать материалы курса, но не сможете выполнить проекты так, как задумано.

---

## Локальный предпросмотр

Этот репозиторий использует VitePress в качестве системы документации.

```sh
npm install
npm run docs:dev        # Dev-сервер с горячей перезагрузкой
npm run docs:build      # Продакшен-сборка
npm run docs:preview    # Предпросмотр собранного сайта
```

Затем откройте локальный URL, который выведет VitePress, в вашем браузере.

---

## Предварительные знания

Обязательные:

- Знакомство с терминалом, Git и локальными средами разработки
- Умение читать и писать код хотя бы на одном распространённом стеке
- Базовый опыт отладки ПО (чтение логов, тестов и анализ runtime-поведения)
- Достаточно времени для выполнения практических заданий курса

Полезные, но не обязательные:

- Опыт работы с Electron, десктопными приложениями или local-first-инструментами
- Основы в области тестирования, логирования или программной архитектуры
- Предыдущий опыт работы с Codex, Claude Code или аналогичными coding-агентами

---

## Основные источники

Первичные:

- [OpenAI: Harness engineering: leveraging Codex in an agent-first world](https://openai.com/index/harness-engineering/)
- [Anthropic: Effective harnesses for long-running agents](https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents)
- [Anthropic: Harness design for long-running application development](https://www.anthropic.com/engineering/harness-design-long-running-apps)
- [OpenAI: Unrolling the Codex agent loop](https://openai.com/index/unrolling-the-codex-agent-loop/)
- [Anthropic: Demystifying evals for AI agents](https://www.anthropic.com/engineering/demystifying-evals-for-ai-agents)
- [LangChain: Improving Deep Agents with harness engineering](https://www.langchain.com/blog/improving-deep-agents-with-harness-engineering)
- [Thoughtworks / Martin Fowler: Harness engineering for coding agent users](https://martinfowler.com/articles/harness-engineering.html)
- [Cursor: Continually improving our agent harness](https://cursor.com/blog/continually-improving-agent-harness)

Полный многоуровневый список ссылок доступен в [`docs/en/resources/reference/`](../../docs/en/resources/reference/index.md).

---

## Структура репозитория

```text
learn-harness-engineering/
├── docs/                          # Сайт документации на VitePress
│   ├── lectures/                  # 12 лекций (index.md + примеры в code/)
│   │   ├── lecture-01-*/
│   │   ├── lecture-02-*/
│   │   └── ... (всего 12)
│   ├── projects/                  # 6 описаний проектов
│   │   ├── project-01-*/
│   │   └── ... (всего 6)
│   └── resources/                 # Многоязычные шаблоны и справочники
│       ├── en/                    # Английские шаблоны, чек-листы, руководства
│       ├── zh/                    # Китайские шаблоны, чек-листы, руководства
│       ├── ru/                    # Русские шаблоны, чек-листы, руководства
│       └── vi/                    # Вьетнамские шаблоны, чек-листы, руководства
├── projects/
│   ├── shared/                    # Общая база Electron + TypeScript + React
│   └── project-NN/               # Директории starter/ и solution/ для каждого проекта
├── skills/                        # Переиспользуемые skills для KI-агентов
│   └── harness-creator/           # Skill для Harness Engineering
├── package.json                   # VitePress + инструменты разработки
└── CLAUDE.md                      # Инструкции Claude Code для этого репозитория
```

---

## Организация курса

- Каждая лекция сфокусирована на одном вопросе
- Курс включает 6 проектов
- Каждый проект требует, чтобы агент выполнял реальную работу
- Каждый проект сравнивает результаты слабого и сильного harness
- Важен измеримый результат, а не количество написанных документов

---

## Skills

Этот репозиторий также содержит переиспользуемые skills для KI-агентов, которые можно установить прямо в вашу IDE или агентское рабочее пространство.

- [**harness-creator**](../../skills/harness-creator/): Skill, помогающий за считанные минуты создать готовое к продакшену harness для вашего собственного проекта.

---

## Другие курсы

Наша команда также создала другие курсы! Ознакомьтесь с ними:

[![Hands-on Modern RL](https://img.shields.io/badge/HANDS--ON_MODERN_RL-0052cc?style=for-the-badge)](https://github.com/walkinglabs/hands-on-modern-rl)

**Hands-on Modern RL**: Открытое практическое учебное пособие, преодолевающее разрыв между базовыми концепциями обучения с подкреплением и LLM-выравниванием, RLVR и продвинутыми агентскими системами.

---

## История звёзд

[![Star History Chart](https://api.star-history.com/svg?repos=walkinglabs/learn-harness-engineering&type=date&legend=top-left)](https://www.star-history.com/#walkinglabs/learn-harness-engineering&type=date&legend=top-left)

---

## Благодарности

Этот курс вдохновлён и содержит идеи из [learn-claude-code](https://github.com/shareAI-lab/learn-claude-code) — прогрессивного руководства по созданию агента с нуля, от единственного цикла до изолированного автономного выполнения.
