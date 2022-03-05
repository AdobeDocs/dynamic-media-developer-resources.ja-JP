---
description: IPS Web サービス API で処理される一般的な操作パラメーターについて説明します。
solution: Experience Manager
title: 操作メソッド
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 020c8e63-ad4e-4c0d-8da6-b51efb2b89a5
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 0%

---

# 操作メソッド{#operations-methods}

この節では、IPS Web サービス API で処理される一般的な操作パラメーターについて説明します。

各操作パラメータの詳細については、 [操作のパラメーター](/help/aem-ips-api/operations/c-operations-intro/c-methods/c-methods.md).

## ハンドル：について {#section-094ce1afa6244fa5b2c762f44ffdca1c}

特定の API 操作で返された参照 IPS オブジェクトを処理します。 ハンドルを後続の操作呼び出しにパラメーターとして渡すこともできます。 ハンドルは文字列データ型 ( `xsd:string`) をクリックします。

ハンドルは、単一のアプリケーションセッション中にのみ使用されます。 さらに、IPS リリース間で形式が変わる可能性があるので、処理を永続的にする必要があります。 インタラクティブアプリケーションを書き込む場合、セッションタイムアウトを実装し、特に IPS のアップグレード後に、セッション間のすべてのハンドルを破棄します。 非インタラクティブアプリケーションを作成する場合は、適切な操作を呼び出して、アプリケーションが実行されるたびにハンドルを取得します。 以下の Java/Axis2 コードのサンプルでは、コードの実行が正しく正しくなく正しく行われています。

**不正なハンドルコード**

このコードサンプルは、会社のハンドルにハードコードされた値 (555) が含まれているので、正しくありません。

```
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle("555");// INCORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

**正しいハンドルコード**

このコードサンプルは、 `getCompanyInfo` 有効なハンドルを返します。 ハードコードされた値に依存しません。 必要なハンドルを返すには、このメソッドまたは他の同等の IPS API を使用します。

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

ほとんどの操作では、 `companyHandle` パラメーター。 会社のハンドルは、 `getCompanyInfo`, `addCompany`、および `getCompanyMembership`.

**userHandle**

この `userHandle` parameter は、特定のユーザーを対象とする操作のオプションのパラメータです。 デフォルトでは、これらの操作は呼び出し元のユーザー（認証用に資格情報が渡されたユーザー）をターゲットにします。 ただし、適切な権限を持つ管理者ユーザーは、別のユーザーを指定できます。 例えば、 `setPassword` operation は通常、認証済みユーザーのパスワードを設定しますが、管理者は `userHandle` パラメーターを使用して、別のユーザーのパスワードを設定します。

会社のコンテキストを必要とする操作の場合 ( `companyHandle` パラメーター ) の場合、認証済みユーザーとターゲットユーザーの両方が、指定した会社のメンバーである必要があります。 会社のコンテキストを必要としない操作の場合、認証済みユーザーとターゲットユーザーの両方が、少なくとも 1 つの共通の会社のメンバーである必要があります。

次の操作でユーザーハンドルを取得できます。

* `getUsers`
* `getAllUsers`
* `getUserInfo`
* `getCompanyMembers`
* `getGroupMembers`
* `addUser`

**accessUserHandle および accessGroupHandle**

デフォルトでは、アクセス権限（読み取り、書き込み、削除）を必要とする操作は、呼び出し元ユーザーの権限コンテキストで動作します。 特定の操作を行うと、 `accessUserHandle` または `accessGroupHandle` パラメーター。 この `accessUserHandle` パラメーターを使用すると、管理者は別のユーザーを装うことができます。 この `accessGroupHandle` パラメータを使用すると、呼び出し元は特定のユーザーグループのコンテキストで操作できます。

**responseFieldArray と excludeFieldArray**

一部の操作では、呼び出し元が応答に含まれるフィールドを制限できます。 フィールドを制限すると、リクエストの処理に必要な時間とメモリを削減し、応答データのサイズを小さくすることができます。 呼び出し元は、 `responseFieldArray` パラメーターを使用するか、列挙型の除外されたフィールドのリストを使用して `excludeFieldArray` パラメーター。

両方 `responseFieldArray` および `excludeFieldArray` 次で区切ったノードパスを使用してフィールドを指定 `/`. 例えば、次のように指定します。 `searchAssets` は、各アセットの名前、最終変更日およびメタデータのみを返します。次を参照してください。

```
<responseFieldArray> 
   <items>assetArray/items/name</items> 
   <items>assetArray/items/lastModified</items> 
   <items>assetArray/items/metadataArray</items> 
</responseFieldArray>
```

同様に、（権限を除く）すべてのフィールドを返すには、次のようにします。

```
<excludeFieldArray> 
   <items>assetArray/items/permissions</items> 
</excludeFieldArray>
```

ノードのパスは、戻りノードのルートを基準とした相対パスになります。 サブ要素のない複合型フィールドを指定する場合 ( 例： `assetArray/items/imageInfo`) の場合、そのすべてのサブ要素が含まれます。 複雑なタイプのフィールドに 1 つ以上のサブ要素を指定する場合 ( 例： `assetArray/items/imageInfo/originalPath`) の場合、そのサブ要素のみが含まれます。

次を含めない場合： `responseFieldArray` または `excludeFieldArray` リクエストでは、すべてのフィールドが返されます。

**ロケール**

IPS 4.0 以降、IPS API では、 `authHeader` ロケールパラメーター。 ロケールパラメータが存在しない場合、HTTP ヘッダー `Accept-Language` が使用されます。 このヘッダーも存在しない場合は、IPS サーバのデフォルトのロケールが使用されます。

また、特定の操作では、明示的なロケールパラメータを使用します。このパラメータは、操作ロケールコンテキストとは異なる場合があります。 例えば、 `submitJob` 手術を受ける `locale` ジョブのログと電子メール通知に使用するロケールを設定するパラメーター。

ロケールパラメーターは形式を使用します `<language_code>[-<country_code>]`

ここで、言語コードは ISO-639 で指定された小文字の 2 文字のコードで、オプションの国コードは ISO-3266 で指定された大文字の 2 文字のコードです。 例えば、米国英語のロケール文字列は次のようになります。 `en-US`.
