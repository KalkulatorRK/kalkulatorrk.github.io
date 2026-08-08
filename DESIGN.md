---
name: Калькулятор РК
description: Operate UI для инструментов радиографического НК
colors:
  bg: "#e8eef4"
  bg-glow-a: "#d5e4f2"
  bg-glow-b: "#cfd9e6"
  surface: "#ffffff"
  bg-panel: "#f4f7fa"
  ink: "#1a2332"
  ink-muted: "#3d4a5c"
  line: "#c5d0dc"
  line-strong: "#8a9aab"
  accent: "#0b4f8c"
  accent-hover: "#093f70"
  focus: "#5b9fd4"
  disabled: "#7a92a8"
  danger: "#9b1c1c"
  danger-soft: "#fff8f8"
  ok: "#0f5c38"
  warn: "#7a4b00"
typography:
  ui:
    fontFamily: "Source Sans 3, Segoe UI, sans-serif"
    fontSize: "16px"
    fontWeight: 400
    lineHeight: 1.45
  page-title:
    fontFamily: "Source Sans 3, Segoe UI, sans-serif"
    fontSize: "1.55rem"
    fontWeight: 700
    lineHeight: 1.2
    letterSpacing: "-0.02em"
  page-title-sm:
    fontFamily: "Source Sans 3, Segoe UI, sans-serif"
    fontSize: "1.35rem"
    fontWeight: 700
  section:
    fontFamily: "Source Sans 3, Segoe UI, sans-serif"
    fontSize: "1.1rem"
    fontWeight: 700
  label:
    fontFamily: "Source Sans 3, Segoe UI, sans-serif"
    fontSize: "0.86rem"
    fontWeight: 600
  meta:
    fontFamily: "Source Sans 3, Segoe UI, sans-serif"
    fontSize: "0.8rem"
    fontWeight: 600
  meta-lg:
    fontFamily: "Source Sans 3, Segoe UI, sans-serif"
    fontSize: "0.95rem"
    fontWeight: 700
  button:
    fontFamily: "Source Sans 3, Segoe UI, sans-serif"
    fontSize: "0.92rem"
    fontWeight: 700
  hint:
    fontFamily: "Source Sans 3, Segoe UI, sans-serif"
    fontSize: "0.78rem"
  unit:
    fontFamily: "Source Sans 3, Segoe UI, sans-serif"
    fontSize: "0.85rem"
    fontWeight: 600
  status:
    fontFamily: "Source Sans 3, Segoe UI, sans-serif"
    fontSize: "0.75rem"
    fontWeight: 700
  helper:
    fontFamily: "Source Sans 3, Segoe UI, sans-serif"
    fontSize: "0.88rem"
rounded:
  xs: "4px"
  control: "6px"
  panel: "8px"
spacing:
  xs: "4px"
  sm: "8px"
  md: "12px"
  lg: "16px"
components:
  button-primary:
    backgroundColor: "{colors.accent}"
    textColor: "#ffffff"
    rounded: "{rounded.control}"
    padding: "10px 14px"
    height: "44px"
  button-secondary:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.ink}"
    rounded: "{rounded.control}"
    padding: "10px 14px"
    height: "44px"
  input:
    backgroundColor: "#ffffff"
    textColor: "{colors.ink}"
    rounded: "{rounded.control}"
    height: "44px"
---

# Design system — Калькулятор РК

## Overview
Режим **Operate**: рабочие формы НК. Ясность ввода и читаемость результата важнее декора. Эталон новой поверхности инструмента: `karta-nk.html` (журнал секций + sticky-сводка + печатный лист).

## Colors
Светлая холодная база (`#e8eef4`), белая поверхность, один акцент `#0b4f8c` с контрастом ≥4.5:1 для белого текста на кнопках. Семантика: danger / ok / warn отдельно. Запрет: purple/violet градиенты, cyan-on-dark glow, кремовый terracotta-bias.

## Typography
UI-лицо: Source Sans 3. Иерархия: заголовок страницы → секция журнала → лейбл → значение в документе. Не Inter / Roboto / Arial как единственный display-стек. Не пропускать уровни заголовков (h1→h2→h3).

## Layout
Плотная рабочая форма. На десктопе: форма | превью документа. На узком экране превью листа может идти выше формы, чтобы документ был в первом viewport. Sticky-панель держит объект/стык и главный action. Карточки только как контейнер взаимодействия; не вкладывать card в card. Журнал секций — делители, не плитки с собственной рамкой внутри рамки.

## Elevation & Depth
Лёгкая граница + при необходимости одно мягкое смещённое затенение. Без glass/backdrop-filter на sticky, без side-tab (`border-left` ≥2px как акцент секции), без zero-offset glow.

## Shapes
Скругление контролов ~6px, панелей ~8px, мелких бейджей ~4px. Поля с единицами: input + unit-суффикс в одной линии.

## Components
- Inputs: явный лейбл, единица рядом, touch target ≥44px
- Primary button: один главный action (сформировать / печать)
- Accordion-секции журнала со статусом заполненности
- Превью документа всегда как лист A4 (пустые ячейки «—»), не как empty-state прямоугольник
- Help: collapsible / inline, не стена текста в первом viewport

## Do's and Don'ts
**Do:** деловой русский язык; ссылки на связанные калькуляторы; печатный CSS для A4; WCAG AA.
**Don't:** emoji как иконки; nested cards; фиолетовый AI-SaaS вид; перегруз первого экрана промо и статистикой; модалки для обычного заполнения формы.
