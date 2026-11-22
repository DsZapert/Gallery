# Галерея

Форк [Gallery Go](https://github.com/googol-apps/Gallery) (версия 1.1.0-foss) — быстрой галереи для Android на Jetpack Compose.

Package ID: `ru.galereya.photos` — ставится рядом с оригиналом.

## Отличия от оригинала

- Нет Firebase, Google Play Services, встроенных покупок и рекламных SDK — осталась только FOSS-сборка.
- Нет всплывающих сообщений автора: «Что нового», реклама плеера, призыв поставить версию из Play Store, просьба поддержать, запрос отзыва.
- Убраны кнопки «Оценить», «Поддержать проект», ссылки на Telegram, GitHub, Crowdin и политику конфиденциальности автора.
- Нижняя панель навигации и кнопка камеры выровнены по центру.
- Только русский язык: прочие переводы и выбор языка удалены.
- Две темы: AMOLED (чисто чёрная, по умолчанию) и белая.
- Стандартная иконка Material «Image» вместо фирменной.

## Сборка

Нужны JDK 17 и Android SDK (compileSdk 37).

```bash
./gradlew assembleCommunityRelease
```

APK появится в `app/build/outputs/apk/community/release/`. Release-сборка подписана debug-ключом, чтобы её можно было сразу установить; для публикации подключите свой keystore в `app/build.gradle.kts`.

Проще всего — залить репозиторий на GitHub: workflow `.github/workflows/build.yml` соберёт APK и выложит его в Actions → Artifacts.

## Лицензия

Apache License 2.0, см. [LICENSE](LICENSE). Оригинальный код © Zakir Sheikh / Googol Apps; изменения форка перечислены выше.
