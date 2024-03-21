## :exclamation:  Это готовый проект Kittygram! 

:smile_cat: Kittygram - блог о домашних питомцах всех расцветок и нравов. Пользователи могут создавать страницы своих питомцев с текстовым описанием, изображением и списком достижений. Проект предусматривает регистрацию пользователей, поддержание базы данных, администрирование ресурсов и подготовлен для разворачивания как на локальном, так и на удаленном сервере. 

:computer: Стек технологий: Python, Django, REST API, JWT, Java, CSS, PostgreSQL, Docker, Nginx, GitHub Actions

### Схема работы проекта
Проект настроен на работу с GitHub Actions (файл kittygram_workflow.yml), по команде git push:  
1) Тестируются backend и frontend блоки
2) Собираются три образа (backend, frontend и gateway)  
3) Три образа обновляются на DockerHub
4) Файл инструкция docker-compose.production.yml копируется на сервер
5) По файлу инструкции проект разворачивается на удаленном сервере
6) По завершению всех действий телеграм бот сообщит об успешном завершении

### Что если вы хотите взять проект за основу:
1) Подготовьте необходимые параметры в GitHub Actions /settings/secrets/actions согласно GitHubActions.example
2) Добавьте IP сервера в ALLOWED_HOSTS в backend\kittygram_backend\settings.py
3) Скопируйте открытые репозитории https://github.com/IvanKiss42/kittygram_frontend и https://github.com/IvanKiss42/kittygram_backend чтобы иметь право их редактировать
4) Переадресуйте соответствующие команды в файлах-инструкциях kittygram_workflow.yml и docker-compose.production.yml на новые репозитории
5) Удачи!

