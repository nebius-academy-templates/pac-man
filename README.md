# PyPacman

Клон Pacman, написанный на Python с Pygame.

## Требования

- Python 3.8 или выше
- pip (менеджер пакетов Python)

## Установка

1. Клонируйте репозиторий:

```bash
git clone <repository-url>
cd PyPacman
```

2. Создайте и активируйте виртуальное окружение:

```bash
python3 -m venv .venv
source .venv/bin/activate       # macOS / Linux
.venv\Scripts\activate          # Windows
```

3. Установите зависимости:

```bash
pip install -r requirements.txt
```

## Запуск игры

```bash
python3 main.py
```

Откроется игровое окно 1024×768.

## Управление

- **Arrow Up** - движение вверх
- **Arrow Down** - движение вниз
- **Arrow Left** - движение влево
- **Arrow Right** - движение вправо

## Геймплей

- Съешьте все точки на карте, чтобы завершить уровень.
- Собирайте power pellets, чтобы временно напугать ghosts (их можно съесть и получить бонусные очки, пока они напуганы).
- Пять ghosts (Blinky, Pinky, Inky, Clyde и Blue) преследуют Pacman, используя разные стратегии поиска цели.
- Ghosts переключаются между режимами scatter и chase на протяжении уровня.
- Game over отсутствует. После прохождения уровень перезапускается, а лучший результат сохраняется между игровыми сессиями.

## Структура проекта

```
PyPacman/
├── main.py                  # Entry point
├── requirements.txt         # Python dependencies
├── levels/
│   ├── level1.json          # Level layout
│   └── stats.json           # Persisted high score
├── assets/                  # Sprites and sounds
└── src/
    ├── configs.py           # Game constants
    ├── runner.py            # Main game loop
    ├── sounds.py            # Sound manager
    ├── game/                # Event and state management
    ├── gui/                 # Screen rendering
    ├── sprites/             # Pacman and ghost sprites
    └── utils/               # Movement, drawing, and graph utilities
```

## Лицензия

GPLv3 - подробности смотрите в [LICENSE](LICENSE).
