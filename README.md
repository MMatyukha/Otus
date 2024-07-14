# Otus
ДЗ #1: Автотест со своими ожиданиями

Необходимо реализовать следующие сценарии при помощи Selenium WebDriver:
Сценарий 1:
Открыть страницу каталога курсов .Найти курс по имени (имя курса должно передаваться как данные в тесте)
Кликнуть по плитке курса и проверить, что открыта страница верного курса
Для поиска курса по имени обязательно необходимо использовать stream api.
Сценарий 2:
Открываем страницу каталога курсов .
Найти курсы, которые стартуют раньше и позже всех. Если даты совпадают, то выбрать все такие курсы у которых дата совпадает.
Проверить, что на карточке самого раннего/позднего курсов отображается верное название курса и дата его начала
Для поиска таких курсов необходимо использовать stream api и reduce. Так же для проверки данных на странице карточки курса необходимо использовать jsoup.
Сценарий 3:
Открыть главную страницу .
В заголовке страницы открыть меню "Обучение" и выбрать случайную категорию курсов
Проверить, что открыт каталог курсов верной категории
Требования к реализации:
создавать объекты в тестах необходимо только через DI
можно использовать любой DI фреймворк (например один из Google Guice, Spring Context) или использовать Java Reflection
можно использовать любой тест раннер, но при использовании junit 5 необходимо использовать классы расширения, а для junit 4 - классы раннеры. Использовать наследование от базового класса при использовании тест раннера junit нельзя
обязательное использование линтеров spotbugs и checkstyle. Шаблон необходимо взять с занятия
обязательно все тесты должны быть написаны в 2 уровневом тест дизайне с использованием шаблонов проектирования
перед кликом и установки фокуса курсора на элемент необходимо выделить элемент рамкой (параметры рамки любые, но рамка должна быть видна на странице) с использованием слушателей. Переиспользование методов интерфейса WebElement не допустимо.
используем только Selenium WebDriver версии 4 и выше. Использование Selenide или SeleniumWebDriver более ранней версии недопустимо.
для сборки и запуска тестов необходимо использовать один из сборщиков (Maven или Gradle)
Дополнительно и по желанию:
Сужение интерфейса WebElement за счет использования типизации на элементах, например для кнопки использование типа Button с соответствующим интерфейсом, который есть на странице только у кнопки. Разрешается сделать свою реализацию или использовать yandex-elements