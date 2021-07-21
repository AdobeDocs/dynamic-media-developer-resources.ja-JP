---
description: IPS WebサービスAPIで処理される一般的な操作パラメーターについて説明します。
solution: Experience Manager
title: 操作メソッド
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: 020c8e63-ad4e-4c0d-8da6-b51efb2b89a5
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 0%

---

# 操作メソッド{#operations-methods}

この節では、IPS WebサービスAPIで処理される一般的な操作パラメーターについて説明します。

各操作パラメーターの詳細については、[操作パラメーター](/help/aem-ips-api/operations/c-operations-intro/c-methods/c-methods.md)を参照してください。

## ハンドル：について {#section-094ce1afa6244fa5b2c762f44ffdca1c}

特定のAPI操作で返される参照IPSオブジェクトを処理します。 ハンドルを後続の操作呼び出しにパラメーターとして渡すこともできます。 ハンドルは、文字列データ型(`xsd:string`)です。

ハンドルは、単一のアプリケーションセッション中にのみ使用することを意図しています。 さらに、IPSリリース間で形式が変わる可能性があるので、ハンドルは持続的に設定する必要があります。 インタラクティブアプリケーションを書き込む場合、セッションタイムアウトを実装し、特にIPSのアップグレード後に、セッション間のすべてのハンドルを破棄します。 非インタラクティブアプリケーションを書き込む場合は、適切な操作を呼び出して、アプリケーションが実行されるたびにハンドルを取得します。 以下のJava/Axis2コードサンプルは、正しくないコード実行を示しています。

**不正なハンドルコード**

このコードサンプルは、会社のハンドルにハードコードされた値(555)が含まれているので、正しくありません。

```
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle("555");// INCORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

**正しいハンドルコード**

このコードサンプルは、有効なハンドルを返すために`getCompanyInfo`を呼び出すので、正しいものです。 ハードコードされた値に依存しません。 必要なハンドルを返すには、このメソッドまたはその他の同等のIPS APIを使用します。

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

ほとんどの操作では、`companyHandle`パラメーターを渡して会社のコンテキストを設定する必要があります。 会社のハンドルは、`getCompanyInfo`、`addCompany`、`getCompanyMembership`などの特定の操作から返されるポインタです。

**userHandle**

`userHandle`パラメーターは、特定のユーザーを対象とする操作のオプションパラメーターです。 デフォルトでは、これらの操作は呼び出し元のユーザー（認証用に資格情報が渡されるユーザー）をターゲットにします。 ただし、適切な権限を持つ管理者ユーザーは、別のユーザーを指定できます。 例えば、`setPassword`操作では通常、認証済みユーザーのパスワードが設定されますが、管理者は`userHandle`パラメーターを使用して、別のユーザーのパスワードを設定できます。

会社コンテキスト（ `companyHandle`パラメーターを使用）を必要とする操作の場合、認証済みユーザーとターゲットユーザーの両方が、指定した会社のメンバーである必要があります。 会社のコンテキストを必要としない操作の場合、認証済みユーザーとターゲットユーザーの両方が、少なくとも1つの共通会社のメンバーである必要があります。

次の操作で、ユーザーハンドルを取得できます。

* `getUsers`
* `getAllUsers`
* `getUserInfo`
* `getCompanyMembers`
* `getGroupMembers`
* `addUser`

**accessUserHandleおよびaccessGroupHandle**

デフォルトでは、アクセス権限（読み取り、書き込み、削除）を必要とする操作は、呼び出し元ユーザーの権限コンテキストで動作します。 特定の操作では、`accessUserHandle`または`accessGroupHandle`パラメーターを使用してこのコンテキストを変更できます。 `accessUserHandle`パラメーターを使用すると、管理者は別のユーザーとして実行できます。 `accessGroupHandle`パラメーターを使用すると、呼び出し元は特定のユーザーグループのコンテキストで操作できます。

**responseFieldArrayとexcludeFieldArray**

一部の操作では、呼び出し元が応答に含まれるフィールドを制限できます。 フィールドを制限すると、リクエストの処理に必要な時間とメモリを削減し、応答データのサイズを小さくすることができます。 呼び出し元は、`responseFieldArray`パラメーターを渡すか、`excludeFieldArray`パラメーターを使用して除外されたフィールドのリストを列挙することで、フィールドの特定のリストを要求できます。

`responseFieldArray`と`excludeFieldArray`の両方で、`/`で区切られたノードパスを使用してフィールドを指定します。 例えば、`searchAssets`が各アセットの名前、最終変更日およびメタデータのみを返すように指定するには、次を参照します。

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

ノードパスは、戻りノードのルートに対する相対パスであることに注意してください。 サブ要素を含まない複合タイプフィールド（`assetArray/items/imageInfo`など）を指定した場合、そのサブ要素がすべて含まれます。 複合型フィールドに1つ以上のサブ要素を指定した場合（例：`assetArray/items/imageInfo/originalPath`）、それらのサブ要素のみが含まれます。

リクエストに`responseFieldArray`または`excludeFieldArray`を含めない場合は、すべてのフィールドが返されます。

**ロケール**

IPS 4.0以降、IPS APIでは、`authHeader`ロケールパラメータを渡すことにより、操作のロケールコンテキストを設定できます。 ロケールパラメータが存在しない場合は、HTTPヘッダー`Accept-Language`が使用されます。 このヘッダーも存在しない場合は、IPSサーバのデフォルトロケールが使用されます。

特定の操作では、明示的なロケールパラメーターも使用しますが、操作ロケールのコンテキストとは異なる場合があります。 例えば、`submitJob`操作では、ジョブのログと電子メール通知に使用するロケールを設定する`locale`パラメーターを取ります。

ロケールパラメーターは、`<language_code>[-<country_code>]`の形式を使用します。

言語コードが小文字の場合、ISO-639で指定された2文字のコード、オプションの国コードが大文字の場合、ISO-3266で指定された2文字のコードです。 例えば、米国英語のロケール文字列は`en-US`です。
