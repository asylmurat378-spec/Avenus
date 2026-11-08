# AVENRO ROLEPLAY Launcher
Сборка: откройте папку в Android Studio (Koala+, JDK 17), Sync, Run. Или: `gradle wrapper && ./gradlew assembleDebug`.
Слои: data/ (модели, Retrofit AvenroApi, репозитории, демо-реализации, GameLauncher, UpdateChecker, Settings), ui/ (тема, экраны, ViewModel).
Ссылки и лимиты — data/Data.kt -> AppConfig.
Подключение backend: замените Demo*Repository на реализации поверх AvenroApi (Retrofit.Builder + GsonConverterFactory, baseUrl = AppConfig.API_BASE_URL).
Подключение CRMP: реализуйте GameLauncher (isClientInstalled / verifyFiles / launch) и подставьте в ServiceLocator.
Фоны/скины: положите URL в Server.imageUrl / Character.imageUrl (Coil) или добавьте drawable.
