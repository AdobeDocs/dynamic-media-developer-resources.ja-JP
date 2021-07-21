---
description: コンテンツデータフォルダに対して、これらのサーバ設定を使用します。
solution: Experience Manager
title: コンテンツデータフォルダー
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin,User
exl-id: 9aa4121f-25f8-49d0-a304-7ae756c046f5
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 0%

---

# コンテンツデータフォルダー{#content-data-folders}

コンテンツデータフォルダに対して、これらのサーバ設定を使用します。

## IS::RootPath — 画像データのルートフォルダ {#section-5c57569514bb4d00b19de31d2e137e3b}

画像、フォント、ICCプロファイルを含む、すべてのソースデータの場所。 絶対ファイルパスまたは&#x200B;*[!DNL install_folder]*&#x200B;に対する相対パスを、セミコロンで区切って指定できます。 空の場合は、*[!DNL install_folder]*&#x200B;がデフォルトのルートになります。 複数の値を指定して、複数のファイルシステムにイメージデータを配分できます。 Image Serverは、要求されたファイルが見つかるまで、指定された順序でルートパスを試みます。

## PS::staticContent.rootPath — 静的コンテンツデータのルートフォルダ {#section-a4f5b6942b7b4abdbf825b1f2e932cfe}

[!DNL /is/static]コンテキスト経由で配信する静的コンテンツソースデータの場所。 絶対ファイルパスまたは&#x200B;*[!DNL install_folder]*&#x200B;に対する相対パスを、セミコロンで区切って指定できます。 空の場合は、*[!DNL install_folder]*&#x200B;がデフォルトのルートになります。

複数の値をセミコロンで区切って指定し、複数のファイルシステムに静的コンテンツを配布できます。 通常、`IS::RootPath`と同じ値に設定します。

Platform Serverは、要求されたファイルが見つかるまで、指定された順序でルートパスを試みます。

>[!NOTE]
>
>デフォルトでは、このフィールドは意図的に存在しない場所([!DNL *[!DNL install_folder]*/static])に設定され、静的コンテンツサービスが効果的に無効になっています。

## IS::SaveDirectory — ファイルルートフォルダの保存 {#section-1c517f8d49ce4cb8b9013e520bf309c9}

`attribute::SavePath`のルートパス（`req=saveToFile`で使用）。 Image Serverには、イメージファイルを作成するサブフォルダーの作成アクセス権限が必要です。
