---
title: アダプティブフォームのコアコンポーネント - フォームコンテナ
description: Web ページへのアダプティブフォームの追加。
role: Architect, Developer, Admin, User
exl-id: 03c4cf7c-51d6-4850-a566-1c0514d52dab
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: ht
source-wordcount: '1524'
ht-degree: 100%

---


# フォームコンテナ {#form-container-adaptive-forms-core-component}

<span class="preview">この記事では、プレリリース機能である&#x200B;**下書き**<!--and **Hamburger Menu Support** -->機能について説明します。プレリリース機能には、[プレリリースチャネル](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html?lang=ja#new-features)を通じてのみアクセスできます。</span>

フォームを使用して価値のある情報を提供すると、web サイトの訪問者のエンゲージメントとユーザー満足度を高めることができます。Adobe Experience Manager（AEM）Sites のアダプティブフォームコンテナを使用すると、web サイトの所有者は、ページに簡単にフォームを追加できます。 これにより、訪問者がフィードバックの提供や問い合わせなどのアクションを合理化することで、web サイトの訪問者と web サイトの所有者または組織とのコミュニケーションが容易になります

{{traditional-aem}}

## 使用方法 {#reasons-to-use-forms-container}

フォームを web サイトに追加したほうが良い理由はいくつかあります。
- **データ収集**：フォームを使用して、市場調査やユーザー行動分析など、様々な目的で web サイトの訪問者からデータを収集できます。

- **リードジェネレーション**：フォームを使用して、見込み客から名前やメールアドレスなどの情報を収集し、販売やマーケティング活動のリードを生成できます。

- **e コマース**：フォームをオンラインショッピングに使用すると、顧客は web サイトを通じて注文や支払いを行えるようになります。

- **問い合わせ**：問い合わせフォームを使用すると、web サイトの訪問者は web サイトの所有者や組織に簡単に連絡できます。

- **調査および投票**：フォームは、調査や調査を通じて web サイトの訪問者からフィードバックや意見を収集するのに使用できます。

- **イベント登録**：フォームをイベント登録に使用すると、web サイトの訪問者はイベントや web セミナーに登録できます。

- **購読**：フォームを web サイトの購読に使用すると、訪問者がニュースレターやその他の標準のコミュニケーションに新規登録できます。

- **ユーザー認証**：フォームをユーザー認証に使用すると、web サイトの訪問者がアカウントを作成し、ログインして制限されたコンテンツや機能にアクセスできるようになります。

- **コンバージョン率の向上**：適切に設計されたフォームがあると、製品の購入やサービスへの新規登録など、ユーザーが簡単に目的のアクションを完了できるようにすることで、コンバージョン率を高めることができます。

## バージョンと互換性 {#version-and-compatibility}

アダプティブフォームのアコーディオンコアコンポーネントは、Cloud Service 向けコアコンポーネント2.0.4 および AEM 6.5.16.0 Forms 向けのコアコンポーネント 1.1.12 の一部として 2023年2月にリリースされました。 次の表に、サポートされているすべてのバージョン、AEM の互換性、対応するドキュメントへのリンクを示します。

| コンポーネントのバージョン | AEM as a Cloud Service | AEM 6.5.16.0 Forms 以降 |
|---|---|---|
| v1 | <br>[リリース 2.0.4](/help/adaptive-forms/version.md) 以降と互換性あり | <br>[リリース 1.1.12](/help/adaptive-forms/version.md) 以降、2.0.0 未満と互換性があります。 |

コアコンポーネントのバージョンとリリースについて詳しくは、[コアコンポーネントのバージョン](/help/adaptive-forms/version.md)ドキュメントをご覧ください。
<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion_jp). -->

## 技術的詳細 {#technical-details}

アダプティブフォームコンテナのコアコンポーネントの最新情報については、[GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/container/v1/container)のテクニカルドキュメントをご覧ください。 コアコンポーネントの開発について詳しくは、[コアコンポーネント開発者向けドキュメント](/help/developing/overview.md)をご覧ください。

## 設定ダイアログ {#configure-dialog}

設定ダイアログを使用すると、フォームコンテナのエクスペリエンスを訪問者に合わせて簡単にカスタマイズできます。 また、フォームコンテナオプションを簡単に定義でき、シームレスなユーザーエクスペリエンスを実現できます。

### 「基本」タブ {#basic-tab}

![「基本」タブ](/help/adaptive-forms/assets/formcontainer_basictab1.png)

