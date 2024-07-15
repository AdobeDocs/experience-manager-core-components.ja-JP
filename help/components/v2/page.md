---
title: ページコンポーネント（v2）
description: ページコンポーネントは、テンプレートエディターと連動するように設計された拡張可能なページコンポーネントです。このコンポーネントを使用すれば、テンプレートエディターでページのヘッダー／フッターおよび構造要素を組み立てることができます。
role: Architect, Developer, Admin, User
exl-id: e85fe4db-6de4-4a84-a54c-bd07a67efed3
source-git-commit: e291d4c1bfd37292d68c236178f9681c4e5ee741
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 100%

---

# ページコンポーネント（v2） {#page-component}

ページコンポーネントは、[テンプレートエディター](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=ja)と連動するように設計された拡張可能なページコンポーネントです。このコンポーネントを使用すれば、テンプレートエディターでページのヘッダー／フッターおよび構造要素を組み立てることができます。

## 使用方法 {#usage}

ページコンポーネントは、コアコンポーネントと編集可能なテンプレートを使用して設計されるあらゆるページの基礎となるものです。ページコンポーネントを使用すれば、ページのヘッダー、フッター、構造を、他のコアコンポーネントを使用する際のテンプレートとして定義できます。

[デザインダイアログ](#design-dialog)を使用すれば、カスタムのクライアント側ライブラリをページ用に定義できます。コンポーネントから編集ダイアログに直接アクセスできる他のコンポーネントとは異なり、ページコンポーネントはページそのものなので、ページコンポーネントの[編集ダイアログ](#edit-dialog)はページプロパティウィンドウになります。

## バージョンと互換性 {#version-and-compatibility}

このドキュメントでは、2018年1月にコアコンポーネントのリリース 2.0.0 で導入されたページコンポーネント v2 について説明します。

>[!CAUTION]
>
>このドキュメントでは、ページコンポーネント v2 について説明します。
>
>ページコンポーネントの現在のバージョンについて詳しくは、[ページコンポーネント](/help/components/page.md)のドキュメントを参照してください。

## プログレッシブ ｗeb アプリのサポート {#pwa-support}

コアコンポーネントのリリース 2.15.0 では、AEM as a Cloud Service の組み込み[プログレッシブ Web アプリ（PWA）機能をサポートするようになりました。](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/enable-pwa.html?lang=ja)サイトレベルでの簡単な設定で、AEM エクスペリエンスを PWA に変えることができます。

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

* **クライアントライブラリ** - 読み込むクライアントライブラリカテゴリを定義します。JavaScript が本文の末尾に追加され、CSS がページの先頭に追加されます。
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

## Adobe Client Data Layer {#data-layer}

ページコンポーネントは、[Adobe Client Data Layer](/help/developing/data-layer/overview.md) をサポートしています。
