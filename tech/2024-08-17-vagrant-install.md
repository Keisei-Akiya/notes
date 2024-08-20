---
author: "Keisei Akiya"
date: 2024-08-17
tags: [markdown, wsl2, vagrant]
---

# Vagrant

## やったこと
- VagrantをWindowsにインストール
- VagrantをWSL2にインストール
- `~/.bashrc`に以下を追加

    ```
    export VAGRANT_WSL_ENABLE_WINDOWS_ACCESS="1"
    export PATH="$PATH:/mnt/c/Program Files/Oracle/VirtualBox"
    ```

- WSL2で以下のコマンドを実行．

`vagrant plugin install virtualbox_WSL2`

## 課題

- 他のコマンドを実行したらエラー
  - Windows Vagrant version: 2.4.1
  - Windows Subsystem for Linux Vagrant version: 2.2.19