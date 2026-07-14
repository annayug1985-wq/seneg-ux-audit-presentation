# UX Audit: seneg.ru
**Date:** 2026-07-13
**Auditor:** Codex (UX Audit Skill + Product Design Audit)
**Audit mode:** Evidence audit

## Executive summary

**Overall score:** 4.8/10 - сильный ассортимент и базовое доверие есть, но сайт заметно устарел и создаёт лишнее трение в первом касании.
**Problems found:** 1 critical, 5 major, 2 minor
**Confidence profile:** высокая по структуре страниц и визуальным проблемам; средняя по формам и accessibility, где не выполнялась полная интеракция.

### Top findings
1. Мобильная версия не адаптирована под современный narrow viewport и ломает первый экран.
2. На главной не хватает одного доминирующего CTA и ясной визуальной иерархии.
3. Навигация и первый экран перегружены конкурирующими блоками и маршрутами.
4. Формы первого контакта слишком тяжёлые для холодного лида.
5. Контент и визуальные маркеры свежести создают ощущение заброшенности.

### Strengths
- У сайта есть понятные контактные данные, адрес, карта и несколько телефонных каналов, что поддерживает базовое доверие.
- Карточки товаров содержат технически полезную информацию, сертификаты и применение, что важно для B2B и рационального выбора.

---

## Audit context

**Site:** https://seneg.ru/
**Industry:** средства защиты древесины
**Target audience:** домовладельцы, дилеры, строительные компании, промышленные покупатели
**Main conversion goal:** заявка, звонок, подбор продукта, переход к покупке через консультацию
**Priority device context:** mixed, с критической важностью мобильного первого касания
**Pages audited:** homepage, product detail, contact page, about page
**Representative templates reviewed:** homepage, product detail, contact/conversion, about/trust
**Tools used:** Edge headless screenshots, web extraction, local image inspection

---

## Evidence notes

**Evidence artifact:** `C:\Users\a_elkin\Documents\Codex\2026-07-13\https-seneg-ru\outputs\seneg-audit\evidence.md`
**Visual evidence available:** yes
**Important limitations:**
- Не проводилась полная отправка форм.
- Не тестировалась клавиатурная навигация и screen reader path.
- Точный замер контраста не выполнялся.

---

## Block 1. Nielsen heuristics

### Problem 1.9: Интерфейс главной страницы перегружен и заставляет пользователя разбираться вместо того, чтобы действовать
- **Priority:** MAJOR
- **Confidence:** High
- **Heuristic:** Aesthetic and minimalist design
- **Where:** главная страница, первый экран и ближайший контентный блок
- **Evidence type:** Observed
- **What was observed:** На первом экране одновременно конкурируют телефоны, callback-кнопка, каталог, горизонтальное меню, audience shortcuts, спецпредложения и дальше ещё категории/новости/подписка/поиск.
- **Why it matters:** Пользователь тратит внимание на навигацию, а не на решение задачи. Это снижает конверсию из рекламного и органического трафика.
- **What to do:** Свести первый экран к одной главной задаче: ценностное предложение, 1 основной CTA, 1-2 вторичных маршрута, а остальное увести ниже.
- **Expected effect:** Более понятный старт и выше шанс первого клика в нужный сценарий.
- **Evidence reference:** `01-home-desktop.png`

