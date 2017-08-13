1.安装xcode-main-line-tools

```
xcode-select --install

```

 2. 安装homebrew

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



