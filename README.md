# OpenCCK Clash Rules

[Русская версия](README_RU.md) | English

This project generates rules for [Clash Premium](https://github.com/Dreamacro/clash/releases/tag/premium) based on domain lists from [OpenCCK](https://iplist.opencck.org/). Automatic builds occur daily at 21:00 UTC using GitHub Actions.

## Available Rule Lists

### Online Addresses (URL)

Use these URLs in your Clash configuration in the `rule-providers` section:

- **Art Content Sites (art.txt)**:
  - `https://raw.githubusercontent.com/DimaBroZY/ClashURLS/release/art.txt`
  - `https://cdn.jsdelivr.net/gh/DimaBroZY/ClashURLS@release/art.txt`

- **Anime Content Sites (art.txt)**:
  - `https://raw.githubusercontent.com/DimaBroZY/ClashURLS/release/anime.txt`
  - `https://cdn.jsdelivr.net/gh/DimaBroZY/ClashURLS@release/anime.txt`
 
- **Minecraft Content Sites (art.txt)**:
  - `https://raw.githubusercontent.com/DimaBroZY/ClashURLS/release/minecraft.txt`
  - `https://cdn.jsdelivr.net/gh/DimaBroZY/ClashURLS@release/minecraft.txt`

 - **Games Content Sites (games.txt)**:
  - `https://raw.githubusercontent.com/DimaBroZY/ClashURLS/release/games.txt`
  - `https://cdn.jsdelivr.net/gh/DimaBroZY/ClashURLS@release/games.txt`

## Usage

### Rule Providers Configuration

```yaml
rule-providers:
    
  minecraft:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/DimaBroZY/ClashURLS@release/minecraft.txt"
    path: ./ruleset/minecraft.yaml
    interval: 86400
  games:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/DimaBroZY/ClashURLS@release/games.txt"
    path: ./ruleset/games.yaml
    interval: 86400
  anime:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/DimaBroZY/ClashURLS@release/anime.txt"
    path: ./ruleset/anime.yaml
    interval: 86400
  art:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/DimaBroZY/ClashURLS@release/art.txt"
    path: ./ruleset/art.yaml
    interval: 86400
```


## Data Sources

All rules are generated based on domain lists from [OpenCCK](https://iplist.opencck.org/):

- Anime Content: https://iplist.opencck.org/?format=text&data=domains&group=anime
- Art: https://iplist.opencck.org/?format=text&data=domains&group=art
- Games: https://iplist.opencck.org/?format=text&data=domains&group=games

## Installation

1. Create a new repository on GitHub
2. Copy files from this project
3. Replace `DimaBroZY/ClashURLS` in README with actual values
4. Enable GitHub Actions in repository settings
5. Run the workflow manually or wait for automatic execution

## Features

- **Multiple Categories**: 7 different rule categories for flexible traffic management
- **CDN Support**: Files available through both GitHub raw URLs and jsDelivr CDN
- **Wildcard Support**: Proper handling of domain wildcards for comprehensive coverage
- **Clash Premium Compatible**: Optimized for Clash Premium core

## License

This project is licensed under the GNU General Public License v3.0 - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [OpenCCK](https://iplist.opencck.org/) for providing comprehensive domain lists
- [Loyalsoldier/clash-rules](https://github.com/Loyalsoldier/clash-rules) for inspiration and project structure

- The open-source community for continuous improvements
