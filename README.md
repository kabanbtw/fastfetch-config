# fastfetch-config

## Fastfetch конфигурация
Я использую `fastfetch` для вывода системной информации при открытии терминала. Мой конфиг (`fastfetch/config.jsonc`) настроен для отображения информации об ОС, окружении GNOME и оборудовании в минималистичном стиле.

### Скриншот
![Fastfetch Output](https://media.discordapp.net/attachments/1420790405242556522/1421000538828570745/image.png?ex=68d77161&is=68d61fe1&hm=b0ef89be32064ed8f57a0235893e919106d16d77f8d469db232c3cfb056aa953&=&format=webp&quality=lossless)

### Настройка fastfetch
1. Установите `fastfetch`:
   ```bash
   sudo pacman -S fastfetch
   ```
2. Скопируйте конфиг в `~/.config/fastfetch/`:
   ```bash
   mkdir -p ~/.config/fastfetch
   cp fastfetch/config.jsonc ~/.config/fastfetch/
   ```
3. Для автоматического запуска `fastfetch` при открытии терминала:
   - **Рекомендация**: Используйте **fish** как shell, так как он проще настраивается и не вызывает ошибок форматирования вывода. Добавьте в `~/.config/fish/config.fish`:
     ```fish
     if status is-interactive
         fastfetch
     end
     ```
   - **Предупреждение**: Использование **zsh** может привести к ошибкам форматирования в `.zshrc`, которые портят внешний вид терминала. Fish более надёжен для этой задачи.

### Конфигурация
Файл конфигурации находится в [`fastfetch/config.jsonc`](https://github.com/kabanbtw/fastfetch-config/blob/main/config.json). Он включает:
- Секции: System Information, Desktop Environment, Hardware Information.
- Кастомные разделители и цветные заголовки.
- Поддержку emoji для визуальной читаемости.

## Статистика
[![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=kabanbtw&layout=compact)](https://github.com/anuraghazra/github-readme-stats)

## Связь
Если хотите обсудить проекты или предложить улучшения, пишите:
- **Email**: epidermis_essential@proton.me
- **Discord**: https://discord.gg/QYRXFdRS

## Лицензия
MIT License
