# 🚀 Flutter Projects Collection

Привет, разработчик! Добро пожаловать в коллекцию Flutter-проектов, где живут фронты, бэки, Docker и вся красота DevOps'а.

---

## 📂 Что тут внутри

### 1. **`dgtu-hack-spring-2025/`** — Main Event  
Полнофункциональное приложение с full-stack подходом:
- **`backend/`** — Django REST API с auth, логикой и всеми красивостями
- **`entry_point/`** — Flutter фронтенд (iOS, Android, Web, десктоп)
- **`docs/`** — полная документация (архитектура, деплой, API)

### 2. **`HangmanGame/`** — Классическая Виселица  
Простой, но полнофункциональный Flutter проект. Идеален для:
- Быстрого запуска ("ты сможешь, даже если Flutter в первый раз")
- Тестирования на разных платформах
- Примера структуры Flutter app

### 3. **`testing/`** — Приложение для тестирование студентов 
Экспериментальные проекты:
- **`backend/`** — вспомогательный сервер для интеграционных тестов
- **`cybertest/`** — Flutter app для каких-то специальных тестов/обучения

### 4. **`MMM/`** — Monthly Money Metrics 💰
Учебное приложение для отслеживания личных доходов/расходов и планирования бюджета.

---

## 🏃 Быстрый старт

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
