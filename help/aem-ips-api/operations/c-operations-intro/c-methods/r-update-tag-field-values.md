---
description: タグフィールドのタグディクショナリ値を更新します。
seo-description: タグフィールドのタグディクショナリ値を更新します。
seo-title: updateTagFieldValues
solution: Experience Manager
title: updateTagFieldValues
topic: Dynamic Media Image Production System API
uuid: 21689469-a0dd-480b-82ba-ebd12956ff8f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 12%

---


# updateTagFieldValues{#updatetagfieldvalues}

タグフィールドのタグディクショナリ値を更新します。

構文

## 認証済みユーザータイプ{#section-0372b742b1344979b0668faacb36fcc6}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-0a3a4bab026746238c9d4009caf42e94}

**Input (updateTagFieldValuesParam)**

<table id="table_15F354FBC043464080BC975AE35E03A4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名前 </th> 
   <th colname="col2" class="entry"> 種類 </th> 
   <th colname="col3" class="entry"> 必須 </th> 
   <th colname="col4" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 会社ハンドル </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> タグフィールドハンドル。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> updateArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型：TagValueUpdateArray</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4">更新するタグフィールド値の配列。 <p>注意： タグ文字列の値のみを更新します。 アセットの関連付けに影響しません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**出力(updateTagFieldValuesReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | はい | 正常に更新されたタグフィールドの数。 |
| `*`warningCount`*` | `xsd:int` | はい | 操作がタグフィールドの更新を試みたときに生成された警告の数です。 |
| `*`errorCount`*` | `xsd:int` | はい | 操作がタグフィールドの更新を試行したときに生成されたエラーの数です。 |
| `*`warningDetailArray`*` | `types:TagValueUpdateFaultArray` | いいえ | 操作がタグフィールドの更新を試みた際に警告を生成したアセットに関連付けられた詳細の配列です。 |
| `*`errorDetailArray`*` | `types:TagValueUpdateFaultArray` | いいえ | 操作がタグフィールドの更新を試みた際にエラーが発生したアセットに関連付けられた詳細の配列です。 |

## 例 {#section-bb4dcf97044c4675974c9b8d27674001}

**リクエスト**

```java
<updateTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <updateArray>
      <items>
         <oldValue>Nurth</oldValue>
         <newValue>North</newValue>
      </items>
      <items>
         <oldValue>Suth</oldValue>
         <newValue>South</newValue>
      </items>
      <items>
         <oldValue>East</oldValue>
         <newValue>West</newValue>
      </items>
      <items>
         <oldValue>Banana</oldValue>
         <newValue>Pear</newValue>
      </items>
   </updateArray>
</updateTagFieldValuesParam>
```

**応答**

```java
<updateTagFieldValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>2</errorCount>
   <errorDetailArray>
      <items>
         <value>East</value>
         <code>30001</code>
         <reason>New tag value 'West' already exists.</reason>
      </items>
      <items>
         <value>Banana</value>
         <code>30001</code>
         <reason>Tag value 'Banana' not found.</reason>
      </items>
   </errorDetailArray>
</updateTagFieldValuesReturn>
```

