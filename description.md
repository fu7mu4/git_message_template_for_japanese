# DESCRIPTION

## なんか直した Fix

だいたい、これ。単純な修正に使う。

### Fix <直したとこ> [ for 〜のため | to 〜するため ]

- Fix typo
    - スペルミスのようなものを直したときは目的を書いたりしない
        - 関数名のミスを直した
        - ドキュメントを直した
- Fix compiler warning
    - 単純な修正につかう、これも目的をいちいち書かないことが多い
        - Fix cpplint warning 静的解析の指摘を直したではなくて何か書いたほうがええ
            - cppcheck とか checkstyle とか golint とかなんでもいける
        - Fix coding style コーディングスタイルを直した
- Fix その他
    - いろいろ使えるので便利
    	- 理由も簡単に説明するときはfor または to
            - for #チケット番号 で そのチケットのためにといえる
            - to で書くときは動詞で説明する、不定詞って覚えている？
    - Fix bug in xxxx that ....という書き方もあるけど、いけるか。

## 新しくなんかを加えた、実装した

追加つまり開発を進めたときに使うことが多い

- Add <加えた機能、加えたもの> to <場所>
    - 何かをどこか(場所)に加えたときに使える
        - Add xxxx functionality to xxxx class とか 
- Add <加えた機能、加えたもの> [ for 〜のため | to 〜するため ]
    - 理由も簡単に説明するときはfor または to
        - for #チケット番号 で そのチケットのためにといえる
        - to で書くときは動詞で説明する、不定詞って覚えている？ 
- Add support for <サポートした機能> 
    - Add <機能> でも書けるけど、これは改まった感じ
        - ちょっと大きい機能なんかもしれん。
	
## ええもんを採用した

- Use <採用したアルゴリズムや機能、もの> [ for 〜のため | to 〜するため]
    - なにかを使うようにしたってことやからAdd でも書ける
- Use <採用したアルゴリズムや機能、もの> instead of <削除した機能、もの>
    - これは 入れ替え。つまりAdd いるもん and remove いらんもん の意味
    - [Google Engineering Practices Documentation](https://google.github.io/eng-practices/) によるとアトミックなコミットはビルドが保証されとかないかんから一コミットに削除と追加を一つにするときがあるっちゅーことやん。
        - 単純にアレ消してこれ加えたではないんやで。
 
## あかんものを消した

 直した(Fix) でも表わせるけど、消したっていいたいとき

- Remove <削除したもの> from <場所>
    - unused とか deprecated とか obsolute とか
    - undefined behavior とか unspecified とか 
    - Remove and Addみたいなときは Use ... instead of ... 使うたって
	- 場所を変えるときは移動の Move を使うて。

## 移動させた

- Move <移動するもの> [ from <元の場所> ] to <移動先の場所> 
    -  ファイルとかクラスとかincludeディレクティブとかの場所を変えたいとき
    -  神クラス や神オブジェクト の一部を移動したったとき。よくやった。えらいぞ!!
        - 分割したった、というのは Split 使ってもええけど、あんまりない。
            - 一コミットにするには複雑すぎるからかな。

## 避けた

問題が起らないように予防したとき、将来的に起きんようにしたとか。

- Avoid <回避するしたい課題、問題>
    - これは発生するかもしれない問題とか、特定環境に依存した問題とか
	- 予防やから、あんまり使わんかもしれんな。

## 良くした。改善した。

- Improve <改善したもの>
    - performance とか、memory usage とか
    - readability とか、maintenancability とか portability とか
    - Improve readbilty of XXX method とか of 使うとええかんじかも？

## 更新したった

なんかのバージョンを上げたときとか、git submodule上げたとかで、リポジトリに変更加えたから更新とかいうのは違うからな。ええか

- Update <更新の対象>
    - Update zlib to version 1.2.11 (Open Source Software等)外部のソフトウェアのバージョンあげたとき

## 変えたった

- Make <変更する対象> <状態>
    - いわゆる5文型の、S V O Cっていうやつ
    	- メソッドや関数の属性などを変えたときに使うて
            - Make xxxx method in xxxx class private
        - 形容詞を比較級にしたら、より...になったという意味になる
            - Make xxxx method more faster


