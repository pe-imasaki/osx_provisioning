# OSX プロビジョニング

## 概要
ansible + homebrew で、osx上で利用するソフトウェアを管理する

## ansible インストール方法
```
$ sudo xcodebuild -license
$ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
$ brew doctor && brew update
$ brew install ansible
```

## 反映方法
```
$ HOMEBREW_CASK_OPTS="--appdir=/Applications" ansible-playbook -i hosts -vv osx_base.yml
```
