---
title: Math.atan2()
slug: Web/JavaScript/Reference/Global_Objects/Math/atan2
tags:
  - JavaScript
  - Math
  - Method
  - Reference
translation_of: Web/JavaScript/Reference/Global_Objects/Math/atan2
---
{{JSRef("Global_Objects", "Math")}}

## Сводка

Метод **`Math.atan2()`** возвращает арктангенс от частного своих аргументов.

## Синтаксис

```
Math.atan2(y, x)
```

### Параметры

- `y`
  - : Первое число.
- `x`
  - : Второе число.

## Описание

Метод `Math.atan2()` возвращает числовое значение от -π до π, представляющее угол тета точки `(x, y)`. Это выраженный в радианах угол, отсчитываемый против часовой стрелки от положительного направления оси X до точки `(x, y)`. Обратите внимание, что первым в метод передаётся координата y, а только вторым — координата x.

В метод `Math.atan2()` аргументы `x` и `y` передаются по отдельности, в то время, как в метод `Math.atan()` передаётся отношение этих двух аргументов.

Поскольку метод `atan2()` является статическим методом объекта `Math`, вы всегда должны использовать его как `Math.atan2()`, а не пытаться вызывать метод на созданном экземпляре объекта `Math` (поскольку объект `Math` не является конструктором).

## Примеры

### Пример: использование метода `Math.atan2()`

```js
Math.atan2(90, 15); // 1.4056476493802699
Math.atan2(15, 90); // 0.16514867741462683

Math.atan2(±0, -0);               // ±PI.
Math.atan2(±0, +0);               // ±0.
Math.atan2(±0, -x);               // ±PI для x > 0.
Math.atan2(±0, x);                // ±0 для x > 0.
Math.atan2(-y, ±0);               // -PI/2 для y > 0.
Math.atan2(y, ±0);                // PI/2 для y > 0.
Math.atan2(±y, -Infinity);        // ±PI для конечного y > 0.
Math.atan2(±y, +Infinity);        // ±0 для конечного y > 0.
Math.atan2(±Infinity, x);         // ±PI/2 для конечного x.
Math.atan2(±Infinity, -Infinity); // ±3*PI/4.
Math.atan2(±Infinity, +Infinity); // ±PI/4.
```

## Спецификации

| Спецификация                                                         | Статус                   | Комментарии                                            |
| -------------------------------------------------------------------- | ------------------------ | ------------------------------------------------------ |
| ECMAScript 1-е издание.                                              | Стандарт                 | Изначальное определение. Реализована в JavaScript 1.0. |
| {{SpecName('ES5.1', '#sec-15.8.2.5', 'Math.atan2')}} | {{Spec2('ES5.1')}} |                                                        |
| {{SpecName('ES6', '#sec-math.atan2', 'Math.atan2')}} | {{Spec2('ES6')}}     |                                                        |

## Совместимость с браузерами

{{Compat}}

## Смотрите также

- {{jsxref("Math.acos()")}}
- {{jsxref("Math.asin()")}}
- {{jsxref("Math.atan()")}}
- {{jsxref("Math.cos()")}}
- {{jsxref("Math.sin()")}}
- {{jsxref("Math.tan()")}}