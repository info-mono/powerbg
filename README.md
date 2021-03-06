<p align="center"><a href="https://github.com/info-mono/powerbg"><img src="https://user-images.githubusercontent.com/43980777/118600621-7135bc80-b7db-11eb-919d-0c2d07fa4a0e.png"></a></p>
<p align="center"><a href="https://github.com/info-mono/powerbg/blob/main/LICENSE"><img src="https://img.shields.io/github/license/info-mono/powerbg?labelColor=383838&color=585858&style=for-the-badge" alt="License: GPL-3.0"></a> <a href="https://gist.github.com/NNBnh/9ef453aba3efce26046e0d3119dab5a7#development-completed"><img src="https://img.shields.io/badge/development-completed-%23585858.svg?labelColor=383838&style=for-the-badge&logoColor=FFFFFF" alt="Development completed"></a></p>

## ๐ก About
**PowerBG** is a tool that add to color string's background like [Powerline](https://github.com/powerline/powerline) written in [`portable sh`](https://github.com/dylanaraps/pure-sh-bible).

## ๐ Setup
### ๐งพ Dependencies
- [Unix commands](https://en.wikipedia.org/wiki/List_of_Unix_commands) to process

### ๐ฅ Installation
#### ๐ง Manually
Option 1: using `curl`
```sh
curl https://raw.githubusercontent.com/info-mono/powerbg/main/bin/powerbg > ~/.local/bin/powerbg
chmod +x ~/.local/bin/powerbg
```

Option 2: using `git`
```sh
git clone https://github.com/info-mono/powerbg.git ~/.local/share/powerbg
ln -s ~/.local/share/powerbg/bin/powerbg ~/.local/bin/powerbg
```

#### ๐ฆ Package manager
For [Bpkg](https://github.com/bpkg/bpkg) user:
```sh
bpkg install info-mono/powerbg
```

For [Basher](https://github.com/basherpm/basher) user:
```sh
basher install info-mono/powerbg
```

> *If you can and want to port PowerBG to other package managers, feel free to do so.*

## โจ๏ธ Usage
Run `powerbg` in the terminal:
```sh
powerbg COLOR STRING COLOR STRING COLOR STRING ...
```

Examples:
```sh
powerbg '0' "$USER" '8' "$PWD"
```

![Example 1](https://user-images.githubusercontent.com/43980777/118599299-84478d00-b7d9-11eb-9195-1ccd8bb74358.png)

```sh
POWERBG_LEFTEND_OUTER='๎ถ' \
POWERBG_RIGHTEND_OUTER='๎ด' \
POWERBG_SEPARATOR_RIGHT='๎ผ ' \
POWERBG_SEPARATOR_SAME=' \033[30m๎ป ' \
powerbg '1' '\033[30mRed' '3' '\033[30mYellow' '3' '\033[30mYellow again' '2' '\033[30mGreen' '6' '\033[30mCyan' '4' '\033[30mBlue' '5' '\033[30mPurple'
```

![Example 2](https://user-images.githubusercontent.com/43980777/118599338-90cbe580-b7d9-11eb-9c78-a7144352707b.png)

```sh
green='\033[30mTree'
cyan='\033[30mSky'
blue='\033[30mWater'
purple='' # Nothing
red='\033[30mApple'

POWERBG_LEFTEND_OUTER='๎ถ' \
POWERBG_RIGHTEND_OUTER='๎ด' \
POWERBG_SEPARATOR_RIGHT='๎ผ ' \
POWERBG_SEPARATOR_SAME=' \033[30m๎ป ' \
powerbg '2' "$green" '6' "$cyan" '4' "$blue" '5' "$purple" '1' "$red"
```

![Example 3](https://user-images.githubusercontent.com/43980777/118599376-9b867a80-b7d9-11eb-9df4-e19b9a5b62e0.png)

## โ๏ธ Configuration
PowerBG is configured through environment variables: `export POWERBG_<SETTING>="<value>"`
|Environment variable     |Valid     |Default|Description                                                                      |
|-------------------------|----------|-------|---------------------------------------------------------------------------------|
|`POWERBG_LEFTEND_OUTER`  |`<string>`|*none* |Set left end outer string                                                        |
|`POWERBG_LEFTEND_INNER`  |`<string>`|*none* |Set left end inner string                                                        |
|`POWERBG_RIGHTEND_OUTER` |`<string>`|`๎ฐ`    |Set right end outer string                                                       |
|`POWERBG_RIGHTEND_INNER` |`<string>`|*none* |Set right end inner string                                                       |
|                         |          |       |                                                                                 |
|`POWERBG_SEPARATOR_LEFT` |`<string>`|*none* |Set separator left string                                                        |
|`POWERBG_SEPARATOR_RIGHT`|`<string>`|`๎ฐ `   |Set separator right string                                                       |
|`POWERBG_SEPARATOR_SAME` |`<string>`|`๎ฑ`  |Set separator string to use when when separating two elements with the same color|

## ๐ Credits
Special thanks to:
- [**Powerline**](https://github.com/powerline/powerline) by [Powerline organization](https://github.com/orgs/powerline/people)

<br><br><br><br>

---

> <h1 align="center">Made with โค๏ธ by <a href="https://github.com/info-mono"><code>@info-mono</code></a></h1>
>
> <p align="center"><a href="https://www.buymeacoffee.com/nnbnh"><img src="https://img.shields.io/badge/buy_me_a_coffee%20-%23F7CA88.svg?logo=buy-me-a-coffee&logoColor=333333&style=for-the-badge" alt="Buy Me a Coffee"></a></p>
