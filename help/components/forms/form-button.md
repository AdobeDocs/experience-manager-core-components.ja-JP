---
title: フォームボタンコンポーネント
description: コアコンポーネントのフォーム非表示コンポーネントを使用すれば、フォームに非表示フィールドを含めることができます。
translation-type: tm+mt
source-git-commit: 95c0621f5423bfa515fe5e8b693e127ea56b4ae0

---


# フォームボタンコンポーネント {#form-button-component}

コアコンポーネントのフォームボタンコンポーネントを使用すれば、アクションをトリガーするボタンをページに含めることができます。

## 使用方法 {#usage}

コアコンポーネントのフォームボタンコンポーネントを使用すれば、フォームの送信をトリガーすることが多いボタンフィールドを作成できます。このコンポーネントは、[フォームコンテナコンポーネント](form-container.md)と共に使用するためのものです。

ボタンのプロパティは、コンテンツ編集者が[設定ダイアログ](#configure-dialog)で定義できます。

## バージョンと互換性 {#version-and-compatibility}

このドキュメントでは、フォームボタンコンポーネントの現在のバージョン（2018 年 1 月にコアコンポーネントのリリース 2.0.0 で導入された v2）について説明します。

コンポーネントのすべてのサポート対象バージョン、コンポーネントの各バージョンと互換性のある AEM バージョン、以前のバージョンのドキュメントへのリンクを次の表に示します。

| コンポーネントのバージョン | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |--- |---|
| v2 | 互換性あり | 互換性あり | 互換性あり | 互換性あり |
| [v1](/help/components/v1/form-button-v1.md) | 互換性あり | 互換性あり | 互換性あり | - |

コアコンポーネントのバージョンとリリースについて詳しくは、[コアコンポーネントのバージョン](/help/versions.md)を参照してください。

## コンポーネント出力のサンプル {#sample-component-output}

To experience the Form Button Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_form_button).

### 技術的詳細 {#technical-details}

フォームボタンコンポーネントに関する最新の技術ドキュメントについては、[GitHub](https://adobe.com/go/aem_cmp_tech_form_button_v2) を参照してください。

コアコンポーネントの開発について詳しくは、[コアコンポーネント開発者向けドキュメント](/help/developing/overview.md)を参照してください。

## 設定ダイアログ {#configure-dialog}

設定ダイアログでは、コンテンツ作成者がボタンのパラメーターを定義できます。

### 「プロパティ」タブ {#properties-tab}

![](/help/assets/screen_shot_2018-01-12at120433.png)

* **種類**

   * **ボタン**
   * **送信**

* **タイトル** - ボタンに表示されるテキスト

   * 指定しない場合は、デフォルトでボタンの種類が表示されます

* **名前** - ボタンの名前（フォームデータと共に送信されます）
* **値** - ボタンの値（フォームデータと共に送信されます）

## デザインダイアログ{#design-dialog}

### 「スタイル」タブ {#styles-tab}

フォームボタンコンポーネントは、AEM [スタイルシステム](/help/get-started/authoring.md#component-styling)をサポートしています。