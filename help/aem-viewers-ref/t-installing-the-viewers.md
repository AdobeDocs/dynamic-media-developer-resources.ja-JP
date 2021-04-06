---
title: 同じサーバでの複数のDynamic Mediaビューアのインストール
description: Dynamic MediaビューアAPIのインストール手順
solution: Experience Manager
feature: Dynamic Mediaクラシック，ビューア，SDK/API
role: 開発者、業務従事者
exl-id: 7a8d7205-d3bf-4ca8-b80a-9072436a3df5
translation-type: tm+mt
source-git-commit: 8207cba7e75c6bff878ef7f11f74b19bb88f1d61
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%

---

# 同じサーバに複数のビューアをインストールする{#installing-multiple-viewers-on-the-same-server}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Dynamic MediaビューアAPIのインストール手順

画像サービングビューアをインストールする前に、画像サービングをインストールしてテストします。

ISビューアのファイルをハードドライブにコピーし、`s7viewers.war`ファイルを`../ImageServing/webapps`ディレクトリにデプロイします。 Image Serverのデプロイ、開始、停止および管理の方法については、画像サービングのドキュメントを参照してください。

>[!NOTE]
>
>画像サービングビューアには、アップグレードインストールはありません。 Adobeでは、インストールを続行する前に、既存のDynamic Mediaビューア(s7viewers)ディレクトリをバックアップすることをお勧めします。

**同じサーバに複数のビューアをインストールするには：**

1. ビューアの.warの名前を目的のコンテキストに変更し、目的の場所にファイルをデプロイします。
1. `config.js`に`this.isViewerRoot`パラメーターを設定します。
1. 新しく作成したビューアフォルダのルートにある`config.js`を開きます。
1. パラメーター`this.isViewerRoot = "/s7viewers"`を`s7viewers.war`ファイルのコンテキストに設定します。 例：`"/s7viewers-4.0"`。
1. ファイルを保存して閉じます。
