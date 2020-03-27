---
description: コンテンツデータフォルダーには、次のサーバー設定を使用します。
seo-description: コンテンツデータフォルダーには、次のサーバー設定を使用します。
seo-title: コンテンツデータフォルダー
solution: Experience Manager
title: コンテンツデータフォルダー
topic: Scene7 Image Serving - Image Rendering API
uuid: 7c4d60ca-8a8b-453c-887d-a6a16eacc883
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# コンテンツデータフォルダー{#content-data-folders}

コンテンツデータフォルダーには、次のサーバー設定を使用します。

## IS::RootPath — イメージデータのルートフォルダ {#section-5c57569514bb4d00b19de31d2e137e3b}

画像、フォント、ICCプロファイルを含む、すべてのソースデータの場所。 絶対ファイルパスまたはに対する相対パスをセミコロンで区切っ *[!DNL install_folder]*&#x200B;て指定できます。 空の場合、がデ *[!DNL install_folder]* フォルトのルートです。 複数の値を指定して、複数のファイルシステムに画像データを配分できます。 要求されたファイルが見つかるまで、Image Serverは指定された順序でルートパスを試みます。

## PS::staticContent.rootPath — 静的コンテンツデータのルートフォルダー {#section-a4f5b6942b7b4abdbf825b1f2e932cfe}

コンテキストを介して配信される静的コンテンツソースデータの [!DNL /is/static] 場所。 絶対ファイルパスまたはセミコロンで区切った相対パスを1つ *[!DNL install_folder]*&#x200B;以上指定できます。 空の場合、がデ *[!DNL install_folder]* フォルトのルートです。

複数の値をセミコロンで区切って指定し、複数のファイルシステムに静的なコンテンツを配信できます。 通常、と同じ値に設定します `IS::RootPath`。

プラットフォームサーバーは、要求されたファイルが見つかるまで、指定された順序でルートパスを試行します。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>デフォルトでは、このフィールドは意図的に存在しない場所([!DNL *[!DNL install_folder]*/static])に設定され、静的コンテンツサービスが効果的に無効になります。

## IS::SaveDirectory — ファイルルートフォルダを保存 {#section-1c517f8d49ce4cb8b9013e520bf309c9}

のルートパ `attribute::SavePath` ス(によって `req=saveToFile`使用)。 Image Serverは、画像ファイルを作成するサブフォルダの作成アクセス権限を持っている必要があります。
