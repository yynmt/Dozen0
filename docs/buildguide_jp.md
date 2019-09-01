# Dozen0 ビルドガイド

![](../images/buildguide_0-0.jpg)

## 目次
- [0. 事前準備](#0-事前準備)
  - [キットの内容物](#キットの内容物)
  - [キット以外に必要な部品](#キット以外に必要な部品)
  - [必要工具](#必要工具)
  - [アイコンの説明](#アイコンの説明)
- [1. ソケットのハンダ付け](#1-ソケットのハンダ付け--)
- [2. リセットスイッチのハンダ付け](#2-リセットスイッチのハンダ付け--)
- [3. ProMicroのハンダ付け](#3-promicroのハンダ付け--)
- [4. スイッチの取り付け](#4-スイッチの取り付け)
- [5. ネジ留め](#5-ネジ留め--)
- [6. ファームウェアの書き込み](#6-ファームウェアの書き込み)
  - [動作確認](#動作確認)
  - [QMK Configuratorの利用](#qmk-configuratorの利用)
  - [QMKビルド環境を構築](#QMKビルド環境を構築)
  - [QMK参考リンク](#QMK参考リンク)
- [7. 完成](#7-完成)

---

## 0. 事前準備

### キットの内容物
![](../images/buildguide_0-1.jpg)

|| 名前 | 数量 | 備考 |
|:---:|---|---:|---|
|1|PCB|1||
|2|トッププレート|1||
|3|ボトムプレート|1||
|4|ミラープレート|1||
|5|MXソケット|12||
|6|Chocソケット|12||
|7|リセットスイッチ|1|6x3mm タクトスイッチ|
|8|ネジ|12|M2 4mm(予備2を含む)|
|9|スペーサ(大)|3|M2 7mm|
|10|スペーサ(小)|3|M2 4mm|
|11|スペーサ(黒)|2|M2 6mm|
|12|ゴム足|4|   |

### キット以外に必要な部品
![](../images/buildguide_0-2.jpg)

|| 名前 | 数量 | 備考 |
|:---:|---|---:|---|
|1|キースイッチ|12|Cherry MXもしくはKailh Choc|
|2|キーキャップ(1U)|12||
|3|ProMicro|1|[遊舎工房](https://yushakobo.jp/shop/promicro-spring-pinheader/)より購入可能|
|4|コンスルー|2|[遊舎工房](https://yushakobo.jp/shop/a01mc-00/)より購入可能|
|-|MicroUSBケーブル|1|   |

### 必要工具
- 温調ハンダごて
  - HAKKO [FX600](https://www.hakko.com/japan/products/hakko_fx600.html)がオススメです。
- ハンダ
- ニッパー
- 精密ドライバー(プラス)
  - 適合ドライバーサイズ #0
- 油性ペン
  - 赤と黒をご用意ください。
  - PCB、トッププレート、ボトムプレートの側面に塗ると見栄えがよくなります。

### アイコンの説明
|アイコン|説明|
|:---:|---|
|<img src="../images/icon_solder.png" width="32px">|ハンダ付けを必要とします。|
|<img src="../images/icon_nipper.png" width="32px">|ニッパーを必要とします。|
|<img src="../images/icon_screw.png" width="32px">|ネジ留めを必要とします。|

---

## 1. ソケットのハンダ付け  <img src="../images/icon_solder.png" width="24px">
　PCBにソケットをハンダ付けします。

![](../images/buildguide_1-1.jpg)

　キットには2種類のソケット、Cherry MX用とKailh Choc用が同梱しています。
使用するキースイッチに合わせてどちらのソケットを使用するか選びます。
もちろん2種類両方のソケットをハンダ付けしても構いません。
今後、異なるキースイッチに交換することがある場合は両方のソケットをハンダ付けしましょう。

![](../images/buildguide_1-2.jpg)

　PCB裏面の白枠に合わせて12個(24個)のソケットをハンダ付けします。
ソケットはそれぞれ2箇所のハンダ付けが必要です。

    ！！！注意！！！
    PCBからソケットが浮かないように気を付けてください。
    PCBからソケットが浮いてしまうとボトムプレートと干渉します。

---

## 2. リセットスイッチのハンダ付け  <img src="../images/icon_nipper.png" width="24px"><img src="../images/icon_solder.png" width="24px">

　PCBにリセットスイッチをハンダ付けします。

![](../images/buildguide_2-1.jpg)

　リセットスイッチの足がボトムプレートに干渉するため、事前に足をニッパーで少し切ります。
PCBに何度か足を差し込みながら切る長さを確認するとよいでしょう。

![](../images/buildguide_2-2.jpg)

　PCB表面からリセットスイッチを取り付け、PCB裏面からハンダ付けします。
PCBの角に近い側のスルーホールは熱が逃げやすくハンダの乗りが悪いので、十分に熱してからハンダを流し込んでください。

---

## 3. ProMicroのハンダ付け  <img src="../images/icon_solder.png" width="24px">
　ProMicroとコンスルーをハンダ付けします。

　大抵の場合、ProMicroには12連のピンヘッダが2つ付属しています。このピンヘッダを使用しても組み立ては可能ですが、Dozen0の組み立てにはコンスルーの使用を推奨しています。コンスルーを使用するとProMicroをPCBから容易に取り外しできるようになります。万が一、ProMicroが何らかの要因で破損した際に非常に便利です。また、コンスルーはProMicroにのみハンダ付けを行えばいいので組み立ても容易になります。

|![](../images/buildguide_3-1.jpg)|![](../images/buildguide_3-2.jpg)|
|---|---|

　コンスルーには推奨される取り付け向きがあります。
画像のようにコンスルー側面の四角い穴がProMicroに寄った向きで取り付けます。
さらに、2つのコンスルーの側面の四角い穴は両方同じ向きとなるようにします。

![](../images/buildguide_3-3.jpg)

　コンスルーの向きをしっかり確認できたらProMicroとコンスルーを24箇所ハンダ付けします。

    ！！！注意！！！
    絶対にPCBとコンスルーをハンダ付けしないでください。
    誤ってPCBとコンスルーをハンダ付けすると取り外しは非常に困難です。

## 4. スイッチの取り付け
　トッププレートの上面から前後の向きに気を付けキースイッチを取り付けます。

![](../images/buildguide_4-1.jpg)

　トッププレートには向きがあります。斜めの斜線が細かく入った面が表です。
そしてフレームの幅が広いほうが手前となります。画像のとおりにキースイッチを取り付けてください。

|![](../images/buildguide_4-2.jpg)|![](../images/buildguide_4-3.jpg)|
|---|---|

　キースイッチを12個取り付け終わったら次にPCBを取り付けます。
キースイッチのピンの折れ曲がりに気を付けてPCBを取り付けます。
キースイッチとPCBが隙間なく固定されていることを確認します。
コンスルーをハンダ付けしたProMicroをPCBに取り付けます。

![](../images/buildguide_4-4.jpg)

---

## 5. ネジ留め  <img src="../images/icon_screw.png" width="24px">
　順にネジを留めていきます。

![](../images/buildguide_5-1.jpg)

　まずPCBにスペーサ(黒)を2本立てて裏面からネジ留めします。
スペーサ(黒)にミラープレートを被せてネジ留めします。

![](../images/buildguide_5-2.jpg)

　次に、ボトムプレート裏面にゴム足を貼り付けます
大きな斜線のある面が裏面です。

![](../images/buildguide_5-3.jpg)

　そしてスペーサをボトムプレート表面に3本立て、裏面からネジ留めします。
使用するスペーサは使用しているキースイッチの種類に応じて違います。
Cherry MXスイッチの場合はスペーサ(大)、Kailh Chocスイッチの場合はスペーサ(小)を使用します。

|![](../images/buildguide_5-4.jpg)|![](../images/buildguide_5-5.jpg)|
|---|---|

　最後に、トッププレートとPCBをボトムプレートに合わせ、トッププレート表面からネジ留めします。
Dozen0のハードウェアはこれで完成です。

---

## 6. ファームウェアの書き込み
　完成したDozen0のハードウェアにファームウェアを書き込んでマクロパッドとして利用できるようにします。Dozen0はQuantum Mechanical Keyboard Firmware(以下、QMK)に対応しており、自由にキーレイアウトをカスタマイズすることが可能です。

### 動作確認
　動作確認のためデフォルトのファームウェアを書き込むには、[QMK Toolbox](https://github.com/qmk/qmk_toolbox)を利用して以下のファームウェアファイル(.hex)をDozen0に取り付けたProMicroに書き込むと動作確認を行うことができます。

- Dozen0 デフォルトファームウェア - [dozen0_default.hex](https://qmk.fm/compiled/dozen0_default.hex)

　デフォルトのキー配列は以下のとおりです。

![](../images/default_layout.png)

　キーレイアウトをカスタマイズするにQMKのビルドが必要となります。QMKのビルドには2つの方法があります。

### QMK Configuratorの利用
　[QMK Configurator](https://config.qmk.fm/)はPCブラウザ上で動作するQMKのビルド環境です。QMK Configuratorを利用して得られたファームウェアファイル(.hex)は前述のQMK Toolboxを利用することでDozen0に取り付けたProMicroに書き込むことができます。

### QMKビルド環境を構築
　QMKのビルドと書き込みを行う環境をお使いのコンピュータに構築し、ビルドから書き込みまで一連の作業をまとめて行う方法です。詳しい方法はお使いのコンピュータの環境により大きく異なるため、ご自身でお調べ下さい。

### QMK参考リンク
- [QMK Toolbox - https://github.com/qmk/qmk_toolbox](https://github.com/qmk/qmk_toolbox)
- [QMK Configurator - https://config.qmk.fm/](https://config.qmk.fm/)
- [Quantum Mechanical Keyboard Firmware - https://github.com/qmk/qmk_firmware/](https://github.com/qmk/qmk_firmware/)
- [QMK Firmware - https://docs.qmk.fm/](https://docs.qmk.fm/)
- [Install Build Tools - QMK Firmware - https://docs.qmk.fm/#/getting_started_build_tools](https://docs.qmk.fm/#/getting_started_build_tools)

---

## 7. 完成
　あなただけのオリジナルマクロパッドの完成です。
![](../images/buildguide_7-1.jpg)
　机の上を片付けて完成したDozen0の写真を撮影しましょう。