- **タイトル** - タイトルを使用すると、フォーム内のコンポーネントを簡単に識別できます。デフォルトでは、コンポーネントの上にタイトルが表示されます。 タイトルを追加しない場合、コンポーネントの名前がタイトルテキストの代わりに表示されます。

- **事前入力サービス** - このオプションを使用すると、ユーザーはアダプティブフォームのレンダリング時にデータを取得するための事前入力サービスを選択できます。 詳しくは、[事前入力サービスの作成および設定方法](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/prepopulate-adaptive-form-fields.html?lang=ja#aem-forms-custom-prefill-service)を参照してください

- **役割**：役割は、スクリーンリーダーなどの支援テクノロジーに対する HTML 要素の目的を指定するのに使用される、HTML 属性です。役割の属性は、要素に追加のコンテキストと意味論的意味を提供するために使用されます。これにより、スクリーンリーダーがコンテンツを解釈して読み上げやすくなります。 例えば AEM Formsでは、フォームフィールドのラベルが「label」という役割を持ち、入力フィールドが「textbox」という役割を持つ場合があります。 これにより、スクリーンリーダーはラベルと入力フィールドの関係を理解し、ユーザーに対して正しく通知できるようになります。

- **クライアントライブラリカテゴリ**：ユーザーはアダプティブフォームごとにカスタム JavaScript ライブラリを設定できます。jQuery および underscore.js サードパーティライブラリに依存する再利用可能な関数のみを、ライブラリに保持することをお勧めします。
**複雑な検証ルール**&#x200B;がある場合、正確な検証スクリプトがカスタム関数の中に存在し、ユーザーがこれらのカスタム関数をフィールド検証式から呼び出すことがあります。 このカスタム関数ライブラリをサーバーサイド検証中に認識させ、利用可能にするために、フォームユーザーは、「アダプティブフォームコンテナ」プロパティの「**[!UICONTROL 基本]**」タブで、AEM クライアントライブラリの名前を設定できます。
ユーザーは、アダプティブフォームごとにカスタム JavaScript ライブラリを設定できます。 ライブラリには、jQuery および underscore.js サードパーティライブラリに依存する、再利用可能な関数のみを保持します。

<!--
- **Enable the hamburger menu for mobile view** - Select the checkbox to integrate a hamburger menu into your form for mobile view. Represented by three horizontal lines stacked vertically, this menu provides a clear and uncluttered display for panels on smaller devices, especially on mobile devices. For more information about the hamburger menu, refer to the [Learn more about the hamburger menu](#learn-more-about-the-hamburger-menu) section. -->


### 「データモデル」タブ {#data-model-tab}

![「送信」タブ](/help/adaptive-forms/assets/formcontainer_fdmtab.png)

フォームデータモデルを使用してフォームをデータソースに接続し、ユーザーのアクションに基づいてデータを送受信することができます。 また、フォームを JSON スキーマに接続して、送信されたデータを事前定義済みの形式で受信することもできます。 必要に応じて、フォームを JSON スキーマまたはフォームデータモデルに接続します。
- JSON スキーマの作成と環境へのアップロード
- フォームデータモデルを作成

### ドラフト

![「送信」タブ](/help/adaptive-forms/assets/formcontainer_autosavetab.png)

- **下書きを自動的に保存**：「**下書きを自動的に保存**」チェックボックスをオンにして、フォームを下書きとして保存できるようにします。
- **環境設定を保存**：「**環境設定を保存**」を「**定期的に下書きを保存**」に設定して、特定の時間間隔でフォームを自動保存します。
  **保存間隔の頻度（秒）**：時間間隔（秒）を指定して、定義された間隔でフォームの自動保存をトリガーする期間を設定します。

### 「送信」タブ {#submission-tab}

ユーザーは、アダプティブフォームの送信に対して様々なアクションを設定できます。

- **リダイレクト URL／パス** - このオプションを使用すると、ユーザーはアダプティブフォームの送信後にユーザーがリダイレクトされる各フォームのページを設定できます。 詳しくは、[リダイレクトページの設定方法](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-redirect-page.html?lang=ja)を参照してください。

![「送信」タブ](/help/adaptive-forms/assets/formcontainer_submissiontab.png)

- **メッセージを表示** - このオプションを使用すると、ユーザーはアダプティブフォームが正常に送信されたときに表示されるメッセージを追加できます。 定義済みのテキストはダイアログボックスに含まれ、ユーザーが変更できます。 「メッセージを表示」ダイアログでは、追加したテキストを書式設定できるリッチテキスト形式のツールがサポートされています。

![「メッセージを表示」タブ](/help/adaptive-forms/assets/formconatiner_showmessage.png)

- **送信アクション** - 送信アクションは、ユーザーがアダプティブフォームの「送信」ボタンをクリックしたときにトリガーされます。 ユーザーは、すぐに使用できるよう用意されているドロップダウンリストから「送信アクション」を選択することができます。 詳しくは、[「送信」タブでの送信アクションの設定](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html?lang=ja#supporting-custom-functions-in-validation-expressions-br)を参照してください。

## デザインダイアログ {#design-dialog}

デザインダイアログでは、フォームコンテナコンポーネントの CSS スタイルを定義および管理できます。

### 「許可されたコンポーネント」タブ {#allowed-components-tab}

![デザインダイアログの「許可されたコンポーネント」タブ](/help/adaptive-forms/assets/formcontainer-allowedcomponents.png)

「**許可されたコンポーネント**」タブでは、テンプレートエディターで、アダプティブフォームエディターのコンポーネント内のパネルに、項目として追加できるコンポーネントを設定できます。

### デフォルトの「コンポーネント」タブ {#default-components-tab}

![デザインダイアログのデフォルトの「コンポーネント」タブ](/help/adaptive-forms/assets/formcontainer-defaultcomponents.png)

「**デフォルトのコンポーネント**」タブでは、テンプレートエディターで、デフォルトで表示されるコンポーネントを、アダプティブフォームエディター内のフォームコンテナコンポーネント内の項目として指定できます。

### 「レスポンシブ設定」タブ {#responsive-tab}

![デザインダイアログの「レスポンシブ設定」タブ](/help/adaptive-forms/assets/formcontainer-responsivestyle.png)

「**レスポンシブ設定**」タブでは、テンプレートエディターで、アダプティブフォームエディターのフォームコンテナコンポーネント内のグリッドの列数を指定できます。

### 「スタイル」タブ {#styles-tab}

アダプティブフォームのファイル添付コアコンポーネントは、AEM の[スタイルシステム](/help/get-started/authoring.md#component-styling)をサポートしています。

![デザインダイアログ](/help/adaptive-forms/assets/formcontainer-styletab.png)

- **デフォルトの CSS クラス**：アダプティブフォームのフォームコンテナコアコンポーネントにデフォルトの CSS クラスを指定できます。

- **許可されたスタイル**：スタイルを表す名前と CSS クラスを指定してスタイルを定義します。 例えば、「bold text」という名前のスタイルを作成し、CSS クラス「font-weight: bold」を指定できます。 アダプティブフォームエディターでアダプティブフォームにこれらのスタイルを使用または適用できます。 スタイルを適用するには、アダプティブフォームエディターでスタイルを適用するコンポーネントを選択し、「プロパティ」ダイアログに移動して「**スタイル**」ドロップダウンリストから希望のスタイルを選択します。 スタイルを更新または変更する必要がある場合は、デザインダイアログに戻り、「スタイル」タブでスタイルを更新して変更を保存します。

### 「カスタムプロパティ」タブ

![カスタムプロパティダイアログ](/help/adaptive-forms/assets/formcontainer-custompropertiestab.png)

カスタムプロパティを使用すると、フォームテンプレートを使用してカスタム属性（キーと値のペア）をアダプティブフォームのコアコンポーネントに関連付けることができます。 カスタムプロパティは、コンポーネントのヘッドレスレンディションのプロパティセクションに反映されます。 これにより、カスタム属性値に基づいて適応する動的なフォーム動作を作成できます。 例えば、開発者は、モバイル、デスクトップ、web プラットフォーム上にヘッドレスフォームコンポーネントの様々なレンディションをデザインできるので、幅広いデバイスでのユーザーエクスペリエンスが大幅に向上します。

- **グループ名**：カスタムプロパティグループを識別する名前を指定できます。 複数のカスタムプロパティグループを追加、削除または並べ替えることができます。 カスタムプロパティグループを追加すると、次のオプションが表示されます。

   - **キーと値のペア**：各カスタムプロパティグループの「**追加**」ボタンをクリックすると、複数のカスタムプロパティ名とカスタムプロパティ値を追加できます。

   - **削除**：タップまたはクリックすると、カスタムプロパティ名とカスタムプロパティ値を削除できます。

   - **並べ替え**：タップまたはクリックしてドラッグすると、カスタムプロパティ名とカスタムプロパティ値の順序を並べ替えることができます。

<!--
## Learn more about the hamburger menu

A hamburger menu, often referred to as a mobile menu or navigation drawer, is a popular design element in mobile user interfaces. It features three horizontal lines stacked vertically, resembling a hamburger. The design efficiently conserves screen space by hiding secondary navigation options until they are needed, especially on smaller devices such as mobile. AEM forms can be efficiently organized within the hamburger menu, enabling users to access various panels within a form without overwhelming the main interface.

Consider a scenario, where a financial institution offers an online loan application form that requires users to provide detailed information across several panels, such as personal details, financial information, loan preferences, and supporting documents. The form includes multiple panels and options that can clutter the interface, especially on mobile devices. Users need an organized way to navigate through these panels without feeling overwhelmed. The hamburger menu is implemented to enhance the user experience on mobile devices.

### Components of hamburger menu

![Hamburger Menu](/help/adaptive-forms/assets/hamburger-menu.png){width=50%, align=center}

**A. Hamburger menu**: The hamburger menu features a navigation panel that slides out or drops down when the hamburger icon is clicked or tapped. The menu displays the panel headings, and selecting a panel shifts the focus to that panel. It allows users to easily navigate between different panels.

![Hamburger Menu](/help/adaptive-forms/assets/hamburger-menu-icon.png){width=50%}

**B. Breadcrumb**: Breadcrumbs indicate the user’s current location within the form. They offer a hierarchical trail that shows the user’s navigation path and helps them understand their position in the form.

**C. Active panel**: The active panel refers to the section or part of the form that is currently being displayed. When a user selects an option from the hamburger menu, the corresponding panel becomes the active panel, showing the relevant fields and information for that section.

### Points to consider while working with the hamburger menu

- The hamburger menu displays only the names of the panels. Here are different scenarios illustrating how the panel name appears in the navigation pane of the hamburger menu based on the configuration properties of the panel:  
  
  - If you set the properties of the panel to hidden, the panel's name does not appear in the navigation pane of the hamburger menu. For example, if you configure the properties of the `Financial Information` panel as `hidden`, the panel name does not appear in the navigation pane of the hamburger menu.
    
    ![Hidden panel](/help/adaptive-forms/assets/hidden-panel.png){width=50%}

  - If you set the properties of the panel to `disabled`, its name appears in the navigation pane of the hamburger menu, but you cannot select or edit it. For example, if you configure the properties of the `Financial Information` panel as `disabled`, the panel name appears in the navigation pane, but it cannot be selected or edited. 
     
    ![Disabled panel](/help/adaptive-forms/assets/disabled-panel.png){width=50%}

  - If you hide the  title of the panel, it does not appear in the navigation pane of the hamburger menu. A blank space shows up instead, but you can navigate to the fields of the panel by clicking on that space. For example, if you hide the title of the `Financial Information` panel, the blank space appears in its place in the navigation pane of the hamburger menu. You can navigate to the fields of the panel by clicking on the blank space.
    
    ![Hidden title panel](/help/adaptive-forms/assets/hidden-title-panel.png){width=50%}

- By default, the navigation pane in the breadcrumb component supports up to three levels of navigation. However, with the custom component, you can configure the navigation hierarchy to accommodate as many levels as needed.
- When using the hamburger menu, the user can navigate between panels using arrows. However, once a panel is selected, the menu automatically closes, and focus shifts to the fields within the chosen panel.

### Advantages to use hamburger menu

- **Space efficiency**: By hiding form navigation options until needed, the hamburger menu maximizes screen space, which is especially beneficial on smaller devices.

- **Clutter reduction**: It minimizes visual clutter by consolidating various form navigation links into a single, collapsible menu.

- **Improved focus**: With fewer visible navigation elements, users can concentrate on the main content of the form without being distracted by secondary options.

- **Simplified design**: It creates a more streamlined user interface, resulting in a cleaner and more organized form layout.

- **Enhanced mobile experience**: On mobile devices, where screen space is limited, the hamburger menu offers an efficient way to access all form navigation options without overwhelming the user.

### How to enable hamburger menu for your form?

To enable hamburger menu for form, perform the following steps:

1. Open form in an edit mode.
1. Open the Content browser, and select the **[!UICONTROL Guide Container]** component of your Adaptive Form. 
1. Click the Guide Container properties ![Guide properties](/help/adaptive-forms/assets/configure_icon.png) icon. The Adaptive Form Container dialog box opens. 
1. Click the  **[!UICONTROL Basic]** tab. 
1. Select the **[!UICONTROL Add hamburger menu support]** checkbox.
1. Click **[!UICONTROL Done]**.

![Basic tab](/help/adaptive-forms/assets/formcontainer_basictab.png)
-->

## 関連記事 {#related-articles}

{{more-like-this}}

## 関連トピック {#see-also}

{{see-also}}