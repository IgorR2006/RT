<div align="center"> <h1> Автоматизированное тестирование веб-сервиса "Ростелеком ID" </h1></div>
<h4> Объект тестирования: https://b2c.passport.rt.ru </h4>
<h4> Инструменты тестирования: Selenium WebDriver <img src="https://github.com/devicons/devicon/blob/master/icons/selenium/selenium-original.svg" title="SE" **alt="SE" width="15" height="15"/>, Pytest <img src="https://github.com/devicons/devicon/blob/master/icons/pytest/pytest-original.svg" title="pytest" **alt="pytest" width="20" height="20"/></h4>
<h4> Среда тестирования: Windows 10 <img src="https://raw.githubusercontent.com/devicons/devicon/1119b9f84c0290e0f0b38982099a2bd027a48bf1/icons/windows8/windows8-original.svg" title="WN" **alt="WN" width="15" height="15"/>, Google Chrome <img src="https://www.svgrepo.com/show/380996/google-chrome-logo-new.svg" title="GO" **alt="GO" width="20" height="20"/>, Microsoft Edge <img src="https://www.svgrepo.com/download/378791/edge.svg" title="GO" **alt="GO" width="20" height="20"/></h4>
<br>
<h4> Отчёт о результатах тестирования: </h4>
<p> Протестированы компоненты: Авторизация, Регистрация. <br>
При тестировании сайта были написаны:
<a href="https://docs.google.com/spreadsheets/d/1fiCdRWrRub1UGQ6K_NCpJZEYIQFfWdPP/edit?usp=sharing&ouid=103842292872009011194&rtpof=true&sd=true"> ручные чек-лист, тест-кейсы и баг- репорты </a>
автоматизированные тесты. <br>
Используемые техники тест-дизайна: Классы Эквивалентности, Граничные Значения.<br>
Выявлено дефектов: 3 <br>

<h4> Тестовая документация: </h4>
<p> <a href="https://docs.google.com/document/d/1K9jjIaOQLKz98EIoGUn-82fzu3bcL0Jn/edit?usp=drive_link&ouid=103842292872009011194&rtpof=true&sd=true"> бриф </a> <br>
 <p> <br>
<h4> Требования к запуску автоматизированных тестов: </h4>
<p> 1. Предустановленный Google Chrome </p>
<p> 2. Предустановленный Python не ниже версии 3.8 </p>
<p> 3. Установка зависимостей из файла requirements.txt </p>
<p> 4. Автотесты настроены на запуск через Run </p>

!!!ВНИМАНИЕ!!!
Для страниц восстановления пароля в позитивных и негативных тестах необходимо ВРУЧНУЮ вводить символы с картинки “капчи” в поле для ввода “капча”, задержка по времени для ввода настроена автоматически. Для проверки авторизации по почте и паролю, так же потребуется ввод капчи вручную!!!
Для генерации временного адреса электронной почты использовался сайт www.1secmail.com
<br>
<h4> Содержание проекта: </h4>
Проект содержит две папки pages  и tests, а так же файлы conftest.py и pytest.ini, requirements.txt.

- conftest.py - фикстура для работы с браузером.

- pytest.ini - маркеры для параметризации.

- requirements.txt. - зависимости

Папка pages содержит следующие файлы:

- registration_email.py - GET-запросы к виртуальному почтовому ящику для получения валидного email и кода для регистрации на сайте и восстановления пароля;

- config.py - основной URL тестируемого сайта;

- auth.py - функции-обертки для локаторов, распределенные по классам в зависимости от тематики тестов;

- base.py - функции для применения к локаторам явных ожиданий, получения главной страницы сайта и пути текущей страницы;

- locators.py - XPath- и CSS-локаторы web-элементов сайта;

- settings.py - данные, используемые в процессе теста.

Папка tests содержит следующие файлы:

- test_registr_positive - позитивные тесты страницы регистрации;

- test_auth_page_positive - позитивные тесты страницы авторизации (в тесте по автоматическому переключению табов используется реальный номер лицевого счета, правильного формата (уже закрыт), в проверках ручных тестов проходит все ОК, в автоматическом режиме переключения не происходит!!! Вместо этого откидывается последняя пара цифр, и перекидывается на номер телефона);

- test_new_password_positive - позитивные тесты страницы восстановления пароля;

- test_registr_positive - позитивные тесты страницы регистрации;

- test_auth_page_negative - негативные тесты страницы авторизации;

- test_new_password_negative - негативные тесты страницы восстановления пароля.
