---
title: ボタンコンポーネント（v1）
description: コアコンポーネントのボタンコンポーネントを使用すると、ボタンを作成および表示することができます。
role: Architect, Developer, Admin, User
exl-id: 63af16e4-dd4d-426d-88ef-769ecd1b3175
index: n
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: ht
source-wordcount: '397'
ht-degree: 100%

---


# ボタンコンポーネント（v1） {#button-component}

コアコンポーネントのボタンコンポーネントを使用すると、ページ上にボタンアイテムを設定および表示することができます。

## 使用方法 {#usage}

コアコンポーネントのボタンコンポーネントを使用すると、ページにボタンを含めることができます。

* ボタンのプロパティは、[設定ダイアログ](#configure-dialog)で選択できます。
* ボタンコンポーネントのスタイルは、[デザインダイアログ](#design-dialog)で定義できます。

## バージョンと互換性 {#version-and-compatibility}

このドキュメントでは、2019年6月にコアコンポーネントのリリース 2.5.0 で導入されたボタンコンポーネント v1 について説明します。

>[!CAUTION]
>
>このドキュメントでは、ボタンコンポーネント v1 について説明します。
>
>ボタンコンポーネントの現在のバージョンについて詳しくは、[ボタンコンポーネント](/help/components/button.md)のドキュメントを参照してください。

## コンポーネント出力のサンプル {#sample-component-output}

ボタンコンポーネントを体験し、その設定オプションや HTML および JSON 出力の例を確認するには、[コンポーネントライブラリ](https://adobe.com/go/aem_cmp_library_button)を参照してください。

## 技術的詳細 {#technical-details}

ボタンコンポーネントに関する最新の技術ドキュメントについては、[GitHub](https://adobe.com/go/aem_cmp_tech_button_v1_jp) を参照してください。

コアコンポーネントの開発について詳しくは、[コアコンポーネント開発者向けドキュメント](/help/developing/overview.md)を参照してください。

## 設定ダイアログ {#configure-dialog}

設定ダイアログでは、ボタンそのものと、ページの訪問者に対するボタンの動作および表示をコンテンツ作成者が定義できます。

### 「プロパティ」タブ {#properties-tab}

![ボタンコンポーネントの編集ダイアログの「プロパティ」タブ](/help/assets/button-edit-properties.png)

* **テキスト** - ボタンに表示するテキスト
* **リンク** - AEM 内のコンテンツページ、外部リソース、アンカーへのリンク
   * **選択ダイアログ**&#x200B;を使用して、AEM 内のパスを選択します。
* **アイコン** - ボタンにアイコンを表示するための識別子
* **ID** - このオプションを使用すると、HTML 内および[データレイヤー](/help/developing/data-layer/overview.md)内のコンポーネントの一意の識別子を制御できます。
   * 空白のままにした場合、一意の ID が自動的に生成されます。生成された ID は結果のページを調べることで確認できます。
   * ID を指定した場合、作者はその ID が一意であることを確認する必要があります。
   * ID を変更すると、CSS、JS、およびデータレイヤーのトラッキングに影響を与える可能性があります。

### 「アクセシビリティ」タブ {#accessibility-tab}

![ボタンコンポーネントの編集ダイアログの「アクセシビリティ」タブ](/help/assets/button-edit-accessibility.png)

「**アクセシビリティ**」タブでは、コンポーネントの「[ARIA アクセシビリティ](https://www.w3.org/WAI/standards-guidelines/aria/)」ラベルの値を設定できます。

* **ラベル** - コンポーネントの ARIA ラベル属性の値

## デザインダイアログ {#design-dialog}

### 「スタイル」タブ {#styles-tab}

ボタンコンポーネントでは、AEM [スタイルシステム](/help/get-started/authoring.md#component-styling)をサポートしています。

## アドビクライアントデータレイヤー {#data-layer}

ボタンコンポーネントは、[アドビクライアントデータレイヤー](/help/developing/data-layer/overview.md)をサポートしています。
