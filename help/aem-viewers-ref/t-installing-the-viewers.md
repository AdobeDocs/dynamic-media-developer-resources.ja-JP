---
description: Dynamic MediaビューアAPIのインストール手順
seo-description: Dynamic MediaビューアAPIのインストール手順
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


# 同じサーバに複数のビューアをインストールする{#installing-multiple-viewers-on-the-same-server}

<!-- Updated June 1, 2020 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Dynamic MediaビューアAPIのインストール手順

画像サービングビューアをインストールする前に、画像サービングをインストールしてテストします。

ISビューアのファイルをハードドライブにコピーし、`s7viewers.war`ファイルを`../ImageServing/webapps`ディレクトリにデプロイします。 Image Serverのデプロイ、開始、停止および管理の方法については、画像サービングのドキュメントを参照してください。

>[!NOTE]
>
>画像サービングビューアには、アップグレードインストールはありません。 Adobeでは、インストールを続行する前に、既存のDynamic Mediaビューアディレクトリをバックアップすることをお勧めします。

**同じサーバにビューアをインストールするには**

1. ビューアの.warの名前を目的のコンテキストに変更し、目的の場所にファイルをデプロイします。
1. `config.js`に`this.isViewerRoot`パラメーターを設定します。
1. 新しく作成したビューアフォルダのルートにある`config.js`を開きます。
1. パラメーター`this.isViewerRoot = "/s7viewers"`を`s7viewers.war`ファイルのコンテキストに設定します。 例：`"/s7viewers-4.0"`。 ファイルを保存して閉じます。
1. ファイルを保存して閉じます。
