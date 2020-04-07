---
description: この手順では、Linuxで初めて画像サービングをインストールする方法を示します。
seo-description: この手順では、Linuxで初めて画像サービングをインストールする方法を示します。
seo-title: 初めてのインストール
solution: Experience Manager
title: 初めてのインストール
topic: Scene7 Image Serving - Image Rendering API
uuid: 6a9a6dd2-2c69-447a-9628-eba08dc4f6c8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 初めてのインストール{#installing-for-the-first-time}

この手順では、Linuxで初めて画像サービングをインストールする方法を示します。

1. root権限でサーバーホストにログインします。
1. フォルダーを作成しま [!DNL /usr/local/scene7/licenses]す。

   画像サービングまたは画像レンダリングのライセンスキーファイル（ファイルのサフィックスが付く）が使 [!DNL .sc8] 用可能な場合は、このフォルダにコピーします。 それ以外の場合は、インストールを続行し、後でライセンスキーをインストールします。
1. 画像サービング配布用tarファイルを解凍し、解凍します。
1. フォル [!DNL ./install-is]ダ内のを実行し、イ [!DNL Setup] ンストールウィザードを起動します。
   ライセンスキーが見つからない場合は、ライセンスファイルの取得方法を説明する手順が表示されます。 この時点でインストールを行うか、画像サービングのインストールを続行し、後でライセンスキーをインストールします。
1. 使用許諾契約書(EULA)が表示されたら、使用許諾契約書を読み、入力して続行 `y` します。

   次の表に示すプロンプトが表示されます。

<table id="table_0E7B673CAD8E4C5EB72F8283A0DDEFC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> メインリスニングポート[8080]:</span> </p> </td> 
   <td colname="col2"> <p>画像サービングと画像レンダリングのメインHTTPリスニングポート。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 管理リスニングポート[8083]:</span> </p> </td> 
   <td colname="col2"> <p>管理リスニングポート。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Maximum HTTP Cache Size (MB) [2000]:</span> </p> </td> 
   <td colname="col2"> <p>メイン応答キャッシュの初期サイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> キャッシュルートフォルダ[/usr/local/scene7/ImageServing/cache]:</span> </p> </td> 
   <td colname="col2"> <p>PSキャッシュフォルダー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Image Server Owner ID [root]:</span> </p> </td> 
   <td colname="col2"> <p>画像サービングサーバをインストールするユーザーアカウント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Image Server Group ID [root]:</span> </p> </td> 
   <td colname="col2"> <p>画像サービングサーバをインストールするグループアカウント。 </p> </td> 
  </tr> 
 </tbody> 
</table>

1. Enterキーを **[!UICONTROL 押して]** 、デフォルト値を受け入れるか、別の値を指定します。

   指定したすべてのポート番号が一意であり、このホストでは使用されないことを確認します。

   **重要：**root以外のアカウントを指定した場合は、Image Serverが読み取りおよび書き込みの必要があるすべてのファイルやフォルダのアクセス権限が、設定ファイルで再設定されたときに正しく設定されていることを確認する必要があります。
>画像サービングがにインストールされまし [!DNL /usr/local/Scene7/ImageServing]た。 特定の画像レンダリングコンテンツがにインストールされま [!DNL /usr/local/Scene7/ImageRendering]す。
>
>インストールが終了すると、インストールウィザードはImage Serverの起動を試みます。 有効なライセンスキーが見つからない場合、Image Serverを起動できません。 有効なライセンスがあり、Image Serverが起動していない場合は、ログファイルを参照してください。
>[!NOTE]
Image Servingのインストール後にライセンスがインストールされる場合は、使用する前にImage Serverを手動で起動する必要があります。
>
>
>

