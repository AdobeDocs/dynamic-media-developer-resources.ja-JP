---
description: この手順では、Linuxで初めて画像サービングをインストールする方法を示します。
seo-description: この手順では、Linuxで初めて画像サービングをインストールする方法を示します。
seo-title: 初めてのインストール
solution: Experience Manager
title: 初めてのインストール
topic: Scene7 Image Serving - Image Rendering API
uuid: 6a9a6dd2-2c69-447a-9628-eba08dc4f6c8
translation-type: tm+mt
source-git-commit: edb21832b3e36a6498c6aad27813cd4b3032b48f
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---


# {#installing-for-the-first-time}初回インストール

この手順では、Linuxで初めて画像サービングをインストールする方法を示します。

1. root権限でサーバーホストにログインします。
1. フォルダー[!DNL /usr/local/scene7/licenses]を作成します。

   画像サービングまたは画像レンダリングのライセンスキーファイル（ファイル名が[!DNL .sc8]のファイル）が使用可能な場合は、このフォルダにコピーします。 それ以外の場合は、インストールに進み、後でライセンスキーをインストールします。
1. 画像サービングの配布tarファイルを解凍し、解凍します。
1. [!DNL Setup]フォルダーにある[!DNL ./install-is]を実行して、インストールウィザードを起動します。

   ライセンスキーが見つからない場合は、ライセンスファイルの取得方法を説明する手順が表示されます。 この時点でインストールするか、画像サービングのインストールを続行して、後でライセンスキーをインストールします。
1. 使用許諾契約書(EULA)が表示されたら、使用許諾契約書を読み、`y`と入力して続行します。

   次の表に示すプロンプトがインストーラーに表示されます。

<table id="table_0E7B673CAD8E4C5EB72F8283A0DDEFC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> メインリスニングポート[8080]:</span> </p> </td> 
   <td colname="col2"> <p>画像サービングおよび画像レンダリングのメインHTTPリスニングポート。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 管理リスニングポート[8083]:</span> </p> </td> 
   <td colname="col2"> <p>管理者リスニングポート。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Maximum HTTP Cache Size (MB) [2000]:</span> </p> </td> 
   <td colname="col2"> <p>メインの応答キャッシュの初期サイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> キャッシュルートフォルダ[/usr/local/scene7/ImageServing/cache]:</span> </p> </td> 
   <td colname="col2"> <p>PSキャッシュフォルダー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Image Server所有者ID [root]:</span> </p> </td> 
   <td colname="col2"> <p>画像サービングサーバをインストールするユーザーアカウント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Image Server Group ID [root]:</span> </p> </td> 
   <td colname="col2"> <p>画像サービングサーバをインストールするグループアカウント。 </p> </td> 
  </tr> 
 </tbody> 
</table>

1. **[!UICONTROL Enter]**&#x200B;キーを押して、デフォルト値を受け入れるか、別の値を指定します。

   指定したポート番号がすべて一意であることを確認し、このホストでは使用しないでください。

   >[!IMPORTANT]
   >
   >root以外のアカウントを指定した場合は、設定ファイルでこれらのフォルダを再設定する際に、Image Serverが読み取りまたは書き込みに必要なすべてのファイルとフォルダのアクセス権限が正しく設定されていることを確認する必要があります。
   >
   >画像サービングが[!DNL /usr/local/Scene7/ImageServing]にインストールされました。 特定の画像レンダリングのコンテンツが[!DNL /usr/local/Scene7/ImageRendering]にインストールされます。
   >
   >インストールが終了する前に、インストールウィザードはImage Serverの開始を試みます。 有効なライセンスキーが見つからない場合、Image Serverは開始できません。 有効なライセンスがあり、Image Serverが起動しない場合は、ログファイルを参照してください。

>[!NOTE]
>
>ライセンスが画像サービングのインストール後にインストールされる場合は、使用前にImage Serverを手動で起動する必要があります。
