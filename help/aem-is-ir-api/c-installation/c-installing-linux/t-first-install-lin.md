---
title: 初めてのインストール
description: この手順では、Linux®でImage Servingを初めてインストールする方法を説明します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f27e6b27-641c-4a88-9ed0-94ada9ba75a9
TQID: 'https://experienceleague.adobe.com/PppWtEjMNn6CPNvnT03PoFjCW2OxbAJjrFYgbPBi7Iw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 383
ht-degree: 0%

---

# 初めてのインストール{#installing-for-the-first-time}

この手順では、Linux®でImage Servingを初めてインストールする方法を説明します。

1. root権限でサーバーホストにログインします。
1. フォルダー[!DNL /usr/local/scene7/licenses]を作成します。

   画像サービングまたは画像レンダリングのライセンスキーのファイル（[!DNL .sc8] ファイル接尾辞を含む）が使用可能な場合は、このフォルダーにコピーします。 それ以外の場合は、インストールに進み、後でライセンスキーをインストールします。
1. 画像サービング配布tar ファイルを解凍して展開します。
1. [!DNL Setup] フォルダーで、[!DNL ./install-is]を実行してインストールウィザードを起動します。

   ライセンスキーが見つからない場合は、ライセンスファイルの取得方法を説明する手順が表示されます。 この時点で行うか、画像サービングのインストールに進み、後でライセンスキーをインストールします。
1. エンドユーザー使用許諾契約（EULA）が表示されたら、使用許諾契約を読み、`y`と入力して続行します。

   インストーラーには、次の表に示すプロンプトが表示されます。

<table id="table_0E7B673CAD8E4C5EB72F8283A0DDEFC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> メイン リスニング ポート [8080]:</span> </p> </td>
   <td colname="col2"> <p>画像サービングと画像レンダリング用のメイン HTTP リスニングポート。 </p> </td>
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">管理者リスニングポート [8083]:</span> </p> </td> 
   <td colname="col2"> <p>管理者リスニングポート。 </p> </td>
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> HTTP キャッシュの最大サイズ （MB） [2000]:</span> </p> </td> 
   <td colname="col2"> <p>メイン応答キャッシュの初期サイズ。 </p> </td>
  </tr>
  <tr> 
   <td colname="col1"> <p><span class="codeph"> キャッシュ ルート フォルダー[/usr/local/scene7/ImageServing/cache]:</span> </p> </td> 
   <td colname="col2"> <p>PS キャッシュフォルダー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">画像サーバー所有者ID [ ルート ]:</span> </p> </td>
   <td colname="col2"> <p>Image Serving サーバーをインストールするユーザーアカウント。 </p> </td>
  </tr>
  <tr> 
   <td colname="col1"> <p><span class="codeph">画像サーバーグループ ID [ ルート ]:</span> </p> </td>
   <td colname="col2"> <p>Image Serving サーバーをインストールするグループアカウント。 </p> </td>
  </tr>
 </tbody>
</table>

1. **[!UICONTROL Enter]**&#x200B;を押して、デフォルト値を受け入れるか、別の値を指定します。

   指定したすべてのポート番号が一意であり、このホストで使用されないようにしてください。

   >[!IMPORTANT]
   >
   >ルート以外のアカウントを指定する場合は、Image Serverが読み取りと書き込みを必要とするすべてのファイルとフォルダーのアクセス権限が、設定ファイルでこれらのフォルダーが再設定されるときに正しく設定されていることを確認する必要があります。
   >
   >画像サービングが[!DNL /usr/local/Scene7/ImageServing]にインストールされました。 特定の画像レンダリングの内容が[!DNL /usr/local/Scene7/ImageRendering]にインストールされています。
   >
   >インストールの終わりに、インストールウィザードがImage Serverの起動を試みます。 有効なライセンスキーが見つからない場合は、Image Serverを起動できません。 有効なライセンスがあり、Image Serverがまだ起動しない場合は、ログファイルを参照してください。

>[!NOTE]
>
>Image Servingをインストールした後にライセンスをインストールする場合は、使用する前にImage Serverを手動で起動する必要があります。
