---
description: 指定した条件に基づいてアセットを検索します。
solution: Experience Manager
title: searchAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 58bd80e4-e9eb-43e4-8508-04e330f0ad26
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '630'
ht-degree: 6%

---

# searchAssets{#searchassets}

指定した条件に基づいてアセットを検索します。

構文

## searchAssets：詳細 {#section-4ad74f12eb754768bf85bd235a7e25f0}

`searchAssets` は、IPS アセットを取得する主な方法です。 このメソッドは、フォルダー階層の参照や名前による特定のアセットの検索など、様々な目的で使用されます。

**応答サイズ**

`searchAssets` は、1 回の呼び出しで最大 1,000 個のアセットを返します。 1 回の呼び出しで最大 10,000 個のアセットを返すには、応答データを `totalRows`、`name`、`handle`、`type` および `subType` フィールドのサブセットに制限します。 より大きなセットを返すには、`resultPage` パラメーターを使用してページングを設定します。

**responseFieldArray または excludeFieldArray を使用して結果ファイルのサイズを制限**

`responseFieldArray` または `excludFieldArray` のパラメーターを使用して、データセットのサイズを制限します。 これらのパラメーターは、メモリの使用と帯域幅を減らすのに役立ち、サーバーの応答時間を改善できます。

## 許可されているユーザータイプ {#section-9c4bc41bb8b4493982197eb13c7cdc55}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>アセットを返すには、ユーザーに読み取りアクセス権が必要です。

## パラメーター {#section-49aabc0600764f55a8b7017d86ded44f}

**入力（searchAssetsParam）**

<table id="table_2972D1BB9CED4F7F9207747AE8CBAE8D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名前 </th> 
   <th colname="col2" class="entry"> 種類 </th> 
   <th colname="col3" class="entry"> 必須？ </th> 
   <th colname="col4" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 検索するアセットを含む会社へのハンドル。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessUserHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 管理者は別のユーザーとして作業できます。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessGroupHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 管理者を別のグループの一部として使用できます。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> フォルダー </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> アセットを検索するためのルートパス。 省略すると、会社のルートフォルダーが使用されます。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeSubfolders</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4">true に設定 <span class="codeph"> ると </span> サブフォルダーを検索できます。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> Publish州の選択。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> trashState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4">ごみ箱の状態の選択。 デフォルトは <span class="codeph"> NotInTrash</span> です。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> conditionMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p><span class="codeph"> keywordArray</span>, </p> <p> <span class="codeph">conditionMatchMode</span> </p> <p> systemFieldConditionArray</span> および <span class="codeph"> metadataConditionArray</span> を <span class="codeph"> します。 デフォルトは <span class="codeph"> MatchAll</span> です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> keywordArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型：StringArray</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p> <p>メモ：非推奨のパラメーターです。 使用しないことをお勧めします。 </p> </p> <p>一致するキーワードの文字列配列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> systemFieldMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>systemFieldCondition</span> の一致を組み合わせるための検索一致モード <span class="codeph"> 選択します。 デフォルトは <span class="codeph"> MatchAll</span> </p>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> systemFieldConditionArray</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> の種類：SystemFieldConditionArray</span> </p> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> システムフィールド条件の配列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tagMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4">検索一致モードの文字列定数。 デフォルトは <span class="codeph"> MatchAll</span> です。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tagConditionArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> のタイプ：TagConditionArray</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>タグフィールド検索用述語の配列。 </p> <p>述語は、<span class="codeph"> tagMatchMode</span><span class="codeph"> の設定に従って結合され、次に keywordArray</span>、<span class="codeph"> systemFieldConditionArray</span>、および <span class="codeph"> metadataConditionArray</span> の任意の語句と <span class="codeph"> conditionMatchMode</span> の設定に従って結合されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> metadataMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4">Search Match metadataCondition</span> の一致を組み合わせ <span class="codeph"> ためのモード。 デフォルトは <span class="codeph"> MatchAll</span> です。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> metadataConditionArray</span> </span> </td> 
   <td colname="col2"> <p> <span class="codeph"> タイプ：MetadataConditionArray</span> </p> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> メタデータフィールド検索条件の配列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型：StringArray</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 検索に含めるアセットタイプの配列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeAssetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型：StringArray</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 検索から除外するアセットタイプの配列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSubTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型：StringArray</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> フィルタリング対象のサブタイプ名のリスト。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> strictSubTypeCheck</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4">true</span><span class="codeph">assetSubTypeArray</span> が空でない場合 <span class="codeph">、サブタイプが assetSubTypeArray</span> に含まれるアセットのみ <span class="codeph"> 返されます。 false<span class="codeph"> 場合 </span> （デフォルト）、サブタイプが定義されていないアセットが返されます。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeByproducts</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> true の場合、PDFページの画像を取り込むなど、プライマリアセットの取り込み中に生成された副産物アセットは、検索結果から除外されます。 初期設定は false。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludByproductArray</span> </span> </td> 
   <td colname="col2"> <p> <span class="codeph"> の種類：ExcludeByproductArray</span> </p> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 検索結果から除外する副産物アセット生成条件の配列。 存在する場合、このパラメーターは excludeByproducts 設定を上書きします。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sting</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 検索するアセットを含むプロジェクトのハンドル。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> recordsPerPage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 返される結果の最大数。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> resultsPage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4">recordsPerPage</span> ページのサイズに基づいて、返す結果 <span class="codeph"> ページを指定します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sortBy</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> アセット並べ替えフィールドの選択。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sortDirection</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 並べ替え方向の選択。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> responseFieldArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型：StringArray</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 応答に含めるフィールドとサブフィールドのリストが含まれます。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeFieldArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型：StringArray</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 応答から除外するフィールドとサブフィールドのリストが含まれます。 </td> 
  </tr> 
 </tbody> 
</table>

**出力（searchAssetsReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| totalRows | `xsd:int` | いいえ | ページあたりのレコード数に制限がない場合に検索で返される行数。 |
| assetArray | `types:AssetArray` | いいえ | 検索によって返されるAssets。 |

## 例 {#section-725484cc09b54772a838ad2cc930b94b}

このコード例では、特定の会社に属する画像アセットを検索します。 簡潔にするために、応答は切り捨てられます。

**リクエスト**

```java
<ns1:searchAssetsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:includeSubfolders>true</ns1:includeSubfolders>
   <ns1:assetTypeArray>
      <ns1:items>Image</ns1:items>
   </ns1:assetTypeArray>
</ns1:searchAssetsParam>
```

**応答**

```java
<searchAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <totalRows>210</totalRows>
   <assetArray>
      <items>
         <assetHandle>24265|1|17061</assetHandle>
         <type>Image</type>
         <name>Autumn Leaves</name>
         ...
      </items>
    </assetArray>
</searchAssetsReturn>
```
