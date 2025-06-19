---
title: "Галерея Builder Pattern: 7 шедевров создания объектов. Часть II"
description: "Продолжение галереи Builder Pattern. Конфиг-объекты, цепочка методов, супрематизм и импрессионизм в коде. Современные паттерны создания объектов."
tags: ["builder-pattern", "design-patterns", "method-chaining", "config-objects", "javascript", "automation", "qa-automation", "object-creation", "testing-patterns", "software-design", "ТестируемСЛюбовью"]
date: 2025-06-19
draft: false
ShowToc: true
TocOpen: true
slug: "builder-pattern-gallery-part-2"
keywords: ["Builder Pattern", "цепочка методов", "конфиг-объекты", "паттерны проектирования", "JavaScript Builder", "автоматизация тестирования"]
categories: ["Паттерны проектирования", "Автоматизация тестирования"]
---

[← Читайте первую часть: Галерея Builder Pattern. Классическое искусство](/posts/builder-pattern-gallery-part-1/)

# Галерея Builder Pattern: 7 шедевров создания объектов. Часть II

![Абстрактная иллюстрация к части 2: Галерея Builder Pattern, современное искусство, супрематизм, импрессионизм](/images/posts/builder-pattern-gallery-part2.webp)
*Иллюстрация: абстрактное искусство, вдохновлённое темой паттернов. Источник: [Freepik](https://ru.freepik.com/free-vector/abstract-art-concept-illustration_13416103.htm#fromView=search&page=1&position=23&uuid=d75a6f7e-cbef-407a-bc4f-0cf2e3ac8136&query=%D0%B3%D0%B0%D0%BB%D0%B5%D1%80%D0%B5%D1%8F)*

## 🎭 Зал 2: Современное искусство

### 3️⃣ «Конфиг-объекты: Супрематизм» (Паттерн статической конфигурации или Static Configuration Pattern)

**Стиль:** Малевич

```javascript
// Минимальный класс для статической конфигурации
class ConfigBuilder {
  static createAdminConfig() {
    return {
      name: 'Администратор',
      permissions: ['all'],
      role: 'admin'
    };
  }
  
  static createUserConfig() {
    return {
      name: 'Пользователь',
      permissions: ['read', 'edit'],
      role: 'user'
    };
  }
  
  static createModeratorConfig() {
    return {
      name: 'Модератор',
      permissions: ['read', 'edit', 'delete'],
      role: 'moderator'
    };
  }
}

// Примеры вызова — как готовые картины
const adminConfig = ConfigBuilder.createAdminConfig();
const userConfig = ConfigBuilder.createUserConfig();
const moderatorConfig = ConfigBuilder.createModeratorConfig();

console.log(adminConfig);
// Результат: { name: 'Администратор', permissions: ['all'], role: 'admin' }
```

🖌️ **Критики говорят:**
> "Гениальный минимализм! Но попробуйте нарисовать треугольник..."

### 4️⃣ «Цепочка методов: Импрессионизм» (Паттерн цепочки методов или Method Chaining Pattern)

**Стиль:** Моне

```javascript
// Минимальный класс Builder
class UserBuilder {
  constructor() {
    this.user = {};
  }
  
  withName(name) {
    this.user.name = name;
    return this; // Возвращаем this для цепочки
  }
  
  withEmail(email) {
    this.user.email = email;
    return this;
  }
  
  withRole(role) {
    this.user.role = role;
    return this;
  }
  
  build() {
    return this.user;
  }
}

// Пример вызова — как мазки кисти
const user = new UserBuilder()
  .withName('Клод Моне')
  .withEmail('monet@impressionism.fr')
  .withRole('artist')
  .build();

console.log(user);
// Результат: { name: 'Клод Моне', email: 'monet@impressionism.fr', role: 'artist' }
```

🖌️ **Критики говорят:**
> "Каждый мазок — отдельный метод! Близко — хаос, издалека — совершенство"

## 🧭 Правила куратора

> Выбирайте кисть по холсту: для эскиза — карандаш, для шедевра — масло

📚 **Хотите углубиться в тему?** 
Изучите подробное руководство по [Builder Pattern на Refactoring.Guru](https://refactoring.guru/ru/design-patterns/builder)

*Нужна помощь?*
Присоединяйтесь к [моему Telegram-каналу @qawithlove](https://t.me/qawithlove) 