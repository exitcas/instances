# instances

[InstanceTicker/InstanceTicker](https://github.com/InstanceTicker/InstanceTicker) で使ってるインスタンスリストです。

各SNSロゴや各インスタンスの favivon などの画像データを含みますので、取り扱い注意であることをご留意ください。

## instances.tsv

- TSV で管理している感じです。

- Google Spreadsheet で作成しています。

- SNS番号 が 0 である場合は、SNS の種類とそのデフォルトのデータとなっており、空欄の場合は無視します。 

|  id  |  sns |  host  |  domain  |  text  |  width  |  tcolor  |  bcolor  |  scolor  |  bicon  |  sicon  |  eicon  |  iicon  |  url  |  entry  |  exity  |  icon  |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
|  id  |  SNS番号 |  ホスト  |  索引用ドメイン  |  表示名  |  画像の横幅  |  表示名色  |  背景色  |  表示名影色  |  画像背景色個別指定  |  同一画像をidで指定  |  eicon  |  画像のライセンス情報  |  Wiki等のリンク  |  エントリ日 |  非エントリ日  |  画像（Webp の Data URI Scheme） |

## instances.db

- SQLite 形式です。

- Table: instances に instances.tsv を格納しています。


# Q and A

<hr>

## うちのインスタンスがねえじゃん or 入れてくれるな！
- 手動更新なので許してください。追加や抹消の依頼は Issue してください。
- 開設や閉鎖のご報告 Issue ありましたら助かります。

<hr>

## favicon はキャッシュプロキシにするか、Google か Hatena の favicon ツールをフリーライドすればいいのではないですか？
- それもいい手ですが、Google 側では、近年仕様変更があったため、使わないようにしています。
- Hatena も表示速度がよくないので、使うにしても申し訳ない感じです。
- 使わない理由としては、アニメーション favicon にも対応させたかったためで、手動且つ個別で変換させています。
- 稀に、SVG 形式の favicon を設定するインスタンスが存在し、それにも対応させるためには、そら手動にでもなります。
- またサイズも異なるため（16x16 ではなく 14x14 となっています）、逐一手動で変換しています。
- ある Misskey サーバーでは、縦横 1000px を超える尋常じゃない画像サイズで favicon にしてるケースもあり、信用ならねえ。

<hr>

## アニメーション favicon の Difference を提示しなさい！

- アニメーション favicon が確認できたのは以下のとおりです。
- 気づいてない場合は Issue でおせーてください。

| Server (Instance) | Original <br>(16x16) | Using |
| :---         |     :---:      |     :---:      |
| qoto.org   | <img src="https://qoto.org/favicon.ico" title="画像" alt="画像" width="16" height="16"> | ![画像](https://itk.pw/LJ? "画像") |
| freecumextremist.com | <img src="https://freecumextremist.com/favicon.png" title="画像" alt="画像" width="16" height="16"> | ![画像](https://itk.pw/kv? "画像") |
| freespeech.group | <img src="https://freespeech.group/favicon.png" title="画像" alt="画像" width="16" height="16"> | ![画像](https://itk.pw/eq? "画像") |
| jigglypuff.club | <img src="https://jigglypuff.club/files/0118e4bf-ef61-4565-805e-7fa6271beb0a" title="画像" alt="画像" width="16" height="16"> | ![画像](https://itk.pw/o8? "画像") |
| fedi.nullob.si | <img src="https://cdn.nullob.si/file/misskey/null/7023a0f6-cf72-4215-8145-5ef3e059820e.gif" title="画像" alt="画像" width="16" height="16"> | ![画像](https://itk.pw/nW? "画像") |


<hr>

## Misskey みたいに favicon 直リン参照にすれば？
- まったく無関係の外部サイトの画像を link rel="icon" で設定するお行儀の悪い Misskey サーバーが数件ありました（誰だよ！某Wikiサイトの画像直リンしてる不届き者は！）。
- このようなケースもあり、 Misskey がこの方法でやってることに少し疑問ではある。

<hr>

## とりあえず、うちの favicon やロゴを無許可で使わないでくれます？
- 画像作者名を明記することなくこのような公開の形となってしまい、申し訳ない気持ちでいっぱいです。
- とりあえず Issue してください。すぐにデフォルトに戻します。。
- SNS開発者さんも、ロゴ画像使用についてなにかあれば、Issue してくだされば、対処していきます。

<hr>

## Hay, Speak in English!
- ごめん。英語まったくわからん。

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
