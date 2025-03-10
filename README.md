# Предупреждение
OfflineChronicle создан для работы на 127.0.0.1, автор отказывается от любой ответственности за понесённый ущерб в случае открытия доступа к блогу через Интернет.

# Порядок установки

## Debian
1. Установите python3: ```apt install python3```
2. Создайте виртуальное окружение: ``python3 -m venv ~/venv``
3. Выберите виртуальное окружение: ``source ~/venv/bin/activate``
4. Скачайте zip-архив с OfflineChronicle: https://github.com/b15eecdd-94d1-493a-af46-d07a236a767a/OfflineChronicle/archive/refs/heads/main.zip
5. Распакуйте в любой каталог.
6. Выберите каталог в котором находится OfflineChronicle.
7. Скачайте зависимости: ``` pip install -r requirements.txt ```
8. Запускайте любой скрипт командой python3.
   
## Windows
1. Скачайте python3 с официального сайта.
2. Запустите установщик.
3. Обязательно выберите опцию "Add Python to PATH" (Добавление пайтон в PATH, для использования языка через командную строку).
4. Завершите установку.
5. Скачайте zip-архив с OfflineChronicle: https://github.com/b15eecdd-94d1-493a-af46-d07a236a767a/OfflineChronicle/archive/refs/heads/main.zip
6. Распакуйте в любой каталог.
7. Откройте консоль и выберите каталог в котором находится OfflineChronicle.
8. Скачайте зависимости: ```pip install -r requirements.txt```
9. Запускайте любой скрипт командой python.

# Команды
### Получить список записей
```
usage: python3 list.py [-h] [-n NAME] [-l LIMIT] [-p PAGE] [-s {DESC,ASC}] [-sep SEPARATOR] [-lb LEFT_BORDER] [-g {Y,N}] [-w WIDTH] [-tz TIMEZONE] [-hi {Y,N}] [-htz {Y,N}]

options:
  -h, --help            show this help message and exit
  -n NAME, --name NAME  Название блога (default: blog)
  -l LIMIT, --limit LIMIT
                        Максимальное количество записей (default: 50)
  -p PAGE, --page PAGE  Номер страницы (default: -1)
  -s {DESC,ASC}, --sort {DESC,ASC}
                        Сортировка (default: ASC)
  -sep SEPARATOR, --separator SEPARATOR
                        Разделитель между постами (default: ----------------------------------------)
  -lb LEFT_BORDER, --left-border LEFT_BORDER
                        Граница слева (default: |)
  -g {Y,N}, --graphics {Y,N}
                        ASCII-графика (default: Y)
  -w WIDTH, --width WIDTH
                        Максимальная ширина строки (default: 40)
  -tz TIMEZONE, --timezone TIMEZONE
                        Часовой пояс (local - локальный часовой пояс) (default: local)
  -hi {Y,N}, --hide-id {Y,N}
                        Скрыть ID? (default: N)
  -htz {Y,N}, --hide-timezone {Y,N}
                        Скрыть часовой пояс? (default: N)
```

### Добавить запись в блог.
```
usage: python3 add.py [-h] [-n NAME]

options:
  -h, --help            show this help message and exit
  -n NAME, --name NAME  Название блога (default: blog)
```

### Удалить запись по id.
```
usage: python3 delete.py [-h] [-n NAME] [-sd {Y,N}]

options:
  -h, --help            show this help message and exit
  -n NAME, --name NAME  Название блога (default: blog)
  -sd {Y,N}, --soft-deletion {Y,N}
                        Мягкое удаление (default: N)
```

### Получить запись по id.
```
usage: python3 get_by_id.py [-h] [-n NAME] [-sep SEPARATOR] [-lb LEFT_BORDER] [-g {Y,N}] [-w WIDTH] [-tz TIMEZONE] [-hi {Y,N}] [-htz {Y,N}]

options:
  -h, --help            show this help message and exit
  -n NAME, --name NAME  Название блога (default: blog)
  -sep SEPARATOR, --separator SEPARATOR
                        Разделитель между постами (default: ----------------------------------------)
  -lb LEFT_BORDER, --left-border LEFT_BORDER
                        Граница слева (default: |)
  -g {Y,N}, --graphics {Y,N}
                        ASCII-графика (default: Y)
  -w WIDTH, --width WIDTH
                        Максимальная ширина строки (default: 40)
  -tz TIMEZONE, --timezone TIMEZONE
                        Часовой пояс (local - локальный часовой пояс) (default: local)
  -hi {Y,N}, --hide-id {Y,N}
                        Скрыть ID? (default: N)
  -htz {Y,N}, --hide-timezone {Y,N}
                        Скрыть часовой пояс? (default: N)

```

