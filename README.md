# Розрахунково графічна робота 
Розрахунково графічна робота на тему «Шаблони проектування»
В даній розрахунково графічній роботі буде розглянуто наступні шаблони проектування:Abstract factory, Facade, Mediator, Asynchronous method invocation.

## Абстрактна фабрика
Abstract Factory (абстрактна фабрика) є патерном проектування, який надає інтерфейс для створення сімейств взаємопов'язаних або залежних об'єктів без зазначення їх конкретних класів. Це дозволяє клієнтському коду створювати об'єкти, не турбуючись про їхню конкретну реалізацію, що сприяє кращій масштабованості та модульності коду.

### Умови використання
Коли система повинна бути незалежною від способу створення, складання і представлення продуктів.
Коли систему потрібно конфігурувати одним з декількох сімейств продуктів.
Коли потрібно забезпечити взаємодію між продуктами одного сімейства.
Коли потрібно надати бібліотеку продуктів, розкриваючи тільки їх інтерфейси, але не реалізацію.

### Особливості використання
Патерн включає в себе кілька фабрик (Concrete Factories), які реалізують інтерфейс Abstract Factory.
Abstract Factory забезпечує методи для створення об'єктів кожного типу продукту.
Клієнт використовує інтерфейс фабрики для створення об'єктів, що зменшує залежність від конкретних класів.

### Статична модель 

![Статична модель Bridge](AbstractFactory.png)

### Динамічна модель 

![Динамічна модель Bridge](AbstractFactory11.png)


## Фасад
Facade (фасад) є патерном проектування, який надає спрощений інтерфейс до складної системи класів, бібліотеки або фреймворка. Фасад визначає високорівневий інтерфейс, який полегшує використання підсистеми, спрощуючи її взаємодію з клієнтським кодом.

### Умови використання

Коли необхідно надати простий інтерфейс до складної підсистеми.
Коли потрібно ізолювати клієнтів від компонентів підсистеми, що дозволяє незалежно змінювати її.
Коли потрібно зменшити кількість об'єктів, з якими взаємодіє клієнт.
### Особливості використання

Фасад містить посилання на всі класи підсистеми і делегує клієнтські запити відповідним методам підсистеми.
Клієнт працює з фасадом, не знаючи про складні взаємодії всередині підсистеми.
Фасад не заперечує використання підсистеми безпосередньо, якщо це необхідно для більш детального управління.

### Статична модель

![Статична модель Bridge](facadestat.png)

### Динамічна модель

![Динамічна модель Bridge](facadedin.png)

## Посередник (Mediator)
Mediator (посередник) є патерном проектування, який визначає об'єкт, що інкапсулює спосіб взаємодії набору об'єктів. Посередник забезпечує слабку зв'язаність між об'єктами, що дозволяє змінювати їх взаємодію незалежно від інших.

### Умови використання

Коли складні комунікації між наборами об'єктів призводять до заплутаного і незручного коду.
Коли потрібно повторно використовувати об'єкт, але не з його специфічними взаємодіями.
Коли необхідно централізувати управління взаємодіями між об'єктами.
### Особливості використання

Посередник має методи для відправлення і отримання повідомлень від об'єктів.
Кожен об'єкт в системі знає лише про посередника і не знає про інших об'єктів.
Спрощує підтримку і розширення коду, оскільки зміни в логіці взаємодії реалізуються в одному місці.


### Статична модель 

![Статична модель Bridge](mediatorstat.png)

### Динамічна модель 
![Динамічна модель Bridge](mediatordin.png)

## Асинхронне викликання методів
Asynchronous Method Invocation (асинхронний виклик методу) є патерном, який дозволяє викликати методи асинхронно, тобто без блокування виконання коду, який викликає метод. Це особливо корисно в сценаріях, де методи виконують довгі операції, наприклад, введення-виведення або обробка даних.

### Умови використання

Коли потрібно виконувати довгі або ресурсомісткі операції, не блокуючи основний потік виконання.
Коли необхідно підвищити продуктивність і відгук системи.
Коли потрібно уникнути блокувань і підвищити масштабованість системи.
### Особливості використання

Використання callback-функцій, промісів або майбутніх об'єктів для обробки результатів асинхронних викликів.
Потребує додаткового управління станом і помилками, що можуть виникнути в асинхронних викликах.
Дозволяє основному потоку продовжувати виконання, поки асинхронний метод завершується в фоновому режимі.
### Статична модель 

![Статична модель Bridge](Asynchronousstat.png)

### Динамічна модель 
![Динамічна модель Bridge](Asynchronousdin.png)
