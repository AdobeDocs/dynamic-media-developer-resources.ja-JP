---
description: 指定した条件に基づいてアセットを検索します。
seo-description: 指定した条件に基づいてアセットを検索します。
seo-title: searchAssets
solution: Experience Manager
title: searchAssets
topic: Scene7 Image Production System API
uuid: 125e9e0d-1856-4e80-9778-ca93cd04b766
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# searchAssets{#searchassets}

指定した条件に基づいてアセットを検索します。

構文

## searchAssets:バージョン情報 {#section-4ad74f12eb754768bf85bd235a7e25f0}

`searchAssets` は、IPSアセットを取得する主な方法です。 この方法は、フォルダ階層の参照や特定のアセットの名前による検索など、様々な目的で使用されます。

**応答サイズ**

`searchAssets` 1回の呼び出しで最大1,000個のアセットを返します。 1回の呼び出しで最大10,000個のアセットを返すには、応答データを、、、、およびフィールドのサブセ `totalRows`ットに `name`制 `handle`限し `type`てくだ `subType` さい。 より大きなセットを返すには、パラメータを使用してページングを設定 `resultPage` します。

**responseFieldArrayまたはexcludeFieldArrayで結果ファイルのサイズを制限**

またはを使用して、データセットのサイズを `responseFieldArray` 制限 `excludFieldArray` します。 これらのパラメーターは、メモリ使用量と帯域幅を減らし、サーバーの応答時間を改善するのに役立ちます。

## 認証されたユーザータイプ {#section-9c4bc41bb8b4493982197eb13c7cdc55}

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 検索するアセットを含む会社のハンドル。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessUserHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 管理者は別のユーザーとして作業できます。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessGroupHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 管理者は、別のグループの一部として作業できます。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> フォ <span class="varname"> ルダ</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> アセットを検索するためのルートパスです。 省略した場合は、会社のルートフォルダが使用されます。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeSubfolders</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4">サブフォルダを検索す <span class="codeph"> る場合は</span> 、trueに設定します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishState</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 公開状態の選択。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> ごみ <span class="varname"> 箱状</span> 態 </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4">ごみ箱の状態の選択。 初期設定は <span class="codeph"> NotInTrashです</span>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> conditionMatchMode <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>キーワード配列の結果を組み合わせるための検索一致モード <span class="codeph"> の選択</span>、 </p> <p> <span class="codeph"> conditionMatchMode</span> </p> <p> <span class="codeph"> systemFieldConditionArray</span>、metadataConditionArray <span class="codeph"> です</span>。 初期設定は <span class="codeph"> MatchAllです</span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> keywordArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 型：StringArray</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p> <p>注意： 非推奨のパラメーター。 使用しないことをお勧めします。 </p> </p> <p>一致するキーワードの文字列配列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> systemFieldMatchMode <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>systemFieldConditionの一致を組み合わせるための検索一致モ <span class="codeph"> ードの</span> 選択。 初期設定は <span class="codeph"> MatchAll</span> </p>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> systemFieldConditionArray <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> タイプ：SystemFieldConditionArray</span> </p> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> システムフィールド条件の配列です。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> tagMatchMode <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4">検索一致モードの文字列定数。 デフォルト値は <span class="codeph"> MatchAllです</span>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tagConditionArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：TagConditionArray</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>タグフィールド検索述部の配列。 </p> <p>述部は、tagMatchMode <span class="codeph"> 設定に従って結合され、次にキーワード</span> Array <span class="codeph"> 、</span>system FieldConditionArray <span class="codeph"></span><span class="codeph"></span><span class="codeph"></span> 、metadataFieldConditionArray、metadataArrayConditionConditionConditionConditionToTheArrayConditionModeMatchModeMatchSetting設定に従って結合されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> metadataMatchMode <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4">Search Match Modes for combining <span class="codeph"> metadataCondition</span> matches. 初期設定は <span class="codeph"> MatchAllです</span>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> metadataConditionArray <span class="varname"></span></span> </td> 
   <td colname="col2"> <p> <span class="codeph"> タイプ：MetadataConditionArray</span> </p> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> メタデータフィールドの検索条件の配列です。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetTypeArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 型：StringArray</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 検索に含めるアセットタイプの配列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> excludeAssetTypeArray <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 型：StringArray</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 検索から除外するアセットタイプの配列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSubTypeArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 型：StringArray</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> フィルターの対象となるサブタイプ名のリストです。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> strictSubTypeCheck <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4">trueおよび <span class="codeph"> assetSubTypeArrayが空で</span> ない場合 <span class="codeph"> 、サブタイプがassetSubTypeArrayに含まれるアセットのみが</span> 返されます <span class="codeph"></span> 。 false(デフォ <span class="codeph"> ルト</span> )の場合、サブタイプが定義されていないアセットが返されます。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> excludeByproducts <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> trueの場合、リッピングされたPDFページの画像など、マスターアセットの取り込み中に生成された副産物アセットは、検索結果から除外されます。 初期設定は false。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> excludByproductArray <span class="varname"></span></span> </td> 
   <td colname="col2"> <p> <span class="codeph"> タイプ：ExcludeByproductArray</span> </p> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 検索結果から除外する副産物アセット生成条件の配列。 このパラメーターが存在する場合、excludeByproducts設定よりも優先されます。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sting</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 検索するアセットを含むプロジェクトのハンドル。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> recordsPerPage <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 返す結果の最大数。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> resultsPage</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4">recordsPerPageページサイズに基づいて、返す結果のページを <span class="codeph"> 指定</span> します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 並べ <span class="varname"> 替え</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> アセットの並べ替えフィールドの選択。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 並べ替 <span class="varname"> え方向</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 並べ替え方向の選択。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> responseFieldArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 型：StringArray</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 応答に含めるフィールドとサブフィールドのリストが含まれます。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> excludeFieldArray <span class="varname"></span></span> </td> 
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

このコードサンプルを使用すると、特定の会社に属する画像アセットを検索できます。 応答は簡潔にするために切り捨てられます。

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

