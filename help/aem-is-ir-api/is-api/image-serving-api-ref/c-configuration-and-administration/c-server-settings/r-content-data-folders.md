---
description: コンテンツデータフォルダに対して、次のサーバ設定を使用します。
solution: Experience Manager
title: コンテンツデータフォルダー
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9aa4121f-25f8-49d0-a304-7ae756c046f5
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# コンテンツデータフォルダー{#content-data-folders}

コンテンツデータフォルダに対して、次のサーバ設定を使用します。

## IS::RootPath — 画像データのルートフォルダ {#section-5c57569514bb4d00b19de31d2e137e3b}

画像、フォント、ICC プロファイルを含む、すべてのソースデータの場所。 ファイルの絶対パスまたはファイルの相対パスを指定できます。 *[!DNL install_folder]*&#x200B;セミコロンで区切られます。 空の場合、 *[!DNL install_folder]* はデフォルトのルートです。 複数の値を指定して、複数のファイルシステムに画像データを配分できます。 Image Server は、要求されたファイルが見つかるまで、指定された順序でルートパスを試行します。

## PS::staticContent.rootPath — 静的コンテンツデータのルートフォルダ {#section-a4f5b6942b7b4abdbf825b1f2e932cfe}

静的コンテンツソースデータの場所で、 [!DNL /is/static] コンテキスト。 ファイルの絶対パスまたはファイルの相対パスを指定できます。 *[!DNL install_folder]*&#x200B;セミコロンで区切られます。 空の場合、 *[!DNL install_folder]* はデフォルトのルートです。

複数の値をセミコロンで区切って指定し、複数のファイルシステムに静的コンテンツを配信できます。 通常、次と同じ値に設定します。 `IS::RootPath`.

この [!DNL Platform Server] は、要求されたファイルが見つかるまで、指定された順序でルートパスを試みます。

>[!NOTE]
>
>デフォルトでは、このフィールドは意図的に存在しない場所 ([!DNL *[!DNL install_folder]*/static]) を使用して、静的コンテンツサービスを効果的に無効にします。

## IS::SaveDirectory — ファイルルートフォルダを保存 {#section-1c517f8d49ce4cb8b9013e520bf309c9}

のルートパス `attribute::SavePath` ( 次で使用： `req=saveToFile`) をクリックします。 Image Server には、イメージファイルを作成するサブフォルダーの作成アクセス権が必要です。
