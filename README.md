# Vision ビルドガイド
[Vision キーボードキット](https://satt.booth.pm/items/2148976)のビルドガイドです。  
組み立ての際は、本ビルドガイドの最後まで目を通した上で作業をはじめることを推奨します。

## 準備
最初に必要な部品および工具があることを確認します。
### 同梱品の確認
|パーツ|備考|
|---|---|
|トップケース|-|
|ボトムケース|-|
|ウェイト|-|
|M2-6mmネジ|12個（ケースに取り付け済み）|
|M3-6mm皿ネジ|4個（ケースに取り付け済み）|
|φ4-7mm樹脂スペーサー|4個（ケースに取り付け済み）|
|M3樹脂ナット|4個（ケースに取り付け済み）|
|1.5mm六角レンチ|1本|
|2.0mmボールポイント六角レンチ|1本|
|アルミプレート|1枚|
|PCB|1枚|
|M2-3.5mmスペーサー|7個|
|M2-3mmネジ|14個|
|スタビライザシム|4個|

### 追加で用意する部品
|部品|個数|
|---|---|
|USB C ケーブル|1本|
|MX互換スイッチ|47-48個|
|MX互換2uスタビライザ|0-2個（後述の理由でDurock/Everglide製がおすすめです）|
|MX用キーキャップ|47-48個|

### 工具
組み立てにはキットに含まれる工具に加え、以下が必要となります
|工具|備考|
|---|---|
|#0番プラスドライバー|-|
|はんだごて|Solderable基板を選択した場合のみ|

### 注意事項
* 一部のパーツは非常に重いです。落下、挟まれ等による怪我がないよう十分に注意して作業を進めてください。
* ネジを締めすぎないように注意してください。無理に力をかけてレンチを回すとネジ穴/頭が破損し、ケースが使用できなくなる恐れがあります。

## 組み立て
### PCBを組み立てる
1. 

### ケースを組み立てる
1. 


## キーマップ

VisionのPCBには標準でVIAファームウェアが書き込まれています。

以下の手順でキーマップを書き換えることができます。

1. [VIA](https://github.com/the-via/releases/releases/)の最新版をリンク先からダウンロードしインストールします

1. VIAを起動し、VisionをPCに接続します。PCBが認識されると自動でVisionのキーマップ編集画面が表示されます

1. `LAYOUTS`タブを選択し、右シフトの構成に合わせて`Long RShift`の設定を変更します
![firmware](./img/firmware/via1.png)

1. `KEYMAP`タブを選択し、キーマップを変更します。変更したいキーの位置をクリックし、下部のキー一覧から必要なキーを選択するとキーマップが都度に書き換えられます。左上の`LAYER`の数字を押すことでレイヤーを選択することができます
![firmware](./img/firmware/via2.png)

* 稀にVIAで表示されるキーマップと実際に書き込まれたキーマップが合致しない等の問題が発生する場合があります。そのような場合は、以下の手順でVIAのリセットを行ってください
  - USBケーブルを抜き、左上のキー（上側のマクロキー）を押しながら再度USBケーブルをさして電源を投入する

VIAに実装されていない機能を使用したい場合は、[QMKファームウェア](https://github.com/qmk/qmk_firmware)をコンパイルし、PCBに書き込む必要があります。
