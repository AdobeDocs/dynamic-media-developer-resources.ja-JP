---
description: サーバスーパーバイザの構成設定が含まれます。
solution: Experience Manager
title: SupervisorRegistry.xml
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: cc6a16fb-fd70-431f-aad6-adb99d4da062
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 0%

---

# SupervisorRegistry.xml{#supervisorregistry-xml}

サーバスーパーバイザの構成設定が含まれます。

この XML ファイルを編集する際は、有効な XML 構文を維持してください。そうしないと、Image Server の起動に失敗する場合があります。

このファイルを編集した後に画像サービングを再起動し、変更が有効になることを確認します。 変更では、以下でハイライト表示されている要素/属性の値のみがサポートされます。 Dynamic Mediaテクニカルサポートの指示に従った場合にのみ、このファイルの他のすべてのコンテンツを編集します。

```
<supervisor>
    <config>
        <tcpport>9910</tcpport>
        <log>SV::log</log>
        <temp>SV::temp</temp>
        <tracelevel>SV::tracelevel</tracelevel>
        <tracestatsinterval>600</tracestatsinterval>
    </config>
    <servers>
        <server id="is">
            <description>Dynamic Media Image Server</description>
            <profile ref="SV::ImageServerMode"/>
            <startPriority>1</startPriority>
            <startDelay>5</startDelay>
            <stopTimeout>60</stopTimeout>
        </server>
        <server id="svg">
            <description>Dynamic Media SVG server</description>
            <profile ref="Java32"/>
            <profile ref="SVG"/>
            <arguments>
                <argument>-XmxSV::SvgHeapSize</argument>
                <argument>-XX:MaxPermSize=200m</argument>
                <argument>-Dcom.sun.management.jmxremote.port=9998</argument>
            </arguments>
            <startPriority>1</startPriority>
            <startDelay>5</startDelay>
            <stopTimeout>60</stopTimeout>
        </server>
        <server id="ps">
            <description>Dynamic Media [!DNL Platform Server]</description>
            <profile ref="Java32"/>
            <profile ref="PlatformServer"/>
            <profile ref="Tomcat"/>
            <arguments>
                <argument>-XmxSV::PsHeapSize</argument>
                <argument>-XX:MaxPermSize=200m</argument>
                <argument>-Dcom.sun.management.jmxremote.port=9999</argument>
            </arguments>
            <startPriority>2</startPriority>
            <startDelay>5</startDelay>
            <stopTimeout>60</stopTimeout>
        </server>
    </servers>
</supervisor>
```
