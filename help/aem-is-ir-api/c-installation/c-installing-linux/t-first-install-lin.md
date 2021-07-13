---
description: この手順では、Linuxに初めて画像サービングをインストールする方法を示します。
solution: Experience Manager
title: 初めてのインストール
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: f27e6b27-641c-4a88-9ed0-94ada9ba75a9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# 初めてのインストール{#installing-for-the-first-time}

この手順では、Linuxに初めて画像サービングをインストールする方法を示します。

1. root権限でサーバーホストにログインします。
1. フォルダー[!DNL /usr/local/scene7/licenses]を作成します。

   画像サービングまたは画像レンダリングのライセンスキーファイル（ファイルサフィックス[!DNL .sc8]を含む）が使用可能な場合は、このフォルダーにコピーします。 それ以外の場合は、インストールを続行し、後でライセンスキーをインストールします。
1. 画像サービング配布tarファイルを解凍し、解凍します。
1. [!DNL Setup]フォルダーにある[!DNL ./install-is]を実行して、インストールウィザードを起動します。

   ライセンスキーが見つからない場合は、ライセンスファイルの取得方法を説明する手順が表示されます。 この時点でインストールするか、画像サービングのインストールを続行し、後でライセンスキーをインストールします。
1. 使用許諾契約(EULA)が表示されたら、使用許諾契約書を読み、`y`と入力して続行します。

   次の表に示すプロンプトが表示されます。

<table id="table_0E7B673CAD8E4C5EB72F8283A0DDEFC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> メインリスニングポート[8080]:</span> </p> </td> 
   <td colname="col2"> <p>画像サービングおよび画像レンダリングのメインHTTPリスニングポート。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 管理リスニングポート[8083]:</span> </p> </td> 
   <td colname="col2"> <p>管理リスニングポート。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 最大HTTPキャッシュサイズ(MB) [2000]:</span> </p> </td> 
   <td colname="col2"> <p>メイン応答キャッシュの初期サイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> キャッシュルートフォルダー[/usr/local/scene7/ImageServing/cache]:</span> </p> </td> 
   <td colname="col2"> <p>PSキャッシュフォルダ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Image Server所有者ID [root]:</span> </p> </td> 
   <td colname="col2"> <p>画像サービングサーバーをインストールするユーザーアカウント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Image Server Group ID [root]:</span> </p> </td> 
   <td colname="col2"> <p>画像サービングサーバーをインストールするグループアカウント。 </p> </td> 
  </tr> 
 </tbody> 
</table>

1. **[!UICONTROL Enter]**&#x200B;キーを押して、デフォルト値を受け入れるか、別の値を指定します。

   指定したポート番号がすべて一意であり、このホストで別途使用されていないことを確認します。

   >[!IMPORTANT]
   >
   >root以外のアカウントを指定する場合は、Image Serverが読み取り/書き込みを必要とするすべてのファイルとフォルダーに対するアクセス権限が、設定ファイルで再設定されたときに正しく設定されていることを確認する必要があります。
   >
   >画像サービングが[!DNL /usr/local/Scene7/ImageServing]にインストールされました。 [!DNL /usr/local/Scene7/ImageRendering]に特定の画像レンダリングコンテンツがインストールされます。
   >
   >インストールが終了すると、インストールウィザードはImage Serverの起動を試みます。 有効なライセンスキーが見つからない場合、Image Serverを起動できません。 有効なライセンスがあり、Image Serverが起動しない場合は、ログファイルを参照してください。

>[!NOTE]
>
>画像サービングをインストールした後にライセンスがインストールされている場合は、使用する前にImage Serverを手動で起動する必要があります。
