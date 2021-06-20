### LaTeXDojinStyle ###

LaTeX(pLaTeX) 用日本語縦書き判型不問小説同人誌スタイルシート。
pLaTeX Style File for Vertical Writing

トニイさんが1999年に発表された「B6判・文庫本(A6判)スタイルオプション」が元です。
元々文庫判の小説同人誌を、行間の調整が下手くそなWordで行うのがいやでいやで
LaTeXに手を出しております。
ですが印刷に出すにあたって、印刷所によっては必要な余白が違ったり、
そもそも変形サイズに対応してなかったり（どこまで期待しているんだ）。
これをまず解消できるよう、サイズを自由に設定できるように改造しました。
その後色々必要なパッケージをスタイルで読み込んでおくように改造。

Usage:
pLaTeXのマクロに対応しています。
あと、ここから呼んでるパッケージもpLaTeXのマクロです。（不要なマクロはコメントアウトしてください）
.texファイルで、\documentclassの記述の後、
\begin{document}の前までに

\usepackage{latexdojinstyle}

と記述してください（推奨はdocumentclassの次の行）。
引数はありません。


37行目付近以降がサイズの設定となります。
----------

\setlength{\paperwidth}{154mm}		% 印刷所から指定された、遊びを含めた原稿指定サイズ幅
\setlength{\paperheight}{216mm}		% 印刷所から指定された、遊びを含めた原稿指定サイズ高さ
\setlength{\honbunwidth}{125mm}		% テキスト本文サイズ幅
\setlength{\honbunheight}{187mm}	% テキスト本文サイズ高さ
\setlength{\dansaiwidth}{3mm}		% 断裁用左右余白幅
\setlength{\dansaiheight}{3mm}		% 断裁用上下余白高さ
\setlength{\kobayohaku}{9mm}		% 木端側の余白サイズ
\setlength{\headsep}{3mm}			% 柱と本文との空き
\setlength{\headheight}{5mm}		% 柱の高さ
\setlength{\oddsidemargin}{10mm}	% 奇数頁マージンサイズ
\evensidemargin\oddsidemargin		% 左右ページで同じ長さのマージンを取る
\topmargin=-1in%
\advance\topmargin by 10mm	 		% 上余白 -1inch+10mm
\footskip=5mm						% 一応フッターの幅を確保

----------
右側にコメントアウトでどこの長さの設定かを記述してあります。
印刷所からの指定がたぶんミリだと思いますので、例としてA4判、余白3ミリの数値を入れてあります。
デフォルトでは奇数頁天に書籍タイトル、偶数頁天に章タイトルが出ますので、
ちょっとこの辺トップマージンサイズなどの記述を修正するつもりです。


###############################################################################################

English:

It is based on the "Vertical Writing B6 size / paperback book (in Japan, It's sized A6) style option" announced by Tony in 1999.
I don't like to use MSWord, which is not good at adjusting line spacing, for the original paperback-style novel "Doujinshi".
It's working on LaTeX.
However, the required margins may differ depending on the printing shop when printing.
In the first place, it does not correspond to the deformation size (how much do you expect).
To solve this problem first, I modified it so that the size can be set freely.
After that, I modified it so that various necessary packages were loaded in style.
We only check the operation in Japanese and Japanese mixed with English.


Usage:
It supports pLaTeX macros.
Also, the package called from here is a macro of pLaTeX. (Comment out unnecessary macros)
In the .tex file, after writing \documentclass, write as follows Before \begin{document}.
Recommended is the next line of documentclass.
There are no arguments.

The size is set from the 23rd line onward.
----------

\setlength{\paperwidth}{154mm}		% Manuscript specified size WIDTH including play specified by the printing shop
\setlength{\paperheight}{216mm}		% Manuscript specified size HEIGHT including play specified by the printing shop
\setlength{\honbunwidth}{125mm}		% Text body size WIDTH
\setlength{\honbunheight}{187mm}	% Text body size HEIGHT
\setlength{\dansaiwidth}{3mm}		% Left and right margin WIDTH for cutting
\setlength{\dansaiheight}{3mm}		% Left and right margin HEIGHT for cutting
\setlength{\kobayohaku}{9mm}		% Margin size on the wood edge side
\setlength{\headsep}{3mm}			% Free space size between pillars and text
\setlength{\headheight}{5mm}		% pillars' HEIGHT
\setlength{\oddsidemargin}{10mm}	% Odd page margin size
\evensidemargin\oddsidemargin		% Take the same length margin on the left and right pages
\topmargin=-1in						%
\advance\topmargin by 10mm 			% Top Margin -1inch+10mm
\footskip=5mm						% footskip

----------

The comment out on the right side describes where the length is set.
I think that the designation from the printing shop is probably millimeters, so as an example, I have entered the numerical values of A4 size and margin 3 mm.

Plans:
By default, the book title appears on odd-numbered pages and the chapter title appears on even-numbered pages.
I'm going to revise the description such as the top margin size around here.
