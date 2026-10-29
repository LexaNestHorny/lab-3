CustomerFeedbackApp — лабораторна №3, варіант 7
.NET MAUI (net8.0-android), MVVM, Shell, CommunityToolkit.Mvvm, sqlite-net-pcl.
Можливості
Додавання, перегляд, редагування та видалення відгуків клієнтів.
Дані постійно зберігаються в SQLite (`FileSystem.AppDataDirectory/feedbacks.db3`).
Асинхронний `DatabaseService`: `GetAllAsync`, `GetByIdAsync`, `InsertAsync`, `UpdateAsync`, `DeleteAsync`.
`DatabaseService` зареєстровано як Singleton в DI; ViewModel не виконує SQL напряму.
Другий екран через Shell із параметром `id`; чернетка зберігається через Preferences.
Запуск
Відкрийте `CustomerFeedbackApp.csproj` у Visual Studio 2022 з .NET MAUI workload, відновіть NuGet, виберіть Android Emulator і натисніть F5.
Перевірка
Додайте відгук; натисніть картку та змініть текст/оцінку, натисніть «Зберегти зміни».
Повністю завершіть застосунок та запустіть знову: відгук має залишитися.
Відкрийте відгук та натисніть «Видалити відгук»; переконайтеся, що він зник зі списку.
Зверніть увагу: записи з лабораторної №2 зберігалися лише в оперативній пам'яті та автоматично не мігрують у SQLite. У цьому проєкті база створюється при першому запуску.
