---
title: "Галерея Builder Pattern: 7 шедевров создания объектов. Часть I"
description: "Изучаем Builder Pattern для создания тестовых данных. 7 паттернов создания объектов с примерами кода. Conditional Builder, Enumeration Builder и другие техники."
tags: ["builder-pattern", "design-patterns", "test-data-generation", "javascript", "automation", "qa-automation", "object-creation", "testing-patterns", "software-design", "test-automation", "qa-coding", "ТестируемСЛюбовью"]
date: 2025-06-18
draft: false
ShowToc: true
TocOpen: true
slug: "builder-pattern-gallery-part-1"
keywords: ["Builder Pattern", "создание тестовых данных", "паттерны проектирования", "JavaScript Builder", "автоматизация тестирования", "объекты в тестах"]
categories: ["Паттерны проектирования", "Автоматизация тестирования"]
---

# Галерея Builder Pattern: 7 шедевров создания объектов. Часть I

**🎨 Галерея Builder Pattern: 7 шедевров создания объектов. Часть I**

Создавать тестовые данные вручную — как рисовать «Чёрный квадрат» пальцами. Возможно, но больно! 💢
Билдеры — ваши кисти и резцы. Выбирайте инструмент как истинный мастер!

## 🖼️ Моя исповедь куратора

Когда-то я писала объекты, как Ван Гог в период безумия — хаотично и страстно. Пока однажды сгенерированные данные не сломали прод…
Теперь я создаю данные с изяществом да Винчи. Добро пожаловать на выставку)))

## 🏛️ Зал 1: Классическое искусство

### 1️⃣ «Натюрморт с if/else» (Ветвление или Conditional Builder Pattern)

**Стиль:** Примитивизм

```javascript
setAge(age) {
  if (age < 0) this.user.age = 0;      // "Младенец с чашей"
  else if (age > 120) this.user.age = 120; // "Старик у моря"
  else this.user.age = age;            // "Портрет неизвестного"
  return this;
}
```

🖌️ **Критики говорят:**
> "Наивно! Очаровательно в простоте, но сложные композиции превращаются в «Гернику»"

### 2️⃣ «switch: Готические витражи» (Перечисление или Enumeration Builder Pattern)

**Стиль:** Средневековая иконопись

```javascript
switch(role) {
  case 'admin': // Святой Пётр с ключами
    this.user.permissions = ['all'];
    break;
  case 'moderator': // Ангел-хранитель
    this.user.permissions = ['read','edit'];
    break;
}
```

🖌️ **Критики говорят:**
> "Строгая симметрия! Но новый святой потребует перестройки собора"

## 🧭 Правила куратора

> Не вешайте авангард в классическую раму

---

📚 **Хотите углубиться в тему?** 
Изучите подробное руководство по [Builder Pattern на Refactoring.Guru](https://refactoring.guru/ru/design-patterns/builder)

*Нужна помощь?*
Присоединяйтесь к [моему Telegram-каналу @qawithlove](https://t.me/qawithlove) 