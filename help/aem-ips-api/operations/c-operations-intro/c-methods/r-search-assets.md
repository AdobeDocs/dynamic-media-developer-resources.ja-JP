---
description: 指定した条件に基づいてアセットを検索します。
solution: Experience Manager
title: searchAssets
feature: Dynamic Media Classic,SDK/API，アセット管理
role: Developer,Admin
exl-id: 58bd80e4-e9eb-43e4-8508-04e330f0ad26
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 7%

---

# searchAssets{#searchassets}

指定した条件に基づいてアセットを検索します。

構文

## searchAssets:について {#section-4ad74f12eb754768bf85bd235a7e25f0}

`searchAssets` は、IPSアセットを取得する主な方法です。この方法は、フォルダー階層を参照したり、特定のアセットを名前で検索したりする目的など、様々な目的で使用されます。

**応答サイズ**

`searchAssets` は、1回の呼び出しで最大1,000個のアセットを返します。1回の呼び出しにつき最大10,000個のアセットを返すには、応答データを`totalRows`、`name`、`handle`、`type`、`subType`の各フィールドのサブセットに制限します。 より大きなセットを返すには、`resultPage`パラメーターでページングを設定します。

**responseFieldArrayまたはexcludeFieldArrayを使用した結果ファイルのサイズの制限**

`responseFieldArray`または`excludFieldArray`パラメーターを使用してデータセットのサイズを制限します。 これらのパラメーターは、メモリの使用と帯域幅の削減に役立ち、サーバーの応答時間を向上させます。

## 許可されたユーザーの種類 {#section-9c4bc41bb8b4493982197eb13c7cdc55}

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
   <td colname="col4"> 検索するアセットを持つ会社へのハンドル。 </td> 
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
   <td colname="col4"> 管理者は別のグループの一部として作業できます。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> フォルダー</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> アセットを検索するためのルートパス。 省略した場合は、会社のルートフォルダーが使用されます。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeSubfolders</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4">サブフォルダーを検索するには、 <span class="codeph"> true</span>に設定します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 公開状態の選択。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> trashState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4">ごみ箱状態の選択。 初期設定は<span class="codeph"> NotInTrash</span>です。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> conditionMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p><span class="codeph"> keywordArray</span>の結果を組み合わせるための検索一致モードの選択 </p> <p> <span class="codeph"> conditionMatchMode</span> </p> <p> <span class="codeph"> systemFieldConditionArray</span>と <span class="codeph"> metadataConditionArray</span>。初期設定は<span class="codeph"> MatchAll</span>です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> keywordArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p> <p>注意： 非推奨のパラメーター。 あなたはそれを使わないことをお勧めします。 </p> </p> <p>一致するキーワードの文字列配列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> systemFieldMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p><span class="codeph"> systemFieldCondition</span>の一致を組み合わせるための検索一致モードの選択。 デフォルトは<span class="codeph"> MatchAll</span>です。 </p>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> systemFieldConditionArray</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> types:SystemFieldConditionArray</span> </p> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> システムフィールド条件の配列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tagMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4">検索一致モード文字列定数。 デフォルトは<span class="codeph"> MatchAll</span>です。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tagConditionArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型：TagConditionArray[がた：TagConditionArray]</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>タグフィールド検索用述語の配列。 </p> <p>述語は、 <span class="codeph"> tagMatchMode</span>の設定に従って結合され、 <span class="codeph">の条件に従って<span class="codeph"> keywordArray</span> 、 <span class="codeph"> systemFieldConditionArray</span> 、 <span class="codeph"> metadataConditionArray</span>内の任意の用語と結合されます。モード</span>設定。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> metadataMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"><span class="codeph"> metadataCondition</span>の一致を組み合わせるための一致モードを検索します。 初期設定は<span class="codeph"> MatchAll</span>です。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> metadataConditionArray</span> </span> </td> 
   <td colname="col2"> <p> <span class="codeph"> 型：MetadataConditionArray[たいぷ：MetadataConditionArray]</span> </p> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> メタデータフィールドの検索条件の配列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 検索に含めるアセットタイプの配列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeAssetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 検索から除外するアセットタイプの配列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSubTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> フィルタリングの対象となるサブタイプ名のリスト。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> strictSubTypeCheck</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"><span class="codeph"> true</span>および<span class="codeph"> assetSubTypeArray</span>が空でない場合は、サブタイプが<span class="codeph"> assetSubTypeArray</span>に含まれるアセットのみが返されます。 <span class="codeph"> false</span> （デフォルト）の場合、サブタイプが定義されていないアセットが返されます。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeByproducts</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> trueの場合、PDFページの切り抜き画像など、プライマリアセットの取り込み中に生成された副産物アセットは、検索結果から除外されます。 初期設定は false。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludByproductArray</span> </span> </td> 
   <td colname="col2"> <p> <span class="codeph"> types:ExcludeByproductArray</span> </p> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 検索結果から除外する副産物アセット生成条件の配列。 存在する場合、このパラメーターはexcludeByproducts設定を上書きします。 </td> 
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
   <td colname="col4"><span class="codeph"> recordsPerPage</span>ページサイズに基づいて、返す結果のページを指定します。 </td> 
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
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 応答に含めるフィールドとサブフィールドのリストが含まれます。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeFieldArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 応答から除外するフィールドとサブフィールドのリストが含まれます。 </td> 
  </tr> 
 </tbody> 
</table>

**出力(searchAssetsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`totalRows`*` | `xsd:int` | いいえ | ページあたりのレコード数に制限がない場合に検索で返される行数。 |
| `*`assetArray`*` | `types:AssetArray` | いいえ | 検索で返されるアセット。 |

## 例 {#section-725484cc09b54772a838ad2cc930b94b}

このコードサンプルでは、特定の会社に属する画像アセットを検索します。 簡潔にするために応答は切り捨てられます。

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
