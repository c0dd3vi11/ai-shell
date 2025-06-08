# `ai-shell` с `GigaChat`

### Установка (из исходников):
```sh
# Должен быть установлен npm (пример для MacOS)
brew install node

# Клонируем для локальной сборки и установки
git clone 'https://github.com/c0dd3vi11/ai-shell.git' "$HOME/ai-shell.git"

# Собираем и устанавливаем
cd "$HOME/ai-shell.git"
npm install
npm run build
npm link
```

### Настройка:
```sh
# Настройка, можно интерактивно через "ai config", а можно командами:
ai config set AI_ENGINE=GigaChat
ai config set GIGACHAT_KEY='<your-giga-chat-key>'
```

Получить ключ (см. справа кнопку "Подключить GigaChat API"):
- https://developers.sber.ru/docs/ru/gigachat/individuals-quickstart

### Примеры команд
Просто запускай и смотри что чат предлагает:
```sh
# Подбор команды
ai my external ip
ai погода в Москве
ai git drop commit with hash1
ai git move commit hash1 before hash2
ai заменить в файле myfile.txt строку Platform на строку Engine

# Просто чат
ai chat
```

## Как выглядит?

Пример:
```sh
> ai my external ip
┌  Ваш скрипт:
| curl ipinfo.io/ip
|
◇  Объяснение:
| - Запустите команду
| - Получите IPv4-адрес через сервис
|
◇  Запустить этот скрипт?
│  ✅ Да
| 
└  Запуск: curl ipinfo.io/ip
12.34.56.78
```

## Дополнительно

Язык:
```sh
# Переключить на русский язык (ИИ тоже будет это учитывать)
ai config set LANGUAGE=ru
```

Выбор модели:
```sh
# Быстрая и легкая модель для простых повседневных задач (по-умолчанию)
ai config set GIGACHAT_MODEL=GigaChat-2

# Усовершенствованная модель для ресурсоемких задач, обеспечивающая максимальную эффективность в обработке данных, креативности и соблюдении инструкций
ai config set GIGACHAT_MODEL=GigaChat-2-Pro

# Мощная модель для самых сложных и масштабных задач, требующих высочайшего уровня креативности и качества исполнения
ai config set GIGACHAT_MODEL=GigaChat-2-Max
```
