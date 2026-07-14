# Audit Evidence: seneg.ru

## Run context

- **Date:** 2026-07-13
- **Audit mode:** Evidence audit
- **Analyst:** Codex
- **Tools used:** Edge headless screenshots, web page extraction, local image inspection
- **Business context source:** inferred

## Inferred business context

- **Industry:** wood protection products and industrial wood-treatment materials
- **Target audience:** homeowners, dealers, wood construction companies, industrial buyers
- **Main conversion goal:** inbound contact via callback/request forms, dealer/contact outreach, product selection
- **Priority device context:** mixed, with mobile important for first-touch traffic

## Site map summary

| URL | Page type | Template group | Primary CTA | Forms | Notes |
|---|---|---|---|---|---|
| https://seneg.ru/ | Homepage | Homepage | `Перезвонить Вам?`, product/category exploration | Newsletter field, top request form exposed in extracted DOM | Old-school portal-style homepage with many competing entry points |
| https://seneg.ru/products/catalogue/decor/aquadecor | Product detail | Product page | `Техподдержка`, `Как купить`, certificates | Product support form | Dense technical copy and weak buying path |
| https://seneg.ru/contacts/scheme | Contact page | Contact/conversion | Contact details, map | No visible short contact form on page body | Useful address/map, but mostly informational |
| https://seneg.ru/about/why | About/trust page | Content/about | None prominent | None prominent in page body | Brand-story page with low conversion value |

## Representative pages selected

- https://seneg.ru/ - homepage and first-touch conversion assessment
- https://seneg.ru/products/catalogue/decor/aquadecor - representative product detail page
- https://seneg.ru/contacts/scheme - representative contact/trust page
- https://seneg.ru/about/why - representative brand/about content page

## Page evidence records

### Page: https://seneg.ru/
- **Page type:** homepage
- **Tool used:** Edge headless screenshot + web extraction
- **Evidence confidence:** High
- **Title:** Сенеж защита древесины
- **Meta description:** not captured in web extract
- **H1:** `Сенеж - Российский эксперт в защите древесины`
- **Primary CTA(s):** `Перезвонить Вам?`, `Как подобрать`, `Как купить`
- **Secondary CTA(s):** audience segment links, category links, top navigation
- **Forms present:** request/info form in extracted page content, newsletter email field, site search
- **Form fields observed:** phone, contact person, email, organization, region/city, message, city/office selector, consent checkbox
- **Contact methods found:** phone, email, physical address
- **Trust signals found:** ISO mention, FSC badge, brand award badge, address, phone numbers
- **Navigation items observed:** Главная, Компания, Качество, Продукция, Оборудование, Исследования, Как купить, Успех Марки, Всё о Защите, Контакты
- **Accessibility notes:** mobile screenshot shows overflow/clipping risk; text is small and dense; keyboard/focus not verified
- **Technical notes:** footer shows `(C) 2006-2022`; homepage news card shows event dated `18-21 октября 2018`; reCAPTCHA badge visible; mobile narrow capture shows no responsive reflow
- **Could not verify:** focus styles, true form success/error handling, screen-reader labeling
- **Screenshot paths:** `C:\Users\a_elkin\Documents\Codex\2026-07-13\https-seneg-ru\outputs\seneg-audit\01-home-desktop.png`, `C:\Users\a_elkin\Documents\Codex\2026-07-13\https-seneg-ru\outputs\seneg-audit\02-home-mobile-narrow.png`

### Page: https://seneg.ru/products/catalogue/decor/aquadecor
- **Page type:** product detail
- **Tool used:** Edge headless screenshot + web extraction
- **Evidence confidence:** High
- **Title:** Сенеж Аквадекор - тонирующий антисептик для дерева
- **Meta description:** not captured in web extract
- **H1:** `Сенеж Аквадекор`
- **Primary CTA(s):** `Техподдержка`, `Как купить`
- **Secondary CTA(s):** certificates, related information links
- **Forms present:** product support form
- **Form fields observed:** name, phone, city, email, organization, topic, message
- **Contact methods found:** phone, callback link
- **Trust signals found:** detailed product specs, certificates link
- **Navigation items observed:** same top navigation and left product catalog
- **Accessibility notes:** long dense copy blocks; small font; sidebar links look low-emphasis
- **Technical notes:** buying path is indirect; calculator widget is visually dated and secondary
- **Could not verify:** support form validation and success state
- **Screenshot paths:** `C:\Users\a_elkin\Documents\Codex\2026-07-13\https-seneg-ru\outputs\seneg-audit\03-product-aquadecor.png`

### Page: https://seneg.ru/contacts/scheme
- **Page type:** contact page
- **Tool used:** Edge headless screenshot + web extraction
- **Evidence confidence:** High
- **Title:** «СЕНЕЖ» — адрес и схема проезда
- **Meta description:** not captured in web extract
- **H1:** `«СЕНЕЖ» — адрес и схема проезда`
- **Primary CTA(s):** map interaction, contact details
- **Secondary CTA(s):** `Как купить`
- **Forms present:** none observed in page body
- **Form fields observed:** none in page body
- **Contact methods found:** address, phone, email, map
- **Trust signals found:** physical office address, route map
- **Navigation items observed:** same top navigation and left product catalog
- **Accessibility notes:** small text and weak hierarchy in route instructions
- **Technical notes:** page is informational rather than action-oriented
- **Could not verify:** map accessibility, keyboard path
- **Screenshot paths:** `C:\Users\a_elkin\Documents\Codex\2026-07-13\https-seneg-ru\outputs\seneg-audit\04-contact-page.png`

