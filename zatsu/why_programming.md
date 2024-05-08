# なぜプログラミングをするのか

ここでは，なぜ我々はプログラミングという，めんどくさいことをするのかについて書き残そうと思う

## 前提

プログラミングとは，雑に言えばプログラムを組む・書くことである．じゃあプログラムとはなんだろうか  
雑に「プログラム」で調べてみたところ，このような記述を発見した

```
プログラム（program）とは、予定（表）、計画（表）、課程、式次第などの意味を持つ英単語。
> https://e-words.jp/w/%E3%83%97%E3%83%AD%E3%82%B0%E3%83%A9%E3%83%A0.html
```

計画であったり過程であったりという単語から，「することをまとめたもの」というニュアンスが感じ取れるだろう  
つまり，コンピュータがすることをまとめたもの，それが「プログラム」なのである

こと IT の世界においてプログラムと言えば一般には「コンピュータ・プログラム」のことを指す．以後断りなければコンピュータ・プログラムのことを単にプログラムと呼ぶことにする

コンピュータとはなにかという話を掘り下げるのは面倒なので簡単な話にとどめておくが，早い話が計算機である．内部であらかじめ決められた通りに計算を進めるものを我々はコンピュータと呼んでいるのである

さて，ここ I.Sys では，主にマイコンとかいうものに対してプログラミングを行っている．さて，マイコンとはなんだろうか

諸説あるのだが，「マイクロコンピュータ」または「マイクロコントローラ」の略と言われている．正直どっちでもいいので好きに理解していただいて構わない  
いづれにしても頭に「マイクロ」というワードがついている．要するにちっさい計算機のことをマイコンと呼んでいるのである   
具体的にどれくらい小さいかと言うと，人差し指の腹に乗るくらいのものが多い．どんなにデカくても手のひらサイズを超えることはなかろう  
いわゆる「IC チップ」という，小さい黒い四角いやつ．あれを想像してくれればだいたいあっている  
そんなに小さいのならマイクロと呼ばれるのも頷けるだろう

そんなマイコンだが，どこで使われているか想像したことはあるだろうか？　あまり意識されないと思うが，結論を言うとこの世のほぼすべての電気を使う製品に使用されている  
例を挙げてみよう．電子レンジ・ファンヒーター・リモコン・空調・テレビ・ゲーム機はもちろんのこと，自動車・ゲーセンのマシンなどデカイものにも当然使われている  
色んなところで使われているのはわかった．じゃあ，どのように使われているのだろうか

基本的には，入力を受け付け，それに応じて何らかの処理・表示をするということを無限に繰り返している  
例えば，リモコンを例に挙げて考えてみよう．テレビのリモコンを想像して欲しい  
彼らは，沢山のスイッチを入力として持っている．出力はほとんどの場合赤外線 LED である  
簡単に言うと，一定間隔でスイッチの状態を読み取り，スイッチが押されたらそれに対応する出力をする．ということをしている．このサイクルを高速に，かつ正確に行っている

そんなマイコンであるが，ソフトウェアがないと動かない．ソフトウェアのないマイコンなどただのガラクタである  
そのソフトウェアを作るという作業がプログラミングなのである

## ハードウェアとソフトウェア

ハードウェアはほとんどの場合ソフトウェアなしには動かない．が，ここで，ソフトウェアなしに動く謎のハードウェアを考えてみよう

「謎のハードウェア」とは言ったが，一応これは実在する．シーケンサや論理回路の集合が該当しうる．だが，それよりももっと高度なものを考えてみることにする  
例えば，先の例で挙げたテレビのリモコン．これくらいなら頑張れば論理回路とアナログ回路だけでも，まぁ作れなくはない  
名付けて「フルアナログリモコン」．使えるように作ったので，当然使えるはずである  
だが，苦労して作ったフルアナログリモコン，本当に「使える」だろうか？  
一口にテレビと言っても種類がある．つまり，リモコンもそれにあわせて何種類か必要になる  
フルアナログリモコンだと，それぞれで違う回路を組まなくてはいけない．つまり，基板や部品が別々になってしまうので管理が面倒だし，なんといっても作るのがダルい  
作るというのは設計と製造両方の意味を持つ

ここで，もし，「全く同じものでも異なる動きを自由に作れるハードウェア」があったらどうだろうか．便利そうだとは思わないかい？  
リモコンであれば，製品ごとに異なる信号を出す必要があるのを，この素晴らしいハードウェアに任せることができる  
そうすると，基板も部品も共通化することができ，コストダウンを図れる

非常に素晴らしいこの夢のようなハードウェア，なんと驚いたことに，実在する．それが，何を隠そう「マイコン」なのである  
ハードウェアだけでは複雑になりすぎるようなものでも，そこにソフトウェアを組み合わせることで，柔軟性を持たせることができるようになる．素晴らしい

ここまで真面目に読んでいれば，ソフトウェアがとても大事なものであることが，なんとなくわかるだろう．ここからはソフトウェアの話に移っていく

