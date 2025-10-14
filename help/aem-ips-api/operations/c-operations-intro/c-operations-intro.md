---
description: IPS Web サービス API で処理される一般的な操作パラメーターについて説明します。
solution: Experience Manager
title: 操作方法
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 020c8e63-ad4e-4c0d-8da6-b51efb2b89a5
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '704'
ht-degree: 0%

---

# 操作方法{#operations-methods}

ここでは、IPS Web サービス API で処理される一般的な操作パラメーターについて説明します。

各操作パラメーターの詳細については、「[&#x200B; 操作パラメーター &#x200B;](/help/aem-ips-api/operations/c-operations-intro/c-methods/c-methods.md)」を参照してください。

## ハンドル：概要 {#section-094ce1afa6244fa5b2c762f44ffdca1c}

特定の API 操作によって返された参照 IPS オブジェクトを処理します。 ハンドルをパラメーターとして、後続の操作呼び出しに渡すこともできます。 ハンドルは文字列データ型（`xsd:string`）です。

ハンドルは、単一のアプリケーションセッション中にのみ使用することを目的としています。 さらに、IPS リリース間で形式が変わる可能性があるので、ハンドルを永続的にする必要があります。 インタラクティブアプリケーションを記述する場合、特に IPS をアップグレードした後は、セッションのタイムアウトを実装し、セッション間のすべてのハンドルを破棄します。 非インタラクティブアプリケーションを記述する場合、アプリケーションが実行されるたびに適切な操作を呼び出してハンドルを取得します。 次の Java/Axis2 コードサンプルは、間違った正しいコード実行を示しています。

**ハンドルコードが正しくありません**

このコードサンプルは、会社ハンドルのハードコーディングされた値（555）を含んでいるので、正しくありません。

```
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle("555");// INCORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

**正しいハンドルコード**

`getCompanyInfo` を呼び出して有効なハンドルを返すので、このコードサンプルは正しいです。 ハードコーディングされた値には依存しません。 必要なハンドルを返すには、このメソッドまたは同等のその他の IPS API を使用します。

```
GetCompanyInfoParam companyInfoParam = new GetCompanyInfoParam(); 
companyInfoParam.setCompanyName("My Company"); GetCompanyInfoReturn companyInfoReturn = ipsApi.getCompanyInfo(companyInfoParam, authHeader); 
String companyHandle = companyInfoReturn.getCompanyInfo().getCompanyHandle(); 
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle(companyHandle); //CORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

## 一般的なハンドルタイプ {#section-e683ac8283284f9688e63f51a494f7a0}

**companyHandle**

ほとんどの操作では、`companyHandle` パラメーターを渡して会社コンテキストを設定する必要があります。 会社ハンドルは、`getCompanyInfo`、`addCompany`、`getCompanyMembership` などの特定の操作によって返されるポインターです。

**userHandle**

`userHandle` パラメーターは、特定のユーザーをターゲットにする操作のオプションのパラメーターです。 デフォルトでは、これらの操作は呼び出し元ユーザー（認証用に資格情報が渡されるユーザー）をターゲットにします。 ただし、適切な権限を持つ管理者ユーザーは、別のユーザーを指定できます。 例えば、`setPassword` の操作は、通常、認証済みユーザーのパスワードを設定しますが、管理者は `userHandle` パラメーターを使用して、別のユーザーのパスワードを設定できます。

会社コンテキストを必要とする操作の場合（`companyHandle` パラメーターを使用）、認証済みユーザーとターゲットユーザーの両方が指定した会社のメンバーである必要があります。 会社のコンテキストを必要としない操作の場合、認証済みユーザーとターゲットユーザーの両方が、1 つ以上の共通会社のメンバーである必要があります。

次の操作で、ユーザーハンドルを取得できます。

* `getUsers`
* `getAllUsers`
* `getUserInfo`
* `getCompanyMembers`
* `getGroupMembers`
* `addUser`

**accessUserHandle と accessGroupHandle**

デフォルトでは、アクセス権限（読み取り、書き込み、削除）を必要とする操作は、呼び出し元のユーザーの権限コンテキストで動作します。 特定の操作では、`accessUserHandle` または `accessGroupHandle` パラメーターを使用してこのコンテキストを変更できます。 `accessUserHandle` パラメーターを使用すると、管理者が別のユーザーとして実行できます。 `accessGroupHandle` パラメーターを使用すると、呼び出し元は特定のユーザーグループのコンテキストで操作できます。

**responseFieldArray と excludeFieldArray**

一部の操作では、応答に含めるフィールドを呼び出し元が制限できます。 フィールドを制限すると、リクエストの処理に必要な時間とメモリを削減し、応答データのサイズを小さくするのに役立ちます。 呼び出し元は、`responseFieldArray` パラメーターを渡して特定のフィールドのリストをリクエストするか、`excludeFieldArray` パラメーターを介して除外されたフィールドのリストを列挙してリクエストできます。

`responseFieldArray` と `excludeFieldArray` は両方とも、`/` で区切られたノードパスを使用してフィールドを指定します。 例えば、`searchAssets` が各アセットの名前、最終変更日およびメタデータのみを返すように指定するには、次を参照してください。

```
<responseFieldArray> 
   <items>assetArray/items/name</items> 
   <items>assetArray/items/lastModified</items> 
   <items>assetArray/items/metadataArray</items> 
</responseFieldArray>
```

同様に、すべてのフィールド（権限を除く）を返します。

```
<excludeFieldArray> 
   <items>assetArray/items/permissions</items> 
</excludeFieldArray>
```

ノードパスは、戻り値のノードルートに対する相対パスであることに注意してください。 サブ要素（例えば、`assetArray/items/imageInfo`）を含まない複合タイプフィールドを指定した場合、そのサブ要素がすべて含まれます。 複合タイプのフィールドに 1 つ以上のサブ要素を指定した場合（例：`assetArray/items/imageInfo/originalPath`）、それらのサブ要素のみが含まれます。

リクエストに `responseFieldArray` または `excludeFieldArray` を含めない場合、すべてのフィールドが返されます。

**ロケール**

IPS 4.0 以降、IPS API では `authHeader` ロケールパラメーターを渡すことで、操作のロケールコンテキストの設定をサポートしています。 ロケールパラメーターが存在しない場合は、HTTP ヘッダー `Accept-Language` が使用されます。 このヘッダーも存在しない場合、IPS サーバーのデフォルトのロケールが使用されます。

また、特定の操作は明示的なロケールパラメーターを取ります。これは操作のロケールコンテキストとは異なる場合があります。 例えば、`submitJob` 操作は、ジョブのログ記録とメール通知に使用されるロケールを設定する `locale` パラメーターを受け取ります。

ロケールパラメーターには、`<language_code>[-<country_code>]` の形式を使用します

言語コードが小文字の場合、ISO-639 で指定される 2 文字のコードで、オプションの国コードは、ISO-3266 で指定される大文字の 2 文字のコードです。 例えば、英語（米国）のロケール文字列は `en-US` です。
