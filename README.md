# fastfetch-config

## Fastfetch конфигурация
Я использую `fastfetch` для вывода системной информации при открытии терминала. [`Мой конфиг`](https://github.com/kabanbtw/fastfetch-config/blob/main/config.json) настроен для отображения информации об ОС, окружении GNOME и оборудовании в минималистичном стиле. Я не претендую на оригинальность, на просторах сети эти конфиги встречаются часто и все +- похожи друг на друга.

### Скриншот
![Fastfetch Output](https://cdn.discordapp.com/attachments/1420790405242556522/1421010110301470760/Screenshot_From_2025-09-26_10-41-58_Edit.png?ex=68d77a4b&is=68d628cb&hm=acaa422800e14c2e579945befa37621404e6e0f6c2688977f60b35a7a476508d&)

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
   - **Предупреждение**: Использование **zsh** может привести к ошибкам форматирования в `.zshrc`, которые портят внешний вид терминала. Fish более надёжен для этой задачи. Однако сам вывод fastfetch без автоматического вывода при открытии терминала может быть реализован на любой оболочке.

### Конфигурация
Файл конфигурации находится в [`fastfetch/config.jsonc`](https://github.com/kabanbtw/fastfetch-config/blob/main/config.json). Он включает:
- Секции: System Information, Desktop Environment, Hardware Information.
- Кастомные разделители и цветные заголовки.
- Поддержку emoji для визуальной читаемости.

## Связь
Если хотите обсудить проекты или предложить улучшения, пишите:
- **Email**: epidermis_essential@proton.me
- **Discord**: https://discord.gg/QYRXFdRS

## Лицензии



[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)