### Поиск
```
usage: python3 search.py [-h] [-n NAME] [-s {DESC,ASC}] [-sep SEPARATOR] [-lb LEFT_BORDER] [-g {Y,N}] [-w WIDTH] [-tz TIMEZONE] [-hi {Y,N}] [-htz {Y,N}]

options:
  -h, --help            show this help message and exit
  -n NAME, --name NAME  Название блога (default: blog)
  -s {DESC,ASC}, --sort {DESC,ASC}
                        Сортировка (default: DESC)
  -sep SEPARATOR, --separator SEPARATOR
                        Разделитель между постами (default: ----------------------------------------)
  -lb LEFT_BORDER, --left-border LEFT_BORDER
                        Граница слева (default: |)
  -g {Y,N}, --graphics {Y,N}
                        ASCII-графика (default: Y)
  -w WIDTH, --width WIDTH
                        Максимальная ширина строки (default: 40)
  -tz TIMEZONE, --timezone TIMEZONE
                        Часовой пояс (local - локальный часовой пояс) (default: local)
  -hi {Y,N}, --hide-id {Y,N}
                        Скрыть ID? (default: N)
  -htz {Y,N}, --hide-timezone {Y,N}
                        Скрыть часовой пояс? (default: N)

```

### Лог
```
usage: python3 get_all_log_records.py [-h] [-n NAME] [-tz TIMEZONE]
                                      [-sep SEPARATOR] [-s {DESC,ASC}]

options:
  -h, --help            show this help message and exit
  -n NAME, --name NAME  Название блога (default: blog)
  -tz TIMEZONE, --timezone TIMEZONE
                        Часовой пояс (local - локальный часовой пояс) (default:
                        local)
  -sep SEPARATOR, --separator SEPARATOR
                        Разделитель между постами (default:
                        ----------------------------------------)
  -s {DESC,ASC}, --sort {DESC,ASC}
                        Сортировка (default: ASC)
```
### Экспорт постов из базы данных в формат txt или json
```
usage: python3 export.py [-h] [-n NAME] [-l LIMIT] [-s {DESC,ASC}] [-tz TIMEZONE] [-f {txt,json}] [-p PATH] [-f2 {Y,N}] [-hi {Y,N}] [-htz {Y,N}]

options:
  -h, --help            show this help message and exit
  -n NAME, --name NAME  Название блога (default: blog)
  -l LIMIT, --limit LIMIT
                        Максимальное количество записей в одном файле (default: unlimited)
  -s {DESC,ASC}, --sort {DESC,ASC}
                        Сортировка (default: ASC)
  -tz TIMEZONE, --timezone TIMEZONE
                        Часовой пояс (local - локальный часовой пояс) (default: local)
  -f {txt,json}, --format {txt,json}
                        Формат (default: txt)
  -p PATH, --path PATH  Куда сохранять? (default: export)
  -f2 {Y,N}, --force {Y,N}
                        Перезаписывать существующий файл? (default: N)
  -hi {Y,N}, --hide-id {Y,N}
                        Скрыть ID в .txt? (default: Y)
  -htz {Y,N}, --hide-timezone {Y,N}
                        Скрыть часовой пояс в .txt? (default: Y)
```

### HTTP-сервер.
Не изменяйте значение параметра host! Вы так можете открыть доступ к HTTP-серверу через Интернет!
```
usage: python3 server.py [-h] [-n BLOGNAME] [-tz TIMEZONE] [-l LIMIT]
                         [-s {DESC,ASC}] [-d {1,2,3,4,5,custom}] [-p PORT]
                         [-ro {Y,N}] [-h2 HOST] [-lh {Y,N}] [-ai ADMIN_IP]
                         [-l2 {Y,N}]

options:
  -h, --help            show this help message and exit
  -n BLOGNAME, --blogname BLOGNAME
                        Название блога (default: blog)
  -tz TIMEZONE, --timezone TIMEZONE
                        Часовой пояс (local - локальный часовой пояс) (default:
                        local)
  -l LIMIT, --limit LIMIT
                        Максимальное количество постов на одной странице
                        (default: 50)
  -s {DESC,ASC}, --sort {DESC,ASC}
                        Сортировка (default: DESC)
  -d {1,2,3,4,5,custom}, --design {1,2,3,4,5,custom}
                        Дизайн (default: 1)
  -p PORT, --port PORT  Порт (default: 5050)
  -ro {Y,N}, --readonly {Y,N}
                        Режим без возможности управлять записями (default: N)
  -h2 HOST, --host HOST
                        Хост (default: 127.0.0.1)
  -lh {Y,N}, --localhost {Y,N}
                        Запретить доступ из внешней сети (default: Y)
  -ai ADMIN_IP, --admin-ip ADMIN_IP
                        IP-адрес администратора (допустимо перечислять через
                        пробел) (default: 127.0.0.1)
  -l2 {Y,N}, --log {Y,N}
                        Выводить лог в консоль (default: Y)
```

### GUI
```
usage: python3 gui.py [-h] [-n BLOGNAME] [-tz TIMEZONE] [-l LIMIT]
                      [-s {DESC,ASC}]

options:
  -h, --help            show this help message and exit
  -n BLOGNAME, --blogname BLOGNAME
                        Название блога (default: blog)
  -tz TIMEZONE, --timezone TIMEZONE
                        Часовой пояс (local - локальный часовой пояс) (default:
                        local)
  -l LIMIT, --limit LIMIT
                        Максимальное количество постов на одной странице
                        (default: 50)
  -s {DESC,ASC}, --sort {DESC,ASC}
                        Сортировка (default: DESC)
```
