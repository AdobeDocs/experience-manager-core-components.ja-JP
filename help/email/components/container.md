---
title: メールコンテナコンポーネント
description: メールコンテナコンポーネントを使用すると、メールコンテンツに複数の追加コンポーネントのコンテナを作成できます。
role: Architect, Developer, Admin, User
exl-id: 3b271e95-0093-4cb1-bb83-8446ba12a821
index: false
source-git-commit: eb77567dc32cccb81a9fc131493d11fb55b7e93b
workflow-type: ht
source-wordcount: '780'
ht-degree: 100%

---


# メールコンテナコンポーネント {#email-container-component}

メールコンテナコンポーネントを使用すると、メールコンテンツに複数の追加コンポーネントのコンテナを作成できます。

## 使用方法 {#usage}

メールコンテナコンポーネントを使用すると、メールコンテンツに複数の追加コンポーネントのコンテナを作成できます。また、他のコンポーネントをグループ化し、共通のスタイルやレイアウトを適用することができます。

* コンテナのプロパティは、[設定ダイアログ](#configure-dialog)で選択することができます。
* メールコンテナコンポーネントをページに追加するときのデフォルト設定は、[デザインダイアログ](#design-dialog)で定義することができます。

メールコンテナコンポーネントをページに追加したら、コンテンツ作成者は、追加のコンポーネントをページにドラッグ＆ドロップすることができます。

## バージョンと互換性 {#version-and-compatibility}

このドキュメントでは、メールコンテナコンポーネントの現在のバージョン（2022年10月にメールコアコンポーネントのリリース X で導入された v1）について説明します。

コンポーネントのすべてのサポート対象バージョン、コンポーネントの各バージョンと互換性のある AEM バージョン、以前のバージョンのドキュメントへのリンクを次の表に示します。

| コンポーネントのバージョン | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|
| v1 | 互換性あり | - | - |

メールコアコンポーネントのバージョンとリリースについて詳しくは、[メールコアコンポーネントのバージョン](/help/email/versions.md)を参照してください。

## 技術的詳細 {#technical-details}

コンテナコンポーネントに関する最新の技術ドキュメントについては、[GitHub を参照](https://adobe.com/go/aem_cmp_tech_email_container_v1)してください。

コアコンポーネントの開発について詳しくは、[コアコンポーネント開発者向けドキュメント](/help/developing/overview.md)を参照してください。

## 設定ダイアログ {#configure-dialog}

設定ダイアログでは、コンテナ項目とその動作およびコンテンツ内での表示をコンテンツ作成者が定義できます。

![メールコンテナコンポーネントの編集ダイアログ](/help/email/assets/email-container-configure.png)

* **レイアウト** - このオプションでは、メールコンテナコンポーネントの動作またはレイアウト動作を定義します。
   * **full-width**
   * **half|half**
   * **one-third|two-third**
   * **two-third|one-third**
   * **third|third|third**
* **背景色** - [設定に応じて](#container-settings-tab)、自由形式の RGB 値として定義するか、カラーピッカーを使用して定義します。
* **背景画像** - [設定に応じて](#container-settings-tab)、コンテナの背景画像を定義します。
* **ID** - このオプションを使用すると、HTML 内のコンポーネントの一意の ID を制御することができます。
   * これを空白のままにした場合、一意の ID が自動的に生成されます。生成された ID は結果のページを調べることで確認できます。
   * ID を指定した場合、作者はその ID が一意であることを確認する必要があります。
   * ID を変更すると、CSS に影響を与える可能性があります。

### 「スタイル」タブ {#styles-tab-edit}

メールコンテナコンポーネントでは、AEM [スタイルシステム](/help/get-started/authoring.md#component-styling)をサポートしています。

ドロップダウンを使用して、コンポーネントに適用するスタイルを選択します。編集ダイアログでの選択項目は、コンポーネントツールバーから選択した項目と同じ効果があります。

このタブを使用するには、[デザインダイアログ](#design-dialog)でこのコンポーネントのスタイルを設定する必要があります。

## デザインダイアログ {#design-dialog}

デザインダイアログでは、メールコンテナコンポーネントの使用時にコンテンツ作成者に提供されるオプションを、テンプレート作成者が定義できます。

### 「許可されたコンポーネント」タブ {#allowed-components-tab}

「**許可されたコンポーネント**」タブでは、メールコンテナコンポーネントにアイテムとして追加できるコンポーネントを、コンテンツ作成者が定義できます。

**「許可されたコンポーネント」**&#x200B;タブは、[テンプレートエディターでレイアウトコンテナのポリシーやプロパティを定義する](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=ja)際の同名のタブと同じように機能します。

### 「デフォルトコンポーネント」タブ {#default-components-tab}

「**デフォルトコンポーネント**」タブは、[ページテンプレートでのデフォルトコンポーネントの定義方法](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=ja)と同様に、特定のアセットタイプがコンテナにドロップされたときにコンテナに追加されるコンポーネントを定義するために使用されます。

### 「コンテナ設定」タブ {#container-settings-tab}

この「**コンテナ設定** 」タブでは、背景画像または背景色を作成者が定義できるかどうかを定義します。

![メールコンテナコンポーネントのデザインダイアログの「コンテナ設定」タブ](/help/email/assets/email-container-design-container-settings.png)

* **背景画像**
   * **背景画像を有効にする** - コンテナの背景画像をコンテンツ作成者が定義できるようにします。
* **背景色**
   * **背景色を有効にする** - コンテナの背景色をコンテンツ作成者が定義できるようにします。
   * **スウォッチのみ** - コンテナの背景色に事前に定義されているカラースウォッチからのみコンテンツ作成者が選択できるようにします。
      * 「**背景色を有効にする**」を選択した場合にのみ使用可能です。
* **許可されるスウォッチ** - コンテンツ作成者がコンテナの背景色を選択できるように事前定義済みカラーを定義します。
   * 「**追加**」ボタンを使用して、事前定義済みのカラースウォッチを追加します。追加が完了すると、以下の列を含むエントリがリストに追加されます。
   * **値** - RGB 値を使用して手動で色を定義します。
      * カラーピッカーをタップまたはクリックすると、個々の RGB 値を調整するか 16 進数値を定義して、色を選択しやすくなります。
   * **削除** - タップまたはクリックすると、スウォッチを削除できます。
   * **並べ替え** - タップまたはクリックしてドラッグし、スウォッチを並べ替えます。

### 「スタイル」タブ {#styles-tab}

メールコンテナコンポーネントでは、AEM [スタイルシステム](/help/get-started/authoring.md#component-styling)をサポートしています。
