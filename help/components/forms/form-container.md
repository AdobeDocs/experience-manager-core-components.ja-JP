---
title: フォームコンテナコンポーネント
description: コアコンポーネントのフォームコンテナコンポーネントを使用すれば、シンプルな送信フォームを作成できます。
role: Architect, Developer, Admin, User
exl-id: 552f9dd5-6a3a-42d9-9969-e62a1f36e811
source-git-commit: 6fbc781db555bc6abaed1d122a9a8756e3d53222
workflow-type: ht
source-wordcount: '914'
ht-degree: 100%

---

# フォームコンテナコンポーネント {#form-container-component}

コアコンポーネントのフォームコンテナコンポーネントを使用すれば、シンプルな送信フォームを作成できます。

## 使用方法 {#usage}

フォームコンテナコンポーネントは、シンプルな WCM フォームをサポートしており、フォームコンポーネントの追加が可能なネスト構造を使用しているので、シンプルな情報送信フォームおよび機能を作成できます。

[設定ダイアログ](#configure-dialog)を使用すると、フォーム送信でトリガーされるアクション、送信を処理する URL、ワークフローをトリガーするかどうかをコンテンツ編集者が定義できます。テンプレート作成者は、[デザインダイアログ](#design-dialog)を使用して、[テンプレートエディターにおける標準レイアウトコンテナ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=ja)のデザインダイアログと同様に、許可されるコンポーネントとそのマッピングを定義できます。

>[!NOTE]
>
>コアコンポーネントのフォームコンテナコンポーネントでは、コアコンポーネントのフォームコンポーネント（ボタン、テキスト、非表示など）のみ使用できます。[基盤コンポーネント](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/siteandpage/default-components-foundation.html?lang=ja)のフォームコンポーネントをコアコンポーネントのフォームコンテナ内で使用すること（およびその逆の使用）はサポートされていません。

## バージョンと互換性 {#version-and-compatibility}

このドキュメントでは、フォームコンテナコンポーネントの現在のバージョン（2018年1月にコアコンポーネントのリリース 2.0.0 で導入された v2）について説明します。

コンポーネントのすべてのサポート対象バージョン、コンポーネントの各バージョンと互換性のある AEM バージョン、以前のバージョンのドキュメントへのリンクを次の表に示します。

| コンポーネントのバージョン | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| v2 | <br>[リリース 2.17.4](/help/versions.md) 以前と互換性あり | 互換性あり | 互換性あり | 互換性あり |
| [v1](/help/components/v1/form-container-v1.md) | 互換性あり | 互換性あり | - | 互換性あり |

コアコンポーネントのバージョンとリリースについて詳しくは、[コアコンポーネントのバージョン](/help/versions.md)を参照してください。

## コンポーネント出力のサンプル {#sample-component-output}

フォームコンテナコンポーネントを体験し、その設定オプションや HTML および JSON 出力の例を確認するには、[コンポーネントライブラリ](https://adobe.com/go/aem_cmp_library_form_container_jp)を参照してください。

## 技術的詳細 {#technical-details}

フォームコンテナコンポーネントに関する最新の技術ドキュメントについては、[GitHub](https://adobe.com/go/aem_cmp_tech_form_container_v2_jp) を参照してください。

コアコンポーネントの開発について詳しくは、[コアコンポーネント開発者向けドキュメント](/help/developing/overview.md)を参照してください。

## 設定ダイアログ {#configure-dialog}

設定ダイアログでは、コンポーネントの送信時に実行されるアクションをコンテンツ作成者が定義できます。

選択した&#x200B;**アクションタイプ**&#x200B;に応じて、コンテナ内で使用可能なオプションが変わります。使用可能なアクションタイプは次のとおりです。

* [Post Form Data](#post-data)
* [Mail](#mail)
* [コンテンツを格納](#store-content)

タイプに関係なく、各アクションに適用される[一般的な設定](#general-settings)があります。

### Post Form Data {#post-data}

フォームが送信されると、「Post Form Data」アクションタイプにより、送信されたデータを JSON 形式でサードパーティに渡して処理させます。

![フォームコンテナコンポーネントの編集ダイアログの「Post Form Data」オプション](/help/assets/form-container-edit-post.png)

* **エンドポイント** - データを処理する HTTPS サービスの完全修飾名
* **エラーメッセージ** - 送信が成功しなかった場合に表示するメッセージ

>[!TIP]
>転送されたフォームデータを処理するためにシステム管理者が調整できる追加のタイムアウトオプションが用意されています。[詳しくは、GitHub の技術ドキュメントを参照してください。](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/actions/rpc)

### Mail {#mail}

アクションタイプが「Mail」の場合、フォームが送信されると、指定した受信者にメールが送信されます。

![フォームコンテナコンポーネントの編集ダイアログのメールオプション](/help/assets/form-container-edit-mail.png)

* **件名** - フォーム送信時に送信されるメールの件名
* **宛先** - フォーム送信時に送信されるメールの差出人のメールアドレス
* **宛先-** - フォーム送信時にメールを受信する受信者のアドレス
   * アドレスを追加するには、「**追加**」ボタンをタップまたはクリックします
   * メールアドレスを削除するには、「**削除**」ボタンをタップまたはクリックします
* **CC** - フォーム送信時に送信されるメールのカーボンコピーを受信する受信者のアドレス
   * アドレスを追加するには、「**追加**」ボタンをタップまたはクリックします
   * メールアドレスを削除するには、「**削除**」ボタンをタップまたはクリックします

### コンテンツを格納 {#store-content}

フォームが送信されると、フォームのコンテンツは、指定されたリポジトリの場所に保存されます。

![フォームコンテナの編集ダイアログのコンテンツ保存オプション](/help/assets/form-container-edit-store.png)

* **コンテンツのパス** - 送信されたコンテンツが格納されるコンテンツリポジトリのパス
* **データを表示** - タップまたはクリックすると、保存された送信済みデータが JSON 形式で表示されます
* **ワークフローを開始** - フォーム送信時に保存されたコンテンツをペイロードとしてワークフローを開始するように設定します

>[!NOTE]
>
>ユーザーデータを管理しやすくしたり、問題点を分離できるようにするために、ユーザー生成コンテンツをリポジトリ内に格納することは、一般的には推奨されません。
>
>代わりに、[Post Form Data](#post-data) アクションタイプを使用して、ユーザーコンテンツを専用のサービスプロバイダーに渡します。

### 一般設定 {#general-settings}

ありがとうページは、選択したアクションタイプに関係なくいつでも定義できます。

![フォームコンテナコンポーネントの編集ダイアログの一般オプション](/help/assets/form-container-edit-general.png)

* **ありがとうページ** - フォーム送信の完了後、ユーザーは指定したページにリダイレクトされます。
   * 選択ダイアログを使用して、AEM 内のリソースを選択します。
   * ありがとうページが AEM にない場合は、絶対 URL を指定します。絶対 URL 以外の URL は、AEM からの相対 URL と解釈されます。
   * 空白のままにすると、送信後にフォームが再度表示されます。
* **ID** - このオプションを使用すると、HTML 内および[データレイヤー](/help/developing/data-layer/overview.md)内のコンポーネントの一意の識別子を制御できます。
   * 空白のままにした場合、一意の ID が自動的に生成されます。生成された ID は結果のページを調べることで確認できます。
   * ID を指定した場合、作者はその ID が一意であることを確認する必要があります。
   * ID を変更すると、CSS、JS、およびデータレイヤーのトラッキングに影響を与える可能性があります。

## デザインダイアログ {#design-dialog}

テンプレート作成者は、デザインダイアログを使用して、[テンプレートエディターにおける標準レイアウトコンテナ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=ja)のデザインダイアログと同様に、許可されるコンポーネントとそのコンテナマッピングを定義できます。

### 「スタイル」タブ {#styles-tab}

フォームコンテナコンポーネントは、AEM [スタイルシステム](/help/get-started/authoring.md#component-styling)をサポートしています。