マイコンの上で動くソフトウェア，どんなことでもコンパイルさえ通ればやってくれるので，非常に複雑なことをしているように思えるが，実はそうでもない  
単純な動作を組み合わせ，高速で処理することで，あたかも複雑なことをしているように見えているだけである  
やってることは基本的に計算であり，四則演算やレジスタ（ごく小規模なメモリのことで，様々な役割のものがある）の読み出し，書き込みくらいしかやっていない  
マイコンの場合，この「レジスタ」がどんな種類のものがどれだけ用意されているかが重要になる．このレジスタの機能こそがマイコンの機能だからである

マイコン自体は単純なことしかできないが，それらを組み合わせて複雑に見える処理をやってくれる．のだが，これをさせるのが非常に大変  
ご存知の方も多いだろうが，マイコンは「機械語」という言葉を解釈して動いている．プログラムも最終的には機械語になるわけだが，それなりに複雑なことをさせようと思うとこの機械語が膨大な量になる  
が，そもそも数字の羅列でしかないのでなんて書いてあるのか分からん．しかもマイコンごとに違う．こんなん書いてられっか！　ということでアセンブリ言語と呼ばれるものを使う．`MOV` や `ADD` などの各種命令がそれぞれ特定の機械語に対応するという，ごく単純な言語である  
だが，それでも膨大な量であることには変わらない．そこで登場するのが一般にプログラミング言語と呼ばれる，C などの高級言語である．ここまで来れば人間でもまぁ読めなくはないし，書けなくはないという程度にまでなる  
一目見るだけでは何がなんだかわからないソースコードも，実はかなり人間に優しい部類なのである  
なので，プログラミングをするときは，このことを頭の片隅においておくと，なにか良いことがあるかもしれない？

そんなこんなで書きやすくなった言語を使って，ちょろっとコードを書いてみよう．Hello world! でも L チカでもいい  
書いたコードは，（C 言語の場合）まずプリプロセッサと呼ばれるプロセスによって処理されたあと，コンパイラによってアセンブリに変換され，アセンブラによって機械語に変換される．この一連の流れのことを一般に「コンパイル」と呼んでいる

このコンパイラはマイコンに搭載されている CPU のアーキテクチャ（つまりは構造）によって変える必要があり，当然ながら吐き出される機械語も異なる．それは別にどうでもいいのだが，このアーキテクチャが若干面白いので少し触れておこう

## アーキテクチャ

マイコンを使った工作の登竜門として有名なものとして Arduino がある．初心者でも始めやすく，お手軽にプログラミングができて便利なのだが，この Arduino 環境向けに開発されたボードには代々「AVR」と呼ばれる CPU コアを積んだマイコンが使用されてきた  
AVR は Atmel 社が開発したアーキテクチャで，8bit である．かなり古い設計と言えよう  
もちろん他にもアーキテクチャは存在する．現在存在するアーキテクチャの 3 大巨頭と言えるのが，「Arm」「x64」「RISC-V」である．x64 は Intel や AMD などが出している，パソコン向けの CPU に搭載されているアーキテクチャで，Arm はスマートフォンやタブレットなどに採用されていることが多い  
残る RISC-V だが，これは比較的新しいアーキテクチャで，一部のマイコン（WCH CH32V シリーズなど）に使われていたりする

他にも PIC や Renesas RX などいろいろあるが，キリがないのでこの辺で

## なぜプログラミングをするのか

ここでこの書き散らしの本題に入る．なぜ我々はプログラミングをするのだろうか

答えは簡単で，ハードウェアを好き勝手動かしたいからである．テキトウなハードウェアを自由に動かせたらそれはそれは楽しいだろう  
ゲーム機を作るもよし，ロボットを作るもよし，単純なリモコンを作るもよし．これらすべて，ソフトウェアの成せる技である

ただし，なんでもかんでもできるわけではない  
例えば数値表現．どんな数字でも表現できるかと言われたらそんなことはなく，限界がある  
昔のゲームで 255 が体力や攻撃力の最大値だったことがあるが，これは 8bit の非負整数で表すことができる最大の値が 255 であることに起因する

ここ I.Sys では主に自律制御のロボットを作っているので，そちらを例に取ってみようか．例えばライントレーサ

ライントレーサは白線を追っかけて走るロボットだが，これを思い通りに動かそうと思ったら当然それなりの量のコードを書き，アルゴリズムを構成する必要がある  
まずは白線をどう検出するか．それだけでなく，モータの制御をどうするか．スタート・ゴールマーカを正確に識別するにはどうすべきか  
それらを考え，コードに起こすということが必要になる．これもプログラミングという作業の一部である

プログラミングというものは往々にしてうまく動いてくれないものであるが，うまく行ったときの喜びはぜひとも皆が味わって欲しいものである．エラーコードと真面目に向き合い，頑張ってほしい