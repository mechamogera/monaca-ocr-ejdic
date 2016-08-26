# monaca-ocr-ejdic

## 概要

英論文を読む時に英単語を認識して単語帳にしてくれるなにか
をやっつけで作ってみた。

携帯で撮影した画像を選択すればOCRした結果を表示し、各単語をクリックしたら英和辞書から内容をとってきて表示するようにした。

## 利用しているサービス

* 開発環境：[Monaca](https://ja.monaca.io/)
 * Onsen UI V2 JS Minimumテンプレートを作ってプロジェクトを作成してほぼindex.htmlのみ編集
* OCR：[Google Cloud Vision API](https://cloud.google.com/vision/)
* 英和辞書：[デ辞蔵Webサービス](https://dejizo.jp/dev/index.html)

## 判明している課題

* UI適当
* エラー処理適当
* 利用している英和辞書固有の問題がありそう
 * 英論文用の用語がない
 * Accentsが引けなかったりする
 * iframeで辞書サイトを表示するようにしてみたがframe表示が禁止されていたりhttp/https混在でうまくいかなかった
 
## アプリを動作させるためには

Google Cloud Vision API用のAPIキーを作成してindex.htmlの"[APIキー]"部分に設定する必要がある。
APIキーの取得方法については[Cloud Vision APIの使い方まとめ (サンプルコード付き)](https://syncer.jp/cloud-vision-api)など参照

## スクリーンショット

![サムネイル](https://raw.githubusercontent.com/mechamogera/monaca-ocr-ejdic/master/image.png)
