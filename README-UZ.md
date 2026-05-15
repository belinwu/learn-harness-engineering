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

> **Muhitlar, holat boshqaruvi, tekshiruv va nazorat mexanizmlarini qurishga bagʻishlangan, KI kod yozuvchi agentlarini ishonchli qiladigan loyihaga asoslangan kurs.**

Learn Harness Engineering — KI kod yozuvchi agentlarini ishlab chiqishga bagʻishlangan kurs. Biz sanoatdagi Harness Engineering sohasining eng ilgʻor nazariya va amaliyotlarini chuqur oʻrganib, sintez qildik. Asosiy manbalarimiz:

- [OpenAI: Harness engineering: leveraging Codex in an agent-first world](https://openai.com/index/harness-engineering/)
- [Anthropic: Effective harnesses for long-running agents](https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents)
- [Anthropic: Harness design for long-running application development](https://www.anthropic.com/engineering/harness-design-long-running-apps)
- [Awesome Harness Engineering](https://github.com/walkinglabs/awesome-harness-engineering)

> **Tezkor boshlash?** [`skills/harness-creator/`](../../skills/) skillʼi sizga oʻz loyihangiz uchun daqiqalar ichida ishlab chiqarish darajasidagi harness (AGENTS.md, funksiya roʻyxatlari, init.sh, tekshiruv oqimlari) yaratishga yordam beradi.

---

## Mundarija

- [Vizual oldindan koʻrish](#vizual-oldindan-ko%C5%A1ish)
- [Harness Engineering nima degani](#harness-engineering-nima-degani)
- [Tezkor boshlash: Agentingizni bugunoq yaxshilang](#tezkor-boshlash-agentingizni-bugunoq-yaxshilang)
- [Yakuniy loyiha: Haqiqiy ilova](#yakuniy-loyiha-haqiqiy-ilova)
- [Oʻqish yoʻli](#o%C5%9Eqish-yo%C5%A7li)
- [Oʻquv dasturi](#o%C5%9Equv-dasturi)
- [Skillʼlar](#skilllar)
- [Boshqa kurslar](#boshqa-kurslar)

---

## Vizual oldindan koʻrish

### Kurs bosh sahifasi
> Kursning toʻliq umumiy koʻrinishi va aniq boshlash yoʻlini taʼminlovchi asosiy falsafalarga kirish.

![Kurs bosh sahifasining oldindan koʻrinishi](../../docs/public/screenshots/readme/zh-home.png)

### Choʻmilishli maʼruzalar
> Haqiqiy muammolar va amaliy loyihalar (masalan, 01-loyiha) boʻyicha chuqur tahlillar, choʻmilishli oʻqish tajribasi uchun.

![Kurs maʼruzasi oldindan koʻrinishi](../../docs/public/screenshots/readme/zh-lecture-01.png)

### Andozalar kutubxonasi
> Koʻp burqli KI agentlarini ishlab chiqishda uchraydigan umumiy muammolarni, masalan kontekst yoʻqotilishi va muddatidan oldin vazifani tugatishni hal qilish uchun moʻljallangan andozalar va moslashtirilgan konfiguratsiyalar.

![Andozalar kutubxonasi oldindan koʻrinishi](../../docs/public/screenshots/readme/zh-resources.png)

## PDF kurs kitoblari

Repozitoriyada endi kurs materiallari uchun PDF yaratish pipelineʼi mavjud.

- Ingliz va xitoy PDFʼlarini mahalliy tarzda yaratish uchun `npm run pdf:build` buyrugʻini bajaring.
- Natija fayllari `artifacts/pdfs/` papkasiga yoziladi.
- README oldindan koʻrish rasmlarini yangilash uchun `npm run screenshots:readme` buyrugʻini bajaring.
- [`release-course-pdfs.yml`](../../.github/workflows/release-course-pdfs.yml) GitHub Actions workflowʼi PDFʼlarni yaratib, GitHub Releasesʼga chiqarishi mumkin.

---

## Model aqlli, harness uni ishonchli qiladi

Aksariyat odamlar ogʻir yoʻl bilan oʻrganadigan bitta qatʼiy haqiqat bor: **Dunyodagi eng kuchli model haqiqiy muhandislik vazifalarida, agar siz unga mos muhit yaratmasangiz, baribir muvaffaqiyatsiz boʻladi.**

Siz buni ehtimol oʻzingiz ham boshdan kechirgansiz. Claude yoki GPTʼga oʻz repozitoriyoringizda vazifa bersangiz. U yaxshi boshlanadi — fayllarni oʻqiydi, kod yozadi, samarali koʻrinadi. Keyin nimadir notoʻgʻri ketadi. Bir qadamni oʻtkazib yuboradi. Testni buzadi. "Tayyor" deydi, lekin hech narsa haqiqatan ishlamaydi. Oʻzingiz qilgandan koʻra koʻproq vaqtni tuzatishga sarflaysiz.

Bu model muammosi emas. Bu harness muammosi.

Dalillar aniq. Anthropic nazorat qilingan tajriba oʻtkazdi: bir xil model (Opus 4.5), bir xil soʻrov ("2D retro oʻyin muharriri yarating"). Harnessʼsiz u 20 daqiqada 9 $ sarfladi va ishlamaydigan narsa yaratdi. Toʻliq harness bilan (rejalashtiruvchi + generator + baholovchi) u 6 soatda 200 $ sarfladi va haqiqatan oʻynash mumkin boʻlgan oʻyin yaratdi. Model oʻzgarmadi. Harness oʻzgardi.

OpenAI Codex bilan xuddi shu haqida xabar berdi: yaxshi harnesslangan repozitoriyada bir xil model "ishonchsiz"dan "ishonchli"ga oʻtadi. Bu marginal yaxshilanish emas — sifat sakrashi.

**Ushbu kurs sizga shu muhitni qanday qurishni oʻrgatadi.**

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

## Harness Engineering nima degani

Harness Engineering — model atrofida toʻliq ish muhiti qurishdir, shunda u ishonchli natijalar beradi. Bu yaxshi promptʼlar yozish haqida emas. Bu model ishlaydigan tizimni loyihalash haqida.

Harnessʼning beshta quyi tizimi bor:

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

Har bir quyi tizimning oʻz vazifasi bor:

- **Koʻrsatmalar (Instructions)** — Agentga nima qilish kerak, qanday tartibda va boshlashdan oldin nima oʻqish kerakligini aytish. Bu bitta ulkan fayl emas; agent ehtiyojiga qarab navigatsiya qiladigan progressiv ochilish strukturasi.
- **Holat (State)** — Nima qilingan, nima bajarilayotgan va keyin nima turib qolganini kuzatish. Diskda saqlanadi, shunda keyingi sessiya aynan oldingi toʻxtagan joydan davom etadi.
- **Tekshiruv (Verification)** — Faqat mavjud test toʻplami dalil sifatida hisoblanadi. Agent bajariluvchi dalilsiz muvaffaqiyat haqida xabar bera olmaydi.
- **Doira (Scope)** — Agentni bir vaqtning oʻzida faqat bitta funksiyaga cheklash. Haddan oshmaslik. Uchta narsani yarim-yorti tugatmaslik. Tugallanmagan ishni yashirish uchun funksiya roʻyxatini qayta yozmaslik.
- **Sessiya hayot sikli (Session Lifecycle)** — Boshida ishga tushirish. Oxirida tozalash. Keyingi sessiya uchun toza qayta boshlash yoʻlini qoldirish.

---

## Bu kurs nega mavjud

Savol "Model lar kod yozoladimi?" emas. Yozoladi. Haqiqiy savol: **Ular haqiqiy repozitoriyalarda, bir nechta sessiyalar davomida, doimiy inson nazoratisiz haqiqiy muhandislik vazifalarini ishonchli bajara oladimi?**

Hozircha javob: harnessʼsiz — yoʻq.

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

Bu kursni qiziqtiradigan haqiqiy savollar:

- Qanday harness dizaynlari vazifani bajash koʻrsatkichlarini yaxshilaydi?
- Qanday dizaynlar qayta ish va notoʻgʻri tugashlarni kamaytiradi?
- Qanday mexanizmlar uzoq davom etuvchi vazifalarni barqaror oldinga surib turadi?
- Qanday strukturalar tizimni bir nechta agent ishga tushirgandan keyin ham saqlab turiladigan qiladi?

---

## Kurs oʻquv dasturi va hujjatlari

Toʻliq kurs materiallarini **[hujjatlar saytida](https://walkinglabs.github.io/learn-harness-engineering/)** topishingiz mumkin.

Oʻquv dasturi uch qismdan iborat:

1. **Maʼruzalar**: Harness Engineering ortidagi nazariyani tushuntiruvchi 12 konseptual blok.
2. **Loyihalar**: Agent asosidagi ish muhitini noldan quradigan 6 ta amaliy loyiha.
3. **Andozalar kutubxonasi**: Bugunoq oʻz repozitoriyalaringizda ishlatish uchun nusxalashga tayyor andozalar (`AGENTS.md`, `feature_list.json`, `init.sh` va h.k.).

---

## Tezkor boshlash: Agentingizni bugunoq yaxshilang

Foyda olish uchun 12 ta maʼruzani ham oʻqish shart emas. Agar siz allaqachon haqiqiy loyihada kod yozuvchi agentdan foydalansangiz, uni hoziryoq yaxshilashingiz mumkin.

Gʻoya oddiy: faqat promptʼlar yozish oʻrniga, agentingizga nima qilish kerak, nima allaqachon qilingan va ish qanday tekshirilishini belgilovchi strukturaviy fayllar toʻplamini bering. Bu fayllar repozitoriyangizda joylashgan, shunda har bir sessiya bir xil holatdan boshlanadi.

```text
    YOUR PROJECT ROOT
    ├── AGENTS.md              <-- agentning ish qoʻllanmasi
    ├── CLAUDE.md              <-- (Claude Code ishlatganingizda alternativa)
    ├── init.sh                <-- install + verify + start ni bajaradi
    ├── feature_list.json      <-- qanday funksiyalar mavjud, qaysilari tugallangan
    ├── claude-progress.md     <-- har bir sessiyada nima boʻlgani
    └── src/                   <-- sizning haqiqiy kodingiz
```

Boshlangʻich andozalarni [andozalar kutubxonasidan](https://walkinglabs.github.io/learn-harness-engineering/en/resources/) yuklab oling va loyihangizga qoʻshing. Shu. Toʻrtta fayl, va agent sessiyalaringiz allaqachon faqat promptʼlarga qaraganda ancha barqaror boʻladi.

---

## Yakuniy loyiha: Haqiqiy ilova

Oltita kurs loyihasi bir xil mahsulot atrofida qurilgan: **Electron asosidagi shaxsiy bilim bazasi uchun desktop ilova**.

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

Bu loyiha shuning uchun tanlanganki, u yuqori amaliy foyda, yetarli haqiqiy mahsulot murakkabligi va harness yaxshilanishlarini kuzatish uchun yaxshi stsenariyani oʻzida birlashtiradi.

Har bir kurs loyihasi (boshlangʻich/yechim) ushbu Electron ilovasining mos rivojlanish bosqichidagi toʻliq nusxasidir. P(N+1) boshlangʻichi P(N) yechimidan hosil qilinadi — ilova rivojlanadi, harness koʻnikmalaringiz esa oʻsadi.

---

## Oʻqish yoʻli

Kurs xronologik tartibda bajarish uchun moʻljallangan. Har bir bosqich oldingisiga asoslanadi.

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

Agar parallel oʻqisangiz, har bir bosqich taxminan bir hafta davom etadi. Agar tezroq borishni xohlasangiz, 1–3 bosqichlarni bitta uzun dam olish kunlarida tugatishingiz mumkin.

---

## Oʻquv dasturi

### Maʼruzalar — har biri muhim savolga javob beruvchi 12 ta konseptual blok

*Har bir maʼruza matnini toʻliq oʻqish uchun [hujjatlar sayti](https://walkinglabs.github.io/learn-harness-engineering/)ga murojaat qiling.*

| Sessiya | Savol | Asosiy gʻoya |
|---------|-------|--------------|
| [L01](../../docs/lectures/lecture-01-why-capable-agents-still-fail/index.md) | Kuchli modellar nega haqiqiy vazifalarda muvaffaqiyatsiz boʻladi? | Benchmarkʼlar va haqiqiy muhandislik oʻrtasidagi farq |
| [L02](../../docs/lectures/lecture-02-what-a-harness-actually-is/index.md) | "Harness" nima degani? | Besh quyi tizim: Koʻrsatmalar, Holat, Tekshiruv, Doira, Hayot sikli |
| [L03](../../docs/lectures/lecture-03-why-the-repository-must-become-the-system-of-record/index.md) | Nega repozitoriy yagona haqiqat manbai boʻlishi kerak? | Agar agent koʻrolmasa, u mavjud emas |
| [L04](../../docs/lectures/lecture-04-why-one-giant-instruction-file-fails/index.md) | Nega bitta ulkan koʻrsatma fayli muvaffaqiyatsiz boʻladi? | Progressiv ochilish: xarita berish, ensiklopediya emas |
| [L05](../../docs/lectures/lecture-05-why-long-running-tasks-lose-continuity/index.md) | Nega uzoq davom etuvchi vazifalar uzluksizlikni yoʻqotadi? | Taraqqiyotni diskda saqlash; toʻxtagan joydan davom ettirish |
| [L06](../../docs/lectures/lecture-06-why-initialization-needs-its-own-phase/index.md) | Nega ishga tushirish alohida bosqichga muhtoj? | Agent ishni boshlashdan oldin muhit ishlashini tekshirish |
| [L07](../../docs/lectures/lecture-07-why-agents-overreach-and-under-finish/index.md) | Nega agentlar haddan oshadi va yarim-yorti tugatadi? | Bir vaqtda bitta funksiya; "Tugadi" ning aniq taʼrifi |
| [L08](../../docs/lectures/lecture-08-why-feature-lists-are-harness-primitives/index.md) | Nega funksiya roʻyxatlari harness primitivlari hisoblanadi? | Agent eʼtiborsiz qoldirolmaydigan, mashina oʻqiyoladigan doira chegaralari |
| [L09](../../docs/lectures/lecture-09-why-agents-declare-victory-too-early/index.md) | Nega agentlar juda erta muvaffaqiyat haqida xabar beradi? | Tekshiruv boʻshliqlari: ishonch = toʻgʻrilik emas |
| [L10](../../docs/lectures/lecture-10-why-end-to-end-testing-changes-results/index.md) | Nega uchdan-uchgacha testlash natijalarni oʻzgartiradi? | Faqat toʻliq pipeline ishga tushirish haqiqiy tekshiruv hisoblanadi |
| [L11](../../docs/lectures/lecture-11-why-observability-belongs-inside-the-harness/index.md) | Nega kuzatuvchanlik harness ichida boʻlishi kerak? | Agent nima qilganini koʻrolmasangiz, u buzgan narsani tuzata olmaysiz |
| [L12](../../docs/lectures/lecture-12-why-every-session-must-leave-a-clean-state/index.md) | Nega har bir sessiya toiza holat qoldirishi kerak? | Keyingi sessiyaning muvaffaqiyati shu sessiyaning tozalanishiga bogʻliq |

### Loyihalar — maʼruza usullarini bir xil Electron ilovasiga qoʻllaydigan 6 ta amaliy loyiha

| Loyiha | Nima qilasiz | Harness mexanizmi |
|---------|--------------|-------------------|
| [P01](../../docs/projects/project-01-baseline-vs-minimal-harness/index.md) | Bir xil vazifani ikki marta bajarish: faqat prompt vs. qoidalarga asoslangan | Minimal harness: AGENTS.md + init.sh + feature_list.json |
| [P02](../../docs/projects/project-02-agent-readable-workspace/index.md) | Repoʼni agent oʻqiy oladigan qayta tuzish | Agent oʻqiy oladigan ish muhiti + doimiy holat fayllari |
| [P03](../../docs/projects/project-03-multi-session-continuity/index.md) | Agentni toʻxtagan joyidan davom ettirish | Taraqqiyot jurnali + sessiya uzatish + koʻp sessiyali uzluksizlik |
| [P04](../../docs/projects/project-04-incremental-indexing/index.md) | Agentning koʻp yoki oz ishlashining oldini olish | Runtime fikr-mulohaza + doira nazorati + inkremental indekslash |
| [P05](../../docs/projects/project-05-grounded-qa-verification/index.md) | Agentni oʻz ishini tekshirishga majburlash | Oʻz-oʻzini tekshirish + asoslangan S&S + dalillarga asoslangan tugatish |
| [P06](../../docs/projects/project-06-runtime-observability-and-debugging/index.md) | Toʻliq harnessʼni noldan qurish (yakuniy loyiha) | Toʻliq harness: barcha mexanizmlar + kuzatuvchanlik + ablyatsiya tadqiqoti |

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

### Andozalar kutubxonasi

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

## Agent sessiyasi hayot sikli

Ushbu kursning asosiy gʻoyalaridan biri: **Agent sessiyasi tuzilgan hayot sikliga amal qilishi kerak, emas xohlagancha ishlashiga.** Bu quyidagicha koʻrinadi:

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

## Bu kurs kim uchun?

Bu kurs quyidagilar uchun moʻljallangan:

- Kod yozuvchi agentlardan foydalanayotgan va koʻproq barqarorlik va sifat xohlaydigan dasturchilar
- Harness dizayni boʻyicha tizimli tushunchaga ega boʻlishni xohlaydigan tadqiqotchilar yoki dasturchilar
- Muhit dizayni agent ish faoliyatiga qanday taʼsir qilishini tushunmoqchi boʻlgan texnik yetakchilar

Bu kurs quyidagilar uchun moʻljallanmagan:

- Dasturlashsiz KI kirishini qidirayotganlar
- Faqat promptʼlar bilan qiziqqan va haqiqiy amalga oshirishni rejalashtirmaydiganlar
- Agentlarni haqiqiy repozitoriyalarda ishlashga tayyor boʻlmagan oʻquvchilar

---

## Talablar

Bu siz haqiqatan kod yozuvchi agentlarni ishga tushiradigan kurs.

Kamida quyidagi vositalardan biriga muhtojsiz:

- Claude Code
- Codex
- Fayl tahrirlash, buyruqlarni bajarish va koʻp bosqichli vazifalarni qoʻllab-quvvatlovchi boshqa IDE yoki CLI kod yozuvchi agent

Kurs quyidagilarni talab qiladi:

- Mahalliy repozitoriyni ochish
- Agentga fayllarni tahrirlashga ruxsat berish
- Agentga buyruqlar bajarishga ruxsat berish
- Natijalarni tekshirish va vazifalarni qayta boshlash

Agar sizda bunday vosita boʻlmasa, kurs materiallarini oʻqiy olasiz, lekin loyihalarni rejalashtirilganidek bajara olmaysiz.

---

## Mahalliy oldindan koʻrish

Ushbu repozitoriy hujjatlar koʻrish vositasi sifatida VitePressʼdan foydalanadi.

```sh
npm install
npm run docs:dev        # Hot reload bilan dev-server
npm run docs:build      # Ishlab chiqarish buildʼi
npm run docs:preview    # Yaratilgan saytni oldindan koʻrish
```

Keyin VitePress koʻrsatadigan mahalliy URLʼni brauzeringizda oching.

---

## Oldindan bilim

Talab qilinadi:

- Terminal, Git va mahalliy rivojlanish muhitlari bilan tanishlik
- Kamida bitta keng tarqalgan ilova stackʼida kodni oʻqish va yozish qobiliyati
- Asosiy dasturiy xatolarni tuzatish tajribasi (logʼlarni oʻqish, testlar va runtime xatti-harakati)
- Amalga oshirishga yoʻnaltirilgan kurs ishi uchun yetarli vaqt

Yordam beradi, lekin majburiy emas:

- Electron, desktop ilovalar yoki local-first vositalar bilan tajriba
- Testlash, logʼlash yoki dasturiy taʼminot arxitekturasi sohasida tajriba
- Codex, Claude Code yoki shunga oʻxshash kod yozuvchi agentlar bilan oldingi tajriba

---

## Asosiy manbalar

Birlamchi:

- [OpenAI: Harness engineering: leveraging Codex in an agent-first world](https://openai.com/index/harness-engineering/)
- [Anthropic: Effective harnesses for long-running agents](https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents)
- [Anthropic: Harness design for long-running application development](https://www.anthropic.com/engineering/harness-design-long-running-apps)
- [OpenAI: Unrolling the Codex agent loop](https://openai.com/index/unrolling-the-codex-agent-loop/)
- [Anthropic: Demystifying evals for AI agents](https://www.anthropic.com/engineering/demystifying-evals-for-ai-agents)
- [LangChain: Improving Deep Agents with harness engineering](https://www.langchain.com/blog/improving-deep-agents-with-harness-engineering)
- [Thoughtworks / Martin Fowler: Harness engineering for coding agent users](https://martinfowler.com/articles/harness-engineering.html)
- [Cursor: Continually improving our agent harness](https://cursor.com/blog/continually-improving-agent-harness)

Toʻliq qatlamli manbalar roʻyxatini [`docs/en/resources/reference/`](../../docs/en/resources/reference/index.md) da topishingiz mumkin.

---

## Repozitoriy strukturasi

```text
learn-harness-engineering/
├── docs/                          # VitePress hujjatlar sayti
│   ├── lectures/                  # 12 ta maʼruza (index.md + code/ misollar)
│   │   ├── lecture-01-*/
│   │   ├── lecture-02-*/
│   │   └── ... (jami 12 ta)
│   ├── projects/                  # 6 ta loyiha tavsifi
│   │   ├── project-01-*/
│   │   └── ... (jami 6 ta)
│   └── resources/                 # Koʻp tilli andozalar va maʼlumotnomalar
│       ├── en/                    # Ingliz andozalari, tekshiruv roʻyxatlari, qoʻllanmalar
│       ├── zh/                    # Xitoy andozalari, tekshiruv roʻyxatlari, qoʻllanmalar
│       ├── ru/                    # Rus andozalari, tekshiruv roʻyxatlari, qoʻllanmalar
│       └── vi/                    # Vetnam andozalari, tekshiruv roʻyxatlari, qoʻllanmalar
├── projects/
│   ├── shared/                    # Umumiy Electron + TypeScript + React asos
│   └── project-NN/               # Loyihaga oid starter/ va solution/ papkalari
├── skills/                        # Qayta ishlatiladigan KI agent skillʼlari
│   └── harness-creator/           # Harness Engineering skillʼi
├── package.json                   # VitePress + dev vositalari
└── CLAUDE.md                      # Ushbu repo uchun Claude Code koʻrsatmalari
```

---

## Kurs qanday tuzilgan

- Har bir maʼruza bitta savolga qaratilgan
- Kurs 6 ta loyihani oʻz ichiga oladi
- Har bir loyiha agentdan haqiqiy ish bajarishni talab qiladi
- Har bir loyiha kuchsiz vs. kuchli harness natijalarini solishtiradi
- Muhim boʻlgan narsa — oʻlchangan farq, nechta hujjat yozilgani emas

---

## Skillʼlar

Ushbu repozitoriy, shuningdek, toʻgʻridan-toʻgʻri IDE yoki agent ish muhitiga oʻrnatishingiz mumkin boʻlgan qayta ishlatiladigan KI agent skillʼlarini oʻz ichiga oladi.

- [**harness-creator**](../../skills/harness-creator/): Oʻz loyihangiz uchun daqiqalar ichida ishlab chiqarish darajasidagi harness yaratishga yordam beradigan skill.

---

## Boshqa kurslar

Bizning jamoamiz yana boshqa kurslar ham yaratdi! Ularni koʻrib chiqing:

[![Hands-on Modern RL](https://img.shields.io/badge/HANDS--ON_MODERN_RL-0052cc?style=for-the-badge)](https://github.com/walkinglabs/hands-on-modern-rl)

**Hands-on Modern RL**: Asosiy RL konsepsiyalaridan LLM alignment, RLVR va ilgʻor agent tizimlarigacha boʻlgan masofani bridjlash uchun ochiq manbali amaliy oʻquv dasturi.

---

## Yulduzlar tarixi

[![Star History Chart](https://api.star-history.com/svg?repos=walkinglabs/learn-harness-engineering&type=date&legend=top-left)](https://www.star-history.com/#walkinglabs/learn-harness-engineering&type=date&legend=top-left)

---

## Minnatdorchilik

Ushbu kurs [learn-claude-code](https://github.com/shareAI-lab/learn-claude-code) dan ilhomlangan va undan gʻoyalar olgan — agentni bitta sikldan izolyatsiya qilingan avtonom bajarishgacha noldan qurish boʻyicha progressiv qoʻllanma.
