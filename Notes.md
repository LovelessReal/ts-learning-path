# 🟦 Основы TypeScript — шпаргалка

Краткое руководство по базовому синтаксису и возможностям TypeScript.

---

## 📘 1. Переменные и типы данных

```ts
let name: string = "Alice";     // строка
const age: number = 25;         // число
let isOnline: boolean = true;   // логическое значение

💡 Если не указать тип — TypeScript определит его автоматически (type inference).
```
№№📗 2. Функции с типами аргументов и возвращаемого значения
```ts
function add(a: number, b: number): number {
  return a + b;
}

const greet = (name: string): string => {
  return `Привет, ${name}!`;
};

💡 После двоеточия : указываются типы параметров и тип возвращаемого значения.
```
📙 3. Условия и циклы

```ts
if (age >= 18) {
  console.log("Совершеннолетний");
} else {
  console.log("Ребёнок");
}

for (let i = 0; i < 5; i++) {
  console.log(i);
}

let count = 0;
while (count < 3) {
  console.log(count);
  count++;
}
💡 Синтаксис полностью совпадает с JavaScript.
```
📒 4. Массивы и объекты
let numbers: number[] = [1, 2, 3];
let names: string[] = ["Anna", "Bob", "Kate"];

let user: { name: string; age: number } = {
  name: "Alice",
  age: 25,
};


💡 Указывай тип элементов массива или описывай структуру объекта.

📔 5. Интерфейсы (interface)
interface User {
  name: string;
  age: number;
  isAdmin?: boolean; // ? — необязательное свойство
}

const person: User = { name: "Tom", age: 30 };


💡 Интерфейсы помогают IDE подсказывать свойства и предотвращать ошибки.

📕 6. Импорт и экспорт файлов (модули)
// math.ts
export function add(a: number, b: number): number {
  return a + b;
}

// app.ts
import { add } from "./math";

console.log(add(2, 3)); // 5


💡 export делает сущность доступной для других файлов,
а import подключает её.
