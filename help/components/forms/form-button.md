---
title: フォームボタンコンポーネント
description: コアコンポーネントのフォーム非表示コンポーネントを使用すれば、フォームに非表示フィールドを含めることができます。
role: Architect, Developer, Admin, User
exl-id: 1e5cff43-57db-4bfc-b2d2-23307eaf5eb3
source-git-commit: 6fbc781db555bc6abaed1d122a9a8756e3d53222
workflow-type: ht
source-wordcount: '413'
ht-degree: 100%

---

# フォームボタンコンポーネント {#form-button-component}

コアコンポーネントのフォームボタンコンポーネントを使用すれば、アクションをトリガーするボタンをページに含めることができます。

## 使用方法 {#usage}

コアコンポーネントのフォームボタンコンポーネントを使用すれば、フォームの送信をトリガーすることが多いボタンフィールドを作成できます。このコンポーネントは、[フォームコンテナコンポーネント](form-container.md)と共に使用するためのものです。

ボタンのプロパティは、コンテンツ編集者が[設定ダイアログ](#configure-dialog)で定義できます。

## バージョンと互換性 {#version-and-compatibility}

このドキュメントでは、フォームボタンコンポーネントの現在のバージョン（2018年1月にコアコンポーネントのリリース 2.0.0 で導入された v2）について説明します。

コンポーネントのすべてのサポート対象バージョン、コンポーネントの各バージョンと互換性のある AEM バージョン、以前のバージョンのドキュメントへのリンクを次の表に示します。

| コンポーネントのバージョン | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| v2 | <br>[リリース 2.17.4](/help/versions.md) 以前と互換性あり | 互換性あり | 互換性あり | 互換性あり |
| [v1](/help/components/v1/form-button-v1.md) | 互換性あり | 互換性あり | - | 互換性あり |

コアコンポーネントのバージョンとリリースについて詳しくは、[コアコンポーネントのバージョン](/help/versions.md)を参照してください。

## コンポーネント出力のサンプル {#sample-component-output}

フォームボタンコンポーネントを体験し、その設定オプションや HTML および JSON 出力の例を確認するには、[コンポーネントライブラリ](https://adobe.com/go/aem_cmp_library_form_button_jp)を参照してください。

### 技術的詳細 {#technical-details}

フォームボタンコンポーネントに関する最新の技術ドキュメントについては、[GitHub](https://adobe.com/go/aem_cmp_tech_form_button_v2_jp) を参照してください。

コアコンポーネントの開発について詳しくは、[コアコンポーネント開発者向けドキュメント](/help/developing/overview.md)を参照してください。

## 設定ダイアログ {#configure-dialog}

設定ダイアログでは、コンテンツ作成者がボタンのパラメーターを定義できます。

### 「プロパティ」タブ {#properties-tab}

![フォームボタンコンポーネントの編集ダイアログ](/help/assets/form-button-edit.png)

* **種類**

   * **ボタン**
   * **送信**

* **タイトル** - ボタンに表示されるテキスト

   * 指定しない場合は、デフォルトでボタンの種類が表示されます

* **名前** - ボタンの名前（フォームデータと共に送信されます）
* **値** - ボタンの値（フォームデータと共に送信されます）

* **ID** - このオプションを使用すると、HTML 内および [データレイヤー](/help/developing/data-layer/overview.md)内のコンポーネントの一意の識別子を制御できます。
   * 空白のままにした場合、一意の ID が自動的に生成されます。生成された ID は結果のページを調べることで確認できます。
   * ID を指定した場合、作者はその ID が一意であることを確認する必要があります。
   * ID を変更すると、CSS、JS、およびデータレイヤーのトラッキングに影響を与える可能性があります。

## デザインダイアログ {#design-dialog}

### 「スタイル」タブ {#styles-tab}

フォームボタンコンポーネントは、AEM [スタイルシステム](/help/get-started/authoring.md#component-styling)をサポートしています。
