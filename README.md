## 目次

- [mtk64ebt](#mtk64ebt)
    - [トラックボール＆ロータリーエンコーダー付きBluetooth接続自作キーボード](#トラックボールロータリーエンコーダー付きbluetooth接続自作キーボード)
    - [Rev.3の特徴](#rev.3の特徴)
    - [フットスイッチ](#フットスイッチ)
- [オンラインストア](#オンラインストア)
- [本体以外に必要なパーツとおすすめ商品](#本体以外に必要なパーツとおすすめ商品)
- [特徴](#特徴)
- [フットスイッチ拡張基板](#フットスイッチ拡張基板)
- [使用方法](#使用方法)
    - [モジュール間接続](#モジュール間接続)
    - [USB接続](#usb接続)
    - [Bluetooth接続](#bluetooth接続)
    - [ロープロファイル化](#ロープロファイル化)
    - [フットスイッチ拡張キット](#フットスイッチ拡張キット)
    - [フットスイッチ無線化モジュール](#フットスイッチ無線化モジュール)
- [ファームウェア](#ファームウェア)
    - [左右構成用ファームウェア](#左右構成用ファームウェア)
    - [左右＋フットスイッチ無線化モジュール用ファームウェア](#左右フットスイッチ無線化モジュール用ファームウェア)
    - [左右＋ドングルモジュール用ファームウェア](#左右ドングルモジュール用ファームウェア)
    - [左右＋ドングルモジュールOLED用ファームウェア](#左右ドングルモジュールoled用ファームウェア)
    - [左右＋ドングルモジュールOLED＋フットスイッチ用ファームウェア](#左右ドングルモジュールoled用ファームウェアフットスイッチ用ファームウェア)
    - [左ボール右エンコーダー＋ドングルモジュールOLED用ファームウェア](#左ボール右エンコーダー＋ドングルモジュールoled用ファームウェア)
    - [ファームウェア書き込み](#ファームウェア書き込み)
- [ソースコード](#ソースコード)
    - [左右構成用ファームウェアブランチ](#左右構成用ファームウェアブランチ)
    - [左右＋フットスイッチ無線化モジュール用ブランチ](#左右フットスイッチ無線化モジュール用ブランチ)
    - [左右＋ドングルモジュール用ブランチ](#左右ドングルモジュール用ブランチ)
    - [左右＋ドングルモジュールOLED用ブランチ](#左右ドングルモジュールoled用ブランチ)
    - [左右＋ドングルモジュールOLED＋フットスイッチ無線化モジュール用ブランチ](#左右＋ドングルモジュールOLED＋フットスイッチ無線化モジュール用ブランチ)
    - [左ボール右エンコーダー＋ドングルモジュールOLED用ブランチ](#左ボール右エンコーダー＋ドングルモジュールoled用ブランチ)
- [ZMK Studioでキーマッピング変更](#zmk-studioでキーマッピング変更)
    - [ブラウザ版 ZMK Studio](#ブラウザ版-zmk-studio)
    - [アプリ版 ZMK Studio](#アプリ版-zmk-studio)
- [KeymapEditorでキーマッピング変更](#keymapeditorでキーマッピング変更)
- [トラックボール設定](#トラックボール設定)
    - [トラックボール設定変更](#トラックボール設定変更)
    - [レイヤー設定変更](#レイヤー設定変更)
    - [トラックボール設定値調整](#トラックボール設定値調整)
- [ケースデータ](#ケースデータ)

# mtk64ebt
<img src="image/rev3/0.mtk64ebt_b_FLR.jpg" width="80%" style="border: 1px solid;"/><br>

### トラックボール＆ロータリーエンコーダー付きBluetooth接続自作キーボード

mtk64ebtは、親指操作トラックボールとロータリーエンコーダーを搭載した完全ワイヤレス接続分割式キーボードです。

トラックボールとエンコーダーの組み合わせにより、直感的で効率的な操作を実現します。

ワイヤレス接続によりケーブルの煩わしさから解放され、どこへでも快適に持ち運べます。

はんだ付けとケースの組み立てが完了している半完成キットです。キースイッチとキーキャップ、トラックボールを取り付けるだけで、すぐに使用を開始することができます。

#### Rev.3の特徴
基板設計とケース設計を更新してRev.3になりました。

##### バッテリーケースのスリム化
部品配置の見直しにより、バッテリーサイズはそのままでバッテリーケースをスリム化しました。(バッテリーケース部厚み 22mm → 18.5mm)
ケース形状も変更してすっきりした見た目になっています。

<img src="image/rev3/3.mtk64ebt_b_side.jpg" width="60%" style="border: 1px solid;"/><br>

##### LEDレンズ
インジケーターLEDにレンズを追加したことにより、視認性が向上しました。
バッテリー残量、接続状態、レイヤー切り替えが確認しやすくなりました。

<img src="image/rev3/mtk64ebt_rev3_LED.JPG" width="60%" style="border: 1px solid;"/><br>

##### フットスイッチ完全無線化
ケーススリム化と生産性向上のため、左右キーボードのフットスイッチ有線接続ジャックを廃止。付属の無線フットスイッチキットによる無線接続に一本化しました。

<img src="image/fooswitch_btmodule_parts.jpg" width="60%" style="border: 1px solid;"/>

##### ベアリング仕様トラックボールケース対応
トラックボール支持球をベアリングに置き換えるケースデータを公開しています。
ご自身でプリントしてベアリング仕様に変更可能です。

<img src="image/rev3/mtk64ebt_bearing_case.jpeg" width="60%" style="border: 1px solid;"/>

ケースの他に、ベアリング(内径 1.5mm 外径 4mm 幅 2mmのシールドタイプ)とM1.4のネジが必要です。
* ベアリング : [ミネベアミスミ DDL-415ZZ](https://amzn.asia/d/fXq8wOI)
* ネジ : [M1.4-0.3 6mm](https://amzn.asia/d/c3SDJWJ)

##### ベアリング仕様トラックボールケースデータ
[mtk64ebt_rev3_ballBearingCase_RH.3mf](casedata/rev3/mtk64ebt_rev3_ballBearingCase_RH.3mf)<br>[mtk64ebt_rev3_bodyBallBeringBottmn_RH.3mf](casedata/rev3/mtk64ebt_rev3_bodyBallBeringBottmn_RH.3mf)

<img src="image/rev3/mtk64ebt_bearing_case_trace.jpeg" width="60%" style="border: 1px solid;"/><br>

### フットスイッチ
[市販のUSBフットスイッチ](https://amzn.asia/d/h7wMR24)の基板を付属のフットスイッチ拡張基盤に差し替えてmtk64の拡張無線フットスイッチとして使用可能です。

フットスイッチも含めて完全ワイヤレス化可能となり、デスク環境からケーブルの煩わしさを一掃できます。

フットスイッチ拡張基板はご自身ではんだ付けと組み立てが必要なキットです。

<img src="image/footswitch.jpg" width="80%" style="border: 1px solid;"/><br>

> [!CAUTION]
> バッテリー駆動用に[リチウムポリマーバッテリー](https://amzn.asia/d/1ivvf2l)を使用します。
> バッテリーの取り扱いを誤った場合や、製造上の不具合により、破裂や発火の恐れがあります。
> 組み立ての際に動作確認は行っていますが、絶対に安全であることを保証するものではありません。
> バッテリーは使用者の責任において使用してください。
> バッテリー、本体基板、その他構成部品を含め、本製品による事故および不利益損害についての一切の責任は使用者にあり、当方が責任を持つものではありません。

* バッテリー駆動時および、充電時は本体側面のバッテリー駆動用スイッチをONにしてください。
* バッテリー不使用時はバッテリー駆動用スイッチをOFFにしてください。
* 充電中は、発火・破裂しても被害のない場所を選定し、周囲に延焼するものを置かないようにして下さい。また充電中はその場を離れ ることなく常に Li-Po の充電状態を監視して下さい。
* バッテリーの取り扱いや製造上の不具合について懸念がある場合や、ご自身の責任で使用できない場合、キーボードからバッテリーを取り外してご使用ください。
USB端子からの給電のみでキーボードを使用できます。

## オンラインストア
https://mentako-ya.myshopify.com

## 本体以外に必要なパーツとおすすめ商品

キーキャップMX互換: [CORSAIR PBT DOUBLE-SHOT 交換用カラーキーキャップセット - 日本語108キー, Arctic White - CH-9911040-JP](https://amzn.asia/d/1FShFiO)

キーキャップChocV2: [XVX ロープロファイル PBT キーキャップ](https://amzn.asia/d/7V1A6T4)

キーキャップChocV1: [Chocfox CFX keycap](https://chosfox.com/products/chocfox-cfx-choc-keycaps?bg_ref=3KtshOemT6)

トラックボール: [ぺリックス PERIPRO-303WH 34mm](https://amzn.asia/d/1paUF5C)

USB Type-cケーブル: https://amzn.asia/d/h8pfZIJ

クッションゴム: [ダイソー クッションゴム透明](https://jp.daisonet.com/products/4903409153222)

T5ドライバー(メンテナンス用): [アネックス(ANEX) ドライバー ヘクスローブ T4x50](https://amzn.asia/d/8RFoACS)

## 特徴

#### 標準的な６０％キーボード相当のキースイッチ＋フットスイッチ拡張で、一般的なキーボードからの移行コストを抑え、フルキーボード以上の操作性を実現します

[ZMK Studio](#zmk-studioでキーマッピング変更)を使用して、キーマッピングを簡単に変更することができます。

<img src="image/zmk_studio_app.png" width="80%" style="border: 1px solid;"/><br>

#### 親指操作トラックボールを搭載しています

キー操作時のトラックボールへの干渉を避けるため、トラックボールの取り付け位置は極力低くオフセットされています

トラックボールケース底面もフラット形状にして、全体の高さを抑えました。

<img src="image/ball_case.png" width="80%" style="border: 1px solid;"/><br>

PMW3610トラックボールセンサーは、センサー基板を小型化して取り付け角度を20度に設定しました.

テンティングなしでも快適にトラックボールを操作することができます。

<img src="image/ball_sensor.png" width="80%" style="border: 1px solid;"/><br>

#### Alps alpine製の低背エンコーダーが２つ搭載されています

30クリックの回転操作とプッシュスイッチが付いており、直感的な操作が可能です。

<img src="image/mtk64erp_encoder.jpg" width="80%" style="border: 1px solid;"/><br>

#### Choc V1、[V2（固定ピンなしモデル）](https://ja.aliexpress.com/item/1005007361067887.html)、およびMX互換キースイッチを全てのキーに取り付けることが可能です

<img src="image/mtk64erp_switches.jpg" width="80%" style="border: 1px solid;"/><br>
<a href="https://ja.aliexpress.com/item/1005007361067887.html"><img src="image/kailh_v2_deepsea.png" width="40%" style="border: 1px solid;"/></a>
<a href="https://ja.aliexpress.com/item/1005007404357477.html"><img src="image/kailh_v2_shadow.png" width="40%" style="border: 1px solid;"/></a><br>

親指部分のみをロープロファイル化することも可能です。

追加の親指キースイッチは、操作性を向上させるため、さらに一段低くオフセットされています。

<img src="image/rev3/5.mtk64ebt_lowpro.jpg" width="80%" style="border: 1px solid;"/><br>

#### MCUに[Seeed Studio XIAO nRF52840](https://jp.seeedstudio.com/Seeed-XIAO-BLE-nRF52840-p-5201.html)を使用しており、無線接続の自作キーボードで課題となる技適対応もクリアしています

技術基準適合証明番号：[211-220207](https://www.tele.soumu.go.jp/giteki/SearchServlet?pageID=jk01&NUM_TYPE=1&NUM=211-220207)

<img src="image/mtk64ebt_mcu.png" width="80%" style="border: 1px solid;"/><br>

無線接続では、有線接続に比べてポーリングレートが低くなりますが、通常利用には問題なく使用することが可能です。（約70hz）

<img src="image/cpi_test_bt.png" width="80%" style="border: 1px solid;"/><br>

USB接続時には、ポーリングレートが向上し、よりスムーズに動作します。（約220hz）精密なトラックボール操作が求められる場面で効果的です。

有線接続時も右手のみUSB接続となり、左手側は無線接続となるので、USBケーブル１本だけで接続となります。左右間接続用のTRRSケーブルは使用しません。

<img src="image/cpi_test_usb.png" width="60%" style="border: 1px solid;"/><br>

#### ドングルを利用可能です

[Seeed Studio XIAO BLE](https://jp.seeedstudio.com/Seeed-XIAO-BLE-nRF52840-p-5201.html) もしくは [nrf54820搭載モジュール](https://www.switch-science.com/products/5531) をドングルとして使用することで、左右のキーボードは無線接続のまま、有線接続相当のポーリングレート（約110~220hz）で動作します。

<img src="image/rev3/mtk64ebt_dongle.jpg" width="60%" style="border: 1px solid;"/><br>

[mtk64ebt ドングル使用時ポーリングレート計測ムービー](https://www.youtube.com/embed/7DrP1KA7Fw4?list=PL_GJMtxZ-TgovRiROU55VTm1dNuUvYyni)

<img src="image/rev3/mtk64ebt_pollingrate.png" width="60%" style="border: 1px solid;"/><br>

#### ドングルにOLEDを取り付けて動作状況を表示できます

[0.96インチ 128×64ドットOLED(SSD1306)](https://akizukidenshi.com/catalog/g/g112031/)のGND,VCC,SCL,SDA を[XiaoBLEの GND,3v3,D10,D9 ](https://files.seeedstudio.com/wiki/XIAO-BLE/pinout2.png)に結線してください。

OLEDのピンヘッダ位置とXiaoBLEの端子位置を合わせてあるので、配線なしでピンヘッダで直付も可能です。

注：リセットスイッチが押しづらいので工夫が必要です。

<img src="image/rev3/mtk64ebt_dongle_display.jpg" width="60%" style="border: 1px solid;"/><br>
<img src="image/rev3/mtk64ebt_dongle_display_2.jpg" width="60%" style="border: 1px solid;"/><br>

#### 本体基盤キットを使用したカスタマイズが可能です

作例：左ボール 右エンコーダ ドングル OLED
（ファームウェア、ケースデータは各セクションを参照）
<img src="image/rev3/10.mtk64ebt_leftball.jpg" width="60%" style="border: 1px solid;"/><br>


#### セントラルのLEDで現在のレイヤーが確認できるようになりました。
```
レイヤー０ ⚫️Black（無点灯）
レイヤー１ 🟣Magenta トラックボール精密モード
レイヤー２ 🔵Cyan    トラックボールモード
レイヤー３ 🟡Yellow  スクロールモード
レイヤー４ 🟢Green
レイヤー５ 🔵Blue
レイヤー６ ⚪️White   自動マウスレイヤー
```

## フットスイッチ拡張基板

[市販のUSBフットスイッチ](https://amzn.asia/d/h7wMR24)の基板を付属のフットスイッチ拡張基盤に差し替えてmtk64のフットスイッチとして使用可能です。

フットスイッチはmtk64の一部として機能するので、レイヤー切り替えやカスタムキーなどキーボード固有の操作が可能です。

<img src="image/mtk64erp_footswitch_4.jpg" width="40%" style="border: 1px solid;"/>
<img src="image/mtk64erp_footswitch_5.jpg" width="36%" style="border: 1px solid;"/><br>

フットスイッチ無線化モジュールに接続して、無線フットスイッチ構成にアップグレード可能です。

<img src="image/footswitch_extend.jpg" width="60%" style="border: 1px solid;"/><br>  

# 使用方法

## モジュール間接続

mtk64bleは、右手モジュールがセントラルモジュールとして動作します。左手モジュールとフットスイッチは右手モジュールに自動的にペアリングされます。

各モジュールのLEDの色と接続状態については、[こちら](https://github.com/mentako-ya/zmk-rgbled-widget/blob/main/README.md)を参照してください。LEDの色によって接続状態が視覚的に確認できるため、接続状況を簡単に把握することができます。

各モジュール間の接続ができない場合は、ファームウェア書き込み手順に従って、各モジュールの接続をリセットしてください。接続の問題を解決して再度正常に動作させることができます。

## USB接続

右手モジュール（セントラルモジュール）は、PCとUSBで有線接続可能です。USB接続時、セントラルモジュールはPCとの通信を行いながら、充電も行います。

左手モジュールやフットスイッチ無線化モジュール（ペリフェラルモジュール）は、USB接続時に充電のみを行います。これらのモジュールは、操作に必要な通信をすべて無線接続でセントラルモジュールと行います。

> [!CAUTION]
> Rev.2以前の右手モジュールと左手モジュールにある3.5mmジャックはフットスイッチ拡張キットを有線接続するための端子です。
> 左右間の有線接続用ではありません。
> 故障の原因となるので、左右のキーボードをTRSケーブルで接続しないでください。

## Bluetooth接続

レイヤー1の「ESC」「1」〜「5」キーを使用して、最大６か所のBluetooth接続先を切り替えることができます。。

<img src="image/ble_connect_1.png" style="border: 1px solid;"/>

<img src="image/ble_connect_2.png" style="border: 1px solid;"/>

接続時には、表示されたPIN番号を入力し、Enterキーを押下してください。接続後にキーボードが動作しない場合は、リセットボタンを押下して再接続を試みてください。これにより、接続の問題を解決し、正常に動作させることができます。

## ロープロファイル化

Choc V1、V2を使用する場合、トッププレート固定用ネジ(T5 8mm)を外してトッププレートを取り除き、付属の6mmねじに付け替えます。ネジの交換にはT5ドライバーを使用します。

## フットスイッチ拡張キット

フットスイッチ拡張キットはご自身で市販のフットスイッチにキットの基盤を組み込み、はんだ付けをするキットです。

フットスイッチの作成方法は[こちらのビルドムービー](https://youtu.be/NavGAliALVc?si=JpO-xi0RZznjVi4-)をご覧ください。

フットスイッチの接続は3.5mm４極のTRRS端子を使用しますが、有線でフットスイッチを接続する場合（3ccccqaac0cm以上のケーブル長が必要な場合）、市販のTRRSケーブルは線が細すぎるので使用できません

TRRS端子とAWG28~26以上（番号が小さい方が太いです）のケーブルを組み合わせて自作します

[遊舎工房自作ケーブルキット](https://shop.yushakobo.jp/products/self-made-cable?_pos=1&_sid=79305908f&_ss=r&variant=39623339737249)

[AWG26 4Cシールドケーブル](https://shop.oyaide.com/products/mogami_2893.html)

配線の色は使用するケーブルのメーカーによって異なります。
４極プラグの端子側とフットスイッチ拡張キット側の結線は下図を参照してください。

<img src="buildgide/footswitch_kit/plug_to_wire_back.jpg" width="60%" style="border: 1px solid;"/><br>
<img src="buildgide/footswitch_kit/plug_to_wire_up.jpg" width="60%" style="border: 1px solid;"/><br>
<img src="buildgide/footswitch_kit/plug_to_wire_side.jpg" width="60%" style="border: 1px solid;"/>


## フットスイッチ無線化モジュール

フットスイッチ無線化モジュールを使用する場合、[Seeed Studio XIAO nRF52840](https://jp.seeedstudio.com/Seeed-XIAO-BLE-nRF52840-p-5201.html)、[リチウムポリマーバッテリー 902030 PH2.0プラグ付き](https://ja.aliexpress.com/item/1005006838195720.html)、[ケース（ご自身で３Dプリント）](casedata/mtk64ebt_footmodule_case_LH.3mf) が別途必要です。

フットスイッチ拡張キットをフットスイッチ無線化モジュールに接続して、mtk64ebtに無線接続します。

フットスイッチキットとフットスイッチ無線化モジュールを接続する場合、フットスイッチ側の線を極力短くするのがオススメです。

写真は[こちらの４極3.5mm端子付きケーブル](https://www.digikey.jp/ja/products/detail/assmann-wsw-components/A-AV-02-45-28-183-S2/16906692)を15cmにカットして使用しています。

<img src="image/fooswitch_btmodule_parts.jpg" width="40%" style="border: 1px solid;"/>
<img src="image/footswitch_extend.jpg" width="40%" style="border: 1px solid;"/> 


## ファームウェア

### 左右構成用ファームウェア
[mtk64ebt_Right_Left.zip](firmware/mtk64ebt_Right_Left.zip)

> [!IMPORTANT]
> フットスイッチ無線化モジュールを使用しない場合、こちらのファームウェアを使用してください。
> フットスイッチ無線化モジュールとの通信待ちで動作が遅くなる場合があります。

### 左右＋フットスイッチ無線化モジュール用ファームウェア
[mtk64ebt_Right_Left_Foot.zip](firmware/mtk64ebt_Right_Left_Foot.zip)

### 左右＋ドングルモジュール用ファームウェア
[mtk64ebt_Right_Left_Dongle.zip](firmware/mtk64ebt_Right_Left_Dongle.zip)

[Seeed Studio XIAO BLE](https://jp.seeedstudio.com/Seeed-XIAO-BLE-nRF52840-p-5201.html) もしくは [nrf54820搭載モジュール](https://www.switch-science.com/products/5531) をドングルとして使用するファームウェアです

フットスイッチ無線化モジュールと兼用です。フットスイッチをドングルとして使用可能です。

解凍したファイルの mtk64_FOOT rgbled_adapter-seeeduino_xiao_ble-zmk.uf2 をドングルに書き込んでください。

#### 左右＋ドングルモジュールOLED用ファームウェア

[mtk64ebt_Right_Left_Dongle_display.zip](firmware/mtk64ebt_Right_Left_Dongle_display.zip)

解凍したファイルの mtk64_FOOT rgbled_adapter dongle_display-seeeduino_xiao_ble-zmk.uf2 をドングルに書き込んでください。
#### 左右＋ドングルモジュールOLED＋フットスイッチ用ファームウェア

[mtk64ebt_Right_Left_Dongle_disp_foot.zip](firmware/mtk64ebt_Right_Left_Dongle_disp_foot.zip)

解凍したファイルの mtk64_DONGLE rgbled_adapter dongle_display-seeeduino_xiao_ble-zmk.uf2 をドングルに書き込んでください。

解凍したファイルの mtk64_FOOT rgbled_adapter dongle_display-seeeduino_xiao_ble-zmk.uf2 をフットスイッチ無線化モジュールに書き込んでください。

#### 左ボール右エンコーダー＋ドングルモジュールOLED用ファームウェア

[mtk64ebt_Right_Left_Dongle_disp_leftball.zip](firmware/mtk64ebt_Right_Left_Dongle_disp_leftball.zip)

解凍したファイルの mtk64_DONGLE rgbled_adapter dongle_display-seeeduino_xiao_ble-zmk.uf2 をドングルに書き込んでください。

### ファームウェア書き込み

1. 右手キーボード、左手手キーボード、フットスイッチ拡張モジュールのバッテリー駆動スイッチをOFFにする

> [!IMPORTANT]
> バッテリーから給電された状態ではファームウェア書き込み後のリセットが正しく行われません

1. 右手キーボードをPCにUSB接続してリセットボタンを短く2回押下

1. 認識された”XIAO-SENSE"に settings_reset-seeeduino_xiao_ble-zmk.uf2 をドロップ

1. 再度リセットボタンを短く2回押下

1. 認識された”XIAO-SENSE"に mtk64_R rgbled_adapter-seeeduino_xiao_ble-zmk.uf2 をドロップ

1. 左手キーボードをPCにUSB接続してリセットボタンを短く2回押下

1. 認識された”XIAO-SENSE"にsettings_reset-seeeduino_xiao_ble-zmk.uf2をドロップ

1. 再度リセットボタンを短く2回押下

1. 認識された”XIAO-SENSE"に mtk64_L rgbled_adapter-seeeduino_xiao_ble-zmk.uf2 をドロップ

1. フットスイッチ無線化モジュールをPCにUSB接続してリセットボタンを短く2回押下

1. 認識された”XIAO-SENSE"にsettings_reset-seeeduino_xiao_ble-zmk.uf2をドロップ

1. 再度リセットボタンを短く2回押下

1. 認識された”XIAO-SENSE"に mtk64_FOOT rgbled_adapter-seeeduino_xiao_ble-zmk.uf2 をドロップ

1. 右手キーボードをPCにUSB接続、左手キーボードとフットスイッチ拡張モジュールはバッテリー駆動スイッチをONにして給電する

1. 各モジュールのリセットスイッチを１回押下、各モジュール間の接続状態をUSB端子横のLEDで確認

- 右手のLEDはPCとのBluetooth接続状態を表す。
接続中🔵、オープン (アドバタイズ)🟡、切断中🔴 が点滅

- 左手とフットスイッチ無線化モジュールのLEDは、右手（セントラル）とのペアリング状態を表す。
接続の場合は🔵、切断の場合は🔴が点滅

LEDの色と接続状態についての詳細は[こちら](https://github.com/mentako-ya/zmk-rgbled-widget/blob/main/README.md)

## ソースコード

https://github.com/mentako-ya/zmk-config-mtk64

#### 左右構成用ファームウェアブランチ

https://github.com/mentako-ya/zmk-config-mtk64/tree/nofoot

#### 左右＋フットスイッチ無線化モジュール用ブランチ

https://github.com/mentako-ya/zmk-config-mtk64/tree/master

#### 左右＋ドングルモジュール用ブランチ

https://github.com/mentako-ya/zmk-config-mtk64/tree/pmw3610-bj-dongle

#### 左右＋ドングルモジュールOLED用ブランチ

https://github.com/mentako-ya/zmk-config-mtk64/tree/pmw3610-bj-dongle-display

#### 左右＋ドングルモジュールOLED＋フットスイッチ無線化モジュール用ブランチ

https://github.com/mentako-ya/zmk-config-mtk64/tree/pmw3610-bj-dongle-display-foot

#### 左ボール右エンコーダー＋ドングルモジュールOLED用ブランチ

https://github.com/mentako-ya/zmk-config-mtk64/tree/pmw3610-bj-dongle-display_left-ball


## ZMK Studioでキーマッピング変更

ZMK Studioを使用することで、ファームウェア書き換えなしでキーマッピングを簡単に変更することができます。

<img src="image/zmk_studio_app.png" width="60%" style="border: 1px solid;"/><br>

### ブラウザ版 ZMK Studio
ブラウザ版のZMK Studioを使用する場合、右手側のモジュールをUSB接続し、[こちら](https://zmk.studio/)にアクセスしてください。

### アプリ版 ZMK Studio
アプリ版のZMK Studioは、[こちら](https://zmk.studio/download)からダウンロードできます。アプリ版では、無線接続のままキーマップの変更が可能です。ケーブルを接続する手間を省き、より柔軟にキーマッピングを調整することができます。

## KeymapEditorでキーマッピング変更

キースイッチのマッピングだけでなく、エンコーダーのキーマッピング、マクロやコンボの追加、編集をしたい場合、[キーマップエディター](https://nickcoutsos.github.io/keymap-editor/)を使用して変更可能です。

キーマップエディターでマッピングを変更するためには、ご自身のgithubアカウントでmtk64ebtのファームウェアリポジトリをフォークして、キーマップエディターで編集する必要があります。

操作はブラウザだけで完結するので、特別なツールは不要です。

1. https://github.com/mentako-ya/zmk-config-mtk64 を開いて画面右上の「Fork」をクリック

<img src="image/keymap_editor/ke_001.png" width="60%" style="border: 1px solid;"/>

2. 「Copy the master branch only」のチェックボックスを外してから、「Create fork」のボタンをクリック

> [!CAUTION]
> 「Copy the master branch only」のチェックボックスを外してください<br>
> チェックをつけたままフォークすると、master以外のブランチ（nofootなど）がコピーされません

<img src="image/keymap_editor/ke_002.png" width="60%" style="border: 1px solid;"/>

3. ご自身のgitHubアカウントにzmk-config-mtk64のフォークが作成されます

<img src="image/keymap_editor/ke_003.png" width="60%" style="border: 1px solid;"/>

4. https://nickcoutsos.github.io/keymap-editor/ を開いて「GitHUb」のアイコンをクリック

<img src="image/keymap_editor/ke_004.png" width="60%" style="border: 1px solid;"/>

5. 先ほどzmk-config-mtk64のフォークを作成したGitHubのアカウントで認証

<img src="image/keymap_editor/ke_005.png" width="60%" style="border: 1px solid;"/>

6. 「Authorize Keymap Editor」をクリック

<img src="image/keymap_editor/ke_006.png" width="60%" style="border: 1px solid;"/>

7. 「Add Repository」をクリック

<img src="image/keymap_editor/ke_007.png" width="60%" style="border: 1px solid;"/>

8. 「Only select repositories」のラジオボタンを選択 -> 「Select repositories」のプルダウンから「zmk-config-mtk64」を選択 -> 「Install」をクリック

<img src="image/keymap_editor/ke_008.png" width="60%" style="border: 1px solid;"/>

9. キーマップエディター画面でフォークしたリポジトリとブランチを選択　フットスイッチ無線化モジュールを使用する場合masterブランチを選択　フットスイッチ無線化モジュールを使用しない場合nofootブランチを選択

<img src="image/keymap_editor/ke_009.png" width="60%" style="border: 1px solid;"/>

10. キーをクリックして編集　例として、エンコーダーのキーマップを変更

<img src="image/keymap_editor/ke_010.png" width="60%" style="border: 1px solid;"/>

11. saveボタンを押して変更したキーマップをコミット

<img src="image/keymap_editor/ke_011.png" width="60%" style="border: 1px solid;"/>

12. フォークした自分のzmk-config-mtk64リポジトリをブラウザで開く -> Actionsメニュー　-> .github/workflows/build.yml選択 ->  「Run workflow」クリック-> Run workflow

<img src="image/keymap_editor/ke_012.png" width="60%" style="border: 1px solid;"/>

13. 実行完了後、「Merge Output Artifacts」を開く

<img src="image/keymap_editor/ke_013.png" width="60%" style="border: 1px solid;"/>

14. Artifact download URL:のリンクから、ビルドしたファームウェアをダウンロード
<img src="image/keymap_editor/ke_014.png" width="60%" style="border: 1px solid;"/>

15. [ファームウェア書き込み](#ファームウェア書き込み)の手順に従って書き込み



## トラックボール設定

各レイヤーごとの動作について説明します。

* **Layer 0** は通常レイヤーです。これはデフォルトのレイヤーで、通常のキーボード操作が行われます。

* **Layer 1** はマウスレイヤー（精密モード）です。このレイヤーでは、マウスの精密な操作が可能となります。細かい動きが必要な場合に使用します。

* **Layer 2** もマウスレイヤーですが、精密モードではありません。通常のマウス操作が行えます。

* **Layer 3** はスクロールレイヤーです。このレイヤーでは、スクロール操作が可能となります。ウェブページやドキュメントの閲覧時に便利です。

* **Layer 4** と **Layer 5** は未使用のレイヤーです。これらのレイヤーには任意のキーコードを設定することができます。ユーザーの好みに応じてカスタマイズが可能です。

* **Layer 6** は自動マウスレイヤーです。トラックボールの操作が一定距離に達すると、自動的にこのレイヤーに切り替わり、N,Mキーで左右クリック操作が可能になります。
一定時間経過後レイヤーは元のレイヤーに戻ります。

### トラックボール設定変更

トラックボールの設定を変更するには、まずリポジトリをフォークしてソースコードを修正する必要があります。フォークとは、他のユーザーのリポジトリを自分のアカウントにコピーし、自由に変更を加えることができる機能です。

フォークしたソースコードを修正すると、GitHub Actionsにより自動的にビルドが行われます。GitHub Actionsは、リポジトリに変更が加えられた際に自動的にビルドやテストを実行するCI/CDツールです。

ビルドが完了すると、生成されたファームウェアをダウンロードして適用することができます。これにより、トラックボールの設定が反映された新しいファームウェアがキーボードにインストールされ、カスタマイズされた動作を実現することができます。

#### レイヤー設定変更

フォークしたソースの設定を修正する際には、以下のリンク先の設定ファイルを参照してください: [mtk64_R.overlay](https://github.com/mentako-ya/zmk-config-mtk64/blob/master/config/boards/shields/mtk64/mtk64_R.overlay#L58-L67)。

```markdown
    trackball: trackball@0 {
        ~
        ~
        snipe-layers = <1>;
        scroll-layers = <3>;
        automouse-layer = <6>;
    };
```

この設定では、トラックボールの各機能に対応するレイヤーが指定されています。

`snipe-layers`は精密操作用のレイヤー1、

`scroll-layers`はスクロール操作用のレイヤー3、

`automouse-layer`は自動マウス操作用のレイヤー6に設定されています。

もしこれらの機能切り替えを使用しない場合は、不要な設定を削除することができます。これにより、不要な機能が無効化されます。

#### トラックボール設定値調整

フォークしたソースの設定を修正してトラックボールセンサーの感度、自動マウスレイヤーに切り替わるまでの移動距離などを設定可能です。

https://github.com/mentako-ya/zmk-config-mtk64/blob/master/config/boards/shields/mtk64/mtk64_R.conf#L17C1-L67


# ケースデータ

[ケースデータ ダウンロード](casedata/)

[mkt64ebt rev1ケース](https://github.com/mentako-ya/mtk64ebt/tree/main/casedata/rev1)

[mkt64ebt rev2ケース](https://github.com/mentako-ya/mtk64ebt/tree/main/casedata/rev2)

[mkt64ebt rev3ケース](https://github.com/mentako-ya/mtk64ebt/tree/main/casedata/rev3)

[XiaoBleドングルケース](https://github.com/mentako-ya/mtk64ebt/blob/main/casedata/XiaoBle/XiaoBleDongle.3mf)

[XiaoBleドングル+OLEDケース](https://github.com/mentako-ya/mtk64ebt/blob/main/casedata/XiaoBleDongleOLED/XiaoBleDongleOLED.3mf)
