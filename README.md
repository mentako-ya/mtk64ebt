## 目次

- [mtk64ebt](#mtk64ebt)
    - [トラックボール＆ロータリーエンコーダー付きBluetooth接続自作キーボード](#トラックボールロータリーエンコーダー付きbluetooth接続自作キーボード)
- [バッテリーに関する注意](#バッテリーに関する注意)
- [オンラインストア](#オンラインストア)
- [本体以外に必要なパーツとおすすめ商品](#本体以外に必要なパーツとおすすめ商品)
- [特徴](#特徴)
    - [親指操作トラックボール搭載](#親指操作トラックボール搭載)
        - [ベアリング仕様トラックボールケース対応](#ベアリング仕様トラックボールケース対応)
        - [ベアリング仕様トラックボールケースデータ](#ベアリング仕様トラックボールケースデータ)
    - [Alps alpine製低背エンコーダー搭載](#alps-alpine製低背エンコーダー搭載)
    - [MCU (Seeed Studio XIAO nRF52840)](#mcu-seeed-studio-xiao-nrf52840)
    - [フットスイッチ対応](#フットスイッチ対応)
    - [ZMK Studio 対応](#zmk-studio-対応)
    - [ドングル対応](#ドングル対応)
        - [ドングルにOLEDを取り付けて動作状況を表示できます](#ドングルにoledを取り付けて動作状況を表示できます)
    - [LED表示](#led表示)
        - [セントラル側のLEDで現在のレイヤーが確認できます](#セントラル側のledで現在のレイヤーが確認できます)
        - [LEDレンズ](#ledレンズ)
- [フットスイッチ拡張基板](#フットスイッチ拡張基板)
    - [フットスイッチ無線化モジュール（概要）](#フットスイッチ無線化モジュール概要)
    - [本体基板キットを使用したカスタマイズが可能です](#本体基板キットを使用したカスタマイズが可能です)
- [使用方法](#使用方法)
    - [モジュール間接続](#モジュール間接続)
    - [USB接続](#usb接続)
    - [Bluetooth接続](#bluetooth接続)
    - [ロープロファイル化](#ロープロファイル化)
    - [フットスイッチ拡張キット](#フットスイッチ拡張キット)
    - [フットスイッチ無線化モジュール](#フットスイッチ無線化モジュール)
- [ファームウェア](#ファームウェア)
    - [Rev4 と Rev3 以前の違い](#rev4-と-rev3-以前の違い)
    - [Rev4用ファームウェア一覧（main）](#rev4用ファームウェア一覧main)
    - [Rev3用ファームウェアについて](#rev3用ファームウェアについて)
    - [ファームウェア書き込み手順](#ファームウェア書き込み手順)
- [ファームウェアのブランチ構成について](#ファームウェアのブランチ構成について)
- [キーマッピング変更](#キーマッピング変更)
    - [ZMK Studioでキーマッピング変更](#zmk-studioでキーマッピング変更)
        - [ブラウザ版 ZMK Studio](#ブラウザ版-zmk-studio)
        - [アプリ版 ZMK Studio](#アプリ版-zmk-studio)
    - [KeymapEditorでキーマッピング変更](#keymapeditorでキーマッピング変更)
- [トラックボール設定](#トラックボール設定)
    - [CPI（感度）動的変更機能 (Rev4)](#cpi感度動的変更機能-rev4)
    - [トラックボール設定変更](#トラックボール設定変更)
        - [自動マウスレイヤー（Layer 6）の設定変更](#自動マウスレイヤーlayer-6の設定変更)
        - [トラックボール感度（CPI）の初期値調整](#トラックボール感度cpiの初期値調整)
- [ケースデータ](#ケースデータ)

# mtk64ebt
<img src="image/rev3/0.mtk64ebt_b_FLR.jpg" width="80%" style="border: 1px solid;"/><br>

## トラックボール＆ロータリーエンコーダー付きBluetooth接続自作キーボード

mtk64ebtは、親指操作トラックボールとロータリーエンコーダーを搭載した完全ワイヤレス接続分割式キーボードです。

トラックボールとエンコーダーの組み合わせにより、直感的で効率的な操作を実現します。

ワイヤレス接続によりケーブルの煩わしさから解放され、どこへでも快適に持ち運べます。

標準的な６０％キーボード相当のキー数 ＋ フルサイズのキースイッチ ＋ フットスイッチ拡張で、一般的なキーボードからの移行コストを抑え、フルキーボード以上の操作性を実現します。

はんだ付けとケースの組み立てが完了している半完成キットです。キースイッチとキーキャップ、トラックボールを取り付けるだけで、すぐに使用を開始することができます。

## バッテリーに関する注意

> [!CAUTION]
> バッテリー駆動用に[リチウムポリマーバッテリー](https://amzn.asia/d/1ivvf2l)を使用します。
> バッテリーの取り扱いを誤った場合や、製造上の不具合により、破裂や発火の恐れがあります。
> 組み立ての際に動作確認は行っていますが、絶対に安全であることを保証するものではありません。
> バッテリーは使用者の責任において使用してください。
> バッテリー、本体基板、その他構成部品を含め、本製品による事故および不利益損害についての一切の責任は使用者にあり、当方が責任を持つものではありません。

* バッテリー駆動時および、充電時は本体側面のバッテリー駆動用スイッチをONにしてください。
* バッテリー不使用時はバッテリー駆動用スイッチをOFFにしてください。
* 充電中は、発火・破裂しても被害のない場所を選定し、周囲に延焼するものを置かないようにしてください。また充電中はその場を離れることなく常に Li-Po の充電状態を監視してください。
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

### 親指操作トラックボール搭載

キー操作時のトラックボールへの干渉を避けるため、トラックボールの取り付け位置は極力低くオフセットされています

トラックボールケース底面もフラット形状にして、全体の高さを抑えました。

<img src="image/ball_case.png" width="80%" style="border: 1px solid;"/><br>

トラックボールセンサーには超小型・超低消費電力の **PixArt PAW3222**（Rev4）を採用し、センサー基板を小型化して取り付け角度を20度に設定しました。（※Rev3はPMW3610搭載）

テンティングなしでも快適にトラックボールを操作することができます。
また、Rev4ではキー操作によるリアルタイムなCPI動的調整（16段階・不揮発性メモリ保存）に対応しています。

<img src="image/ball_sensor.png" width="80%" style="border: 1px solid;"/><br>

#### ベアリング仕様トラックボールケース対応
トラックボール支持球をベアリングに置き換えるケースデータを公開しています。
ご自身でプリントしてベアリング仕様に変更可能です。

<img src="image/rev3/mtk64ebt_bearing_case.jpeg" width="60%" style="border: 1px solid;"/>

ケースの他に、ベアリング(内径 1.5mm 外径 4mm 幅 2mmのシールドタイプ)とM1.4のネジが必要です。
* ベアリング : [ミネベアミスミ DDL-415ZZ](https://amzn.asia/d/fXq8wOI)
* ネジ : [M1.4-0.3 6mm](https://amzn.asia/d/c3SDJWJ)

#### ベアリング仕様トラックボールケースデータ
[mtk64ebt_rev3_ballBearingCase_RH.3mf](casedata/rev3/mtk64ebt_rev3_ballBearingCase_RH.3mf)<br>[mtk64ebt_rev3_bodyBallBeringBottmn_RH.3mf](casedata/rev3/mtk64ebt_rev3_bodyBallBeringBottmn_RH.3mf)

<img src="image/rev3/mtk64ebt_bearing_case_trace.jpeg" width="60%" style="border: 1px solid;"/><br>

### Alps alpine製低背エンコーダー搭載

30クリックの回転操作とプッシュ操作による、直感的な操作が可能です。
一般的なエンコーダーと比較して、クリックトルク、プッシュトルク共に軽い操作感です。

<img src="image/mtk64erp_encoder.jpg" width="80%" style="border: 1px solid;"/><br>

#### Choc V1、[V2（固定ピンなしモデル）](https://ja.aliexpress.com/item/1005007361067887.html)、およびMX互換キースイッチを全てのキーに取り付けることが可能です

<img src="image/mtk64erp_switches.jpg" width="80%" style="border: 1px solid;"/><br>
<a href="https://ja.aliexpress.com/item/1005007361067887.html"><img src="image/kailh_v2_deepsea.png" width="40%" style="border: 1px solid;"/></a>
<a href="https://ja.aliexpress.com/item/1005007404357477.html"><img src="image/kailh_v2_shadow.png" width="40%" style="border: 1px solid;"/></a><br>

親指部分のみをロープロファイル化することも可能です。

追加の親指キースイッチは、操作性を向上させるため、さらに一段低くオフセットされています。

<img src="image/rev3/5.mtk64ebt_lowpro.jpg" width="80%" style="border: 1px solid;"/><br>

### MCU (Seeed Studio XIAO nRF52840)

[Seeed Studio XIAO nRF52840](https://jp.seeedstudio.com/Seeed-XIAO-BLE-nRF52840-p-5201.html)を使用しており、無線接続の自作キーボードで課題となる技適対応もクリアしています。

技術基準適合証明番号：[211-220207](https://www.tele.soumu.go.jp/giteki/SearchServlet?pageID=jk01&NUM_TYPE=1&NUM=211-220207)

<img src="image/mtk64ebt_mcu.png" width="80%" style="border: 1px solid;"/><br>

光学式センサーに **PAW3222** を採用しており、Bluetooth（BLE）接続およびUSB接続のポーリングレート実測値と理論値は以下の通りです。

#### Bluetooth（BLE）接続時
- **理論値**：最大約133Hz（BLE規格の最小接続インターバル 7.5ms 換算）
- **実測値**：平均約109Hz / 最大130Hz
- 一般的なオフィスワークや日常的なPC操作には十分滑らかに使用することが可能です。

<img src="image/polling_rate_bluetooth.png" width="60%" style="border: 1px solid;"/><br>

#### USB（有線）接続時
- **理論値**：最大1000Hz (1ms)
- **実測値**：平均約979Hz / 最大984Hz
- ゲーミングマウスと同等の極めて高いポーリングレートを発揮し、高リフレッシュレートモニター環境でも吸い付くような滑らかで精密なトラックボール操作が可能です。
- 有線接続時もトラックボール搭載側（右手側等）のみUSB接続となり、反対側（左手側）は無線接続となるため、PCとの間はUSBケーブル1本のみで配線できます（左右間接続用のTRRSケーブルは使用しません）。

<img src="image/polling_rate_usb.png" width="60%" style="border: 1px solid;"/><br>

### フットスイッチ対応
[市販のUSBフットスイッチ](https://amzn.asia/d/h7wMR24)の基板を付属のフットスイッチ拡張基板に差し替えて、mtk64の拡張無線フットスイッチとして使用可能です。

付属のフットスイッチ無線化モジュールを使用することで、フットスイッチも含めた完全ワイヤレス構成に対応します。

フットスイッチ拡張基板およびフットスイッチ無線化モジュールは、ご自身ではんだ付けと組み立てが必要なキットです。詳細は[フットスイッチ拡張基板](#フットスイッチ拡張基板)および[フットスイッチ無線化モジュール](#フットスイッチ無線化モジュール)を参照してください。

<img src="image/footswitch.jpg" width="80%" style="border: 1px solid;"/><br>

### ZMK Studio 対応

[ZMK Studio](#zmk-studioでキーマッピング変更)を使用して、キーマッピングを簡単に変更することができます。

<img src="image/zmk_studio_app.png" width="80%" style="border: 1px solid;"/><br>

### ESBを使用したドングル対応

[Seeed Studio XIAO BLE](https://jp.seeedstudio.com/Seeed-XIAO-BLE-nRF52840-p-5201.html) を専用ドングルとして使用することで、左右のキーボードは完全無線のまま、Nordic独自の超高速ワイヤレスプロトコル **ESB (Enhanced ShockBurst)** による超低遅延通信を行います。

完全ワイヤレスでありながら、USB直接接続と同等の **1000Hz (1ms)** に近いポーリングレートを実現し、トラックボールの追従性が飛躍的に向上します。（※Rev3ではBLEドングルによる約110~220Hz動作）

- **理論値**：1000Hz (1ms)
- **実測値**：平均約980Hz / 最大984Hz

<img src="image/rev3/mtk64ebt_dongle.jpg" width="60%" style="border: 1px solid;"/><br>

<img src="image/polling_rate_dongle.png" width="60%" style="border: 1px solid;"/><br>

#### ドングルにOLEDを取り付けて動作状況を表示できます

[0.96インチ 128×64ドットOLED(SSD1306)](https://akizukidenshi.com/catalog/g/g112031/)のGND,VCC,SCL,SDA を[XiaoBLEの GND,3v3,D10,D9 ](https://files.seeedstudio.com/wiki/XIAO-BLE/pinout2.png)に結線してください。

OLEDのピンヘッダ位置とXiaoBLEの端子位置を合わせてあるので、配線なしでピンヘッダで直付も可能です。

注：リセットスイッチが押しづらいので工夫が必要です。

<img src="image/rev3/mtk64ebt_dongle_display.jpg" width="60%" style="border: 1px solid;"/><br>
<img src="image/rev3/mtk64ebt_dongle_display_2.jpg" width="60%" style="border: 1px solid;"/><br>

##### OLEDディスプレイ画面の表示内容

<img src="image/DONGLE/oled_display_preview.png" width="65%" style="border: 1px solid;"/><br>

| 領域 / アイコン | 表示内容 | 説明 |
| :--- | :--- | :--- |
| **左上 (出力状態)** | 🔌 USB / 📶 Bluetooth (1〜5) | 接続モード、選択中のBTプロファイル番号、接続状態（✓）を表示。現在選択されている出力の上部にバーが表示されます。 |
| **右上 (バッテリー)** | 🔋 L: 80% / R: 90% | 左右ペリフェラルのバッテリー残量（%）と電池アイコンをリアルタイム表示。 |
| **左中 (トラックボール)** | `CPI:1600`<br>`X:  +0`<br>`Y:  +0` | 現在のCPI解像度およびトラックボールのX/Y累積移動量をリアルタイム表示。 |
| **右中 (マスコット)** | めんたこ | 打鍵速度に連動してアニメーション。 |
| **左下 (モディファイア)** | `^` `⌥` `⌘` `⇧` | 現在押下中のモディファイアキー（Ctrl, Opt, Cmd, Shift）に下線（`_`）が表示されます。 |
| **中下 (ポインティング機能)** | 🎱 (A) Automouse<br>↕️ Scroll反転 | **Automouse**: 有効時に下線（`_`）が表示されます。<br>**Scroll反転**: スクロール反転有効時に下線（`_`）が表示されます。 |
| **右下 (レイヤー)** | `DEF`, `SNP`, `MSE` ... | 現在アクティブな最上位レイヤー名（`DEF`, `SNP`, `MSE`, `SCR`, `L4`, `L5`, `AML` 等）が右端に表示されます。 |

### LED表示

#### セントラル側のLEDで現在のレイヤーが確認できます
```
レイヤー０ ⚫️Black（無点灯）
レイヤー１ 🟣Magenta トラックボール精密モード
レイヤー２ 🔵Cyan    トラックボールモード
レイヤー３ 🟡Yellow  スクロールモード
レイヤー４ 🟢Green
レイヤー５ 🔵Blue
レイヤー６ ⚪️White   自動マウスレイヤー
```

#### LEDレンズ
インジケーターLEDにレンズを装着することで高い視認性を実現し、バッテリー残量や接続状態、レイヤー切り替えがわかりやすくなりました。

<img src="image/rev3/mtk64ebt_rev3_LED.JPG" width="60%" style="border: 1px solid;"/><br>

## フットスイッチ拡張基板

[市販のUSBフットスイッチ](https://amzn.asia/d/h7wMR24)の基板を付属のフットスイッチ拡張基板に差し替えてmtk64のフットスイッチとして使用可能です。

フットスイッチはmtk64の一部として機能するので、レイヤー切り替えやカスタムキーなどキーボード固有の操作が可能です。

<img src="image/mtk64erp_footswitch_4.jpg" width="40%" style="border: 1px solid;"/>
<img src="image/mtk64erp_footswitch_5.jpg" width="36%" style="border: 1px solid;"/><br>
<img src="image/footswitch_extend.jpg" width="60%" style="border: 1px solid;"/><br>  

### フットスイッチ無線化モジュール（概要）
付属のフットスイッチ無線化モジュールにより完全無線接続のフットスイッチが完成します。

<img src="image/fooswitch_btmodule_parts.jpg" width="60%" style="border: 1px solid;"/><br>

#### 本体基板キットを使用したカスタマイズが可能です

作例：左ボール 右エンコーダ ドングル OLED
（ファームウェア、ケースデータは各セクションを参照）
<img src="image/rev3/10.mtk64ebt_leftball.jpg" width="60%" style="border: 1px solid;"/><br>



## 使用方法

## モジュール間接続

mtk64ebtは、右手モジュールがセントラルモジュールとして動作します。左手モジュールとフットスイッチは右手モジュールに自動的にペアリングされます。

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

レイヤー1の「ESC」「1」〜「5」キーを使用して、最大６か所のBluetooth接続先を切り替えることができます。

<img src="image/ble_connect_1.png" style="border: 1px solid;"/>

<img src="image/ble_connect_2.png" style="border: 1px solid;"/>

接続時には、表示されたPIN番号を入力し、Enterキーを押下してください。接続後にキーボードが動作しない場合は、リセットボタンを押下して再接続を試みてください。これにより、接続の問題を解決し、正常に動作させることができます。

## ロープロファイル化

Choc V1、V2を使用する場合、トッププレート固定用ネジ(T5 8mm)を外してトッププレートを取り除き、付属の6mmねじに付け替えます。ネジの交換にはT5ドライバーを使用します。

## フットスイッチ拡張キット

フットスイッチ拡張キットはご自身で市販のフットスイッチにキットの基板を組み込み、はんだ付けをするキットです。

フットスイッチの作成方法は[こちらのビルドムービー](https://youtu.be/NavGAliALVc?si=JpO-xi0RZznjVi4-)をご覧ください。

フットスイッチの接続は3.5mm４極のTRRS端子を使用しますが、有線でフットスイッチを接続する場合（30cm以上のケーブル長が必要な場合）、市販のTRRSケーブルは線が細すぎるので使用できません。

TRRS端子とAWG28~26以上（番号が小さい方が太いです）のケーブルを組み合わせて自作します。

[遊舎工房自作ケーブルキット](https://shop.yushakobo.jp/products/self-made-cable?_pos=1&_sid=79305908f&_ss=r&variant=39623339737249)

[AWG26 4Cシールドケーブル](https://shop.oyaide.com/products/mogami_2893.html)

配線の色は使用するケーブルのメーカーによって異なります。
４極プラグの端子側とフットスイッチ拡張キット側の結線は下図を参照してください。

<img src="image/footswitch_kit/plug_to_wire_back.jpg" width="60%" style="border: 1px solid;"/><br>
<img src="image/footswitch_kit/plug_to_wire_up.jpg" width="60%" style="border: 1px solid;"/><br>
<img src="image/footswitch_kit/plug_to_wire_side.jpg" width="60%" style="border: 1px solid;"/>


## フットスイッチ無線化モジュール

フットスイッチ無線化モジュールを使用する場合、[Seeed Studio XIAO nRF52840](https://jp.seeedstudio.com/Seeed-XIAO-BLE-nRF52840-p-5201.html)、[リチウムポリマーバッテリー 902030 PH2.0プラグ付き](https://ja.aliexpress.com/item/1005006838195720.html)、[ケース（ご自身で3Dプリント）](casedata/rev3/mtk64ebt_rev3_footmodule_case.3mf) が別途必要です。

フットスイッチ拡張キットをフットスイッチ無線化モジュールに接続して、mtk64ebtに無線接続します。

フットスイッチキットとフットスイッチ無線化モジュールを接続する場合、フットスイッチ側の線を極力短くするのがオススメです。

写真は[こちらの４極3.5mm端子付きケーブル](https://www.digikey.jp/ja/products/detail/assmann-wsw-components/A-AV-02-45-28-183-S2/16906692)を15cmにカットして使用しています。

<img src="image/fooswitch_btmodule_parts.jpg" width="40%" style="border: 1px solid;"/>
<img src="image/footswitch_extend.jpg" width="40%" style="border: 1px solid;"/> 


## ファームウェア

### Rev4 と Rev3 以前の違い

| 比較項目 | Rev4（最新） | Rev3 以前 |
| :--- | :--- | :--- |
| **トラックボールセンサー** | **PAW3222** にアップデート | 従来センサー |
| **ドングル通信プロトコル** | **Nordic ESB** を採用<br>ペリフェラル $\to$ ドングル間を超低遅延通信（最大 1000Hz） | BLE (Bluetooth Low Energy) 通信 |

* **トラックボールセンサーの刷新**: トラックボールセンサーが **PAW3222** にアップデートされ、高精度な操作とリアルタイム CPI 変更に対応しました。
* **超低遅延 ESB 通信（ドングル構成）**: ドングル使用時に、ペリフェラル（左右手・フットスイッチ）からドングル間の無線通信に **Nordic ESB (Enhanced ShockBurst)** を使用し、最大 1000Hz (1ms) の超低遅延レスポンスを実現しています。

> [!IMPORTANT]
> センサーや通信仕様の変更に伴い、**Rev4 と Rev3 以前でファームウェアの互換性はありません**。
> mtk64ebt Rev3 以前のキーボードをお使いの場合は、本リポジトリの [`firmware/rev3/`](firmware/rev3/) ディレクトリ、または各 `_rev3` ブランチ（例: [right_left_rev3 ブランチ](https://github.com/mentako-ya/zmk-config-mtk64/tree/right_left_rev3#readme)）のファームウェアをご使用ください。

---

### Rev4用ファームウェア一覧

本リポジトリでは、接続方式に応じてファームウェアを分離・最適化して提供しています。

#### 1. Bluetooth 接続（BLE Split / ドングル不要）構成【デフォルトブランチ: [`right_left_rev4`](https://github.com/mentako-ya/zmk-config-mtk64/tree/right_left_rev4)】

ドングルを使わず、右手（Central）と PC を Bluetooth でペアリングし、左手・フットスイッチとも安定した BLE Split 通信を行う標準構成です。
本リポジトリの [`firmware/rev4/`](firmware/rev4/) ディレクトリより最新版をダウンロードいただけます。

| No | 構成名 | パッケージ名 (ZIP) | 含まれるファームウェア (.uf2) |
| :--- | :--- | :--- | :--- |
| 1 | **左右構成** | [mtk64ebt_Right_Left.zip](firmware/rev4/mtk64ebt_Right_Left.zip) | `mtk64_R.uf2`, `mtk64_L.uf2`, `settings_reset.uf2` |
| 2 | **左右＋フットスイッチ** | [mtk64ebt_Right_Left_Foot.zip](firmware/rev4/mtk64ebt_Right_Left_Foot.zip) | `mtk64_R.uf2`, `mtk64_L.uf2`, `mtk64_FOOT.uf2`, `settings_reset.uf2` |

> [!TIP]
> 直接接続用のファームウェアビルドやカスタマイズは、[zmk-config-mtk64](https://github.com/mentako-ya/zmk-config-mtk64) のデフォルトブランチ **[`right_left_rev4`](https://github.com/mentako-ya/zmk-config-mtk64/tree/right_left_rev4)** をご使用ください。

---

#### 2. ドングル接続（1000Hz ESB超低遅延）構成【ブランチ: [`right_left_dongle_rev4`](https://github.com/mentako-ya/zmk-config-mtk64/tree/right_left_dongle_rev4)】

専用 USB ドングルを Central 親機とし、左右手・フットスイッチを 1000Hz ポーリングの超低遅延 Nordic ESB プロトコルで通信させるハイパフォーマンス構成です。
ファームウェアは [zmk-config-mtk64 Releases](https://github.com/mentako-ya/zmk-config-mtk64/releases) よりダウンロードいただけます。

| No | 構成名 | パッケージ名 (ZIP) | 含まれるファームウェア (.uf2) |
| :--- | :--- | :--- | :--- |
| 1 | **左右＋ドングルOLED＋フット** | `mtk64ebt_Right_Left_Dongle_disp_foot.zip` | `mtk64_DONGLE_display.uf2`, `mtk64_R_dongle.uf2`, `mtk64_L_dongle.uf2`, `mtk64_FOOT_dongle.uf2`, `settings_reset.uf2` |
| 2 | **左右＋ドングルOLED** | `mtk64ebt_Right_Left_Dongle_display.zip` | `mtk64_DONGLE_display.uf2`, `mtk64_R_dongle.uf2`, `mtk64_L_dongle.uf2`, `settings_reset.uf2` |
| 3 | **左右＋ドングル（画面なし）** | `mtk64ebt_Right_Left_Dongle.zip` | `mtk64_DONGLE.uf2`, `mtk64_R_dongle.uf2`, `mtk64_L_dongle.uf2`, `settings_reset.uf2` |
| 4 | **左ボール右エンコーダー＋ドングルOLED** | `mtk64ebt_Right_Left_Dongle_disp_leftball.zip` | `mtk64_DONGLE_display.uf2`, `mtk64_L_leftball.uf2`, `mtk64_R_leftball.uf2`, `settings_reset.uf2` |

> [!TIP]
> ドングル構成のファームウェアビルドやカスタマイズは、[zmk-config-mtk64](https://github.com/mentako-ya/zmk-config-mtk64) の **[`right_left_dongle_rev4`](https://github.com/mentako-ya/zmk-config-mtk64/tree/right_left_dongle_rev4)** ブランチをご使用ください。

### Rev3用ファームウェアについて

> [!NOTE]
> mtk64ebt Rev3用ファームウェアは、本リポジトリの [`firmware/rev3/`](firmware/rev3/) ディレクトリ、または [rev3 ブランチ](https://github.com/mentako-ya/mtk64ebt/tree/rev3#readme) を参照してください。

### ファームウェア書き込み手順

1. 右手キーボード、左手キーボード、フットスイッチ拡張モジュールのバッテリー駆動スイッチをOFFにする

> [!IMPORTANT]
> バッテリーから給電された状態ではファームウェア書き込み後のリセットが正しく行われません。

1. **右手キーボード書き込み**:
   * 右手キーボードをPCにUSB接続して、基板上のリセットボタンを短く2回押下（ダブルクリック）。
   * 認識されたリムーバブルディスク ”XIAO-SENSE" に `settings_reset.uf2` をドラッグ＆ドロップ（自動再起動）。
   * 再度リセットボタンを短く2回押下し、”XIAO-SENSE" に対応する右手ファームウェア（直接接続なら `mtk64_R.uf2` または `mtk64_R_foot.uf2`、ドングル構成なら `mtk64_R_dongle.uf2`）をドロップ。

1. **左手キーボード書き込み**:
   * 左手キーボードをPCにUSB接続して、リセットボタンを短く2回押下。
   * ”XIAO-SENSE" に `settings_reset.uf2` をドロップ。
   * 再度リセットボタンを短く2回押下し、各ZIPパッケージに含まれる左手用ファームウェア（直接接続なら `mtk64_L.uf2`、ドングル構成なら `mtk64_L_dongle.uf2` / 左ボールなら `mtk64_L_leftball.uf2`）をドロップ。

1. **ドングル / フットスイッチ書き込み（使用時）**:
   * **ドングルモジュール**: PCにUSB接続してリセットボタンを短く2回押下し、`mtk64_DONGLE_display.uf2`（画面なしは `mtk64_DONGLE.uf2`）をドロップ。
   * **フットスイッチ無線化モジュール**: PCにUSB接続してリセットボタンを短く2回押下し、`settings_reset.uf2` を書き込んだ後、対応するファームウェア（直接接続なら `mtk64_FOOT.uf2`、ドングル構成なら `mtk64_FOOT_dongle.uf2`）をドロップ。

1. **接続確認**:
   * 右手キーボード（またはドングル）をPCにUSB接続し、左手キーボードとフットスイッチ拡張モジュールはバッテリー駆動スイッチをONにして給電します。
   * 各モジュールのリセットスイッチを1回押下し、USB端子横のLEDで接続状態を確認します。
   * 右手（またはドングル）のLED: PCとの接続状態を表す（接続中🔵、オープン/アドバタイズ🟡、切断中🔴）。
   * 左手・フットスイッチのLED: セントラルとのペアリング状態を表す（接続中🔵、切断中🔴）。

LEDの色と接続状態についての詳細は [zmk-rgbled-widget](https://github.com/mentako-ya/zmk-rgbled-widget/blob/main/README.md) を参照してください。

## ファームウェアのブランチ構成について

[zmk-config-mtk64](https://github.com/mentako-ya/zmk-config-mtk64) リポジトリでは、接続方式に応じてブランチを分離して最適化・ビルドしています。

* **Bluetooth 接続（BLE Split / ドングル不要）専用【デフォルトブランチ: [`right_left_rev4`](https://github.com/mentako-ya/zmk-config-mtk64/tree/right_left_rev4)】**:
  * ドングル不要で PC と左右キーボードを Bluetooth ペアリングする標準構成です。外出先やノート PC で手軽に使用できます。
* **ドングル接続（1000Hz ESB超低遅延）専用【ブランチ: [`right_left_dongle_rev4`](https://github.com/mentako-ya/zmk-config-mtk64/tree/right_left_dongle_rev4)】**:
  * 専用 USB ドングルを親機とし、左右・フットスイッチを 1000Hz ポーリングの超低遅延 Nordic ESB プロトコルで通信させるハイパフォーマンス構成です。
  * ドングル（OLEDあり/なし）、フットスイッチ併用、左手ボール構成など 4 つのドングル構成に対応しています。
* **Rev3（旧版）**:
  * 各構成ごとに `_rev3` サフィックスを付与したブランチ（例: [`right_left_rev3`](https://github.com/mentako-ya/zmk-config-mtk64/tree/right_left_rev3)）にて維持されています。

## キーマッピング変更

### ZMK Studioでキーマッピング変更

ZMK Studioを使用することで、ファームウェア書き換えなしでキーマッピングを簡単に変更することができます。

<img src="image/zmk_studio_app.png" width="60%" style="border: 1px solid;"/><br>

#### ブラウザ版 ZMK Studio
ブラウザ版のZMK Studioを使用する場合、右手側のモジュールをUSB接続し、[こちら](https://zmk.studio/)にアクセスしてください。

#### アプリ版 ZMK Studio
アプリ版のZMK Studioは、[こちら](https://zmk.studio/download)からダウンロードできます。アプリ版では、無線接続のままキーマップの変更が可能です。ケーブルを接続する手間を省き、より柔軟にキーマッピングを調整することができます。

### KeymapEditorでキーマッピング変更

キースイッチのマッピングだけでなく、エンコーダーのキーマッピング、マクロやコンボの追加、編集をしたい場合、[キーマップエディター](https://nickcoutsos.github.io/keymap-editor/)を使用して変更可能です。

キーマップエディターでマッピングを変更するためには、ご自身のgithubアカウントでmtk64ebtのファームウェアリポジトリをフォークして、キーマップエディターで編集する必要があります。

操作はブラウザだけで完結するので、特別なツールは不要です。

1. https://github.com/mentako-ya/zmk-config-mtk64 を開いて画面右上の「Fork」をクリック

<img src="image/keymap_editor/ke_001.png" width="60%" style="border: 1px solid;"/>

2. 「Create fork」のボタンをクリックしてフォークを作成します

<img src="image/keymap_editor/ke_002.png" width="60%" style="border: 1px solid;"/>

3. ご自身のgitHubアカウントにzmk-config-mtk64のフォークが作成されます

<img src="image/keymap_editor/ke_003.png" width="60%" style="border: 1px solid;"/>

4. https://nickcoutsos.github.io/keymap-editor/ を開いて「GitHub」のアイコンをクリック

<img src="image/keymap_editor/ke_004.png" width="60%" style="border: 1px solid;"/>

5. 先ほどzmk-config-mtk64のフォークを作成したGitHubのアカウントで認証

<img src="image/keymap_editor/ke_005.png" width="60%" style="border: 1px solid;"/>

6. 「Authorize Keymap Editor」をクリック

<img src="image/keymap_editor/ke_006.png" width="60%" style="border: 1px solid;"/>

7. 「Add Repository」をクリック

<img src="image/keymap_editor/ke_007.png" width="60%" style="border: 1px solid;"/>

8. 「Only select repositories」のラジオボタンを選択 -> 「Select repositories」のプルダウンから「zmk-config-mtk64」を選択 -> 「Install」をクリック

<img src="image/keymap_editor/ke_008.png" width="60%" style="border: 1px solid;"/>

9. キーマップエディター画面でフォークしたリポジトリと作業ブランチ（直接接続なら `right_left_rev4`、ドングル構成なら `right_left_dongle_rev4`）を選択します。

<img src="image/keymap_editor/ke_009.png" width="60%" style="border: 1px solid;"/>

10. キーをクリックして編集　例として、エンコーダーのキーマップを変更

<img src="image/keymap_editor/ke_010.png" width="60%" style="border: 1px solid;"/>

11. saveボタンを押して変更したキーマップをコミット

<img src="image/keymap_editor/ke_011.png" width="60%" style="border: 1px solid;"/>

12. フォークした自分のzmk-config-mtk64リポジトリをブラウザで開く -> Actionsメニュー -> .github/workflows/build.yml選択 -> 「Run workflow」クリック -> Run workflow
（またはローカルでコミットして `git push origin <作業ブランチ名>` すると自動的にビルドが開始されます）

<img src="image/keymap_editor/ke_012.png" width="60%" style="border: 1px solid;"/>

13. 実行完了後、フォーク先リポジトリの「Releases」（`latest-main`）または Actions 実行画面最下部の「Artifacts」から、ご自身の構成に対応するファームウェア ZIP をダウンロードします。

14. [ファームウェア書き込み手順](#ファームウェア書き込み手順)に従って書き込みます。

#### 左ボール右エンコーダー構成のキーマップ対応について
* ドングル構成用の **`right_left_dongle_rev4` ブランチ** では、全ドングル構成（通常ドングル、左ボール構成、フットスイッチ構成など）が一括ビルドされます。
* `config/mtk64.keymap` の変更は、通常の右手ボール構成だけでなく左ボール構成（`mtk64ebt_Right_Left_Dongle_disp_leftball.zip` 等）にも自動的に反映されます。
* 左ボール構成を使用する場合、左手でトラックボールを操作しながら右手でクリック操作を行えるよう標準マッピング（レイヤー1・2・6にマウスボタン配置）されています。左手側にクリックキーを配置したい場合も、`mtk64.keymap` の左手側キーにお好みのマウスキー（`&mkp MB1` 等）を割り当てるだけで自由に変更できます。



## トラックボール設定

各レイヤーごとの動作について説明します。

* **Layer 0** は通常レイヤーです。これはデフォルトのレイヤーで、通常のキーボード操作が行われます。

* **Layer 1** はマウスレイヤー（精密モード）です。このレイヤーでは、マウスの精密な操作が可能となります。細かい動きが必要な場合に使用します。右手最右列には **`cpi_inc`**（感度UP）/ **`cpi_dec`**（感度DOWN）キーが配置されています。

* **Layer 2** もマウスレイヤーですが、精密モードではありません。通常のマウス操作が行えます。同様に右手最右列に **`cpi_inc`** / **`cpi_dec`** キーが配置されています。

* **Layer 3** はスクロールレイヤーです。このレイヤーでは、スクロール操作が可能となります。ウェブページやドキュメントの閲覧時に便利です。

* **Layer 4** と **Layer 5** は未使用のレイヤーです。これらのレイヤーには任意のキーコードを設定することができます。ユーザーの好みに応じてカスタマイズが可能です。

* **Layer 6** は自動マウスレイヤーです。トラックボールの操作が一定距離に達すると、自動的にこのレイヤーに切り替わり、N,Mキーで左右クリック操作が可能になります。一定時間経過後レイヤーは元のレイヤーに戻ります。

### CPI（感度）動的変更機能 (Rev4)

Rev4 では、ソースコードを再ビルドすることなく、**キーボードのキー操作だけでリアルタイムにトラックボールの感度（CPI）を変更可能** です。

* **キー配置（デフォルトキーマップ）**:
  * デフォルトのキーマップでは、**レイヤー1（精密モード）の右手キーボード右下** に配置されています。
    * **`cpi_inc`**（感度UP）: 右手最右列・下から2段目
    * **`cpi_dec`**（感度DOWN）: 右手最右列・最下段（右下端）
  * ※レイヤー2（マウスモード）でも同様に右手キーボード右下に配置されています。
* **操作方法**:
  * **`cpi_inc` キー押下**: CPI が 1 ステップ増加（高速化）
  * **`cpi_dec` キー押下**: CPI が 1 ステップ減少（低速化）
* **16段階の調整範囲**:
  `608` $\leftrightarrow$ `790` $\leftrightarrow$ `1003` $\leftrightarrow$ `1216` $\leftrightarrow$ `1428` $\leftrightarrow$ `1611` $\leftrightarrow$ `1824` $\leftrightarrow$ `2036` $\leftrightarrow$ `2249` $\leftrightarrow$ `2462` $\leftrightarrow$ `2827` $\leftrightarrow$ `3222` $\leftrightarrow$ `3617` $\leftrightarrow$ `4012` $\leftrightarrow$ `4408` $\leftrightarrow$ `4826` CPI
* **不揮発性メモリ（NVS）への自動保存**:
  変更した CPI 設定は自動的に内部ストレージに永続保存されるため、キーボードの電源を切ったりバッテリーを交換しても前回の感度設定がそのまま維持されます。
* **ドングル OLED へのリアルタイム表示**:
  OLED ディスプレイ付きドングルを使用している場合、現在の CPI 値（例: `CPI:1600`）が画面上にリアルタイム表示されます。

### トラックボール設定変更

トラックボールの設定を変更するには、リポジトリをフォークしてソースコードを修正する必要があります。

フォークとは、他のユーザーのリポジトリを自分のアカウントにコピーし、自由に変更を加えることができる機能です。

変更した設定をフォークしたリポジトリにコミットすると、GitHub Actionsにより自動的にファームウェアがビルドされます。
> [!NOTE]
> GitHub Actionsは、リポジトリに変更が加えられた際に自動的にビルドやテストを実行するCI/CDツールです。

ビルドされたファームウェアをダウンロードしてキーボードに書き込み、変更したトラックボール設定でキーボードを使用できます。

#### 自動マウスレイヤー（Layer 6）の設定変更

トラックボール操作時に自動的にマウスレイヤー（Layer 6）へ切り替わる動作は、[`config/mtk64.keymap`](https://github.com/mentako-ya/zmk-config-mtk64/blob/right_left_rev4/config/mtk64.keymap#L16-L18) で設定されています。

```dts
&mkp_input_listener {
    input-processors = <&zip_temp_layer 6 5000>;
};
```

* **第1引数 (`6`)**: 自動遷移先のマウスレイヤー番号（デフォルトは Layer 6）。
* **第2引数 (`5000`)**: トラックボール操作を止めてから元のレイヤーに自動復帰するまでの時間（ミリ秒、`5000` = 5秒）。

また、キー入力後にトラックボールが反応するまでのアイドル時間などは、[`config/boards/shields/mtk64/mtk64_trackball.dtsi`](https://github.com/mentako-ya/zmk-config-mtk64/blob/right_left_rev4/config/boards/shields/mtk64/mtk64_trackball.dtsi#L60-L65) で調整可能です：

```dts
zip_temp_layer: zip_temp_layer {
    compatible = "zmk,input-processor-temp-layer";
    #input-processor-cells = <2>;
    require-prior-idle-ms = <500>;
    excluded-positions = <43 44 45 46 47>; // MB4, MB5, MB1, MB2, MB3
};
```

* `require-prior-idle-ms = <500>;`: タイピング中の誤爆を防ぐため、キー入力後 500ms 経過してからトラックボールを操作した際に自動レイヤー切り替えが発動します。
* `excluded-positions`: マウスボタン（MB1〜MB5）を押した際にタイマーがリセットされる除外キー位置です。

#### トラックボール感度（CPI）の初期値調整

通常はキーボード右下の **`cpi_inc`** / **`cpi_dec`** キーで 16 段階にリアルタイム調整可能ですが、ファームウェア起動時のデフォルト初期値を変更したい場合は、[`config/boards/shields/mtk64/mtk64_trackball.dtsi`](https://github.com/mentako-ya/zmk-config-mtk64/blob/right_left_rev4/config/boards/shields/mtk64/mtk64_trackball.dtsi#L39) の `res-cpi` を編集します：

```dts
trackball: trackball@0 {
    compatible = "pixart,paw32xx";
    ...
    res-cpi = <1558>; /* デフォルト初期CPI */
};
```


## ケースデータ

[ケースデータ ダウンロード](casedata/)

[mtk64ebt rev1ケース](https://github.com/mentako-ya/mtk64ebt/tree/main/casedata/rev1)

[mtk64ebt rev2ケース](https://github.com/mentako-ya/mtk64ebt/tree/main/casedata/rev2)

[mtk64ebt rev3ケース](https://github.com/mentako-ya/mtk64ebt/tree/main/casedata/rev3)

[mtk64ebt rev4ケース](https://github.com/mentako-ya/mtk64ebt/tree/main/casedata/rev4)

[XiaoBleドングルケース](https://github.com/mentako-ya/mtk64ebt/blob/main/casedata/XiaoBle/XiaoBleDongle.3mf)

[XiaoBleドングル+OLEDケース](https://github.com/mentako-ya/mtk64ebt/blob/main/casedata/XiaoBleDongleOLED/XiaoBleDongleOLED.3mf)