### Page: https://seneg.ru/about/why
- **Page type:** about/trust content
- **Tool used:** web extraction
- **Evidence confidence:** Medium
- **Title:** Почему «СЕНЕЖ»
- **Meta description:** not captured in web extract
- **H1:** `Почему «СЕНЕЖ»`
- **Primary CTA(s):** none prominent
- **Secondary CTA(s):** generic site navigation
- **Forms present:** none observed in content area
- **Form fields observed:** none
- **Contact methods found:** site-wide phones and footer email
- **Trust signals found:** brand narrative
- **Navigation items observed:** same global navigation
- **Accessibility notes:** long uninterrupted text blocks
- **Technical notes:** page is heavy on brand story and light on practical proof
- **Could not verify:** visual hierarchy beyond extracted text
- **Screenshot paths:** none

## Raw findings log

### Finding candidate
- **ID:** 4.2-a
- **Checklist item:** 4.2 / 4.8 / 4.9
- **Observed / Extracted / Inferred:** Observed
- **Confidence:** High
- **Page:** https://seneg.ru/
- **Observation:** In the narrow mobile screenshot, the desktop-style header remains split across columns and content appears clipped instead of responsively reflowing.
- **Potential impact:** Mobile visitors face immediate comprehension and navigation friction.
- **Needs final report?** yes

### Finding candidate
- **ID:** 2.2-a
- **Checklist item:** 2.1 / 2.2 / 2.3
- **Observed / Extracted / Inferred:** Observed
- **Confidence:** High
- **Page:** https://seneg.ru/
- **Observation:** The first screen is dominated by decorative header graphics, top phones, category lists, and multiple links; the main next action is not visually dominant.
- **Potential impact:** Lower first-screen clarity and reduced conversion from cold traffic.
- **Needs final report?** yes

### Finding candidate
- **ID:** 5.1-a
- **Checklist item:** 5.1 / 5.3 / 1.9
- **Observed / Extracted / Inferred:** Observed
- **Confidence:** High
- **Page:** https://seneg.ru/
- **Observation:** The homepage combines top navigation, left catalog, audience shortcuts, news, newsletter, search, and category tabs in one screen.
- **Potential impact:** Cognitive overload and slower path selection.
- **Needs final report?** yes

### Finding candidate
- **ID:** 2.4-a
- **Checklist item:** 2.4 / 2.5 / 1.6
- **Observed / Extracted / Inferred:** Extracted
- **Confidence:** High
- **Page:** https://seneg.ru/
- **Observation:** The request form asks for phone, name, email, region/city, message, office selection, consent, and other fields for first contact.
- **Potential impact:** Higher abandonment on initial inquiry.
- **Needs final report?** yes

### Finding candidate
- **ID:** 3.9-a
- **Checklist item:** 3.9 / 3.10 / 2.8
- **Observed / Extracted / Inferred:** Observed
- **Confidence:** High
- **Page:** https://seneg.ru/
- **Observation:** Homepage content references a news item dated October 2018, and the footer copyright ends at 2022.
- **Potential impact:** Signals neglect and weakens trust in current support and availability.
- **Needs final report?** yes

### Finding candidate
- **ID:** 2.12-a
- **Checklist item:** 2.12
- **Observed / Extracted / Inferred:** Observed
- **Confidence:** High
- **Page:** https://seneg.ru/products/catalogue/decor/aquadecor
- **Observation:** Product page shows rich specs and certificates but no obvious price, dealer finder, stock cue, or short buy/request-quote action near the product summary.
- **Potential impact:** Users must do extra work to understand how to buy.
- **Needs final report?** yes

### Finding candidate
- **ID:** 3.6-a
- **Checklist item:** 3.6 / 3.11
- **Observed / Extracted / Inferred:** Observed
- **Confidence:** High
- **Page:** https://seneg.ru/products/catalogue/decor/aquadecor
- **Observation:** Product content is text-heavy, small, and optimized more for technical completeness than quick scanning.
- **Potential impact:** Slower comprehension, especially for non-expert buyers.
- **Needs final report?** yes

### Finding candidate
- **ID:** 2.9-a
- **Checklist item:** 2.9
- **Observed / Extracted / Inferred:** Observed
- **Confidence:** High
- **Page:** https://seneg.ru/contacts/scheme
- **Observation:** Contact details are easy to find and include phone, email, address, and map.
- **Potential impact:** Positive trust support.
- **Needs final report?** maybe

## Constraints and caveats

- Keyboard-only navigation was not tested.
- Live form submission was not completed.
- Exact contrast measurement was not run; accessibility notes are quick-pass estimates.
- Mobile evidence comes from a narrow viewport screenshot, not full touch interaction.
