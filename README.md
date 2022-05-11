# instances

- [InstanceTicker/InstanceTicker](https://github.com/InstanceTicker/InstanceTicker) で使ってるインスタンスリストです。

- 各SNSロゴや各インスタンスの favivon などの画像データを含みますので、取り扱い注意であることをご留意ください。

- SNS (Social networking service) means "social media" in Japanglish...

## instances.tsv

- TSV で管理している感じです。

- Google Spreadsheet で作成しています。

- SNS番号 が `0` である場合は、SNS の種類とそのデフォルトのデータとなっており、空欄の場合は無視され、注釈がかけるようになります。 
- 画像データは、Webp の Data URI Schemeを入れます。`deta:` から入力します。

|  id  |  sns |  host  |  domain  |  text  |  width  |  tcolor  |  bcolor  |  scolor  |  bicon  |  sicon  |  eicon  |  iicon  |  url  |  entry  |  exity  |  icon  |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
|  id  |  SNS番号 |  ホスト  |  索引用ドメイン  |  表示名  |  画像の横幅  |  表示名色  |  背景色  |  表示名影色  |  画像背景色個別指定  |  同一画像をidで指定  |  eicon  |  画像のライセンス情報  |  Wiki等のURL  |  エントリ日 or 最古存在確認日時)  |  非エントリ日  |  画像データ |

## <s>instances.db</s>

- 面倒なので配布やめました。


# Issue にて要望を受け付けます。

<hr>

## うちのインスタンスがねえじゃん or 入れてくれるな！
- 手動更新なので許してください。追加や抹消の依頼は Issue してください。
- 開設や閉鎖のご報告 Issue ありましたら助かります。

<hr>


## 各サーバーの favicon の 画像データについて

### favicon はキャッシュプロキシにするか、Google か Hatena の favicon ツールをフリーライドすればいいのではないですか？
- それもいい手ですが、Google 側では、近年仕様変更があったため、使わないようにしています。
- Hatena も表示速度がよくないので、使うにしても申し訳ない感じです。
- 使わない理由としては、アニメーション favicon にも対応させたかったためで、手動且つ個別で変換させています。
- 稀に、SVG 形式の favicon を設定するインスタンスが存在し、それにも対応させるためには、そら手動にでもなります。
- またサイズも異なるため（16x16 ではなく 14x14 となっています）、逐一手動で変換しています。（16x16 のまま放置にしてるケースもあります）
- ある Misskey サーバーでは、縦横 1000px を超える尋常じゃない画像サイズで favicon にしてるケースもあり、信用ならねえ。

<hr>

### Misskey みたいに favicon 直リン参照にすれば？
- まったく無関係の外部サイトの画像を link rel="icon" で設定するお行儀の悪い Misskey サーバーが数件ありました（誰だよ！某Wikiサイトの画像直リンしてる不届き者は！）。
- このようなケースもあり、 Misskey がこの方法でやってることに少し疑問ではある。

<hr>

### とりあえず、うちの favicon やロゴを無許可で使わないでくれます？
- 画像作者名を明記することなくこのような公開の形となってしまい、申し訳ない気持ちでいっぱいです。
- とりあえず Issue してください。すぐにデフォルトに戻します。。
- SNS開発者さんも、ロゴ画像使用についてなにかあれば、Issue してくだされば、対処していきます。

<hr>

### SNS Logo の Difference を提示しなさい！

- 以下のとおりです。
- 抹消線はリストから除外にされたものです。

