
![](https://img.shields.io/badge/language-ruby-red.svg) &nbsp;
![](https://img.shields.io/badge/license-MIT-green.svg) &nbsp;
![](https://img.shields.io/badge/version-3.0.2-green.svg)

- [Introduction](#introduction)
- [Install](#install)
- [Use](#use)

## [Introduction](#Introduction)
  This is a script for translate other language to Chinese, or otherwise. The translated result with print in system msg. It need internet connection.

  It accept a argument from command option, if not any argument was given, it will  try to get content you last selected.

## Install
1. Clone transc into `~/.transc` .
git clone https://github.com/otorain/transc.git ~/.transc

2. Add `~/.transc` to your `$PATH` for access the `transc` command-line utility.
  - for **Bash**
    ```bash
      $ echo "export PATH=$HOME/.transc/:$PATH" >> ~/.bash_profile

      $ source ~/.bash_profile
    ```
  - for **Ubuntu Desktop**
    ```bash
      $ echo "export PATH=$HOME/.transc/:$PATH" >> ~/.bashrc

      $ source ~/.bashrc
    ```
  - for **zsh**
    ```bash
      $ echo "export PATH=$HOME/.transc/:$PATH" >> ~/.zshrc`

      $ source ~/.zshrc
    ```

3. Install `Ruby` for execute script and install `xsel` for translate from selected content.
  - for **Arch Linux**
    ```bash
      $ sudo pacman -S ruby xsel
    ```


  - for **Ubuntu**, **Debian** or **Deepin**
    ```bash
      $ sudo apt-get install ruby xsel
    ```

  - for **CentOS** or **RedHat**
    ```bash
      $ sudo yum install ruby xsel
    ```

## [Use](#Use)
  `transc` translate to your system language($LANG) in default. if the system language i


  so I can use `transc` as below:

  1. translate from Chinese to English:
    ```bash
      transc -f chinese
      # or
      transc "你好
    ```

  2. translate from English to Chinese
    `transc "hello"`

  3. translate from
