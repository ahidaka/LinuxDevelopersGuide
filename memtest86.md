# Linux Developers Guide

ahidaka / LinuxDevelopersGuide / memtest86.md
<br/>

## memtest86+

DOS / Windows 版のツールだが Linuxにも関係あるので掲載。

Memtest86+ はその昔の Memtest86 の頃から、かなり厳格にPCのメモリーモジュールのエラーチェックを行うツールとして有名で、「Memtest86を一晩実行すればメモリーエラーが分かる」等、PC自作や業務用PCのメンテナンスには欠かせないツールだった。

その発祥にも由来する問題は、DOSが起動するフロッピーディスク1枚に入れて使用する必要がある点で、このためだけにDOS起動可能なFD数枚と、USB-FDD 2セットを30年以上管理・維持し続けて来た。今では Ubuntu等のLinuxブートCDにも含まれる様になったが、肝心かなめなツールであるにも関わらず著名度が低く、一般にそれほど受け入れられているとは言えない状況だった。

それがやっとUSBブートに対応したので、是非とも使って欲しい。インストールは簡単で、zip ファイル展開後、起動してUSBドライブを選択、**Create** ボタンをクリックするだけだ。

USBから起動すれば自動的にスタートする。1回テスト内容はかなり高度に進化しているらしく、従来版では15分程度動作させないと出なかったエラーが起動後すぐに報告される様になった。これなら一連テストを1passすればOKではないかと思う。勿論過剰なエラー報告は無く、正常なメモリーであれば何回実行してもエラーとはならない。

また、メモリーテスト中の CPU 温度情報がリアルタイムで表示される様になった。これで CPU 負荷時の温度情報がわかり、CPUファンの目詰まり情報も確認できる。

試しに約35年も昔の、使い道が無かった **1MB** USB メモリーに入れてみたが問題なく動作している。一家に一セット、余剰のUSBメモリーの利用方法として用意しておくと良い。

### ダウンロードサイト


[Memtest86](http://www.memtest.org/)

http://www.memtest.org/

![Memtest86サイト](Image/memtest86topP.png)

**Download (Pre-built & ISOs)** をクリックする。

<br/>

![Memtest86+USB版ダウンロード](Image/memtest86P.png)

**Download - Auto-installer for USB Key (Win 7/8/10)** が目的の zip ファイル。

<br/>

### 参考サイト

[BTOパソコン.jp](https://btopc.jp/) Memtest86+最新版ダウンロードとUSBインストール
https://btopc.jp/repair/memtest86-usb-boot.html
