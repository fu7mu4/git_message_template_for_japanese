# どうしたらええん?

gitのテンプレートがないんやったらこの カンペ を そのまま commit.templateにしてもよし。

```bash
git config --global commit.template ~/.commit_template
git clone https://github.com/fu7mu4/git_message_template_for_japanese.git
cp git_message_template_for_japanese/commit_messeage_sample.txt  ~/.commit_template
```
gitのテンプレートがあるんやったらこの カンペ を そのうしろに追加したら、知らんけど。

```bash
git clone https://github.com/fu7mu4/git_message_template_for_japanese.git
cat git_message_template_for_japanese/commit_messeage_sample.txt >> YOUR_GIT_COMMIT_TEMPLATE
```

## もうちょっと続き

1. git add してコミットする。

```bash
git commit
```

そうしたら いつもの vim か何かエディタのコミット画面になるけど、そんときに
下にカンペでるから、これをコピーして書けば楽やねん。

```
#########1#########2#########3#########4#########5#########6#########7#########8
# see https://github.com/fu7mu4/git_message_template_for_japanese/blob/master/description.md
# Fix typo
# Fix compiler warning [ in <場所> ]
# Fix <直したとこ> [ for 〜のため | to 〜するため ]
# Add <加えた機能、加えたもの> to <場所>
# Add <加えた機能、加えたもの> [ for 〜のため | to 〜するため]
# Add support for <サポートした機能> 
```

文字数は数字でわかるし、どれかなーっと思ったら [description](./description.md) URLに移動したらいいし。

どうせみんな git bash でvim 使うてるんやろうからvimで説明するけど。

1. hjkl を使うてFix typo のFのところにカーソル移動して、
2. `y$`を入力して 行末までコピー
3. hjkl を使うて ######....の行の頭に移動して、
4. `P`で上の行に ペースト

ちなみに、# から始まる行はそのまま保存してもコミットメッセージには含まれへんからいらん行は消さんでもええ。

あと `<なんか>` はプログラムの要素とか機能やからそれくらいは単語を仕様か何かからひろってきてな。

`[ ]`はUNIXのマニュアルにもある、省略可能っていう意味やから。
そう `Fix compiler warning [ in <場所l> ]` は `Fix compiler warning`だけでも、ええし、`Fix compiler warning in hogehoge.c` でもええっちゅうことですわ。

`hjkl` や `y$` がわからん人はvim のキーバインドを覚えた方がええ。
vimtutor で簡単なのはマスターできるからしてみて。
