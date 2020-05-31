
![](https://img.shields.io/badge/language-ruby-red.svg) &nbsp;
![](https://img.shields.io/badge/license-MIT-green.svg) &nbsp;
![](https://img.shields.io/badge/version-3.0.2-green.svg)


# Transc
  `Transc`是一个翻译脚本，可以将中文翻译成其它语言，或者相反，但是不支持其它语言间的互译。因为是通过 api 翻译的，所以需要在有网络的环境下运行。

  如果没有传递参数的话，它将会获取最近一次选中的文本内容进行翻译

## 目录
- [安装](#安装)
- [使用](#使用)
- [最佳实践](#最佳实践)

## 安装
#### 1. 克隆到`~/.transc`目录.

```bash
git clone https://github.com/otorain/transc.git ~/.transc
```

#### 2. 添加`~/.transc`目录到`$PATH`变量中，以便直接使用命令
  - for **Bash**
    ```bash
      $ echo 'export PATH="$HOME/.transc:$PATH"' >> ~/.bash_profile

      $ source ~/.bash_profile
    ```
  - for **Ubuntu Desktop**
    ```bash
      $ echo 'export PATH="$HOME/.transc:$PATH"' >> ~/.bashrc

      $ source ~/.bashrc
    ```
  - for **zsh**
  ```bash
    $ echo 'export PATH="$HOME/.transc:$PATH"' >> ~/.zshrc

    $ source ~/.zshrc
  ```

#### 3. 安装`Ruby`和`xsel`
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

## 使用
  在默认情况下，如果传入的是其它语言，则翻译为中文，如果传入的是中文，则翻译为英语，用法如下：

  ```bash
  transc -f zh -t en 你好 # 会收到一条消息，内容为 Hello
  ```

  可用选项有：
  - **-f** : 指定翻译的源语言
  - **-t** : 指定翻译的目标语言
  - **-h** : 查看帮助
  - **-v** : 查看版本

#### 1. 中文翻译为英语
```bash
  $ transc "你好"  # hello
```

#### 2. 中文翻译为西班牙语
```bash
  $ transc -t es "你好" # Hola
```

#### 3. 英语翻译为中文
```bash
  $ transc "hello" # 你好
```

#### 4. 韩语翻译为中文
```bash
  $ transc "안녕하세요" # 你好
```

## 最佳实践
可以把`transc`命令绑定到快捷键上，这样就可以实现选中文本翻译的功能。使用不带参数的`transc`，如果选中的是英文或是其它语言（日语，法语，韩语...），则会翻译成中文，选中的是中文则会翻译成英文。
