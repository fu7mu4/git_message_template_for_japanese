# これはなんですか?

git_message_template_for_japanese は コミットメッセージのタイトルを英語で書くためのテンプレートです。

*ねむたくなってきたので、今日はここまで。*

# ようわからんけど?

git ちゅーのはコミットするときにコミットメッセージとかいうのを入力するんやけど、
それって英語で書かなあかん、英語で書いてかっこつけたいってときあるやん。

でも英語でよう書けんやん、自分。どうする?今からガッコいく? コミットでかっこつけたいためだけに
スクール通う?よく使う単語3000個おぼえる?そんなんようやらんやん。無理やん。
それにコミットメッセージ教えてっていってスクールの先生教えてくれるか? そんな先生おらんやろ。

でも *チョットダケ英語デキル* いいたいやん?

それやったら、最初の一行、あれだけ英語にしたらええんちゃうんって、それやったらできるやん、
このカンニングペーパーじゃなかったチートシートをテンプレートにいれるか、追加したら。
それにこの方法やったらバレへんやん? Googleさんの翻訳してるのバレんのいややん?

# どうしたらええん?

gitのテンプレートがないんやったらこの カンペ を そのまま commit.templateにしてもよし。

```bash
git config --global commit.template ~/.commit_template
cp かんぺ ~/.commit_template
```
gitのテンプレートがあるんやったらこの カンペ を そのうしろに追加したら、知らんけど。

```bash
cat かんぺ >> まえからあるテンプレート
```

# License /つこうてええんか?

"THE BEER-WARE LICENSE" (Revision 42):
<fu7mu4@gmail.com> wrote this file. As long as you retain this notice you can do whatever you want with this stuff. 
If we meet some day, and you think this stuff is worth it, you can buy me a beer in return.

つまりこれを誰かにあげるときに、この上の2行だけ残してくれたら自由にしていいってことですわ。
あと、どっかであったときにもし感謝したかったら、酒をおごってくれてもいい。(おごらんでもいい)
もちろん、チートシートを誰かにあげるんやったらこれをのこさなあかんけど、自分でつかうならどうでもええ。
