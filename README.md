TaskManager 🗓️

![C#](https://img.shields.io/badge/c%23-%23239120.svg?style=for-the-badge&logo=csharp&logoColor=white)
![.NET](https://img.shields.io/badge/.NET-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![WPF](https://img.shields.io/badge/WPF-0078D6?style=for-the-badge&logo=windows&logoColor=white)
![SQL Server](https://img.shields.io/badge/SQL%20Server-CC2927?style=for-the-badge&logo=microsoft%20sql%20server&logoColor=white)
![Entity Framework](https://img.shields.io/badge/Entity%20Framework-512BD4?style=for-the-badge&logo=nuget&logoColor=white)

TaskManager — это современное настольное приложение-органайзер для эффективного управления персональными и профессиональными задачами. Разработано на платформе .NET с использованием WPF и Microsoft SQL Server.

📋 Содержание
- [О проекте](#о-проекте)
- [Функциональные возможности](#функциональные-возможности)
- [Технологический стек](#технологический-стек)
- [Требования к системе](#требования-к-системе)
- [Установка и запуск](#установка-и-запуск)
- [База данных](#база-данных)
- [Структура проекта](#структура-проекта)
- [Планы развития](#планы-развития)
- [Автор](#автор)

🎯 О проекте

TaskManager создан для автоматизации процессов планирования и тайм-менеджмента. Приложение позволяет:
- Создавать и редактировать задачи с установкой дедлайнов
- Назначать приоритеты и категории
- Отслеживать прогресс выполнения
- Сохранять данные между сеансами работы

Проект разработан в рамках учебной практики в ГБПОУ КАИТ №20 и демонстрирует владение современными технологиями разработки desktop-приложений.

✨ Функциональные возможности

- ✅ "Создание и редактирование задач" с подробным описанием
- ⏰ "Установка дедлайнов" с визуальным отображением срочности
- 🔥 "Система приоритетов":
  - Высокий
  - Средний  
  - Низкий
- 📂 Категоризация задач:
  - Работа
  - Личное
  - Учеба
- 📊 "Отслеживание прогресса" с отметкой о выполнении
- 💾 "Постоянное хранение данных" в Microsoft SQL Server
- 🎨 "Интуитивно понятный интерфейс" на WPF

🛠 Технологический стек

| Технология | Назначение |
|------------|------------|
| C# | Язык программирования |
| .NET 6.0/8.0 | Платформа разработки |
| WPF + XAML | Графический интерфейс |
| Microsoft SQL Server | СУБД для хранения данных |
| ADO.NET / Entity Framework | Доступ к данным |
| MVVM Pattern | Архитектурный паттерн |

💻 Требования к системе

- "ОС": Windows 10/11 или Windows Server 2019+
- "NET" .NET 6.0 SDK или выше
- "SQL Server": Microsoft SQL Server 2019+ или SQL Server Express
- "ОЗУ": минимум 4 ГБ (рекомендуется 8 ГБ)
- "Диск": 100 МБ свободного места

🚀 Установка и запуск
git clone https://github.com/yourusername/TaskManager.git
cd TaskManager

🗃️ База данных

Убедитесь, что SQL Server запущен 
Создайте базу данных TaskManagerDB 
Настройте строку подключения в app.config:

<connectionStrings>
    <add name="TaskManagerEntities" 
         connectionString="metadata=res://*/TaskManagerModel.csdl|res://*/TaskManagerModel.ssdl|res://*/TaskManagerModel.msl;provider=System.Data.SqlClient;provider connection string=&quot;data source=.\SQLEXPRESS;initial catalog=TaskManagerDB;integrated security=True;MultipleActiveResultSets=True;App=EntityFramework&quot;" 
         providerName="System.Data.EntityClient" />
</connectionStrings>

📁 Структура проекта

TaskManager/
├── TaskManager.sln                    # Файл решения
├── TaskManager/                        # Основной проект
│   ├── App.xaml                        # Точка входа приложения
│   ├── MainWindow.xaml                  # Главное окно
│   ├── Views/                           # Окна и пользовательские контролы
│   │   ├── TaskEditWindow.xaml          # Окно редактирования задачи
│   │   └── AboutWindow.xaml              # Окно "О программе"
│   ├── ViewModels/                       # ViewModel (MVVM)
│   │   ├── MainViewModel.cs
│   │   └── TaskViewModel.cs
│   ├── Models/                            # Модели данных
│   │   └── Task.cs
│   ├── Data/                               # Работа с БД
│   │   ├── TaskManagerContext.cs           # Контекст БД (EF)
│   │   └── TaskRepository.cs               # Репозиторий
│   ├── Converters/                          # Конвертеры для XAML
│   │   ├── BooleanToVisibilityConverter.cs
│   │   └── PriorityToColorConverter.cs
│   └── Helpers/                             # Вспомогательные классы
│       └── DatabaseHelper.cs
└── README.md                                # Этот файл

🗺 Планы развития

-Добавить напоминания о задачах
=Реализовать экспорт задач в Excel/PDF
=Добавить возможность создания подзадач
=Интеграция с календарем Outlook
=Темная тема интерфейса
=Синхронизация с облачными сервисами
=Мобильная версия приложения

👩‍💻 Автор

Анискина Ольга Алексеевна
Студентка группы ИСП291
ГБПОУ КАИТ №20, отделение «ДатаХаб»

  📧 Email: anisamalix@gmail.com
  💼 GitHub: @anisamalix

📄 Лицензия
Проект разработан в образовательных целях в рамках учебной практики. Все права защищены.

🙏 Благодарности
Преподавателю Аферову А.А. за руководство и ценные советы
Колледжу ГБПОУ КАИТ №20 за предоставленную материально-техническую базу
Отделению «ДатаХаб» за современную среду для разработки

Разработано в 2026 году в рамках учебной практики ПМ 01 "Разработка модулей программного обеспечения для компьютерных систем"






