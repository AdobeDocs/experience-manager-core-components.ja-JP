---
title: メールタイトルコンポーネント
description: メールタイトルコンポーネントは、インプレース編集機能を備えたメールのセクション見出しコンポーネントです。
role: Architect, Developer, Admin, User
exl-id: f65b6973-bb36-406f-bbea-f85a23f5340b
source-git-commit: 33976c0e745ad091a142109f70541f01a31edc5b
workflow-type: tm+mt
source-wordcount: '636'
ht-degree: 100%

---


# メールタイトルコンポーネント {#email-title-component}

メールタイトルコンポーネントは、インプレース編集機能を備えたメールのセクション見出しコンポーネントです。

## 使用方法 {#usage}

メールタイトルコンポーネントは、メールのセクションのタイトルまたは見出しとして使用するためのものです。

* 使用可能な見出しレベルは、[デザインダイアログ](#design-dialog)でテンプレート作成者が定義できます。
* コンテンツ作成者は、[編集ダイアログ](#edit-dialog)で、使用可能な見出しレベルから選択できます。

利便性の向上のため、見出しテキストの簡単なインプレース編集も可能です。

## バージョンと互換性 {#version-and-compatibility}

このドキュメントでは、メールタイトルコンポーネントの現在のバージョン（2022年10月にメールコアコンポーネントのリリース x で導入された v1）について説明します。

コンポーネントのすべてのサポート対象バージョン、コンポーネントの各バージョンと互換性のある AEM バージョン、以前のバージョンのドキュメントへのリンクを次の表に示します。

| コンポーネントのバージョン | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | 互換性あり | 互換性あり |

コアコンポーネントのバージョンとリリースについて詳しくは、[コアメールコンポーネントのバージョン](/help/versions.md)を参照してください。

## コンポーネント出力のサンプル {#sample-component-output}

タイトルコンポーネントを体験し、その設定オプションや HTML および JSON 出力の例を確認するには、[コンポーネントライブラリ](https://adobe.com/go/aem_cmp_library_email_title)を参照してください。

### 技術的詳細 {#technical-details}

タイトルコンポーネントに関する最新の技術ドキュメントについては、[GitHub](https://adobe.com/go/aem_cmp_tech_email_title_v1) を参照してください。

コアコンポーネントの開発について詳しくは、[コアコンポーネント開発者向けドキュメント](/help/developing/overview.md)を参照してください。

## 編集ダイアログ {#edit-dialog}

編集ダイアログでは、コンテンツ作成者がタイトルテキストを定義したり、見出しレベルを選択したりできます。

* **タイトル** - 空白の場合、ページタイトルが使用されます
   * キャンペーンアイコンをクリックして、[Adobe Campaign 変数を選択](/help/email/campaign-variables.md)ダイアログを開き、Adobe Campaign から動的コンテンツを挿入します。
* **種類 / サイズ** - タイトルの見出しレベルを定義します
* **リンク** - タイトルのリンク先のコンテンツを定義します。コンテンツページへのパス、外部 URL、ページアンカーのいずれかを指定できます。
   * キャンペーンアイコンをクリックして、[Adobe Campaign 変数を選択](/help/email/campaign-variables.md)ダイアログを開き、Adobe Campaign から動的コンテンツを挿入します。
* **ID** - このオプションを使用すると、HTML 内のコンポーネントの一意の ID を制御できます。
   * 空白のままにした場合、一意の ID が自動的に生成されます。生成された ID は結果のページを調べることで確認できます。
   * ID を指定した場合、作者はその ID が一意であることを確認する必要があります。
   * ID を変更すると、CSS に影響を与える可能性があります。

![メールタイトルコンポーネントの編集ダイアログ](/help/email/assets/email-title-edit.png)

インプレースエディターを使用して、タイトルコンポーネントのテキストを編集することもできます。

![メールタイトルコンポーネントのインプレース編集](/help/email/assets/email-title-edit-inline.png)

### 「スタイル」タブ {#styles-tab-edit}

メールタイトルコンポーネントでは、AEM [スタイルシステム](/help/get-started/authoring.md#component-styling)をサポートしています。

ドロップダウンを使用して、コンポーネントに適用するスタイルを選択します。編集ダイアログでの選択項目は、コンポーネントツールバーから選択した項目と同じ効果があります。

ドロップダウンメニューを使用するには、[デザインダイアログ](#design-dialog)でこのコンポーネントのスタイルを設定する必要があります。

![タイトルコンポーネントの編集ダイアログの「スタイル」タブ](/help/email/assets/email-title-edit-styles.png)

## デザインダイアログ {#design-dialog}

デザインダイアログでは、コンテンツ作成者が使用する際のタイトルコンポーネントのデフォルト見出しレベルをテンプレート作成者が定義できます。

### 「サイズ」タブ {#sizes-tab}

![タイトルコンポーネントのデザインダイアログ](/help/email/assets/email-title-design.png)

* **作成者に許可されたタイプ / サイズ** - コンテンツ作成者がメールタイトルコンポーネントを使用する際に選択できる見出しタイプを有効または無効にします。
* **デフォルトのタイプ／サイズ** - コンテンツ作成者がメールタイトルコンポーネントをページに追加したときに自動的に割り当てられる見出しタイプを定義します。
* **リンクを無効化** - メールタイトルコンポーネントでのリンクのサポートを無効にして、コンテンツ作成者がタイトルからリンクできないようにします。

### 「スタイル」タブ {#styles-tab}

電子メールタイトルコンポーネントでは、AEM [スタイルシステム](/help/get-started/authoring.md#component-styling)をサポートしています。