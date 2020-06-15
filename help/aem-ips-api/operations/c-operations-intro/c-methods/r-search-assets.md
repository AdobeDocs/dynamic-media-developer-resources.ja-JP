---
description: 指定した条件に基づいてアセットを検索します。
seo-description: 指定した条件に基づいてアセットを検索します。
seo-title: searchAssets
solution: Experience Manager
title: searchAssets
topic: Scene7 Image Production System API
uuid: 125e9e0d-1856-4e80-9778-ca93cd04b766
translation-type: tm+mt
source-git-commit: 55015831ed1971a305ddbd8085c95626507355e0
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 7%

---


# searchAssets{#searchassets}

指定した条件に基づいてアセットを検索します。

構文

## searchAssets: バージョン情報 {#section-4ad74f12eb754768bf85bd235a7e25f0}

`searchAssets` は、IPSアセットを取得する主な方法です。 このメソッドは、フォルダー階層の参照や、特定のアセットの名前による検索など、様々な目的に使用します。

**応答サイズ**

`searchAssets` 1回の呼び出しで最大1000個のアセットを返します。 1回の呼び出しで最大10,000個のアセットを返すには、応答データを、、、、、、および `totalRows`各フィールドのサブセットに制限し `name``handle``type``subType` ます。 より大きいセットを返すには、 `resultPage` パラメーターを使用してページングを設定します。

**responseFieldArrayまたはexcludeFieldArrayによる結果ファイルサイズの制限**

またはの `responseFieldArray``excludFieldArray` パラメーターを使用して、データセットのサイズを制限します。 これらのパラメーターは、メモリの使用量と帯域幅を削減し、サーバーの応答時間を改善するのに役立ちます。

## 認証済みユーザータイプ {#section-9c4bc41bb8b4493982197eb13c7cdc55}

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
>アセットを返すには、読み取りアクセス権が必要です。

## パラメータ {#section-49aabc0600764f55a8b7017d86ded44f}

**入力(searchAssetsParam)**

<table id="table_2972D1BB9CED4F7F9207747AE8CBAE8D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名前 </th> 
   <th colname="col2" class="entry"> 種類 </th> 
   <th colname="col3" class="entry"> 必須? </th> 
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
   <td colname="col4"> 管理者は、別のグループの一部として作業できます。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folder</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> アセットを検索するためのルートパスです。 省略した場合は、会社のルートフォルダが使用されます。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeSubfolders</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4">サブフォルダを検索する場合は <span class="codeph"> true</span> に設定します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 発行状態の選択。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> trashState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4">ごみ箱状態の選択 初期設定は <span class="codeph"> NotInTrash</span>です。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> conditionMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>keywordArrayの結果を組み合わせるための検索一致モードの選択 <span class="codeph"></span>、 </p> <p> <span class="codeph"> conditionMatchMode</span> </p> <p> <span class="codeph"> systemFieldConditionArray</span>、 <span class="codeph"> metadataConditionArray</span>。 初期設定は <span class="codeph"> MatchAll</span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> keywordArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型：StringArray</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p> <p>注意：  非推奨パラメーター。 使用しないことをお勧めします。 </p> </p> <p>一致するキーワードの文字列配列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> systemFieldMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>systemFieldConditionが一致する場合の組み合わせに使用する検索一致モードの選択 <span class="codeph"> 。</span> 初期設定は <span class="codeph"> MatchAllです</span> </p>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> systemFieldConditionArray</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 型：SystemFieldConditionArray</span> </p> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> システムフィールド条件の配列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tagMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4">検索一致モードの文字列定数。 デフォルト値は <span class="codeph"> MatchAll</span>です。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tagConditionArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型：TagConditionArray</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>タグフィールド検索述語の配列。 </p> <p>述部は、 <span class="codeph"> tagMatchMode</span> 設定に従って結合され、次に <span class="codeph"> キーワード配列内の任意の語句と結合されます。</span>システムフィールド条件配列 <span class="codeph"> 、メタデータ条件配列、メタデータ</span>配列 <span class="codeph"> の</span><span class="codeph"></span> 配列一致モードの設定 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> metadataMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4">metadataConditionが一致する場合を組み合わせるための検索一致 <span class="codeph"> モード</span> 。 初期設定は <span class="codeph"> MatchAll</span>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> metadataConditionArray</span> </span> </td> 
   <td colname="col2"> <p> <span class="codeph"> 型：MetadataConditionArray</span> </p> </td> 
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
   <td colname="col4"> フィルタするサブタイプ名のリスト。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> strictSubTypeCheck</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4">true <span class="codeph"> でassetSubTypeArray</span> が空でない場合 <span class="codeph"> 、setSubTypeArray</span><span class="codeph"></span> にサブタイプが含まれているアセットのみが返されます。 false <span class="codeph"> (デフォルト</span> )の場合、サブタイプが定義されていないアセットが返されます。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeByproducts</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> trueの場合、リッピングされたPDFページの画像など、プライマリアセットの取り込み中に生成された副産物アセットは、検索結果から除外されます。 初期設定は false。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeByproductArray</span> </span> </td> 
   <td colname="col2"> <p> <span class="codeph"> タイプ：ExcludeByproductArray</span> </p> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 検索結果から除外する副産物アセット生成条件の配列。 このパラメーターが存在する場合、excludeByproducts設定よりも優先されます。 </td> 
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
   <td colname="col4"> 返す結果の最大数。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> resultsPage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4">recordsPerPage <span class="codeph"></span> ページサイズに基づいて、返す結果のページを指定します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sortBy</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> アセットの並べ替えフィールドの選択 </td> 
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

**出力(searchAssetsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`totalRows`*` | `xsd:int` | いいえ | ページあたりのレコード数に制限がない場合に検索で返される行数。 |
| ` *`assetArray`*` | `types:AssetArray` | いいえ | 検索で返されるアセット。 |

## 例 {#section-725484cc09b54772a838ad2cc930b94b}

このコードのサンプルを使用すると、特定の会社に属する画像アセットを検索できます。 応答が短くなるため切り捨てられます。

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

