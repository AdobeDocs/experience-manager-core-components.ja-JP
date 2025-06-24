---
title: 'ソーシャル共有コンポーネント '
description: コアコンポーネントのソーシャル共有コンポーネントは、Facebook および Pinterest の共有ウィジェットです。
role: Architect, Developer, Admin, User
exl-id: 8bd53c76-da91-479b-b416-f978682a3d43
index: false
source-git-commit: dd30def59a8f037864da875ef4c831b11f766e57
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 96%

---


# ソーシャル共有コンポーネント {#social-sharing-component}

コアコンポーネントのソーシャル共有コンポーネントは、Facebook および Pinterest の共有ウィジェットです。

>[!NOTE]
>
>ソーシャル共有コンポーネントは、コアコンポーネント [ リリース 2.18.0.](/help/versions.md) で非推奨（廃止予定）となりました

{{traditional-aem}}

## 使用方法 {#usage}

ソーシャル共有コンポーネントでは、ページに Facebook および Pinterest の共有リンクを追加します。これは多くの場合、ページのヘッダーまたはフッターに含まれています。

他のコンポーネントとは異なり、ソーシャル共有コンポーネントの設定は、テンプレート作成者の場合は[最初のページのプロパティ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=ja)、コンテンツ作成者の場合は[ページのプロパティ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html?lang=ja)で行います。

## バージョンと互換性 {#version-and-compatibility}

このドキュメントでは、ソーシャル共有コンポーネントの最新のバージョン（コアコンポーネントのリリース 1.0.0 で導入された v1）について説明します。

コンポーネントのすべてのサポート対象バージョンおよびコンポーネントの各バージョンと互換性のある AEM バージョンを次の表に示します。

| コンポーネントのバージョン | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| v1 | <br>[リリース 2.17.4](/help/versions.md) 以前と互換性あり | 互換性あり、非推奨 | 互換性あり、非推奨 | 互換性あり、非推奨 |

コアコンポーネントのバージョンとリリースについて詳しくは、[コアコンポーネントのバージョン](/help/versions.md)を参照してください。

### 技術的詳細 {#technical-details}

コンポーネント共有に関する最新の技術ドキュメントについては、[GitHub](https://adobe.com/go/aem_cmp_tech_sharing_v1_jp) を参照してください。

コアコンポーネントの開発について詳しくは、[コアコンポーネント開発者向けドキュメント](/help/developing/overview.md)を参照してください。

## 編集ダイアログ {#edit-dialog}

![共有コンポーネントの編集ダイアログ](/help/assets/sharing-edit.png)

* **ID** - このオプションを使用すると、HTML 内および[データレイヤー](/help/developing/data-layer/overview.md)内のコンポーネントの一意の識別子を制御できます。
   * 空白のままにした場合、一意の ID が自動的に生成されます。生成された ID は結果のページを調べることで確認できます。
   * ID を指定した場合、作者はその ID が一意であることを確認する必要があります。
   * ID を変更すると、CSS、JS、およびデータレイヤーのトラッキングに影響を与える可能性があります。

共有には特別なページヘッダーが必要なので、共有はすべてページレベルで有効にする必要があります。そのため、コンテンツ作成者の場合、共有コンポーネントの編集オプションは、「共有」タブの[ページのプロパティ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html?lang=ja)で使用できます。

## デザインダイアログ {#design-dialog}

共有には特別なページヘッダーが必要なので、共有はすべてページレベルで有効にする必要があります。そのため、テンプレート作成者の場合、共有コンポーネントのデザインオプションは、[最初のページのプロパティ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=ja)で使用できます。
