---
title: ページコンポーネント（v2）
description: ページコンポーネントは、テンプレートエディターと連動するように設計された拡張可能なページコンポーネントです。このコンポーネントを使用すれば、テンプレートエディターでページのヘッダー／フッターおよび構造要素を組み立てることができます。
role: Developer, Admin, User
exl-id: e85fe4db-6de4-4a84-a54c-bd07a67efed3
index: false
TQID: https://experienceleague.adobe.com/p1V-3XLpA6H-rC-zWIYFqbPkd6HW7bBLWFXaj8aeNAs
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
subfeature_v2:
  - id: f86a5563-8f73-4ec0-be7d-a1782604870a
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 662
ht-degree: 100%

---

# ページコンポーネント（v2） {#page-component}

ページコンポーネントは、[テンプレートエディター](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=ja)と連動するように設計された拡張可能なページコンポーネントです。このコンポーネントを使用すれば、テンプレートエディターでページのヘッダー／フッターおよび構造要素を組み立てることができます。

## 使用方法 {#usage}

ページコンポーネントは、コアコンポーネントと編集可能なテンプレートを使用して設計されるあらゆるページの基礎となるものです。 ページコンポーネントを使用すれば、ページのヘッダー、フッター、構造を、他のコアコンポーネントを使用する際のテンプレートとして定義できます。

[デザインダイアログ](#design-dialog)を使用すれば、カスタムのクライアント側ライブラリをページ用に定義できます。 コンポーネントから編集ダイアログに直接アクセスできる他のコンポーネントとは異なり、ページコンポーネントはページそのものなので、ページコンポーネントの[編集ダイアログ](#edit-dialog)はページプロパティウィンドウになります。

## バージョンと互換性 {#version-and-compatibility}

このドキュメントでは、2018年1月にコアコンポーネントのリリース 2.0.0 で導入されたページコンポーネント v2 について説明します。

>[!CAUTION]
>
>このドキュメントでは、ページコンポーネント v2 について説明します。
>
>ページコンポーネントの現在のバージョンについて詳しくは、[ページコンポーネント](/help/components/page.md)のドキュメントを参照してください。

## プログレッシブ ｗeb アプリのサポート {#pwa-support}

コアコンポーネントのリリース 2.15.0 では、AEM as a Cloud Service のビルトインの[プログレッシブ web アプリ（PWA）機能](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/enable-pwa.html?lang=ja)をサポートするようになりました。 サイトレベルでの簡単な設定で、AEM エクスペリエンスを PWA に変えることができます。

### 技術的詳細 {#technical-details}

ページコンポーネントに関する最新の技術ドキュメントについては、[GitHub](https://adobe.com/go/aem_cmp_tech_page_v2_jp) を参照してください。

コアコンポーネントの開発について詳しくは、[コアコンポーネント開発者向けドキュメント](/help/developing/overview.md)を参照してください。

## 編集ダイアログ {#edit-dialog}

ページコンポーネントはページ全体を表しているので、通常は編集ダイアログで設定する内容が、[ページのプロパティ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html?lang=ja)ウィンドウにあります。

## デザインダイアログ {#design-dialog}

ページコンポーネントはページ全体を表しているので、ページテンプレートを編集する際は、**ページ情報／ページポリシー**&#x200B;でデザインダイアログにアクセスします。

![ページポリシー](/help/assets/page-policy.png)

>[!NOTE]
>
>以前のバージョンの AEM では、**ページポリシー**&#x200B;は&#x200B;**ページデザイン**&#x200B;と呼ばれていました。

### 「プロパティ」タブ {#properties-tab}

ページデザインウィンドウを使用すれば、読み込むクライアントライブラリとページの Web リソースライブラリを定義できます。

* **クライアントライブラリ** - 読み込むクライアントライブラリカテゴリを定義します。 JavaScript が本文の末尾に追加され、CSS がページの先頭に追加されます。
* **クライアントライブラリ JavaScript ページ先頭** - ページの先頭に読み込む JavaScript クライアントライブラリカテゴリを定義します。
   * ここで定義したカテゴリが「**クライアントライブラリ**」フィールドにも存在する場合は、JavaScript が本文の末尾ではなくページの先頭に読み込まれます。
   * カテゴリが「**クライアントライブラリ**」フィールドにも存在する場合を除き、CSS は読み込まれません。

* **Web リソースクライアントライブラリ** - favicon などの Web リソースを提供するために使用されるクライアントライブラリカテゴリです。

* **メインコンテンツ要素セレクターにスキップ** - ページのメインコンテンツに直接スキップするアクセシビリティ機能として使用されます。

![ページコンポーネントデザインのダイアログ](/help/assets/page-design.png)

「**クライアントライブラリ**」と「**クライアントライブラリ JavaScript ページ先頭**」の両方のフィールドにライブラリを次のように設定できます。

* 新しいフィールドを追加するには、フィールドの下にある「**追加**」ボタンをクリックまたはタップします。
* フィールドを削除するには、削除するフィードの横にあるごみ箱アイコンをクリックまたはタップします。
* 読み込み順序を変更するには、移動するフィールドの横にあるハンドルをクリックまたはタップしてドラッグします。

クライアント側ライブラリの使用に関する詳細は、[クライアント側ライブラリの使用](https://helpx.adobe.com/jp/experience-manager/6-5/sites/developing/using/clientlibs.html)を参照してください。

>[!CAUTION]
>
>ページ先頭のクライアントライブラリを個別に定義する機能は、コアコンポーネントリリース 2.2.0 で導入されました。

### 「スタイル」タブ {#styles-tab}

ページコンポーネントでは、AEM [スタイルシステム](/help/get-started/authoring.md#component-styling)をサポートしています。

## アドビクライアントデータレイヤー {#data-layer}

ページコンポーネントは、[アドビクライアントデータレイヤー](/help/developing/data-layer/overview.md)をサポートしています。
