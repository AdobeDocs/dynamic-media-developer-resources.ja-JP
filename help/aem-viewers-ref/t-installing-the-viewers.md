---
title: 同じサーバでの複数のDynamic Mediaビューアのインストール
description: Dynamic Media Viewers APIのインストール手順です。
solution: Experience Manager
feature: Dynamic Media Classic，ビューア，SDK/API
role: Developer,Business Practitioner
exl-id: 7a8d7205-d3bf-4ca8-b80a-9072436a3df5
source-git-commit: 8207cba7e75c6bff878ef7f11f74b19bb88f1d61
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 0%

---

# 同じサーバでの複数のビューアのインストール{#installing-multiple-viewers-on-the-same-server}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Dynamic MediaビューアAPIのインストール手順

画像サービングビューアをインストールする前に、画像サービングをインストールしてテストします。

ISビューアのファイルをハードドライブにコピーし、`s7viewers.war`ファイルを`../ImageServing/webapps`ディレクトリにデプロイします。 Image Serverのデプロイ、開始、停止、管理の方法については、画像サービングのドキュメントを参照してください。

>[!NOTE]
>
>画像サービングビューアにはアップグレードインストールはありません。 Adobeでは、インストールを続行する前に、既存のDynamic Mediaビューア(s7viewers)ディレクトリをバックアップすることをお勧めします。

**同じサーバに複数のビューアをインストールするには：**

1. ビューアの.warの名前を目的のコンテキストに変更し、目的の場所にファイルをデプロイします。
1. `config.js`に`this.isViewerRoot`パラメーターを設定します。
1. 新しく作成したビューアフォルダのルートで`config.js`を開きます。
1. `this.isViewerRoot = "/s7viewers"`パラメーターを`s7viewers.war`ファイルのコンテキストに設定します。 例えば、`"/s7viewers-4.0"`のように指定します。
1. ファイルを保存して閉じます。
