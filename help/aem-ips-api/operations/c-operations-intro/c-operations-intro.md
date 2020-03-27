---
description: この節では、IPS WebサービスAPIで処理される一般的な操作パラメータについて説明します。
seo-description: この節では、IPS WebサービスAPIで処理される一般的な操作パラメータについて説明します。
seo-title: 操作メソッド
solution: Experience Manager
title: 操作メソッド
topic: Scene7 Image Production System API
uuid: 713646a7-1108-4f93-bec2-3fbe7e548515
translation-type: tm+mt
source-git-commit: 806e7e670ee98e1fb6adf52ffc95fb989fa69400

---


# 操作メソッド{#operations-methods}

この節では、IPS WebサービスAPIで処理される一般的な操作パラメータについて説明します。

各操作パラメーターの詳細については、「操作パラメーター」を参 [照してくださ](/help/aem-ips-api/operations/c-operations-intro/c-methods/c-methods.md)い。

## ハンドル：バージョン情報 {#section-094ce1afa6244fa5b2c762f44ffdca1c}

特定のAPI操作によって返された参照IPSオブジェクトを処理します。 後続の操作呼び出しにハンドルをパラメーターとして渡すこともできます。 ハンドルは、文字列データ型( `xsd:string`)です。

ハンドルは、単一のアプリケーションセッション中のみ使用されます。 さらに、IPSリリース間で形式が変わる可能性があるので、ハンドルを永続的な形式にする必要があります。 インタラクティブアプリケーションを書き込む場合は、セッションのタイムアウトを実装し、特にIPSのアップグレード後に、セッション間のすべてのハンドルを破棄します。 非インタラクティブアプリケーションを作成する場合は、適切な操作を呼び出して、アプリケーションを実行するたびにハンドルを取得します。 以下のJava/Axis2コードの例は、正しくなく正しいコード実行を示しています。

**不正なハンドルコード**

このコードサンプルには、会社のハンドルに対してハードコードされた値(555)が含まれているので、正しくありません。

```
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle("555");// INCORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

**正しいハンドルコード**

このコードサンプルは、有効なハンドルを返すために呼び出さ `getCompanyInfo` れるので、正しいものです。 ハードコードされた値に依存しません。 必要なハンドルを返すには、このメソッドまたは他のIPS APIを使用します。

```
GetCompanyInfoParam companyInfoParam = new GetCompanyInfoParam(); 
companyInfoParam.setCompanyName("My Company"); GetCompanyInfoReturn companyInfoReturn = ipsApi.getCompanyInfo(companyInfoParam, authHeader); 
String companyHandle = companyInfoReturn.getCompanyInfo().getCompanyHandle(); 
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle(companyHandle); //CORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

## 一般的なハンドルの種類 {#section-e683ac8283284f9688e63f51a494f7a0}

**companyHandle**

ほとんどの操作では、パラメータを渡すことで会社のコンテキストを設定する必要が `companyHandle` あります。 会社のハンドルは、、、などの特定の操作によって返さ `getCompanyInfo`れるポ `addCompany`インタで `getCompanyMembership`す。

**userHandle**

このパラ `userHandle` メーターは、特定のユーザーをターゲットにする操作のオプションのパラメーターです。 デフォルトでは、これらの操作は呼び出し元のユーザー（認証用に資格情報が渡されるユーザー）をターゲットにします。 ただし、適切な権限を持つ管理者ユーザーは別のユーザーを指定できます。 例えば、操作では `setPassword` 通常、認証されたユーザーのパスワードが設定されますが、管理者は、このパラメーターを使用し `userHandle` て別のユーザーのパスワードを設定できます。

会社のコンテキストを必要とする操作（パラメーターを使用）の場 `companyHandle` 合、認証済みユーザーとターゲットユーザーの両方が、指定した会社のメンバーである必要があります。 会社のコンテキストを必要としない操作の場合、認証済みユーザーとターゲットユーザーの両方が、少なくとも1つの共通の会社のメンバーである必要があります。

次の操作で、ユーザーハンドルを取得できます。

* `getUsers`
* `getAllUsers`
* `getUserInfo`
* `getCompanyMembers`
* `getGroupMembers`
* `addUser`

**accessUserHandleとaccessGroupHandle**

デフォルトでは、アクセス権限（読み取り、書き込み、削除）を必要とする操作は、呼び出し元のユーザーの権限コンテキストで実行されます。 一部の操作では、またはパラメータを使用してこのコンテキストを変 `accessUserHandle` 更で `accessGroupHandle` きます。 このパラメ `accessUserHandle` ーターを使用すると、管理者は別のユーザーを装うことができます。 このパラ `accessGroupHandle` メータを使用すると、呼び出し元は特定のユーザーグループのコンテキストで動作できます。

**responseFieldArrayおよびexcludeFieldArray**

一部の操作では、呼び出し元が応答に含めるフィールドを制限できます。 フィールドを制限すると、リクエストの処理に必要な時間とメモリを減らし、応答データのサイズを小さくすることができます。 呼び出し元は、パラメーターを渡すか、またはパラメーターを介して除外さ `responseFieldArray` れたフィールドの列挙型リストを使用して、特定のフィールドのリストを要求で `excludeFieldArray` きます。

との両方 `responseFieldArray` で、 `excludeFieldArray` で区切られたノードパスを使用してフィールドを指定しま `/`す。 例えば、各アセットの名前、 `searchAssets` 最終変更日およびメタデータのみを返すように指定するには、次を参照します。

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

ノードパスは、返されるノードのルートを基準とした相対パスです。 複雑なタイプのフィールドにサブ要素(例えば、 `assetArray/items/imageInfo`)を含めないで指定した場合、そのサブ要素がすべて含まれます。 複雑なタイプのフィールドに1つ以上のサブ要素を指定すると( `assetArray/items/imageInfo/originalPath`など)、それらのサブ要素のみが含まれます。

リクエストにまたはを含めな `responseFieldArray` い場合 `excludeFieldArray` は、すべてのフィールドが返されます。

**ロケール**

IPS 4.0以降、IPS APIは、ロケールパラメータを渡すことによる操作のロケールコンテキストの設定をサポー `authHeader` トしています。 ロケールパラメーターが存在しない場合は、HTTPヘッダ `Accept-Language` ーが使用されます。 このヘッダも存在しない場合は、IPSサーバの既定のロケールが使用されます。

特定の操作では、明示的なロケールパラメーターも使用します。これは、操作のロケールコンテキストとは異なる場合があります。 例えば、この操作では、ジ `submitJob` ョブのログお `locale` よび電子メール通知に使用するロケールを設定するパラメーターを使用します。

ロケールパラメーターは、 `<language_code>[-<country_code>]`

言語コードがISO-639で指定された小文字の2文字のコードで、オプションの国コードがISO-3266で指定された大文字の2文字のコードである場合。 例えば、米国英語のロケール文字列はです `en-US`。