| SNS   | SNS Class Name| Logo                              |
| ----- | ------------- | --------------------------------- | 
|   1   | Mastodon (jp) | ![Logo](https://itk.pw/1? "Logo") |
|   2   | Mastodon      | ![Logo](https://itk.pw/2? "Logo") |
|   3   | Pleroma       | ![Logo](https://itk.pw/3? "Logo") |
|   4   | Misskey       | ![Logo](https://itk.pw/4? "Logo") |
|   5   | PeerTube      | ![Logo](https://itk.pw/5? "Logo") |
|   6   | GNU Social    | ![Logo](https://itk.pw/6? "Logo") |
|   7   | Write Freely  | ![Logo](https://itk.pw/7? "Logo") |
|   8   | Pixelfed      | ![Logo](https://itk.pw/8? "Logo") |
|   9   | Microblog.pub | ![Logo](https://itk.pw/9? "Logo") |
|   10  |               |                                   |
|   11  | Bookwyrm      | ![Logo](https://itk.pw/b? "Logo") |
|   12  | Socialhome    | ![Logo](https://itk.pw/c? "Logo") |
|   13  | Dolphin       | ![Logo](https://itk.pw/d? "Logo") |
|   14  | Plume         | ![Logo](https://itk.pw/e? "Logo") |
|   15  | Friendica     | ![Logo](https://itk.pw/f? "Logo") |
|   16  |<s> Gab Social </s>| ![Logo](https://itk.pw/g? "Logo") |
|   17  |<s> Hubzilla </s>| ![Logo](https://itk.pw/h? "Logo") |
|   18  | Prismo        | ![Logo](https://itk.pw/i? "Logo") |
|   19  |<s> Juick </s> | ![Logo](https://itk.pw/j? "Logo") |
|   20  |               |                                   |
|   21  | Lemmy         | ![Logo](https://itk.pw/l? "Logo") |
|   22  | Meow.fan      | ![Logo](https://itk.pw/m? "Logo") |
| 23-59 |               |                                   |
|   60  | Unknown       | ![Logo](https://itk.pw/Y? "Logo") |
|   61  |               |                                   |

<hr>

### アニメーション favicon の Difference を提示しなさい！

- アニメーション favicon が確認できたのは以下のとおりです。
- われわれが、アニメーション favicon が確認できず気づいてない場合は Issue でおせーてください。
- アニメーションスピードが異なるのは、縮小したときの見栄えと容量削減のためです。

| Server (Instance) | Original<br>(16x16) | Using<br>(14x14) |
| :---         |     :---:      |     :---:      |
| qoto.org   | <img src="https://res.cloudinary.com/miy/a/2959.gif" title="画像" alt="画像" width="16" height="16"> | ![画像](https://itk.pw/LJ? "画像") |
| freecumextremist.com | <img src="https://res.cloudinary.com/miy/a/1271.png" title="画像" alt="画像" width="16" height="16"> | ![画像](https://itk.pw/kv? "画像") |
| freespeech.group | <img src="https://res.cloudinary.com/miy/a/894.png" title="画像" alt="画像" width="16" height="16"> | ![画像](https://itk.pw/eq? "画像") |
| waifuism.life | <img src="https://res.cloudinary.com/miy/a/1287.png" title="画像" alt="画像" width="16" height="16"> | ![画像](https://itk.pw/kL? "画像") |
| jigglypuff.club | <img src="https://res.cloudinary.com/miy/a/1496.gif" title="画像" alt="画像" width="16" height="16"> | ![画像](https://itk.pw/o8? "画像") |
| fedi.nullob.si | <img src="https://res.cloudinary.com/miy/a/1484.gif" title="画像" alt="画像" width="16" height="16"> | ![画像](https://itk.pw/nW? "画像") |


<hr>

## Hay, Speak in English!
- ごめん。おいらは英語まったくわからん。
- Google or Deeple の翻訳サイト使ってください。

<hr>

# Licence

## EN
- This repository is not licensed as it contains data for each site's favicon image (.webp converted to base64).
- Please use and folk at your own risk...
- The favicon image is copyrighted by each image creator.

## JA
- このリポジトリには、各サイトのファビコンイメージ（.webpがbase64に変換されたもの）のデータが含まれているため、ライセンスはありません。
- ご利用やフォークする場合は自己責任で。。
- favicon 画像は、それぞれの画像作者様に著作権があります。
