# Модерния ръководител на езика за програмиране JavaScript

Това хранилище съдържа българския превод на "*Модерния ръководител на езика за програмиране JavaScript*", публикувано в [https://javascript.info](https://javascript.info).

**Ето как можете да спомогнете за проекта:**

- Погледнете [прогреса на българския превод](https://github.com/javascript-tutorial/bg.javascript.info/issues/1).
- Изберете свободна статия, която искате да превеждате.
- Добавете коментар с заглавието на статията, напр. `An Introduction to JavaScript`.
    - Нашия бот ще го маркира, така че всички да разберат, че ти я превеждаш.
    - Коментарът ти трябва да съдържа само заглавието на статията.
- "Fork"-нете хранилището, преведете го и ни изпратете "Pull Request" когато е говото.
    - Заглавието на "Pull Request"-а трябва да съвпада с заглавието на статията. Ботът ще напише номера й на дадения проблем.

Моля, любезно разрешете на поддръжниците да преглеждат, обединяват или да поискат промени в превода ви.

Ако поддръжниците не отговарят или искаш да станеш поддръжник, пиши ни в [главното хранилище](https://github.com/javascript-tutorial/en.javascript.info/issues/new).

**Нека другите знаят какво превеждате, в таблото за съобщения или чатове на вашия език. Поканете ги да се присъединят!**

🎉 Благодарим Ви!

Името ти и размера на приноса ти ще се появи в страницата "About project" (За проекта) когато преводът се публикува.

Пълния списък със езиците може да се намери в <https://javascript.info/translate>.

## Структура

Всяка глава, статия или задача има своята папка.

Папката е именовано така `N-url`, където `N` е номер със цел сортиране и `url` където е част от линк с името на материала.

Типът на материала се определя чрез файла вътре в папката:

- `index.md` означава глава
- `article.md` означава статия
- `task.md` означава задача (решението трябва да бъде описано в `solution.md` файла)

Всяка от тези файлове започва от `# Title header`, след това текст с Markdown формат, лесно редактиран със обикновен текстов редактор.

Допълнителните ресурси и примери за дадена статия или задача също са в същата папка.

## Съвети за превод

Моля запазете прекъсванията на линиите и параграфите "както са": не добавете и не премахвайте същестуващите такива.
Направете го лесно за сливане на бъдещи промени от английската версия към превода.

Ако виждате, че английската версия може да се бъде подобрен - чудесно, изпратете ни "Pull Request" за него.

### Термини

- Някои специфични термини може и да не са превеждат, напр. "Function Declaration" (на български: Декларация за функция) могат да останат каквито са.
- За други термини като `resolved promise`, `slash`, `regexp`, и др. - погледнете в терминологичен речник. Ако го няма, погледнете наръчниците за превод, напр. в [MDN](https://developer.mozilla.org/en-US/).

### Термини със значение

На английски много термини имат очевидно значение. За човек, който не разбира английски, няма такова значение.

Моля, имейте това предвид, че понякога са необходими допълнителни обяснения или превод, например такива м/у английския и испанския:

```md
`ReadableStream` objects allows to read data chunk-by-chunk.
```

```md
`ReadableStream` ("flujo legible") objeto ...
```

### Текстовете в полетата с код

- Преведете коментарите.
- Преведете съобщенията от потребителите и примерните изречения/думи.
- НЕ превеждайте име на на променливите, класовете или идентификаторите.
- Бъдете сигурни, че след превода кодът работи :)

Примерно:

```js
// Example
const text = "Hello, world";
document.querySelector('.hello').innerHTML = text;
```

✅ Добро (преведи коментар):

```js
// Например
const text = 'Здравей свят';
document.querySelector('.hello').innerHTML = text;
```

❌ Лошо (НЕ превеждате имена на класове):

```js
// Например
const text = 'Здравей свят';
// ".hello" е име на клас
// НЕ ПРЕВЕЖДАЙТЕ
document.querySelector('.здравей').innerHTML = text;
```

Моля забележете, че понякога кодът е следват от снимка. Ако преведете например текста `Hello` -> `Здравей` в кода, то вие трябва да го преведете и в снимката.

При този случай сигурно ще е по-лесно да не се превежда подобен текст. По-късно ще видите повече за превеждането на снимки.

### Външни връзки

Ако външната връзка е към Wikipedia, напр. `https://en.wikipedia.org/wiki/JavaScript`, и версията на тази статия съществува на вашия език в прилично качество, то ще е по-добре да промените тази връзка с версията на вашия език.

Например:

```md
[JavaScript](https://en.wikipedia.org/wiki/JavaScript) is a programming language.
```

✅ Добро (en -> bg):

```md
[JavaScript](https://bg.wikipedia.org/wiki/JavaScript) (чете се джаваскрипт) е интерпретируем език за програмиране, ...
```

За връзки към MDN е достатъчно и частичните преведени версии.

Ако статията във външната връзка няма преведена версия на вашия език, оставете ги "каквито са".

### Метаданни

Някои файлове, попринцип задачите, имат YAML метаданни най-отгоре и са разграничени с `---`:

```md
importance: 5

---
...
```

Моля НЕ превеждайте "importance" (или други подобни метаданни).

### Анкери

Някои заглавия имат `[#anchor]` в края, напр.

```md
## Spread operator [#spread-operator]
```

Моля, НЕ превеждайте или Не премахвайте парчето с `[#...]`, то е за URL-а.

### Снимки

Повечето илюстрации използват "SVG" формат. Текстът в тях се заменя с преведените им варианти.

Преведения текст е в `images.yml` файл в главната директория на ръководство.

Файловия формат е YAML:

```yaml
image.svg:        # Файл на изображението
  "hello world":  # Английска фраза
    text: "Hola mundo"  # превод
    position: "centre"  # "center" или "right", ако е необходимо центриране или дясното подравняване на превода
```

## Пускане локално

Може да стартирате сървъра на ръководството локално, за да видите как изглежда.

Сървърът и инструкциите за инсталиране са в следната връзка > <https://github.com/javascript-tutorial/server>.
