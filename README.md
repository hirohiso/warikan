# 飲み会の割り勘ドメイン ( BIGLOBE 教育用 )

本課題は BIGLOBE の DDD 教育用に [割り勘ドメイン](https://github.com/j5ik2o/warikan-domain-java) を簡易にしたものです。

## 成果物

各問の成果物は以下の 2 つとします。

1. モデル

2. 実装 ( UT 含む )

## 実装言語

- Java 8

- Groovy ( UT のみ )

## 問 1

下記の仕様を満たすモデルと実装を作成してください。

- 飲み会には **支払い区分** ( 多め、普通、少なめ ) が存在します。

- 支払い区分ごとに **支払い割合** が決まっています。

  - 支払い割合は固定とします ( 飲み会ごとに変更できる必要はありません ) 。

- システムに飲み会の参加者 ( 支払い区分ごと ) と **請求金額** を入力すると、支払い区分ごとの **支払い金額** と **不足金額** を返します。

  - 例えば ( 多め、普通、少なめ ) = ( 1, 2, 0 ) の 3 人で飲み会をして請求金額が 20000 円だった場合、1 人あたりの支払金額は ( 多め、普通 ) = ( 7500, 6250 ) で、不足金額は 0 円になります。
  - 上記サンプルは **多めの人は普通の人の 2 割り増しで支払う** として計算した場合です。支払い割合は回答者が自由に設定して構いません。

- 割り勘の方法は自由に決めて良いです。

  - 例えば、支払金額は 100 円単位としても良いです。この場合、上記サンプルの 1 人当たりの支払い金額は ( 多め、普通 ) = ( 7500, 6200 ) で、不足金額は 100 円になります。

## 問 2

問 1 の仕様を以下のように変更してください。

- 飲み会ごとに支払い割合を変更できる。

  - 飲み会ごとの支払い割合をどこかに保存する必要がありますが、保存先は DB でもファイルでもなんでも良しとします。
