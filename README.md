## Уровни тестирования
* Модульное тестирование: проверяем модули, отдельно "Накопилка" и "Заполнение анкеты"
* Интеграционное тестирование - проверяем взаимодействие между компонентами (Переход с главной страницы на страницу "Накопилки", переход из "Накопилки" в заполнение анкеты)

## Виды тестирования
* Функциональное тестирование - проверяем функциональность на соответствие требованиям
* Дымовое тестирование - проверяем, что работает вкладка "Накопилка" и путь к ней

## План автоматизации тестирования формы заявки на накопительный счет “Накопилка”

## Перечень автоматизированных сценариев
1. Проверка открытия страницы Альфа-Банка
2. Проверка наличия вкладки Вклады -> "Накопилка"
3. Проверка открытия страницы "Накопилка"
4. Проверка обоих кнопок "Заполнить заявку"
5. Проверить вкладку "Новым клиентам" и кликаем на "Заполнить анкету", проверяем, что перешли в форму заполнения анкеты и заполняем ее
6. Проверить вкладку "Клиентам Альфа-банка" и проверяем появившейся интерфейс
7. Проверить вкладку "Я получаю зарплату в Альфа-банке" , проверить ссылки на Альфа-клик либо Альфа-мобайл, сравнивая что открылось после нажатия на ссылки с заглавными страницами приложения
8. Проверить вкладку "Я не получаю зарплату в Альфа-банке", в зависимости от того, что откроется, протестировать либо анкету, либо появление уведомления и/или ссылки)
9. Раскрыть "Как пополнить счет" и "Как снять наличные со счета" и проверить, появился ли текст

## Форма анкеты:
### Позитивные сценарии
1. Проверяем что будет, если правильно заполнить форму валидными значениями (Имя создать с помощью фейкера на русском, номер также с помощью фейкера, нажать клавишу с согласием на обработку)
2. Проверяем что будет, если правильно заполнить форму валидными значениями (Имя сделать двойное, с дефисом, номер с помощью фейкера, нажать клавишу с согласием на обработку)
3. Проверяем действительность ссылки на обработку персональных данных

* Ожидаемый результат
1. Появится надпись "Спасибо, мы с вами свяжемся" и произойдет перехода на страницу с вкладами
2. Появится надпись "Спасибо, мы с вами свяжемся" и произойдет перехода на страницу с вкладами
3. В сплывающем окне открывается документ о соглашении

### Негативные сценарии
1. Проверяем что будет, если заполнить все поля, кроме имени
2. Проверяем что будет, если заполнить все поля, кроме номера
3. Проверяем что будет, если заполнить все поля, но не ставим галочку напротив согласия
4. Проверяем на некорректность заполнения формы, ставим на поле имя значение из фейкера, но на английском языке
5. Проверяем на некорректность заполнения формы, ставим на поле имя, значение в один символ русской буквы
6. Проверяем на некорректность заполнения формы, ставим на поле номер значение, и на единицу меньше правильного числа цифр в номере
7. Проверяем на некорректность заполнения формы, ставим на поле номер значение, на единицу больше правильного числа цифр в номере
8. Проверяем на некорректность заполнения формы, ставим на поле номер любое символьное значение, например, "+"
9. Проверяем поле Имя граничными значениями

* Ожидаемый результат
1. Появится надпись, что поле обязательно для заполнения
2. Появится надпись, что поле обязательно для заполнения
3. Надпись "Я согласен…" должна выделиться красным цветом
4. Появится надпись, что неправильно введено значение
5. Появится надпись, что неправильно введено значение
6. Появится надпись, что неправильно введено значение
7. Появится надпись, что неправильно введено значение или номер должен состоять из 10 цифр
8. Появится надпись, что неправильно введено значение или номер должен состоять из 10 цифр
9. Появится надпись, что неправильно введено значение

### Скриншоты
Скрин 1
https://github.com/Mikhail9030/AQATestPlan/blob/master/%D1%81%D0%BA%D1%80%D0%B8%D0%BD1.bmp
Скрин 2
https://github.com/Mikhail9030/AQATestPlan/blob/master/%D1%81%D0%BA%D1%80%D0%B8%D0%BD2.bmp
Скрин 3
https://github.com/Mikhail9030/AQATestPlan/blob/master/%D1%81%D0%BA%D1%80%D0%B8%D0%BD3.bmp

## Перечень используемых инструментов с обоснованием выбора
* Java - язык, на котором будем писать код
* IntelliJ IDEA - программа, в которой пишем код
* Gradle - система автоматической сборки внутри IntelliJ IDEA;
* JUnit 5 - библиотека для тестирования
* Selenide - так как работаем с веб-страницей и ищем появившиеся значения с помощью html и css
* Allure - используем для наглядного изображения прохождения тестов и ошибок
* Git - для контроля версий

## Перечень необходимых разрешений/данных/доступов от банка
* Разрешение на тестирование страниц сайта с помощью автоматизированного ПО
* Разрешение на доступ к приложению
* Разрешение на доступ к базе данных
* Предоставление тестовых аккаунтов для тестирования открытия вклада через мобильное приложение "Альфа-Мобайл" и веб версии личного кабинета.

## Перечень и описание возможных рисков при автоматизации
* Неоправданная стоимость автоматизации
* Искажение результатов тестов в связи с отсутствием доступа к реальной БД
* Недоступность сайта или страницы
* Дополнительная нагрузка на сайт

## Перечень необходимых специалистов для автоматизации
* Достаточно будет одного QA Инженера, которы владеет всеми необходимыми для этого навыками и инструментами

## Интервальная оценка с учётом рисков
* Уточнение требований, cогласования и получение разрешений — 2 часа
* Написание авто-тестов + рефакторинг кода — 8 часов
* Резерв времени на написание баг-репортов — 4 часа
* Подготовка отчета о тестировании — 3 часа
* Итого: 17 часов + дополнительно с учетом рисков 3 часа, выходит примерно 20 часов.