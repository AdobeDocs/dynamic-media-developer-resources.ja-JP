---
description: ダイナミックメディアビューアAPIのインストール手順を説明します。
seo-description: ダイナミックメディアビューアAPIのインストール手順を説明します。
seo-title: 同じサーバでの複数のビューアのインストール
solution: Experience Manager
title: 同じサーバでの複数のビューアのインストール
topic: Dynamic media
uuid: 91ae8eb5-1d23-4fa3-a0d6-a4a0ed0eb104
translation-type: tm+mt
source-git-commit: a0983053795cc119eb57386c005e1f8a7c2fa3e4
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---


# 同じサーバでの複数のビューアのインストール{#installing-multiple-viewers-on-the-same-server}

<!-- Updated June 1, 2020 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

ダイナミックメディアビューアAPIのインストール手順を説明します。

画像サービングビューアをインストールする前に、画像サービングをインストールしてテストします。

ISビューアのファイルをハードドライブにコピーし、その `s7viewers.war` ファイルを `../ImageServing/webapps` ディレクトリにデプロイします。 Image Serverのデプロイ、開始、停止および管理の方法については、画像サービングのドキュメントを参照してください。

>[!NOTE]
>
>画像サービングビューアには、アップグレードインストールはありません。 インストールを続行する前に、既存のダイナミックメディアビューアディレクトリをバックアップしておくことをお勧めします。

**同じサーバにビューアをインストールするには**

1. ビューアの.warの名前を目的のコンテキストに変更し、目的の場所にファイルをデプロイします。
1. で `this.isViewerRoot` パラメータを設定し `config.js`ます。
1. 新しく作成 `config.js` したビューアフォルダのルートにあるを開きます。
1. パラメータ `this.isViewerRoot = "/s7viewers"` ーを `s7viewers.war` ファイルのコンテキストに設定します。 For example, `"/s7viewers-4.0"`. ファイルを保存して閉じます。
1. ファイルを保存して閉じます。
