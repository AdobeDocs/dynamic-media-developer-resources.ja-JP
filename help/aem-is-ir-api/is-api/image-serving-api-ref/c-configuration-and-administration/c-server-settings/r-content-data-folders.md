---
description: コンテンツデータフォルダーには、次のサーバー設定を使用します。
seo-description: コンテンツデータフォルダーには、次のサーバー設定を使用します。
seo-title: コンテンツデータフォルダー
solution: Experience Manager
title: コンテンツデータフォルダー
topic: Scene7 Image Serving - Image Rendering API
uuid: 7c4d60ca-8a8b-453c-887d-a6a16eacc883
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---


# コンテンツデータフォルダー{#content-data-folders}

コンテンツデータフォルダーには、次のサーバー設定を使用します。

## IS::RootPath — 画像データのルートフォルダ {#section-5c57569514bb4d00b19de31d2e137e3b}

画像、フォント、ICCプロファイルを含む、すべてのソースデータの場所。 絶対ファイルパスまたはに対する相対パスを、セミコロンで区切って1つ以上指 *[!DNL install_folder]*&#x200B;定できます。 空の場合、 *[!DNL install_folder]* がデフォルトのルートです。 複数の値を指定して、複数のファイルシステムに画像データを配分できます。 要求されたファイルが見つかるまで、Image Serverは指定された順序でルートパスを試します。

## PS::staticContent.rootPath — 静的コンテンツデータのルートフォルダー {#section-a4f5b6942b7b4abdbf825b1f2e932cfe}

コンテキストを介して配信される静的コンテンツソースデータの場所 [!DNL /is/static] です。 絶対ファイルパスまたはに対する相対パスをセミコロンで区切って指定 *[!DNL install_folder]*&#x200B;します。 空の場合、 *[!DNL install_folder]* がデフォルトのルートです。

複数の値をセミコロンで区切って指定すると、静的なコンテンツを複数のファイルシステムに分散できます。 通常、と同じ値に設定し `IS::RootPath`ます。

Platformサーバーは、要求されたファイルが見つかるまで、指定された順序でルートパスを試します。

>[!NOTE]
>
>デフォルトでは、このフィールドは意図的に存在しない場所([!DNL *[!DNL install_folder]*/static])に設定され、静的コンテンツサービスが効果的に無効になっています。

## IS::SaveDirectory — ファイルルートフォルダの保存 {#section-1c517f8d49ce4cb8b9013e520bf309c9}

のルートパス `attribute::SavePath` (によって使用 `req=saveToFile`)。 Image Serverは、画像ファイルを作成するサブフォルダーの作成アクセス権限が必要です。