### Problem 1.6: Формы собирают слишком много информации на раннем этапе
- **Priority:** MAJOR
- **Confidence:** High
- **Heuristic:** Error prevention
- **Where:** форма `Перезвонить Вам?/Запрос информации`
- **Evidence type:** Extracted
- **What was observed:** Для первого обращения запрашиваются телефон, контактное лицо, email, регион/город, текст сообщения, представительство, согласие и др.
- **Why it matters:** Чем выше усилие на старте, тем больше отказов, особенно у новых посетителей с мобильных устройств.
- **What to do:** Для первого шага оставить 2-3 поля: имя, телефон или email, краткий вопрос. Остальные детали собирать после первичного контакта.
- **Expected effect:** Рост числа заявок без ухудшения качества лидов.
- **Evidence reference:** [homepage extract](https://seneg.ru/)

### Items without problems
- `1.5` Базовая консистентность навигации и шаблонов по страницам присутствует.

### Could not verify
- `1.1` Поведение лоадеров и submit feedback без отправки форм не проверялось.
- `1.10` Реальные тексты ошибок форм не проверялись.

---

## Block 2. Conversion

### Problem 2.2: На первом экране нет одного очевидного следующего шага
- **Priority:** MAJOR
- **Confidence:** High
- **Aspect:** CTA
- **Where:** главная страница, hero area
- **Evidence type:** Observed
- **What was observed:** Главный CTA `Перезвонить Вам?` маленький и теряется среди контактов, списков и декоративных изображений.
- **Why it matters:** Когда следующий шаг неочевиден, часть трафика просто скроллит, теряется или уходит.
- **What to do:** Сделать один главный CTA крупнее и смыслово конкретнее: `Подобрать состав`, `Получить консультацию`, `Где купить`.
- **Expected effect:** Больше переходов в коммерчески полезный сценарий.
- **Evidence reference:** `01-home-desktop.png`, `02-home-mobile-narrow.png`

### Problem 2.1: Ценностное предложение есть по смыслу, но не собрано в современный продающий блок
- **Priority:** MAJOR
- **Confidence:** High
- **Aspect:** Value proposition
- **Where:** главная страница
- **Evidence type:** Observed
- **What was observed:** Формулировка про российскую экспертизу в защите древесины есть, но визуально и структурно она уступает множеству вторичных элементов.
- **Why it matters:** Холодный посетитель должен сразу понять, почему выбрать бренд и что делать дальше.
- **What to do:** Собрать hero как единый коммерческий блок: сильный заголовок, 2-3 буллета выгод, доверительный маркер, CTA.
- **Expected effect:** Быстрее считывается ценность и снижается когнитивная нагрузка.
- **Evidence reference:** `01-home-desktop.png`

### Problem 2.12: На карточке товара нет короткого маршрута к покупке или расчёту
- **Priority:** MAJOR
- **Confidence:** High
- **Aspect:** Price transparency / buying path
- **Where:** страница `Сенеж Аквадекор`
- **Evidence type:** Observed
- **What was observed:** Есть техподдержка, сертификаты и длинное описание, но нет явной цены, кнопки запроса цены, поиска дилера или понятного блока `где купить`.
- **Why it matters:** Пользователь получает спецификацию, но не получает следующий коммерческий шаг.
- **What to do:** Добавить рядом с карточкой товара блок `Где купить`, `Узнать цену`, `Подобрать объём`, `Скачать инструкцию`.
- **Expected effect:** Быстрее переход из интереса в заявку.
- **Evidence reference:** `03-product-aquadecor.png`

### Problem 2.10: На длинных страницах CTA не повторяются достаточно системно
- **Priority:** MINOR
- **Confidence:** Medium
- **Aspect:** CTA placement
- **Where:** product detail pages
- **Evidence type:** Observed
- **What was observed:** После длинного технического описания пользователю снова не подсказывают следующий шаг крупным блоком.
- **Why it matters:** Чем длиннее страница, тем важнее напоминать о следующем действии.
- **What to do:** Повторять CTA после ключевых секций и в конце страницы.
- **Expected effect:** Более высокий conversion-through-scroll.
- **Evidence reference:** `03-product-aquadecor.png`

### Items without problems
- `2.6` Альтернативные контакты есть: телефоны, email, адрес.
- `2.9` Контактные данные заметны и поддерживают доверие.

### Could not verify
- `2.11` Реальный thank-you state после отправки формы не проверялся.

---

## Block 3. Content

### Problem 3.9: Контент выглядит устаревшим
- **Priority:** MAJOR
- **Confidence:** High
- **Aspect:** Freshness
- **Where:** homepage footer and news block
- **Evidence type:** Observed
- **What was observed:** На главной видна новость от октября 2018 года, а в футере стоит `(C) 2006-2022`.
- **Why it matters:** Даже сильный бренд теряет доверие, когда сайт выглядит неактуальным. Пользователь начинает сомневаться в поддержке, наличии и живости компании.
- **What to do:** Обновить футер до текущего года, вынести свежие новости/кейсы или убрать блок новостей, если он не поддерживается.
- **Expected effect:** Больше доверия и меньше ощущения “архивного” сайта.
- **Evidence reference:** [homepage extract](https://seneg.ru/)

### Problem 3.6: Тексты трудно быстро сканировать
- **Priority:** MINOR
- **Confidence:** High
- **Aspect:** Readability
- **Where:** product detail and about pages
- **Evidence type:** Observed
- **What was observed:** Мелкий кегль, длинные абзацы, высокая плотность текста и слабая визуальная пауза между смысловыми блоками.
- **Why it matters:** Пользователи не читают такие страницы линейно. Они ищут короткие подтверждения и быстрые ответы.
- **What to do:** Увеличить кегль, межстрочность, сократить абзацы, усилить карточки преимуществ и FAQ-структуру.
- **Expected effect:** Лучше считываются выгоды и технические различия продукта.
- **Evidence reference:** `03-product-aquadecor.png`

### Items without problems
- `3.2` На ключевых страницах есть уникальные H1.
- `3.8` На товарных страницах есть содержательные технические доказательства, а не только декоративный контент.

### Could not verify
- `3.5` Наличие корректных alt-атрибутов для всех изображений не проверялось полноценно.

---

## Block 4. Technical and visual quality

### Problem 4.2: Мобильная версия не выглядит адаптивной
- **Priority:** CRITICAL
- **Confidence:** High
- **Aspect:** Mobile
- **Where:** главная страница на narrow viewport
- **Evidence type:** Observed
- **What was observed:** В мобильном кадре хедер и каталог сохраняют десктопную композицию, часть контента обрезана, правая колонка и блоки читаются тяжело.
- **Why it matters:** Это прямой барьер для мобильного трафика: хуже читаемость, сложнее навигация, выше отказы.
- **What to do:** Пересобрать мобильную и планшетную сетку: одноколоночный hero, компактное меню, перенос каталога в раскрывающиеся блоки, нормальные touch targets.
- **Expected effect:** Снижение bounce rate и рост глубины просмотра/конверсии с мобильных устройств.
- **Evidence reference:** `02-home-mobile-narrow.png`

### Problem 4.10: Визуальная система выглядит морально устаревшей
- **Priority:** MAJOR
- **Confidence:** High
- **Aspect:** Visual quality
- **Where:** homepage and product detail
- **Evidence type:** Observed
- **What was observed:** Градиенты, плашки, разрозненные иконки, смешение декоративных элементов и старые UI-паттерны создают ощущение устаревшего корпоративного сайта.
- **Why it matters:** Пользователи переносят визуальное впечатление на ощущение надёжности продукта и сервиса.
- **What to do:** Обновить UI-систему без потери бренда: типографика, spacing, карточки, CTA, формы, сетка.
- **Expected effect:** Рост доверия и лучшее восприятие качества бренда.
- **Evidence reference:** `01-home-desktop.png`, `03-product-aquadecor.png`

### Items without problems
- `4.1` HTTPS работает.
- `4.5` Изображения и карта в просмотренных страницах отображаются.

### Could not verify
- `4.4` Реальная производительность не измерялась инструментально.
- `4.6` Поведение сайта при отключённом JS не проверялось.

---

## Block 5. Information architecture

### Problem 5.1: Архитектура перегружает пользователя количеством одновременных путей
- **Priority:** MAJOR
- **Confidence:** High
- **Aspect:** Navigation
- **Where:** homepage
- **Evidence type:** Observed
- **What was observed:** Сразу доступны верхнее меню, боковой каталог, тематические блоки, новости, полезные материалы, поиск и аудитории.
- **Why it matters:** Пользователь без знания внутренней структуры бренда не понимает, какой путь для него главный.
- **What to do:** Сформировать 3-5 основных сценариев и выстроить навигацию вокруг них: выбрать продукт, где купить, для профессионалов, документы, контакты.
- **Expected effect:** Меньше растерянности и выше скорость перехода в нужный раздел.
- **Evidence reference:** `01-home-desktop.png`

### Items without problems
- `5.2` До ключевых разделов можно дойти быстро.
- `5.6` В футере есть повтор контактов.

### Could not verify
- `5.8` XML sitemap отдельно не проверялась.

---

## Block 6. Accessibility quick pass

### Problem 6.4: Touch targets и мобильная читаемость выглядят рискованно
- **Priority:** MAJOR
- **Confidence:** High
- **Aspect:** Mobile accessibility
- **Where:** главная страница на mobile
- **Evidence type:** Observed
- **What was observed:** Небольшие ссылки, плотные списки и перегруженный хедер затрудняют касание и чтение.
- **Why it matters:** Это ухудшает доступность для широкой аудитории, включая пользователей с моторными и зрительными ограничениями.
- **What to do:** Увеличить размеры интерактивных зон, интервалы и базовый шрифт на мобильных.
- **Expected effect:** Лучше usability и меньше ошибочных нажатий.
- **Evidence reference:** `02-home-mobile-narrow.png`

### Items without problems
- `6.2` У основных форм есть видимые подписи полей.

### Could not verify
- `6.1` Точный contrast ratio не измерялся.
- `6.3` Focus indicators не проверялись.
- `6.6` Корректность accessible names для всех иконок и controls не проверялась.

---

## Prioritized fix plan

### CRITICAL - act immediately
| # | Problem | Block | Action | Expected impact | Effort |
|---|---|---|---|---|---|
| 1 | Мобильная версия ломает первый экран | 4 | Пересобрать responsive layout главной и ключевых шаблонов | Снижение отказов и рост мобильной конверсии | High |

### MAJOR - next sprint
| # | Problem | Block | Action | Expected impact | Effort |
|---|---|---|---|---|---|
| 2 | Нет одного доминирующего CTA | 2 | Переделать hero и CTA hierarchy | Выше first-click conversion | Medium |
| 3 | Перегруженная IA | 5 | Упростить навигацию и сценарии выбора | Быстрее путь к продукту/контакту | Medium |
| 4 | Тяжёлые формы | 1/2 | Сократить поля первого контакта | Больше заявок | Medium |
| 5 | Устаревшие маркеры свежести | 3 | Обновить футер, новости, кейсы | Выше доверие | Low |
| 6 | Слабый buy path на product pages | 2 | Добавить `где купить/узнать цену/подобрать` | Рост коммерческих переходов | Medium |
| 7 | Touch targets и mobile accessibility | 6 | Увеличить размеры ссылок и интервалов | Лучше мобильный UX | Medium |

### MINOR - backlog
| # | Problem | Block | Action | Expected impact | Effort |
|---|---|---|---|---|---|
| 8 | Плотные тексты и слабая scanability | 3 | Переформатировать тексты и подзаголовки | Быстрее понимание выгод | Medium |
| 9 | CTA не повторяются по длинной странице | 2 | Добавить повторные CTA в середине и конце | Чуть выше conversion-through-scroll | Low |

---

## Recommended sequence

1. Починить mobile layout главной и товарных шаблонов.
2. Пересобрать главную вокруг value proposition и одного основного CTA.
3. Сократить формы и упростить коммерческий путь `подобрать/где купить/узнать цену`.

---

## Methodology

Аудит сочетает визуальную проверку через headless screenshots, ручной просмотр сохранённых изображений и извлечение содержимого страниц. Выводы приоритизированы по влиянию на доверие, навигацию и конверсию. Там, где не было полной интеракции, ограничения помечены явно.
