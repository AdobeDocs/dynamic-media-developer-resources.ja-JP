---
description: コンテンツデータフォルダーには、これらのサーバー設定を使用します。
solution: Experience Manager
title: コンテンツデータフォルダー
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9aa4121f-25f8-49d0-a304-7ae756c046f5
TQID: 'https://experienceleague.adobe.com/IM1zNaaqC0zD36pUobHIL0Z-rlcrZoujnPbpBtOXq1Y'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 226
ht-degree: 0%

---

# コンテンツデータフォルダー{#content-data-folders}

コンテンツデータフォルダーには、これらのサーバー設定を使用します。

## IS::RootPath - イメージ データ ルート フォルダー {#section-5c57569514bb4d00b19de31d2e137e3b}

画像、フォント、ICC プロファイルを含む、すべてのソースデータの場所。 これは、セミコロンで区切られた&#x200B;*[!DNL install_folder]*&#x200B;に関連する1つ以上の絶対ファイルパスまたはパスにすることができます。 空の場合、*[!DNL install_folder]*&#x200B;がデフォルトのルートになります。 複数の値を指定して、複数のファイルシステムに画像データを配信できます。 Image Serverは、要求されたファイルが見つかるまで、指定された順序でルートパスを試行します。

## PS::staticContent.rootPath – 静的コンテンツデータルートフォルダー {#section-a4f5b6942b7b4abdbf825b1f2e932cfe}

[!DNL /is/static] コンテキストを介して配信される静的コンテンツソースデータの場所。 1つ以上の絶対ファイルパスまたは&#x200B;*[!DNL install_folder]*&#x200B;からの相対パスを、セミコロンで区切って指定できます。 空の場合、*[!DNL install_folder]*&#x200B;がデフォルトのルートになります。

複数の値をセミコロンで区切って指定すると、複数のファイルシステムに静的コンテンツを配信できます。 通常は`IS::RootPath`と同じ値に設定されます。

[!DNL Platform Server]は、要求されたファイルが見つかるまで、指定された順序でルートパスを試行します。

>[!NOTE]
>
>デフォルトでは、このフィールドは意図的に存在しない場所（[!DNL *[!DNL install_folder]*/static]）に設定されており、静的コンテンツサービスは無効になっています。

## IS::SaveDirectory - ファイル保存ルートフォルダー {#section-1c517f8d49ce4cb8b9013e520bf309c9}

`attribute::SavePath`のルートパス（`req=saveToFile`によって使用）。 Image Serverには、画像ファイルを作成するサブフォルダーに対するアクセス権限が必要です。
