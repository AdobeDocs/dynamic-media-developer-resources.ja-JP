---
description: Scene7ビューアAPIのインストール手順を説明します。
seo-description: Scene7ビューアAPIのインストール手順を説明します。
seo-title: 同じサーバへの複数のビューアのインストール
solution: Experience Manager
title: 同じサーバへの複数のビューアのインストール
topic: Dynamic media
uuid: 91ae8eb5-1d23-4fa3-a0d6-a4a0ed0eb104
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 同じサーバへの複数のビューアのインストール{#installing-multiple-viewers-on-the-same-server}

Scene7ビューアAPIのインストール手順を説明します。

画像サービングビューアをインストールする前に、画像サービングをインストールしてテストします。

ISビューアのファイルをハードドライブにコピーし、そのファイルをディレ `s7viewers.war` クトリにデプロイ `../ImageServing/webapps` します。 Image Serverのデプロイ、起動、停止および管理の方法については、画像サービングのドキュメントを参照してください。

>[!NOTE]
>
>画像サービングビューア用のアップグレードインストールはありません。 インストールを続行する前に、既存のScene7ビューアディレクトリをバックアップすることをお勧めします。

**ビューアを同じサーバにインストールするには**

1. ビューアの.warの名前を目的のコンテキストに変更し、目的の場所にファイルをデプロイします。
1. でパラメータ `this.isViewerRoot` ーを設定しま `config.js`す。
1. 新しく `config.js` 作成したビューアフォルダのルートにあるを開きます。
1. ファイルのコ `this.isViewerRoot = "/s7viewers"` ンテキストにパラメータを設定 `s7viewers.war` します。 For example, `"/s7viewers-4.0"`. ファイルを保存して閉じます。
1. ファイルを保存して閉じます。
