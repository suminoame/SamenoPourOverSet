# VRC Pour Over Set 説明書（Manual）

© 2026 Sameno Works(sumisame) All rights reserved.

[Booth Link](https://sameno.booth.pm/items/7656169)

英文での説明は下部にございます。

Please scroll down for the English version. 

------

更新履歴 / Release

2026/07/24: Manual v1.0.0 Released. 

<img src="./source/p0.png" width="420px">

# 事前準備

本パッケージを使用する際は、Unity 2022.3.22f1のプロジェクトをご用意ください。

Unity 2019とは互換性がありませんのでご注意ください。

本商品はWorld Phys Boneを使用しています。VRCSDKは ver3.10.0以降を必ず使用してください。

本商品はUdonSharp(U#)を使用しています。VCC(VRChat Creator Companion)のWorlds U#でプリインストールされている最新バージョンの U# を使用してください。

VCC経由でインストールされるU#以外のバージョンは動作サポート対象外とさせていただきます。  

本商品はシェーダーにliltoonを使用しています。 

本商品をインストールする前に、以下URLまたはVCCより最新の「liltoon」をプロジェクトにインポートしてください。

liltoon

https://lilxyzw.booth.pm/items/3087170

# クイックスタート

## 1. 導入

### 手順 (1)
Unitypackageファイルをインポート後、「Assets\SamenoLab\VRCPourOverCoffee」にある「DripSet - Quick Start」から、「PourOverCoffee」をSceneに配置します。

### 手順(2)
お好みで「Assets\SamenoLab\VRCPourOverCoffee\DripSet - Quick Start」にある「Color - xxx」フォルダから、
お好みのスキンのPrefabを、手順(1)で先に設置した「PourOverCoffee」の配下に配置します。

以上でセットアップは完了です。

**⚠️注意事項**
複数のPrefabを設置する場合は、「**改変の手引き**」の注意事項をご確認ください。

### 2. 改変の手引き
本アセットでは、シーン全体を管理するルートオブジェクト（最上位オブジェクト）として、`PourOverCoffee`を使用します。
またコーヒー豆の情報を保存するオブジェクトとして、`Config`という名称のオブジェクトが存在します。
`PourOverCoffee` および `Config`は、**シーン内に必ず1つだけ存在するように配置してください**。


各種スキンPrefabは複数配置して組み合わせることができますが、本アセットに含まれるケトル、ドリッパー、サーバーなどのオブジェクトは、すべて`PourOverCoffee`の子オブジェクトとして配置する必要があります。

**正しい配置例**

PourOverCoffee
├─ Config
├─ Base Set
├─ Color - Silver Steel
│  ├─ Kettle
│  ├─ Dripper
│  └─ ...
├─ Color - Midnight Roast
│  ├─ Kettle
│  ├─ Dripper
│  └─ ...
└─ Color - Amber Sunset


**誤った配置例**

PourOverCoffee
├─ Config
├─ Base Set
└─ Color - Silver Steel

Color - Midnight Roast
Color - Amber Sunset

このように`PourOverCoffee`の外に配置されたPrefabは、システムから正しく認識されず、設定の反映などが正常に動作しない場合があります。

<img src="./source/s0.png" width="1200px">

**重要**

- `PourOverCoffee`はシーン内に1つだけ配置します。
- スキンPrefabは複数配置できます。
- すべてのスキンPrefabを`PourOverCoffee`の子オブジェクトにしてください。
- `Config`はシステムが使用するオブジェクトです。通常は移動、削除を行わないでください。


### 3. オブジェクトの複製

「Base Set」または「Color - xxx」のオブジェクトは「ctrl+D」で複製可能です。

複製後のオブジェクトは、特に設定不要でそのまま使用できます。

**⚠️注意事項**
「Color - xxx」のPrefab内には、非アクティブな状態で全てのカラーバリエーションのオブジェクトを配置しています。
非アクティブなオブジェクトは、デフォルトでは「Editor Only」（シーン上では見えるもののワールドにアップロードされない）状態になっています。
非アクティブなオブジェクトをワールドで使用したい場合は、「Editor Only」から「UnTagged」に変更してアップロードしてください。

<img src="./source/s1.png" width="1200px">

# ギミックの仕様と設定

各機器個別のマニュアルは現在準備中です。

基本的な使い方は、アセット内のタブレット端末よりご確認いただけます。

# お問い合わせ

不具合やご不明点に関するお問い合わせはBoothメッセージまでご連絡ください。  

https://sameno.booth.pm/

本商品を使用した作品のシェアは、ハッシュタグ「#さめのワークス」をご活用ください！  


---

# English Version  

English text translated using DeepL.

# Preparation in advance

Please have a Unity 2022.3.22f1 project when using this package.

It is not compatible with Unity 2019.

Please make sure to use VRCSDK 3.10.0 or later for this asset.

This product uses UdonSharp (U#).  

Please create a Unity project from Worlds U# in VCC (VRChat Creator Companion), and import this product.  

Other than VCC Worlds U# projects are not covered by support.  

## Sharder  

This asset uses liltoon and **lilPBR** shaders. 

Before installing this asset, please import the latest versions of both liltoon and **lilPBR** into your project via the URL below or through VCC. 

https://lilxyzw.booth.pm/items/3087170

# Setup

## Introduction  

After importing the Unitypackage file, place the prefab named “SamenoLatteArtSet” located in Assets/SamenoLab/VRCLatteArt anywhere in your scene.This completes the setup.

## Duplicating Objects

Objects directly under “SamenoLatteArtSet” can be duplicated by pressing “ctrl+D”.
No special settings are required after duplication in Unity.

# Gimmick Specifications

Individual manuals for each device are currently under preparation.

Basic usage instructions can be found on the tablet device included in the asset.

# Contact

If you have any questions about problems or concerns, please contact Booth Messages.  

https://sameno.booth.pm/

To share your work using this product, please use the hashtag #SamenoWorks !