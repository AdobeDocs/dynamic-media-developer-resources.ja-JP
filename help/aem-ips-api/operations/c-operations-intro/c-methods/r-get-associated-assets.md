---
description: 指定したアセットに関連付けられたアセットと、その関係の詳細を取得します。
seo-description: 指定したアセットに関連付けられたアセットと、その関係の詳細を取得します。
seo-title: getAssociatedAssets
solution: Experience Manager
title: getAssociatedAssets
topic: Scene7 Image Production System API
uuid: 70c2f8aa-9104-42b0-b85b-14f90f1ead52
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getAssociatedAssets{#getassociatedassets}

指定したアセットに関連付けられたアセットと、その関係の詳細を取得します。

構文

## 認証されたユーザータイプ {#section-453cc706400345778713cda249bfac16}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-d11d0dab59e94e89b466123a0ebfa82e}

**入力(getAssociatedAssetsParam)**

<table id="table_DBB97A6507EB48479FFFD2184FF8F07C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>名前 </p> </th> 
   <th colname="col2" class="entry"> <p>種類 </p> </th> 
   <th colname="col3" class="entry"> <p>必須 </p> </th> 
   <th colname="col4" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyHandle</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>はい </p> </td> 
   <td colname="col4"> <p>アセットを所有する会社に対するハンドル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> assetHandle</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>はい </p> </td> 
   <td colname="col4"> <p>アセットハンドル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> responseFieldArray</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型：StringArray</span> </p> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>必要な応答フィールドの配列。 「はじめに」のresponse- FieldArray/excludeFieldArrayを参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> excludeFieldArray <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型：StringArray</span> </p> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>除外された応答フィールドの配列。 「はじめに」のresponse- FieldArray/excludeFieldArrayを参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**出力(getAssociatedAssetsReturn)**

<table id="table_B894B4B6EFA24359A0250A8A4523EA8D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>名前 </p> </th> 
   <th colname="col2" class="entry"> <p>種類 </p> </th> 
   <th colname="col3" class="entry"> <p>必須 </p> </th> 
   <th colname="col4" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> containerArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：AssetArray</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>指定したアセットを含むセットおよびテンプレートアセットの配列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> memberArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：AssetArray</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>指定したセットまたはテンプレートアセットに含まれるアセットの配列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> layerReferenceArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：AssetArray</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>レイヤーまたはテンプレートURLで参照されているアセットの配列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ownerArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：AssetArray</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>指定したアセットを所有するアセットの配列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> derivedArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：AssetArray</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>指定したアセットの生成に使用されたアセットの配列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> generatorArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：GenerationInfoArray</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>generatorArrayは <span class="codeph"></span> 、このアセットの作成方法を示します。 例えば、assetHandlerが <span class="codeph"> PDFの画像ページだった場合</span> 、PDFプロセッサツールが含まれ、PdfFileアセットが参照されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 生 <span class="varname"> 成配列</span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：GenerationInfoArray</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>生成され <span class="codeph"> た配列は</span> 、このアセットの作成方法を反転します。 例えば、生成された <span class="codeph"> Arrayに</span> 、このassetHandlerから生成された画像のリストを含めることができます(PdfFileア <span class="codeph"> セットの場合</span> )。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> thumbAsset <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：アセット</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>要求アセットに関連付けられているサムアセット情報です。 サムアセットが割り当てられていない場合、応答でフィールドは省略されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

パラメーターを使用するか、応 `responseFieldArray` 答サ `excludeFieldArray` イズを制限することができます。 特に、元のアセットレコ `GenerationInfo` ードと生成されたア `generatorArray` セットレコードの両方を含めるように、に返される項目また `generatedArray` はデフォルトの項目が返されます。 PDFアセットタイプの場合、この動作により、応答内の「元の」PDFアセットレコードの不要な複数のコピーが生成されます。 この問題は、を追加することで排除で `generatedArray/items/originator` きま `excludeFieldArray`す。 または、に含める応答フィールドの明示的なリストを指定できます `responseFieldArray`。

## 例 {#section-8946ea4b9cb94912a8408249c897f192}

次の基本例は、PDFから抽出された画像のジェネレーターのハンドルの要求です。 PDFを含 `containerArray` む項目の長さ1が含ま `assetHandle` れます。

**リクエスト**

```java
<soap:Envelope xmlns:soap="http://www.w3.org/2003/05/soap-envelope" xmlns:beta="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
   <soap:Body>
      <beta:getAssociatedAssetsParam>
         <beta:companyHandle>c|11</beta:companyHandle>
         <beta:assetHandle>a|197</beta:assetHandle>
         <beta:responseFieldArray>
            <beta:items>containerArray/items/assetHandle</beta:items>
         </beta:responseFieldArray>
      </beta:getAssociatedAssetsParam>
   </soap:Body>
</soap:Envelope>
```

**応答**

```java
<soapenv:Envelope xmlns:soapenv="http://www.w3.org/2003/05/soap-envelope">
   <soapenv:Body>
      <getAssociatedAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
         <containerArray>
            <items>
               <assetHandle>a|207</assetHandle>
            </items>
         </containerArray>
      </getAssociatedAssetsReturn>
   </soapenv:Body>
</soapenv:Envelope>
```

上記の例の逆は次のとおりです。

**リクエスト**

```java
<soap:Envelope xmlns:soap="http://www.w3.org/2003/05/soap-envelope" xmlns:beta="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
   <soap:Body>
      <beta:getAssociatedAssetsParam>
         <beta:companyHandle>c|11</beta:companyHandle>
         <beta:assetHandle>a|177</beta:assetHandle>
        <beta:responseFieldArray>
           <beta:items>generatedArray/items/originator/assetHandle</beta:items>
         </beta:responseFieldArray>
      </beta:getAssociatedAssetsParam>
   </soap:Body>
</soap:Envelope>
```

**応答**

```java
<soapenv:Envelope xmlns:soapenv="http://www.w3.org/2003/05/soap-envelope">
   <soapenv:Body>
      <getAssociatedAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
         <generatedArray>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
         </generatedArray>
      </getAssociatedAssetsReturn>
   </soapenv:Body>
</soapenv:Envelope>
```

次の例では、を使用して会社にグループを追加します `groupHandleArray`。 この例では、1つのグループのみを使用します。

**リクエスト**

```java
<ns1:addGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray><ns1:items>225</ns1:items></ns1:groupHandleArray>
</ns1:addGroupMembershipParam>
```

**応答**

なし
