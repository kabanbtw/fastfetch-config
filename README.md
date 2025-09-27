
# Fastfetch Beauty Config

A custom configuration for `fastfetch`, a tool to display system information in the terminal upon opening. [My config](https://github.com/kabanbtw/fastfetch-config/blob/main/config.json) is designed to show OS, desktop environment, and hardware details in a minimalist style. This setup is not unique—similar configs are common online and share many similarities.

## Screenshot
![Fastfetch Output](https://media.discordapp.net/attachments/1420800072282804227/1421053928283570259/Screenshot_From_2025-09-26_10-41-58_Edit.png?ex=68d7a31a&is=68d6519a&hm=d272b3be28bd106b5e5044125b85b31e56b17e7b2b564395e15f21672edcbc12&=&format=webp&quality=lossless)

## Setting Up Fastfetch

1. Install `fastfetch`:
   ```bash
   sudo pacman -S fastfetch
   ```

2. Copy the config to `~/.config/fastfetch/`:
   ```bash
   mkdir -p ~/.config/fastfetch
   cp config.jsonc ~/.config/fastfetch/
   ```

3. To run `fastfetch` automatically when opening the terminal:
   - **Recommended**: Use the **Fish** shell for easier setup and consistent formatting. Add to `~/.config/fish/config.fish`:
     ```fish
     if status is-interactive
         fastfetch
     end
     ```
   - **Note**: Adding fastfetch to ~/.zshrc may cause formatting issues, which can disrupt terminal appearance. While fastfetch output works correctly in any shell (Zsh, Bash, Fish, etc.), Fish provides a more consistent experience for automatic startup.

## Configuration

The configuration file is available [Here](https://github.com/kabanbtw/fastfetch-config/blob/main/config.json). It includes:
- Sections: System Information, Desktop Environment, Hardware Information.
- Custom separators and colored headers.
- Emoji support for better visual readability.

## Contact

For discussions or suggestions, reach out:
- **Email**: epidermis_essential@proton.me
- **Discord**: https://discord.gg/2bFvWXRS6u

## License

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)
