# Рабочее окружение

Для выполнения работ потребуется:

1. Платформа разработки **.NET Core SDK 2.2**, https://dotnet.microsoft.com/download/dotnet-core/2.2
1. Редактор **Visual Studio Code**, https://code.visualstudio.com/download
2. NoSQL база данных **Redis**, https://redis.io/download

Полезно ознакомиться https://docs.microsoft.com/ru-ru/dotnet/core/tutorials/with-visual-studio-code

# Работа №1 Синхронное взаимодействие компонентов (HTTP REST)
## Цель
Научиться организовать взаимодействие двух процессов посредством протокола REST HTTP

## Задание
Разработать приложение, состоящее из компонентов **Frontend** и **Backend**, организовать взаимодействие компонентов по протоколу REST HTTP.

## Описание
Компонент **Frontend** предоставляет пользователю форму ввода текста. По нажатию на кнопку отсылки данные из формы отправляются в компонент **Backend** посредством HTTP запроса.
На стороне компонента **Backend** при получении данных генерируется идентификатор, данные помещаются в хранилище (идентификатор в качестве ключа), 
значение идентификатора возвращается в ответе на запрос.

### Компонент **Frontend**
Веб приложение на фреймворке ASP.Net MVC.

Создание проекта и запуск:
1. Создать директорию *Frontend* и перейти в неё.
2. Создать структуру проекта: **dotnet new mvc**
3. Запустить приложение: **dotnet run**

Открытие проекта в редакторе VSCode: **code .**

В директории src/Frontend содержится демонстрационная версия компонента Frontend.
Изменения в демо-проекте:
1. В файле *Controllers/HomeController.cs* добавить методы *Upload*
2. Реализовать TODO часть.
  Для выполнения HTTP запроса удобнее всего воспользоваться классом *HttpClient*
  https://docs.microsoft.com/ru-ru/aspnet/web-api/overview/advanced/calling-a-web-api-from-a-net-client
3.	Создать файл *Views/Home/Upload.cshtml* с формой ввода
4.	Запустить компонент: в Integrated terminal выполнить **dotnet run**
  Форма ввода будет доступна в браузере по адресу http://localhost:5000/Home/Upload

### Компонент **Backend**
ASP.Net WebApi приложение.

Создание проекта и запуск:
1. Создать директорию *Backend* и перейти в неё.
2. Создать структуру проекта: **dotnet new webapi**
3. Запустить приложение: **dotnet run**

Открытие проекта в редакторе VSCode: **code .**

В директории src/Backend содержится демонстрационная версия компонента Backend
