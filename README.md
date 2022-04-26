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

インスタンスリスト不定期更新な感じ。

## instances.db

- SQLite 形式です。

- Table: instances に instances.tsv を格納しています。


# Q and A
<hr>
## うちのインスタンスがねえじゃん or 入れてくれるな！
- 手動更新なので許してください。追加や抹消の依頼は Issue してください。
- 開設や閉鎖のご報告 Issue ありましたら助かります。

## favicon は、自動取得し形式を変換（キャッシュプロキシー的な？）するか、Google か Hatena の favicon ツールをフリーライドすればいいのではないですか？
- それもいい手ですが、Google 側では、近年仕様変更があったため、使わないようにしています。
- Hatena も表示速度がよくないので、使うにしても申し訳ない感じです。
- 使わない理由としては、アニメーション favicon にも対応させたかったためで、手動且つ個別で変換させています。
- 稀に、SVG 形式の favicon を設定するインスタンスが存在し、それにも対応させるためには、そら手動にでもなります。
- またサイズも異なるため（16x16 ではなく 14x14 となっています）、逐一手動で変換しています。

## とりあえず、うちの favicon やロゴを無許可で使わないでくれます？
- 画像作者名を明記することなくこのような公開の形となってしまい、全国のツク▢ークンのみなさまには申し訳ない気持ちでいっぱいです。
- とりあえず Issue してください。すぐにデフォルトに戻します。。
- SNS開発者さんも、ロゴ画像使用についてなにかあれば、Issue してくだされば、対処していきます。

## Hay, Speak in English!
- ごめん。英語まったくわからん。


# Licence

## EN
- This repository is not licensed as it contains data for each site's favicon image (.webp converted to base64).
- Please use and folk at your own risk...

## JA
- このリポジトリには、各サイトのファビコンイメージ（.webpがbase64に変換されたもの）のデータが含まれているため、ライセンスはありません。
- ご利用やフォークする場合は自己責任で。。
