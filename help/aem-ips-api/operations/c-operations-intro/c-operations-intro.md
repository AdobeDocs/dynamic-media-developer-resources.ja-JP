---
description: この節では、IPS Web Service APIで処理される一般的な操作パラメータについて説明します。
seo-description: この節では、IPS Web Service APIで処理される一般的な操作パラメータについて説明します。
seo-title: 操作メソッド
solution: Experience Manager
title: 操作メソッド
topic: Scene7 Image Production System API
uuid: 713646a7-1108-4f93-bec2-3fbe7e548515
translation-type: tm+mt
source-git-commit: 806e7e670ee98e1fb6adf52ffc95fb989fa69400
workflow-type: tm+mt
source-wordcount: '718'
ht-degree: 0%

---


# 操作メソッド{#operations-methods}

この節では、IPS Web Service APIで処理される一般的な操作パラメータについて説明します。

各操作パラメーターの詳細な説明については、[操作パラメーター](/help/aem-ips-api/operations/c-operations-intro/c-methods/c-methods.md)を参照してください。

## ハンドル：{#section-094ce1afa6244fa5b2c762f44ffdca1c}について

特定のAPI操作によって返された参照IPSオブジェクトを処理します。 後続の操作呼び出しにハンドルをパラメーターとして渡すこともできます。 ハンドルは、文字列データ型(`xsd:string`)です。

ハンドルは、単一のアプリケーションセッション中のみ使用されます。 さらに、IPSリリース間で形式が変わる可能性があるので、処理を持続的に行う必要があります。 インタラクティブアプリケーションを書き込む場合、セッションタイムアウトを実装し、特にIPSのアップグレード後に、セッション間のすべてのハンドルを破棄します。 非インタラクティブアプリケーションを作成する場合は、適切な操作を呼び出して、アプリケーションを実行するたびにハンドルを取得します。 以下のJava/Axis2コードのサンプルは、誤った正しいコード実行を示します。

**不正なハンドルコード**

このコードサンプルは、会社ハンドルにハードコードされた値(555)が含まれているので、正しくありません。

```
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle("555");// INCORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

**正しいハンドルコード**

このコードサンプルは正しいです。有効なハンドルを返すために`getCompanyInfo`を呼び出します。 ハードコードされた値に依存しません。 必要なハンドルを返すのに相当する、このメソッドまたは他のIPS APIを使用します。

```
GetCompanyInfoParam companyInfoParam = new GetCompanyInfoParam(); 
companyInfoParam.setCompanyName("My Company"); GetCompanyInfoReturn companyInfoReturn = ipsApi.getCompanyInfo(companyInfoParam, authHeader); 
String companyHandle = companyInfoReturn.getCompanyInfo().getCompanyHandle(); 
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle(companyHandle); //CORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

## 共通ハンドルの種類{#section-e683ac8283284f9688e63f51a494f7a0}

**companyHandle**

ほとんどの操作では、`companyHandle`パラメーターを渡して会社コンテキストを設定する必要があります。 会社ハンドルは、`getCompanyInfo`、`addCompany`、`getCompanyMembership`などの特定の操作によって返されるポインタです。

**userHandle**

`userHandle`パラメーターは、特定のユーザーがターゲットする操作のオプションのパラメーターです。 デフォルトでは、これらの操作は呼び出し元のユーザー（認証用に資格情報が渡されるユーザー）をターゲットします。 ただし、適切な権限を持つ管理者ユーザーは、別のユーザーを指定できます。 例えば、`setPassword`操作は通常、認証済みユーザーのパスワードを設定しますが、管理者は`userHandle`パラメーターを使用して別のユーザーのパスワードを設定できます。

会社コンテキストを必要とする操作（`companyHandle`パラメーターを使用）の場合、認証済みユーザーとターゲットユーザーの両方が、指定した会社のメンバーである必要があります。 会社コンテキストを必要としない操作の場合、認証済みユーザーとターゲットユーザーの両方が、少なくとも1つの共通会社のメンバーである必要があります。

次の操作で、ユーザーハンドルを取得できます。

* `getUsers`
* `getAllUsers`
* `getUserInfo`
* `getCompanyMembers`
* `getGroupMembers`
* `addUser`

**accessUserHandleとaccessGroupHandle**

デフォルトでは、アクセス権限（読み取り、書き込み、削除）を必要とする操作は、呼び出し元ユーザーの権限コンテキストで動作します。 一部の操作では、`accessUserHandle`または`accessGroupHandle`パラメーターを使用してこのコンテキストを変更できます。 `accessUserHandle`パラメーターを使用すると、管理者が別のユーザーを装うことができます。 `accessGroupHandle`パラメーターは、呼び出し元が特定のユーザーグループのコンテキストで動作することを許可します。

**responseFieldArrayおよびexcludeFieldArray**

一部の操作では、呼び出し元が応答に含めるフィールドを制限できます。 フィールドを制限すると、リクエストの処理に必要な時間とメモリを削減し、応答データのサイズを小さくするのに役立ちます。 呼び出し元は、`responseFieldArray`パラメーターを渡すか、`excludeFieldArray`パラメーターを介して除外されたフィールドのリストを列挙して、フィールドの特定のリストを要求できます。

`responseFieldArray`と`excludeFieldArray`の両方は、`/`で区切られたノードパスを使用してフィールドを指定します。 例えば、`searchAssets`が各アセットの名前、最終変更日、およびメタデータのみを返すように指定するには、次を参照します。

```
<responseFieldArray> 
   <items>assetArray/items/name</items> 
   <items>assetArray/items/lastModified</items> 
   <items>assetArray/items/metadataArray</items> 
</responseFieldArray>
```

同様に、（権限を除く）すべてのフィールドを返すには：

```
<excludeFieldArray> 
   <items>assetArray/items/permissions</items> 
</excludeFieldArray>
```

ノードパスは、戻りノードのルートに対する相対パスであることに注意してください。 複合型フィールドにその副要素を含めない（例：`assetArray/items/imageInfo`）と指定した場合、その副要素がすべて含まれます。 複合型フィールドに1つ以上の副要素（例：`assetArray/items/imageInfo/originalPath`）を指定すると、それらの副要素のみが含まれます。

リクエストに`responseFieldArray`または`excludeFieldArray`を含めない場合は、すべてのフィールドが返されます。

**ロケール**

IPS 4.0以降、IPS APIは、`authHeader`ロケールパラメータを渡すことによる操作のロケールコンテキストの設定をサポートしています。 ロケールパラメータが存在しない場合は、HTTPヘッダ`Accept-Language`が使用されます。 このヘッダも存在しない場合は、IPSサーバの既定のロケールが使用されます。

一部の操作では、明示的なロケールパラメーターも使用します。これは、操作のロケールコンテキストとは異なる場合があります。 例えば、`submitJob`操作では、ジョブのログおよび電子メール通知に使用するロケールを設定する`locale`パラメーターを使用します。

ロケールパラメーターは、`<language_code>[-<country_code>]`の形式を使用します

言語コードがISO-639で指定された小文字の2文字のコードで、オプションの国コードがISO-3266で指定された大文字の2文字のコードである場合、 例えば、米国英語のロケール文字列は`en-US`です。
