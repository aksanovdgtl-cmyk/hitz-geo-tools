# HITZ GEO Tools

**Бесплатные GEO-инструменты HITZ** · [English](#english) · [Русский](#русский)

[![License: MIT](https://img.shields.io/badge/license-MIT-22f360.svg)](LICENSE) [![Live tools](https://img.shields.io/badge/live-hitz.agency%2Fen%2Ftools-232323.svg)](https://hitz.agency/en/tools)

## English

Free, open-source tools for GEO (generative engine optimization): checking whether a website can be read, understood and cited by ChatGPT, Gemini, Perplexity, Claude, Google AI Overviews and Yandex Alice. Every tool runs online at [hitz.agency/en/tools](https://hitz.agency/en/tools) and has its own repository with the same code, tests and a one-command deploy to Cloudflare Workers.

### Tools

| Tool | What it does | Live | Source |
|---|---|---|---|
| AI Crawler Access Checker | Reads robots.txt and shows access for 9 AI crawlers (GPTBot, OAI-SearchBot, ClaudeBot, PerplexityBot, Google-Extended and others), split by AI search, user fetch and training | [open](https://hitz.agency/en/tools/ai-crawler-check) | [ai-crawler-check](https://github.com/aksanovdgtl-cmyk/ai-crawler-check) |
| llms.txt Checker and Generator | Scores a site's llms.txt from 0 to 100 and builds a new file from four fields | [open](https://hitz.agency/en/tools/llms-txt) | [llms-txt-generator](https://github.com/aksanovdgtl-cmyk/llms-txt-generator) |
| GEO Page Audit | Scores a page 0-100 for AI answer readiness: answer, entity, trust and technical signals | [open](https://hitz.agency/en/tools/geo-audit) | [geo-audit](https://github.com/aksanovdgtl-cmyk/geo-audit) |
| Schema / JSON-LD Checker | Finds and parses JSON-LD blocks, lists Schema.org types, flags syntax errors and relative URLs | [open](https://hitz.agency/en/tools/schema-check) | [jsonld-schema-check](https://github.com/aksanovdgtl-cmyk/jsonld-schema-check) |
| Brand Entity Check | 18 entity signals of the home page (name, Organization, `sameAs`, contacts) plus a Wikidata lookup | [open](https://hitz.agency/en/tools/brand-entity) | [brand-entity-check](https://github.com/aksanovdgtl-cmyk/brand-entity-check) |
| Prompt Map Generator | 30-90 prompts customers ask AI assistants about a business, by intent, with CSV export | [open](https://hitz.agency/en/tools/prompt-map) | [geo-prompt-map](https://github.com/aksanovdgtl-cmyk/geo-prompt-map) |

### A quick GEO check in six steps

1. **Can AI systems reach the site?** Run the [AI crawler check](https://hitz.agency/en/tools/ai-crawler-check): search crawlers such as OAI-SearchBot, Claude-SearchBot and PerplexityBot should not be blocked if you want to be cited.
2. **Is there a short map of the site for language models?** Check or create [llms.txt](https://hitz.agency/en/tools/llms-txt).
3. **Can a key page be quoted?** Run the [GEO page audit](https://hitz.agency/en/tools/geo-audit) on a service or article page: a direct answer after the H1, question headings, lists, author, date and sources.
4. **Is the structured data valid?** Check the same page with the [Schema / JSON-LD checker](https://hitz.agency/en/tools/schema-check).
5. **Is the brand one clear entity?** Run the [brand entity check](https://hitz.agency/en/tools/brand-entity): the same name, domain, Organization markup and `sameAs` profiles everywhere.
6. **What do customers ask?** Build a [prompt map](https://hitz.agency/en/tools/prompt-map) and run it in each AI system regularly to measure mentions and citations.

### How the tools work

The pages are plain HTML, CSS and JavaScript. Checks that need to fetch a site run in a Cloudflare Worker written in TypeScript: it streams HTML through HTMLRewriter with byte limits, fetches public websites only (DNS over HTTPS check before every request and redirect), rate-limits requests and returns JSON. Each repository has unit tests and API tests that run the Worker in Miniflare with fixtures instead of real network.

### Official documentation

- AI crawlers: [OpenAI](https://platform.openai.com/docs/bots), [Anthropic](https://support.claude.com/en/articles/8896518-does-anthropic-crawl-data-from-the-web-and-how-can-site-owners-block-the-crawler), [Perplexity](https://docs.perplexity.ai/guides/bots), [Google common crawlers and Google-Extended](https://developers.google.com/search/docs/crawling-indexing/google-common-crawlers)
- robots.txt: [RFC 9309](https://www.rfc-editor.org/rfc/rfc9309)
- llms.txt: [llmstxt.org](https://llmstxt.org/)
- Structured data: [schema.org](https://schema.org/docs/gs.html), [JSON-LD](https://json-ld.org/), [Google: introduction to structured data](https://developers.google.com/search/docs/appearance/structured-data/intro-structured-data)

### How to cite

Use **Cite this repository** ([CITATION.cff](CITATION.cff)) or:

> HITZ. GEO Tools. https://hitz.agency/en/tools

### About HITZ

[HITZ](https://hitz.agency/en) is a GEO agency based in Almaty and Tashkent. We help brands get mentioned and cited in AI answers. Guides on GEO, AEO and AI search (in Russian): [hitz.agency/blog](https://hitz.agency/blog).

---

## Русский

Бесплатные инструменты с открытым кодом для GEO (generative engine optimization): проверяют, может ли сайт быть прочитан, понят и процитирован ChatGPT, Алисой, Gemini, Perplexity, Claude и Google AI Overviews. Каждый инструмент работает онлайн на [hitz.agency/tools](https://hitz.agency/tools), у каждого свой репозиторий с тем же кодом, тестами и публикацией в Cloudflare Workers одной командой.

### Инструменты

| Инструмент | Что делает | Онлайн | Код |
|---|---|---|---|
| Проверка доступа AI-краулеров | Читает robots.txt и показывает доступ для 9 AI-ботов (GPTBot, OAI-SearchBot, ClaudeBot, PerplexityBot, Google-Extended и других) по задачам: AI-поиск, запрос пользователя, обучение | [открыть](https://hitz.agency/tools/ai-crawler-check) | [ai-crawler-check](https://github.com/aksanovdgtl-cmyk/ai-crawler-check) |
| Проверка и генератор llms.txt | Оценивает llms.txt сайта от 0 до 100 и собирает новый файл из четырех полей | [открыть](https://hitz.agency/tools/llms-txt) | [llms-txt-generator](https://github.com/aksanovdgtl-cmyk/llms-txt-generator) |
| GEO-аудит страницы | Балл 0-100 готовности страницы к AI-ответам: ответ, сущность, доверие, техника | [открыть](https://hitz.agency/tools/geo-audit) | [geo-audit](https://github.com/aksanovdgtl-cmyk/geo-audit) |
| Проверка Schema / JSON-LD | Находит и разбирает блоки JSON-LD, перечисляет типы Schema.org, отмечает ошибки синтаксиса и относительные адреса | [открыть](https://hitz.agency/tools/schema-check) | [jsonld-schema-check](https://github.com/aksanovdgtl-cmyk/jsonld-schema-check) |
| Проверка сущности бренда | 18 сигналов сущности на главной (название, Organization, `sameAs`, контакты) и поиск в Wikidata | [открыть](https://hitz.agency/tools/brand-entity) | [brand-entity-check](https://github.com/aksanovdgtl-cmyk/brand-entity-check) |
| Генератор карты промтов | 30-90 промтов, которые клиенты задают нейросетям о бизнесе, по интентам, с выгрузкой в CSV | [открыть](https://hitz.agency/tools/prompt-map) | [geo-prompt-map](https://github.com/aksanovdgtl-cmyk/geo-prompt-map) |

### Быстрая GEO-проверка в шесть шагов

1. **Пускает ли сайт нейросети?** [Проверка AI-краулеров](https://hitz.agency/tools/ai-crawler-check): поисковые боты OAI-SearchBot, Claude-SearchBot и PerplexityBot не должны быть закрыты, если вы хотите попадать в ответы со ссылкой.
2. **Есть ли у сайта короткая карта для языковых моделей?** Проверьте или соберите [llms.txt](https://hitz.agency/tools/llms-txt).
3. **Можно ли процитировать главную страницу услуги?** [GEO-аудит](https://hitz.agency/tools/geo-audit): прямой ответ после H1, вопросные подзаголовки, списки, автор, дата и источники.
4. **Корректна ли разметка?** Проверьте ту же страницу в [Schema / JSON-LD](https://hitz.agency/tools/schema-check).
5. **Собран ли бренд в одну сущность?** [Проверка сущности бренда](https://hitz.agency/tools/brand-entity): одинаковые название, домен, разметка Organization и профили в `sameAs`.
6. **О чем спрашивают клиенты?** Соберите [карту промтов](https://hitz.agency/tools/prompt-map) и регулярно прогоняйте ее в нейросетях, чтобы считать упоминания и цитирования.

### Разборы в блоге HITZ

- [Что такое GEO в 2026: гайд по оптимизации под нейросети](https://hitz.agency/blog/chto-takoe-geo-2026)
- [AI-краулеры и robots.txt: каких ботов пускать на сайт](https://hitz.agency/blog/ai-kraulery-robots-txt)
- [llms.txt: что это, зачем нужен и как настроить](https://hitz.agency/blog/chto-takoe-llms-txt)
- [Чанки: как нейросеть режет страницу и что цитирует](https://hitz.agency/blog/chanki-i-izvlekaemyy-otvet)
- [Schema.org для нейросетей: какие типы разметки работают](https://hitz.agency/blog/schema-org-dlya-neyrosetey)
- [Сущность бренда в поиске: sameAs, Wikidata, граф знаний](https://hitz.agency/blog/sushchnost-brenda-sameas)
- [Промпты вместо ключевых слов: как собрать рабочий набор](https://hitz.agency/blog/prompty-vmesto-klyuchey)
- [Как измерить видимость в нейросетях: метрики и инструменты](https://hitz.agency/blog/kak-izmerit-vidimost-v-neyrosetyah)

### Как устроены инструменты

Страницы написаны на обычных HTML, CSS и JavaScript. Проверки, которым нужно загрузить сайт, работают в Cloudflare Worker на TypeScript: HTML читается потоком через HTMLRewriter с лимитами по объему, загружаются только публичные сайты (проверка DNS через DoH перед каждым запросом и перенаправлением), есть лимит запросов, ответ в JSON. В каждом репозитории модульные тесты и тесты API, которые запускают Worker в Miniflare с подставными ответами вместо настоящей сети.

### Как сослаться

Кнопка GitHub **Cite this repository** ([CITATION.cff](CITATION.cff)) или строка:

> HITZ. GEO-инструменты. https://hitz.agency/tools

### О HITZ

[HITZ](https://hitz.agency/) - GEO-агентство из Алматы и Ташкента. Помогаем брендам попадать в ответы нейросетей. Разборы про GEO, AEO и AI-поиск: [hitz.agency/blog](https://hitz.agency/blog).

### Лицензия

[MIT](LICENSE) © 2026 HITZ. Название и логотип HITZ под лицензию MIT не подпадают.
