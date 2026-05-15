---
description: キャッシュエントリは、属性CacheValidationPolicy （デフォルトでは.iniまたは特定の画像カタログの.ini ファイル）で選択されたカタログベースまたは有効期限ベースのキャッシュ検証を使用して自動的に更新されます。
solution: Experience Manager
title: 応答キャッシュの検証
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d2baa6e6-2700-450f-af1e-88b6d33d0e0c
TQID: 'https://experienceleague.adobe.com/VnvYNkc3yijayG8tnJKHsp94Qto8VZj9OkIgfIv1Kc0'
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
source-wordcount: 311
ht-degree: 0%

---

# 応答キャッシュの検証{#response-cache-validation}

キャッシュエントリは、属性：:CacheValidationPolicy （default.iniまたは特定の画像カタログの.ini ファイル）で選択したカタログベースまたは有効期限ベースのキャッシュ検証を使用して自動的に更新されます。

カタログベースの検証では、`catalog::LastModified` （または`attribute::LastModified`、または[!DNL catalog.ini] ファイルのファイル変更時間）がキャッシュエントリの作成日時よりも新しい場合、既存のキャッシュエントリは古いと見なされます。

有効期限ベースの検証では、最新の検証から5分後にキャッシュエントリが古くなります。 どちらの場合も、サーバーは、リクエストの作成に関連するすべての画像ファイルのファイル日付を確認することで、古いキャッシュエントリを検証します。 ファイルの日付が変更されていない場合、キャッシュエントリのタイムスタンプが更新され、キャッシュされた日付は有効と見なされます。

主に画像カタログに登録されている画像を含む一般的なアプリケーションでは、カタログベースの検証がパフォーマンス上の優位性をもたらします。 画像カタログを含まないアプリケーションでは、有効期限ベースのキャッシュ検証を使用する必要があります。 これを実現する方法の1つは、[!DNL default.ini]に`attribute::cacheValidationPolicy=0`を設定し、特定のすべての画像カタログファイルに`1`を設定することです。

キャッシュエントリは無効になり、リクエストに含まれるカタログエントリが返信画像の変更を引き起こす可能性のある方法で変更されると、再生成される可能性があります。 例えば、`catalog::Modifier`の内容が変更されます。

>[!NOTE]
>
>Dynamic Media ピラミッド TIFF（PTIFF）画像は、検証のために、ファイルの日付をファイルヘッダーに内部的に保持します。 ファイルシステムが保持するファイル変更時間は、非PTIFF ファイルが変更されたかどうかを確認するために使用されます。

キャッシュ検証プロセスに参加するのは画像ファイルのみです。 フォントファイルまたはICC プロファイルファイルを変更しても、キャッシュエントリが自動的に無効化されることはありません。
