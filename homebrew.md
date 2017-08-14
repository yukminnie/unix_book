1.安装xcode-main-line-tools

```
xcode-select --install
```

1. 安装homebrew

```
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

3.添加至虚拟环境

```
echo 'export PATH="/usr/local/bin:$PATH"' >> ~/.bash_profile
```

4.新开命令行测试

```
brew doctor
```

5.命令列举

```
brew install <package_name>

brew update

brew outdated

brew upgrade <package_name>

brew cleanup

brew list --versions
```

6.切换中科大默认源

```
替换brew.git:
cd "$(brew --repo)"
git remote set-url origin https://mirrors.ustc.edu.cn/brew.git

替换homebrew-core.git:
cd "$(brew --repo)/Library/Taps/homebrew/homebrew-core"
git remote set-url origin https://mirrors.ustc.edu.cn/homebrew-core.git
```

7.同时切换Homebrew Bottles源

```
bash 用户:
echo 'export HOMEBREW_BOTTLE_DOMAIN=https://mirrors.ustc.edu.cn/homebrew-bottles' >> ~/.bash_profile
source ~/.bash_profile

zsh 用户:
echo 'export HOMEBREW_BOTTLE_DOMAIN=https://mirrors.ustc.edu.cn/homebrew-bottles' >> ~/.zshrc
source ~/.zshrc
```

8.切换官方源

```
1.注释重启

2.重置brew.git:
cd "$(brew --repo)"
git remote set-url origin https://github.com/Homebrew/brew.git

重置homebrew-core.git:
cd "$(brew --repo)/Library/Taps/homebrew/homebrew-core"
git remote set-url origin https://github.com/Homebrew/homebrew-core.git
```



