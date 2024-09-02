---
author: "Keisei Akiya"
date: 2024-08-17
tags: [markdown, wsl2, vagrant]
---

# Vagrant

## やったこと

- Vagrant を Windows にインストール
- Vagrant を WSL2 にインストール
- `~/.bashrc`に以下を追加

  ```bash
  export VAGRANT_WSL_ENABLE_WINDOWS_ACCESS="1"
  export PATH="$PATH:/mnt/c/Program Files/Oracle/VirtualBox"
  ```

- WSL2 で以下のコマンドを実行．

`vagrant plugin install virtualbox_WSL2`

## 課題

- 他のコマンドを実行したらエラー
  - Windows Vagrant version: 2.4.1
  - Windows Subsystem for Linux Vagrant version: 2.2.19
