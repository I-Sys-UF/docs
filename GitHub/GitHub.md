# GitHub について

GitHub とは，バージョン管理システムである Git の仕組みを利用し，世界中の人々が自身の作品を保存・公開できるようにした Web サービスのことをいいます  
本来はコードの管理に使われるものですが，その機能の豊富さからタスク管理に使用することもできます．<https://github.com/I-Sys-UF/onboarding> はまさにそうです

## 用語集

<https://docs.github.com/ja/get-started/quickstart/github-glossary> に一通り載っている．わからない単語があったら `F3` キーなどを使って単語検索してみよう  
もちろん Google 検索を使ってもいい

## からくり工房 I.Sys の方針

- コードに変更を加えるときは，かならず新たにブランチを切ってそこで行う
- タスク管理は Issue を活用する
- コミットメッセージは簡潔に，かつ分かりやすく
- README はなるべく書く．Markdown で書けるので，文字装飾や HTML タグも活用しよう
- Public に公開するリポジトリには可能な限りライセンスを設定する
  - 大体は MIT や Apache License でいいが，ちゃんと調べて理解して選択すべし
  - Creative Commons でももちろん良い
  - `LICENCE` ファイルを追加する OR README に記載する のどちらか，あるいは両方で
- 分からないときは誰かに聞く（これは GitHub だけでなく広く全般に言えること）

## 雑多な tips

タスク管理に Issue を使う際，`- [ ] task1` のような書き方をすると以下のようになります

- [ ] task1

すべきタスクを羅列しておき，終わったら都度チェックを入れることで何が終わっていて何が終わっていないのかが明確になるメリットがあります  
また，Issue を立てるときに Close 条件を書いておくと，その Issue が目指すべき姿が分かりやすくなるのでなるべく書きましょう

書き方は Markdown に準じます．以下に書き方の一例を示しますので参考にしてください  
GitHub Flavored Markdown での書き方については，[このページ](https://docs.github.com/ja/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) を参照のこと

```md
# Issue タイトル

ここにやりたいこととかを書く

## TODO

- [ ] タスク１
- [ ] タスク２
- [ ] タスク３
- [ ] タスク４
- [ ] タスク５
- [ ] タスク６

## Close 条件

タスクが全て完了したら / 〇〇が使えるようになったら 等
```
