# Linux Developers Guide

ahidaka / LinuxDevelopersGuide / Ubuntu-Raspberry-pi.md
<br/>

## Raspberry Pi 用 Ubuntu入手とインストール

現在 Raspberry Pi 用イメージとして、18.04 / 20.04 の 32bit / 64bit 版のイメージが公開されている。
以降、次の手順で作業する。

- Ubuntu イメージの入手と展開
- マイクロSDカードへの書き込み
- Raspberry piへの装着と起動
- Ubuntu の初期設定

### Ubuntu イメージの入手と展開

ダウンロードは次の Ubuntu 英語版ページから。簡単なインストール手順の説明が掲載されている。

https://ubuntu.com/download/raspberry-pi

https://ubuntu.com/download/raspberry-pi/thank-you

"*.xz" 形式でダウンロードするため、SDカードリーダーで書き込む前に、[7-Zip](https://sevenzip.osdn.jp/) 等のツールで展開して ***.img** ファイルを取り出しておく。

### マイクロSDカードへの書き込み

ダウンロードした ***.img** ファイルは、[Win32DiskImager](https://sourceforge.net/projects/win32diskimager/) を使用してマイクロSDカードに書き込む。

https://sourceforge.net/projects/win32diskimager/

### Raspberry piへの装着と起動

Raspberry pi に書き込んだマイクロSDカード装着後、必ずキーボードとモニターを装着してからRaspberry piの電源を入れる。

### Ubuntu の初期設定

User: ubuntu
Password: ubuntu
でログイン後、パスワード変更を強制される。
まず古いパスワード(ubuntu) を入力してから、新しいパスワードと確認パスワードを入力すれば完了。

以上
