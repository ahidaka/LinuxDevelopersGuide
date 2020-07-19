# Linux Developers Guide

ahidaka / LinuxDevelopersGuide
<br/>

## CPIO

ファイルシステムやディレクトリの丸ごとコピー、バックアップ。

### ツリー構造毎コピー（findとの組み合わせ）

```sh
$ find . | cpio -dump /somewhare/target_dir
```
単一ファイルコピー：echoやlsとの組み合わせ
（通常はcp -aで十分だが、/dev/等 cpで取れないものを含むFilesystem複製に有効、所有者や権限も保持）

```sh
$ echo *something* | cpio -dump /somewhare/target_dir

$ ls *somedir*/* | cpio -dump /somewhare/target_dir
```

指定ファイルのツリーをコピー

```sh
#!/bin/sh
for file in `echo b* c* d* e* i* lib m* r* s* u* v*`; do
    echo file = $file
    find $file | cpio -dump /home/backup
done
```

※cpioでは他にアーカイブの作成と復元もできるが、普段使わないので使い方は省略。

### cpio の主なオプション
<P>-d, --make-directories <br/>
必要に応じてディレクトリを作成。

-u, --unconditional <br/>
全てのファ イルを上書き。

-m, --preserve-modification-time <br/>
コピー先ファイル生成時に、コピー元の更新時刻を復元。

-p, --pass-through <br/>
パススルー（コピー）・モード。

-v, --verbose <br/>
冗長モード。ファイル名表示。
