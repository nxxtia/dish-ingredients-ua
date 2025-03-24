# dish-ingredients-ua
Цей репозиторій містить структуровані словники інгредієнтів, що використовуються в описах страв українською мовою.
Розміщено базу інгредієнтів українською мовою, структуровану за категоріями (наприклад, овочі, м'ясо, спеції, сир тощо), а також відповідність пестливих форм їхнім базовим назвам. Репозиторій призначений для використання в NLP-задачах, аналізі меню, підготовці баз даних для ресторанів, систем рекомендацій або інших проєктах.

## Структура репозиторію

- `ingredients.json` – головний словник інгредієнтів, згрупованих за категоріями.
- `diminutive-map.js` – відповідність пестливих і розмовних форм базовим назвам, наприклад `"бурячок" → "буряк"`.

## Категорії інгредієнтів

- М'ясо, Птиця, Риба, Морепродукти, Хліб, Макарони, Сир
- Овочі, Фрукти, Ягоди, Бобові, Горіхи, Спеції, Солодке
- Молоко та яйця, Трави та зелень, Гриби, Кулінарні добавки, Напої
- Комахи, Суші, Субпродукти, Інше

## Можливе застосування

- Стандартизація інгредієнтів в NLP-проєктах
- Порівняння та нормалізація даних із меню
- Створення пошуковиків для страв
- Лематизація та очищення текстових даних
- Підрахунок унікальних інгредієнтів або категорій

## Приклад використання

```js
const diminutiveMap = require('./diminutiveMap');

function normalizeWord(word) {
  return diminutiveMap[word.toLowerCase()] || word.toLowerCase();
}

console.log(normalizeWord("апельсинчик")); // "апельсин"
```

## Як зробити внесок
Якщо ви хочете доповнити словник, створіть Pull Request або відкрийте Issue.

## Автор
Цей репозиторій належить [@nxxtia](https://github.com/nxxtia)



