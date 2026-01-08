---
description: このページは、スキルとFEVERイベントを含む譜面を公式エンジンに追加するためのものです。
---

# (JP)スキルとFEVERイベントの追加

## スキル＆FEVERイベントについて

MMWでは、公式譜面をインポートすると、通常の方法では追加できない追加の要素が表示されます。

| イベント                                                                                                     | 説明                                                                            |
| -------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| <div><figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure></div> | `SKILL`: スキルカードのうちの1枚を発動。青い「Skill」タグで表示されます。                                  |
| <div><figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure></div> | `FEVER CHANCE`: イベントをきっかけしてFEVERバーを構築（マルチライブ専用）。オレンジ色の「FEVER▲」き矢印タグとして表示されます。 |
| <div><figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure></div> | `FEVER START`: FEVERイベントを開始（マルチライブ専用）。オレンジ色の「FEVER▼」き矢印タグで表示されます。             |

## 追加方法は？

1. [MMW4CC](../getting-started/usage-guide-mmw4cc.md)の**プロジェクトファイル**（`.mmws`/`.ccmmws`）を開き、次のようにイベントを追加してください：

```
SKILL: 「ダメージノート」の2番目の左側延長レーン
FEVER CHANCE:「タップノート」の2番目の右側延長レーン
FEVER START:「クリティカルノート」の2番目の右側延長レーン
```

{% hint style="warning" %}
**`SKILL`イベントを6つ、`FEVER CHANCE`を1つ、`FEVER START`を1つ**まで追加可能です。
{% endhint %}

<figure><img src="../.gitbook/assets/image.png" alt="" width="375"><figcaption></figcaption></figure>

2. 追加したイベント以外のすべてを削除&#x3057;**（`Ctrl+S`で保存しないでください）**、[キーボードショートカット](../getting-started/usage-guide-mmw4cc.md#shortcut-configuration-key-config)（デフォルトは`Ctrl+E`）を使用して`.sus`形式でエクスポートします。ファイル名は`skillfever.sus`または他の任意の名前を付けることができます。
3. ファイルを開き、下にスクロールすると、次のようなテキストが表示されます：

```
#HISPEED 00
#00710:41
#HISPEED 00
#02310:41
#HISPEED 00
#03610:0041
#HISPEED 00
#05010:0041
#HISPEED 00
#0631f:0011
#HISPEED 00
#06510:0041
#HISPEED 00
#0751f:0021
#HISPEED 00
#08310:41
```

4. `#HISPEED 00` 行を削除してください。すると、次のように表示されます：

```
#00710:41
#02310:41
#03610:0041
#05010:0041
#0631f:0011
#06510:0041
#0751f:0021
#08310:41
```

5. そのテキストをコピーし、メインの.susファイル内&#x306E;**`#MEASUREHS 00`の後**に貼り付けてください。

```
#REQUEST "ticks_per_beat 480"

#00002:4

#BPM01:164
#BPM02:20.5
#BPM03:102.5

#TIL00: "0.0:1"
#HISPEED 00
#MEASUREHS 00

[以下のスキル＆FEVERイベントの行を貼り付けてください]
#00710:41
#02310:41
#03610:0041
#05010:0041
#0631f:0011
#06510:0041
#0751f:0021
#08310:41

[残りの部分は譜面作成の部分です。]
#00008:01
#03008:0200000300000000
.....
```

6. MMWでメインの`.sus`ファイルを開いて確認してください。正しく設定されていれば、以下のイベントが表示されます！

<figure><img src="../.gitbook/assets/image (1).png" alt="" width="563"><figcaption></figcaption></figure>
