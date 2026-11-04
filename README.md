# 🚀 Flutter Projects Collection

Привет, разработчик! Добро пожаловать в коллекцию Flutter-проектов, где живут фронты, бэки, Docker и вся красота DevOps'а.

---

## 📑 Оглавление проектов

| Проект | Описание | Папка | Flutter-приложение |
| --- | --- | --- | --- |
| [Spring Hack 2026](#spring-hack-2026) | Приложение для весеннего хакатона | [dgtu-hack-spring-2025](./dgtu-hack-spring-2025) | `dgtu-hack-spring-2025/entry_point` |
| [HangmanGame — Виселица](#hangmangame) | Игра на угадывание слов | [HangmanGame](./HangmanGame) | `HangmanGame` |
| [CyberTest](#cybertest) | Приложение для тестирования студентов | [testing](./testing) | `testing/cybertest` |
| [MMM — Monthly Money Metrics](#mmm) | Учёт личных финансов | [MMM](./MMM) | `MMM` |
| [SkyTime — мониторинг растительности](#skytime) | Анализ спутниковых временных рядов NDVI | [kosmohack-2026](./kosmohack-2026) | `kosmohack-2026/frontend` |
| [BugHunt — тренажёр поиска багов](#bughunt) | Практика поиска дефектов для QA | [bughunt](./bughunt) | `bughunt/frontend` |

## 📂 Что тут внутри

### Spring Hack 2026

[Репозиторий](https://github.com/DanielE330/spring-hack-2026) · Папка: `dgtu-hack-spring-2025/`.

Приложение для весеннего хакатона: Django REST API в `backend/`, Flutter-фронтенд в `entry_point/` и документация в `docs/`.
Существующее имя папки сохранено.

### HangmanGame

[Репозиторий](https://github.com/DanielE330/HangmanGame) · Папка: `HangmanGame/`.

Классическая «Виселица» — игра на угадывание слов на Flutter. Приложение находится в корне проекта.

### CyberTest

[Репозиторий](https://github.com/DanielE330/cybertest) · Папка: `testing/`.

Приложение для тестирования студентов с Flutter-клиентом в `cybertest/` и FastAPI-бэкендом в `backend/`.
Репозиторий ранее назывался `test-online`; существующие путь `testing/` и URL submodule сохранены.

### MMM

[Репозиторий](https://github.com/DanielE330/MMM) · Папка: `MMM/`.

Monthly Money Metrics — учебное приложение для отслеживания личных доходов, расходов и планирования бюджета. Flutter-приложение находится в корне проекта.

### SkyTime

[Репозиторий](https://github.com/DanielE330/kosmohack-2026) · Папка: `kosmohack-2026/`.

Проект «КОСМОХАКАТОНА» 2026 для мониторинга растительности сельскохозяйственных полигонов по спутниковым временным рядам NDVI: восстановление пропусков и обнаружение аномалий.
Flutter-клиент находится в `frontend/`, FastAPI-бэкенд с PostgreSQL — в `backend/`, модели обработки данных — в `ml/`.

### BugHunt

[Репозиторий](https://github.com/DanielE330/bughunt) · Папка: `bughunt/`.

Тренажёр для практики поиска багов: сценарии с наблюдениями, десять уровней трёх сложностей, очки и таблица лидеров.
Flutter Web-клиент находится в `frontend/`, FastAPI-бэкенд с SQLite — в `backend/`. Для запуска полного стека предусмотрен Docker Compose.

---

## 🏃 Быстрый старт

### Получить проекты

При первом клонировании загрузите submodule вместе с коллекцией:

```bash
git clone --recurse-submodules https://github.com/DanielE330/flutter-projects.git
cd flutter-projects
```

Если коллекция уже клонирована, выполните из её корня:

```bash
git submodule update --init --recursive
```

Пути к Flutter-приложениям всех шести проектов указаны в оглавлении. Настройки бэкенда и переменных окружения смотрите в README соответствующего проекта.

### Для Flutter проекта (например, HangmanGame или MMM)
```bash
cd HangmanGame
flutter pub get
flutter run
```

### Для полного стека (dgtu-hack-spring-2025)

**Вариант 1: Бэкенд + Фронт локально**
```bash
# Бэкенд (с Docker)
cd dgtu-hack-spring-2025/backend
docker-compose up --build

# В другом терминале — Фронт
cd dgtu-hack-spring-2025/entry_point
flutter pub get
flutter run
```

**Вариант 2: Просто запустить фронт**
```bash
cd dgtu-hack-spring-2025/entry_point
flutter pub get
flutter run
```

---

## 📖 Структура типовой папки Flutter проекта

```
project/
├── lib/              # Главный Dart код (бизнес-логика, UI)
├── test/             # Юнит и виджет тесты
├── android/          # Native Android код (Gradle, manifest)
├── ios/              # Native iOS код (Xcode)
├── web/              # Веб версия (HTML, JS)
├── windows/          # Desktop Windows
├── linux/            # Desktop Linux
├── macos/            # Desktop macOS
├── pubspec.yaml      # Конфиг проекта + зависимости
└── analysis_options.yaml  # Lint правила
```

---

## 🛠 Полезные команды

### Анализ кода
```bash
flutter analyze           # Проверка синтаксиса и стиля
flutter pub outdated     # Какие пакеты устарели
```

### Тестирование
```bash
flutter test             # Запуск всех тестов
flutter test --coverage  # С coverage
```

### Очистка и переблиб
```bash
flutter clean            # Удалить сборку
flutter pub get          # Переустановить пакеты
```

### Форматирование
```bash
dart format lib/         # Форматирование кода
```

### Сборка
```bash
flutter build apk        # APK для Android
flutter build ios        # iOS (нужен Mac)
flutter build web        # Веб версия
flutter build windows    # Exe для Windows
```

---

## 🔑 Как контрибьютить

1. **Создать ветку** от main в style: `feature/описание` или `fix/описание`
2. **Писать чистый код:**
   - `flutter analyze` должна молчать
   - `flutter test` должны пройти все тесты
   - Коммиты с понятными сообщениями
3. **Коммит чек-лист:**
   - ✅ Код работает локально
   - ✅ Тесты написаны/обновлены
   - ✅ Нет debug prints и console.log
   - ✅ Сообщение коммита понятно
4. **Pull Request** с описанием что поменялось

---

## 📚 Документация

- **`docs/ARCHITECTURE.md`** (в dgtu-hack-spring-2025) — как всё устроено
- **`docs/DEPLOYMENT.md`** — как запустить в production
- **`docs/API.md`** — endpoints и их поведение
- **`QUICKSTART.md`** — быстрый старт в каждом проекте
- **`SECURITY.md`** — что нельзя делать в коде

---

## ⚡ Горячие клавиши (в flutter run)

```
r       — Hot reload (быстро перезагрузить кода без потери состояния)
R       — Hot restart (полная перезагрузка приложения)
d       — Отключить debug prints
h       — Помощь
q       — Выход
```

---

## 🐛 Когда что-то не работает

1. **Очки:**
   ```bash
   flutter clean
   flutter pub get
   flutter run
   ```

2. **Проверить версии:**
   ```bash
   flutter --version
   dart --version
   ```

3. **Погугль ошибку** в `docs/` или GitHub Issues

4. **Если совсем беда:** `rm -rf ~/flutter` и переинсталлируй Flutter (последний вариант)

---

## 🎯 Основные правила (но серьезно)

| Что | Нельзя | Можно |
|-----|--------|-------|
| Debug prints | `print('debug');` везде | Удалить перед PR, или использовать log package |
| Api ключи | Коммитить в код | `.env` файл или secure storage |
| Magic numbers | `if (x > 42)` без комментария | `const int MAGIC_VALUE = 42;` + комментарий |
| Async | `await` в UI build | Использовать `FutureBuilder` или `StreamBuilder` |

---

## 🚢 Деплой

Информация по деплою в каждом проекте:
- **dgtu-hack-spring-2025:** смотри `docs/DEPLOYMENT.md`
- **HangmanGame:** можно собратье APK/IPA вручную через `flutter build`
- **Cybertest:** см. `SETUP_AUTH.md`


**Happy Coding! 🎉**  
И помни: `if (bugs == expected_behavior) { celebrate(); }`
