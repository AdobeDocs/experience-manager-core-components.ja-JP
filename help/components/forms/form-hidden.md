---
title: フォーム非表示コンポーネント
description: コアコンポーネントのフォーム非表示コンポーネントを使用すれば、非表示フィールドを表示できます。
role: Developer, Admin, User
exl-id: 0364cd3b-3c09-46db-9392-a67e3f9ea7a5
TQID: https://experienceleague.adobe.com/4A6TDfa-zTap73hcgFA-fbjbKqd3dF11Zgs-eEypE0Y
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 432
ht-degree: 100%

---

# フォーム非表示コンポーネント{#form-hidden-component}

コアコンポーネントのフォーム非表示コンポーネントを使用すれば、非表示フィールドを表示できます。

## 使用方法 {#usage}

コアコンポーネントのフォーム非表示コンポーネントを使用すれば、非表示フィールドを作成して、現在のページに関する情報を AEM に返すことができます。このコンポーネントは、[フォームコンテナコンポーネント](form-container.md)と共に使用するためのものです。

フィールドのプロパティは、コンテンツ編集者が[設定ダイアログ](form-hidden.md)で定義できます。

## バージョンと互換性 {#version-and-compatibility}

このドキュメントでは、フォーム非表示コンポーネントの現在のバージョン（2018年1月にコアコンポーネントのリリース 2.0.0 で導入された v2）について説明します。

コンポーネントのすべてのサポート対象バージョン、コンポーネントの各バージョンと互換性のある AEM バージョン、以前のバージョンのドキュメントへのリンクを次の表に示します。

| コンポーネントのバージョン | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| v2 | <br>[リリース 2.17.4](/help/versions.md) 以前と互換性あり | 互換性あり | 互換性あり | 互換性あり |
| [v1](/help/components/v1/form-hidden-v1.md) | 互換性あり | 互換性あり | - | 互換性あり |

コアコンポーネントのバージョンとリリースについて詳しくは、[コアコンポーネントのバージョン](/help/versions.md)を参照してください。

## コンポーネント出力のサンプル {#sample-component-output}

フォーム非表示コンポーネントを体験し、その設定オプションや HTML および JSON 出力の例を確認するには、[コンポーネントライブラリ](https://adobe.com/go/aem_cmp_library_form_hidden_jp)を参照してください。

### 技術的詳細 {#technical-details}

フォームの非表示メントコンポーネントに関する最新の技術ドキュメントについては、[GitHub](https://adobe.com/go/aem_cmp_tech_form_hidden_v2_jp) を参照してください。

コアコンポーネントの開発について詳しくは、[コアコンポーネント開発者向けドキュメント](/help/developing/overview.md)を参照してください。

## 設定ダイアログ {#configure-dialog}

設定ダイアログでは、コンテンツ作成者が非表示フィールドのパラメーターを定義できます。

![フォーム非表示の編集ダイアログ](/help/assets/form-hidden-edit.png)

* **名前** - フィールドの名前（フォームデータと共に送信されます）
* **値** - フィールドの値（フォームデータと共に送信されます）
* **ID** - このオプションを使用すると、HTML 内および[データレイヤー](/help/developing/data-layer/overview.md)内のコンポーネントの一意の識別子を制御できます。
   * 空白のままにした場合、一意の ID が自動的に生成されます。生成された ID は結果のページを調べることで確認できます。
   * ID を指定した場合、作者はその ID が一意であることを確認する必要があります。
   * ID を変更すると、CSS、JS、およびデータレイヤーのトラッキングに影響を与える可能性があります。

フォーム非表示コンポーネントには通常、表示される属性がありません。そのため、「**名前**」フィールドと「**値**」フィールドの値が割り当てられている場合、エディターのコンポーネントのプレースホルダーにはそれらのフィールド値が表示され、作成者が適切なフォーム非表示コンポーネントを識別できるようになっています。

![フォーム非表示コンポーネントの例](/help/assets/form-hidden-example.png)

## デザインダイアログ {#design-dialog}

### 「スタイル」タブ {#styles-tab}

フォーム非表示コンポーネントは、AEM [スタイルシステム](/help/get-started/authoring.md#component-styling)をサポートしています。
