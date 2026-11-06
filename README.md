# Arduino Manager GUI

Кроссплатформенный менеджер библиотек и плат Arduino на Go + Fyne
с автоматической публикацией бинарников через GitHub Actions.

![Version](https://img.shields.io/badge/version-1.0.0-blue)
![Go](https://img.shields.io/badge/Go-1.22-00ADD8?logo=go)
![Fyne](https://img.shields.io/badge/Fyne-2.8.0-76549A)

## 📸 Скриншоты приложения

### Главное окно
![Главное окно](screenshots/01-main-window.png)

### Поиск библиотек
![Поиск](screenshots/02-search.png)

### Режим плат
![Платы](screenshots/03-boards.png)

## 🚀 Возможности

- Поиск библиотек Arduino на GitHub и в локальном индексе
- Поиск и установка ядер плат (ESP32, ESP8266, STM32, AVR и др.)
- Управление установленными библиотеками и платами
- Отмена длительных операций (Esc)
- Горячие клавиши (Ctrl+F, Ctrl+1/2/3, Ctrl+R, Ctrl+K)

## 🛠 Этапы разработки

### Этап 1. Инициализация проекта
- Создан Go-модуль `github.com/.../arduino-manager-gui`
- Подключена Fyne v2.8.0
- Написан `main.go` с GUI и логикой менеджера

### Этап 2. Настройка CI/CD
- Создан `.github/workflows/release.yml`
- Настроена матрица сборок: Linux / Windows / macOS
- Добавлена установка системных зависимостей Fyne

![Workflow](screenshots/04-actions-workflow.png)

### Этап 3. Публикация релиза
- Создан тег `v1.0.0`
- GitHub Actions собрал 3 бинарника
- Артефакты опубликованы в GitHub Releases

![Release](screenshots/05-release-page.png)

## 📦 Установка

### Из готовых бинарников
Скачать архив для вашей ОС со страницы [Releases](../../releases).

### Сборка из исходников
```bash
git clone https://github.com/<логин>/arduino-manager-gui.git
cd arduino-manager-gui
go build -o arduino-manager .
./arduino-manager