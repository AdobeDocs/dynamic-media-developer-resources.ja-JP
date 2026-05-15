---
title: 同じサーバーに複数のDynamic Media ビューアをインストールする
description: Dynamic Media ビューア APIのインストール手順。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 7a8d7205-d3bf-4ca8-b80a-9072436a3df5
TQID: 'https://experienceleague.adobe.com/Zz0BTc333AIELPKRWFeIxhNvTyOJZH1RHLYNvZpt-ZY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 160
ht-degree: 0%

---

# 同じサーバーに複数のビューアをインストールする{#installing-multiple-viewers-on-the-same-server}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Dynamic Media ビューア APIのインストール手順。

Image Serving ビューアをインストールする前に、Image Servingをインストールしてテストします。

IS ビューア ファイルをハード ドライブにコピーしてから、`s7viewers.war` ファイルを`../ImageServing/webapps` ディレクトリにデプロイします。 Image Serverのデプロイ、開始、停止、および管理の方法については、Image Servingのドキュメントを参照してください。

>[!NOTE]
>
>画像サービングビューアのアップグレードインストールはありません。 Adobeでは、インストールを続行する前に、既存のDynamic Media ビューア（s7viewers）ディレクトリをバックアップすることをお勧めします。

**同じサーバーに複数のビューアをインストールするには：**

1. ビューアの.warの名前を目的のコンテキストに変更し、目的の場所にファイルをデプロイします。
1. `config.js`で`this.isViewerRoot` パラメーターを設定します。
1. 新しく作成したビューアーフォルダーのルートで`config.js`を開きます。
1. パラメーター`this.isViewerRoot = "/s7viewers"`を`s7viewers.war` ファイルのコンテキストに設定します。 例：`"/s7viewers-4.0"`。
1. ファイルを保存して閉じます。
