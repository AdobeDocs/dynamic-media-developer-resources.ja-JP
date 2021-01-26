---
description: 管理者は、コンテンツ管理システムとの調整やテンプレート操作のための新しいメタデータフィールドを作成できます。 作成されるメタデータフィールドの例としては、キーワード、画像の作成者に関する情報、著作権保持者の情報などがあります。
seo-description: 管理者は、コンテンツ管理システムとの調整やテンプレート操作のための新しいメタデータフィールドを作成できます。 作成されるメタデータフィールドの例としては、キーワード、画像の作成者に関する情報、著作権保持者の情報などがあります。
seo-title: createMetadataField
solution: Experience Manager
title: createMetadataField
topic: Dynamic Media Image Production System API
uuid: 50ab61fa-df44-4305-ad9f-693c4aea1e69
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 7%

---


# createMetadataField{#createmetadatafield}

管理者は、コンテンツ管理システムとの調整やテンプレート操作のための新しいメタデータフィールドを作成できます。 作成されるメタデータフィールドの例としては、キーワード、画像の作成者に関する情報、著作権保持者の情報などがあります。

構文

## 認証済みユーザータイプ{#section-2f61d79f8cac4692bfa53b95035ddd89}

* `IpsAdmin`

## パラメータ {#section-f8260bc8dd0a4570bc7f714f81ab975f}

**入力(createMetadataFieldParam)**

<table id="table_E5B249BBED3B4D2F9CEE2CCF27472D1B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> パラメーター名 </th> 
   <th colname="col2" class="entry"> 種類 </th> 
   <th colname="col3" class="entry"> 必須 </th> 
   <th colname="col4" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> メタデータフィールドが属する会社の名前。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> アセットタイプ. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 作成するメタデータフィールドの名前。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4">メタデータフィールドの種類。 <p>メタデータフィールド型の定数は、使用可能な型を定義します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> defaultValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>作成するメタデータフィールドの初期設定値（例：<span class="codeph"> Scene 7</span>）。 </p> <p>タグフィールドの種類ではデフォルト値がサポートされていないので、省略する必要があります。 タグフィールドタイプに空でないデフォルト値が指定されている場合、エラーが返されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> isHidden</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> IPSシステム固有のメタデータを非表示または公開します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> isEnforced</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>値が設定されたときにメタデータフィールドが適用（検証）されるかどうかを示すbooleanフラグです。 </p> <p>trueに設定した場合、<span class="codeph"> setAssetMetadata</span> /<span class="codeph"> batchSetAssetMetadata</span>に不正な値が設定されていると、フォルトがスローされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> initialTagValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 選択したタグが参照できる共有列挙値のセットを作成できます。 </td> 
  </tr> 
 </tbody> 
</table>

**出力(createMetadataFieldReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`fieldHandle`*` | `xsd:string` | はい | 新しいメタデータフィールドへのハンドル。 |

## 例 {#section-ba66be30f36b4aeba1bc721b0b92fdfc}

次のコードのサンプルを使用すると、`createMetadataField`という名前の文字列型メタデータフィールドを作成できます。 応答は、新しいメタデータフィールドにハンドルを返します。

**リクエスト**

```java
<createMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <assetType>Image</assetType>
   <name>createMetadataField</name>
   <fieldType>String</fieldType>
   <initialTagValue>Fall</initialTagValue>
   <defaultValue>Default</defaultValue>
</createMetadataFieldParam>
```

**応答**

```java
<createMetadataFieldReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <fieldHandle>m|21|IMAGE|createMetadataField</fieldHandle>
</createMetadataFieldReturn>
```

