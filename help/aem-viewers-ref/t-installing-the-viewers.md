---
title: 同じサーバーへの複数の Dynamic Media ビューアのインストール
description: Dynamic Media ビューア API のインストール手順。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 7a8d7205-d3bf-4ca8-b80a-9072436a3df5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# 同じサーバーへの複数のビューアのインストール{#installing-multiple-viewers-on-the-same-server}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Dynamic Media ビューア API のインストール手順。

画像サービングビューアをインストールする前に、画像サービングをインストールしてテストします。

IS ビューアファイルをハードドライブにコピーし、`s7viewers.war` ファイルを `../ImageServing/webapps` ディレクトリにデプロイします。 Image Server のデプロイ、開始、停止、管理方法については、画像サービングのドキュメントを参照してください。

>[!NOTE]
>
>画像サービングビューアのアップグレードインストールはありません。 Adobeでは、インストールを続行する前に、既存の Dynamic Media ビューア（s7viewers）ディレクトリをバックアップすることをお勧めします。

**同じサーバーに複数のビューアをインストールするには：**

1. ビューアの.war の名前を目的のコンテキストに変更し、ファイルを目的の場所にデプロイします。
1. `this.isViewerRoot``config.js` パラメーターを設定します。
1. 新しく作成したビューアフォルダーのルートにある `config.js` を開きます。
1. パラメーター `this.isViewerRoot = "/s7viewers"` を `s7viewers.war` ファイルのコンテキストに設定します。 例：`"/s7viewers-4.0"`。
1. ファイルを保存して閉じます。
