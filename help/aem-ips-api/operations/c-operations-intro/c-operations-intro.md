---
description: IPS Web サービス APIで処理される一般的な操作パラメーターについて説明します。
solution: Experience Manager
title: 運用方法
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 020c8e63-ad4e-4c0d-8da6-b51efb2b89a5
TQID: 'https://experienceleague.adobe.com/ZoT9qmMjkkdVARrEvxhRn3Tvme1anUZ4-i1xLv0acb8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 717
ht-degree: 0%

---

# 運用方法{#operations-methods}

この節では、IPS Web サービス APIで処理される一般的な操作パラメーターについて説明します。

各操作パラメーターの詳細については、[操作パラメーター](/help/aem-ips-api/operations/c-operations-intro/c-methods/c-methods.md)を参照してください。

## ハンドル：概要 {#section-094ce1afa6244fa5b2c762f44ffdca1c}

特定のAPI操作によって返される参照IPS オブジェクトを処理します。 後続の操作呼び出しにハンドルをパラメーターとして渡すこともできます。 ハンドルは文字列データ型（`xsd:string`）です。

ハンドルは、単一のアプリケーションセッションでのみ使用することを目的としています。 さらに、IPS リリース間で形式が変更される可能性があるため、ハンドルを永続的にする必要があります。 インタラクティブなアプリケーションを作成する場合、セッションのタイムアウトを実装し、特にIPS アップグレード後にセッション間のすべてのハンドルを破棄します。 非インタラクティブアプリケーションを作成する場合は、アプリケーションが実行されるたびに適切な操作を呼び出してハンドルを取得します。 次のJava/Axis2 コードサンプルは、誤った正しいコード実行を示しています。

**ハンドル コードが正しくありません**

このコードサンプルは、会社ハンドルのハードコードされた値（555）を含んでいるため、正しくありません。

```
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle("555");// INCORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

**ハンドルコードを修正**

有効なハンドルを返すために`getCompanyInfo`が呼び出されるため、このコードサンプルは正しいです。 ハードコードされた値には依存しません。 必要なハンドルを返すには、このメソッドまたは他のIPS API同等のメソッドを使用します。

```
GetCompanyInfoParam companyInfoParam = new GetCompanyInfoParam(); 
companyInfoParam.setCompanyName("My Company"); GetCompanyInfoReturn companyInfoReturn = ipsApi.getCompanyInfo(companyInfoParam, authHeader); 
String companyHandle = companyInfoReturn.getCompanyInfo().getCompanyHandle(); 
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle(companyHandle); //CORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

## 共通ハンドルタイプ {#section-e683ac8283284f9688e63f51a494f7a0}

**companyHandle**

ほとんどの操作では、`companyHandle` パラメーターを渡すことで、会社のコンテキストを設定する必要があります。 会社ハンドルは、`getCompanyInfo`、`addCompany`、`getCompanyMembership`などの特定の操作によって返されるポインターです。

**userHandle**

`userHandle` パラメーターは、特定のユーザーをターゲットとする操作のオプション パラメーターです。 デフォルトでは、これらの操作は呼び出し元ユーザー（認証用に資格情報が渡されるユーザー）をターゲットにします。 ただし、適切な権限を持つ管理者ユーザーは、別のユーザーを指定できます。 例えば、`setPassword`操作は通常、認証済みユーザーのパスワードを設定しますが、管理者は`userHandle` パラメーターを使用して別のユーザーのパスワードを設定できます。

会社のコンテキスト（`companyHandle` パラメーターを使用）を必要とする操作の場合、認証済みユーザーとターゲットユーザーの両方が指定された会社のメンバーである必要があります。 会社のコンテキストを必要としない操作の場合、認証済みユーザーとターゲットユーザーの両方が、少なくとも1つの共通会社のメンバーである必要があります。

次の操作は、ユーザーハンドルを取得できます。

* `getUsers`
* `getAllUsers`
* `getUserInfo`
* `getCompanyMembers`
* `getGroupMembers`
* `addUser`

**accessUserHandleとaccessGroupHandle**

デフォルトでは、アクセス権限（読み取り、書き込み、削除）を必要とする操作は、呼び出し元ユーザーの権限コンテキストで実行されます。 特定の操作では、`accessUserHandle`または`accessGroupHandle` パラメーターを使用してこのコンテキストを変更できます。 `accessUserHandle` パラメーターを使用すると、管理者は別のユーザーになりすますことができます。 `accessGroupHandle` パラメーターを使用すると、呼び出し元は特定のユーザーグループのコンテキストで操作できます。

**responseFieldArrayおよびexcludeFieldArray**

一部の操作では、呼び出し元が応答に含めるフィールドを制限できます。 フィールドを制限することで、リクエストの処理に必要な時間とメモリを削減し、応答データのサイズを削減できます。 呼び出し元は、`responseFieldArray` パラメーターを渡すか、`excludeFieldArray` パラメーターを介して除外されたフィールドのリストを列挙して、特定のフィールドのリストを要求できます。

`responseFieldArray`と`excludeFieldArray`のどちらも、`/`で区切られたノードパスを使用してフィールドを指定します。 例えば、`searchAssets`が各アセットの名前、最終変更日、メタデータのみを返すように指定するには、次を参照してください。

```
<responseFieldArray> 
   <items>assetArray/items/name</items> 
   <items>assetArray/items/lastModified</items> 
   <items>assetArray/items/metadataArray</items> 
</responseFieldArray>
```

同様に、すべてのフィールドを返すには（権限を除く）:

```
<excludeFieldArray> 
   <items>assetArray/items/permissions</items> 
</excludeFieldArray>
```

ノードパスは、返されるノードのルートに対する相対パスであることに注意してください。 サブ要素を含まない複合型フィールドを指定した場合（例：`assetArray/items/imageInfo`）、そのサブ要素はすべて含まれます。 複合タイプフィールドで1つ以上のサブ要素（例：`assetArray/items/imageInfo/originalPath`）を指定した場合、それらのサブ要素のみが含まれます。

リクエストに`responseFieldArray`または`excludeFieldArray`を含めない場合、すべてのフィールドが返されます。

**ロケール**

IPS 4.0以降、IPS APIでは、`authHeader` ロケールパラメーターを渡すことにより、操作のロケールコンテキストの設定をサポートしています。 ロケールパラメーターが存在しない場合は、HTTP ヘッダー`Accept-Language`が使用されます。 このヘッダーも存在しない場合は、IPS サーバーのデフォルトのロケールが使用されます。

特定の操作では、操作ロケールコンテキストとは異なる場合がある、明示的なロケールパラメーターも使用します。 例えば、`submitJob`操作では、ジョブのログ記録とメール通知に使用されるロケールを設定する`locale` パラメーターが使用されます。

ロケールパラメーターは`<language_code>[-<country_code>]`形式を使用します

言語コードは小文字の2文字コードで、オプションの国コードは大文字の2文字コードで、ISO-3266で指定されます。 例えば、US Englishのロケール文字列は`en-US`です。
