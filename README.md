# Linux Developers Guide

 ahidaka / LinuxDevelopersGuide
 
 ## CPIO
 
 <PRE>findとの組み合わせ（ツリー構造を維持）

# find . | cpio -dump /somewhare/target_dir

単一ファイルコピー：echoやlsとの組み合わせ（通常はcp -aで十分だが、cpで取れないものを含む場合には...）

# echo *something* | cpio -dump /somewhare/target_dir

# ls *somedir*/* | cpio -dump /somewhare/target_dir

指定ファイルのツリーをコピー

#!/bin/sh
for file in `echo b* c* d* e* i* lib m* r* s* u* v*`; do
    echo file = $file
    find $file | cpio -dump /home/backup
done

※cpioでは他にアーカイブの作成と復元もできるが、普段使わないので使い方は省略。</PRE>
<H3><A name="2">３．簡単マニュアル</A></H3>
<H4>cpio の主なオプション</H4>
<P>-d, --make-directories <BR>
必要に応じてディレクトリを作成。<BR>
<BR>
-u, --unconditional <BR>
全てのファ イルを上書き。<BR>
<BR>
-m, --preserve-modification-time <BR>
コピー先ファイル生成時に、コピー元の更新時刻を復元。<BR>
<BR>
-p, --pass-through <BR>
パススルー（コピー）・モード。<BR>
<BR>
-v, --verbose <BR>
冗長モード。ファイル名表示。</P>
