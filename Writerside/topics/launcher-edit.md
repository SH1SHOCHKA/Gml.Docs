# Редактирование лаунчера

### Введение

Gml.Launcher - это проект, разработанный с использованием фреймворка Avalonia, который является кроссплатформенным UI фреймворком для .NET. Этот документ предоставляет обзор структуры проекта и инструкции по редактированию файлов проекта.

### Структура проекта

Проект Gml.Launcher организован в несколько основных директорий, каждая из которых выполняет определенную функцию. Ниже приведено подробное описание каждой директории и её содержимого:

#### Папка Common

- **common**
    - `.editorconfig`: Файл конфигурации для редактора кода, который помогает поддерживать единый стиль кода.
    - `.gitignore`: Файл, указывающий, какие файлы и директории следует игнорировать в системе контроля версий Git.
    - `dotnet.yml`: Файл конфигурации для CI/CD в GitHub Actions.
    - `load-repositories.bat`: Скрипт для загрузки репозиториев на Windows.
    - `load-repositories.sh`: Скрипт для загрузки репозиториев на Unix-подобных системах.
    - `README.md`: Основной файл с описанием проекта.

#### Launcher

- **launcher**
    - **Gml.Launcher**
        - **Dependencies**: Директория для зависимостей проекта.
        - **Assets**
            - **Fonts**: Директория для шрифтов.
            - **Images**: Директория для изображений.
            - **Resources**: Директория для других ресурсов.
            - **Styles**: Директория для стилей (например, XAML файлы для стилизации интерфейса).
        - **Core**: Основные файлы и логика приложения.
        - **Models**
            - `Language.cs`: Класс для представления языковых данных.
            - `ProfileInfoItem.cs`: Класс для представления информации профиля.
            - `SettingsInfo.cs`: Класс для представления настроек.
        - **ViewModels**
            - **Base**: Базовые классы для моделей представления.
            - **Components**: Компоненты для моделей представления.
            - **Pages**: Страницы для моделей представления.
            - `MainWindowViewModel.cs`: Модель представления для главного окна.
            - `SplashScreenViewModel.cs`: Модель представления для экрана загрузки.
        - **Views**
            - **Components**: Компоненты для представлений.
            - **Pages**
                - `LoginPageView.axaml`: Представление для страницы входа.
                - `OverviewPageView.axaml`: Представление для страницы обзора.
                - `ProfilePageView.axaml`: Представление для страницы профиля.
                - `SettingsPageView.axaml`: Представление для страницы настроек.
            - **SplashScreen**
                - `SplashScreen.axaml`: Представление для экрана загрузки.
                - `SplashScreen.axaml.cs`: Код-бихайнд для экрана загрузки.
            - `MainWindow.axaml`: Представление для главного окна.
        - `App.axaml`: Основное приложение (XAML).
        - `App.axaml.cs`: Код-бихайнд для основного приложения.
        - `app.manifest`: Манифест приложения.
        - `FodyWeavers.xml`: Конфигурация для Fody (инструмент для работы с IL кодом).
        - `Program.cs`: Основной файл запуска приложения.

#### Source (src)

- **src**: Директория с исходным кодом.

#### Tests

- **tests**: Директория с тестами проекта.

### Инструкции по редактированию

1. **Редактирование кода**: Для редактирования кода используйте любой текстовый редактор или IDE, поддерживающие C# и XAML (например, Visual Studio, JetBrains Rider или Visual Studio Code).
2. **Добавление зависимостей**: Для добавления новых зависимостей используйте NuGet пакетный менеджер.
3. **Работа с представлениями и моделями представления**:
    - **Models**: Добавьте или измените классы в директории Models для обновления данных и логики.
    - **ViewModels**: Измените или добавьте классы в директории ViewModels для обновления логики представления.
    - **Views**: Измените XAML файлы в директории Views для обновления UI.

### Сборка и запуск

1. **Установка зависимостей**: Выполните команду `dotnet restore` для установки всех необходимых зависимостей.
2. **Сборка проекта**: Выполните команду `dotnet build` для сборки проекта.
3. **Запуск проекта**: Выполните команду `dotnet run` для запуска приложения.

Следуя этой документации, вы сможете понять структуру проекта Gml.Launcher и легко вносить необходимые изменения.