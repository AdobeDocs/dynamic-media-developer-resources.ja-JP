---
description: これらのサーバー設定をコンテンツ データ フォルダーに使用します。
solution: Experience Manager
title: コンテンツデータフォルダー
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9aa4121f-25f8-49d0-a304-7ae756c046f5
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# コンテンツデータフォルダー{#content-data-folders}

これらのサーバー設定をコンテンツ データ フォルダーに使用します。

## IS::RootPath – 画像データのルートフォルダ {#section-5c57569514bb4d00b19de31d2e137e3b}

画像、フォント、ICC プロファイルを含む、すべてのソースデータの場所。 1 つ以上の絶対ファイルパスまたは *[!DNL install_folder]* に対する相対パスをセミコロンで区切って指定できます。 空の場合は、デフォル *[!DNL install_folder]* ルートです。 複数の値を指定して、複数のファイルシステムに画像データを分散させることができます。 Image Server は、要求されたファイルが見つかるまで、指定された順序でルートパスを試行します。

## PS::staticContent.rootPath – 静的コンテンツ データのルート フォルダー {#section-a4f5b6942b7b4abdbf825b1f2e932cfe}

[!DNL /is/static] コンテキストを介して配信されることを意図した静的コンテンツソースデータの場所。 1 つ以上の絶対ファイルパス、または *[!DNL install_folder]* に対する相対パスをセミコロンで区切って指定できます。 空の場合は、デフォル *[!DNL install_folder]* ルートです。

複数の値をセミコロンで区切って指定すると、静的コンテンツを複数のファイルシステムに分散させることができます。 通常は、`IS::RootPath` と同じ値に設定します。

[!DNL Platform Server] は、リクエストされたファイルが見つかるまで、指定された順序でルートパスを試します。

>[!NOTE]
>
>デフォルトでは、このフィールドは存在しない場所（[!DNL *[!DNL install_folder]*/static]）に意図的に設定されており、静的コンテンツサービスが効果的に無効になります。

## IS::SaveDirectory - ファイル ルートフォルダを保存する {#section-1c517f8d49ce4cb8b9013e520bf309c9}

`attribute::SavePath` のルートパス （`req=saveToFile` で使用）。 Image Server には、画像ファイルを作成するサブフォルダーに対する作成アクセス権が必要です。
