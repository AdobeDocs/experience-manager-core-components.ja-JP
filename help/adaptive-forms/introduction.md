---
title: AEM アダプティブフォームのコアコンポーネントの概要
description: アダプティブフォームのコアコンポーネントの柔軟性を利用して魅力的な登録フォームを作成し、Adobe Experience Manager を使って提供します。
role: Architect, Developer, Admin, User
source-git-commit: e1ee09854a40c960f8a907149240b755c95fe176
workflow-type: tm+mt
source-wordcount: '2229'
ht-degree: 99%

---

# アダプティブフォームのコアコンポーネント  {#adaptive-forms-core-components-introduction}

Adobe Experience Manager のアダプティブフォームのコアコンポーネントを使用すると、魅力的な登録エクスペリエンスを実現できます。

## コアコンポーネント {#overview}

Adobe Experience Manager（AEM）のコンポーネントとは、ページやフォームの作成に使用される構築ブロックを意味します。 作成者がコンテンツを作成および管理するためのシンプルで強力な方法が提供されると同時に、開発者はカスタムコンポーネントの作成に必要な柔軟性と拡張性を活用できます。 これらは、web サイトやフォームの開発時間を短縮し、メンテナンスコストを削減するように設計されており、特定のニーズに合わせて柔軟かつ容易にカスタマイズできます。

また、コアコンポーネントはレスポンシブに設計されており、デスクトップ、タブレット、スマートフォンなど様々なデバイスに対応します。 また、web コンテンツを作成するための堅牢で信頼性の高いソリューションであり、最新の web 標準規格とベストプラクティスにも準拠しています。

全体的に、コアコンポーネントは AEM で web コンテンツを作成および管理するための不可欠なツールであり、開発時間と保守コストの削減に役立つ一方で、web サイト訪問者に優れたユーザーエクスペリエンスを提供する強力で柔軟なソリューションです。

## アダプティブフォームのコアコンポーネント

アダプティブフォームのコアコンポーネントとは、Adobe Experience Manager WCM コアコンポーネントの基盤上に構築され、BEM に準拠した、オープンソースの 29 個のコンポーネントのセットです。これらは、ユーザーのデバイス、ブラウザー、画面サイズに適合するアダプティブフォームの作成に使用するように特別に設計されています。

これらのコンポーネントは、テキストフィールド、チェックボックス、ドロップダウンメニューなど、様々なフォームフィールドオプションを提供することで、例外的なデータ取得および登録エクスペリエンスを作成するために使用できます。 また、検証、条件付きロジック、レスポンシブデザインなどの機能も含まれ、ユーザーフレンドリーで使いやすいフォームを作成できます。

さらに、これらのコンポーネントはオープンソースなので、開発者は組織の特定のニーズに合わせて簡単にカスタマイズおよび拡張できます。 また、これらのコンポーネントは、拡張性と保守性が確保される BEM 手法に基づいて構築されています。

![アダプティブフォームの画像](assets/sample-adaptive-form.png)

## 機能 {#features}

|  |  |
|---|---|
| 本番で使用可能 | アダプティブフォームのコアコンポーネントは、24 個の堅牢な WCM コンポーネントです。 |
| クラウド対応 | [AEM Forms as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/home.html?lang=ja) で使用可能です。 |
| 用途が広い | コンポーネントは、ほぼすべてのレイアウトの作成にフォーム作成者が使用できる汎用的な概念を表します。 |
| 設定可能 | テンプレートレベルの[コンテンツポリシー](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/full-stack/components-templates/templates.html?lang=ja#content-policies)で、許可される機能と許可されない機能を定義します。 |
| 高いアクセシビリティ | ARIA ラベル、キーボードナビゲーションおよび支援テクノロジー（スクリーンリーダーなど）用のテキストを提供します。 |
| テーマ設定可能 | コンポーネントは[スタイルシステム](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/style-system.html?lang=ja)を実装し、マークアップは [BEM CSS の命名規則](https://getbem.com/)に従っています。 |
| カスタマイズ可能 | いくつかのパターンが用意されているので、HTML の調整から高度な機能の再利用まで、カスタマイズが容易になっています。 |
| バージョン管理 | [バージョン管理ポリシー](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-policies)が設定されているので、影響を受ける可能性のある改善の際にも、コアコンポーネントが原因でサイトが機能しなくなることはありません。 |
| オープンソース | 何か問題がある場合は、改善案を寄稿できます。 |

<!-- comply with [WCAG 2.1 standard](https://www.w3.org/TR/WCAG21/), -->


## メリット {#benefits}

データキャプチャのエクスペリエンスは、リードジェネレーションと登録において重要です。アダプティブフォームのコアコンポーネントは、データキャプチャ用に最適化されたフォームを作成するための強力なソリューションです。 基盤コンポーネントを介してこれらのエクスペリエンスを作成するために、コアコンポーネントを使用する理由には次のようなものがあります。

* **[GitHub で利用可能](https://github.com/adobe/aem-core-forms-components)**：AEM アダプティブフォームのコアコンポーネントはオープンソースであり、GitHub で利用できます。包括的なドキュメントも用意されています。これにより、開発者はコンポーネントとその動作を理解し、開発に貢献することが容易になります。 また、[aemcomponents.dev](https://www.aemcomponents.dev/) web サイトは、開発者がコンポーネントの動作を確認し、詳細なドキュメントにアクセスできる貴重なリソースです。

* **[BEM モデルを使用したスタイル設定](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-themes-in-core-components)**：コアコンポーネントは、BEM（ブロック要素修飾子）モデルに従ってスタイル設定されます。BEM は、CSS を整理するための、広く使用されている確立された手法です。これにより、開発者はスタイルの編成方法と、特定のニーズに合わせてスタイルを変更する方法を理解しやすくなります。

* **サードパーティライブラリへの依存なし**:コアコンポーネントの利点の 1 つは、JQuery や Underscore など、サードパーティの JavaScript ライブラリに依存しない点です。 これにより、コンポーネントが高速で軽量になり、既存の AEM 実装に統合しやすくなります。

* **パフォーマンスとアクセシビリティへの焦点**：コアコンポーネントは、パフォーマンスとアクセシビリティを考慮して構築されており、それは Google Lighthouse のスコアと web のバイタルスコアに大きく反映されています。 これにより、開発者はアクセシブルでパフォーマンスの高い web ページを容易に作成できます。これは、現在のデジタル環境でますます重要になっています。

* **Sites 30 のテンプレートおよびテーマのフォームコンポーネント**：コアコンポーネントは、Sites 30 のテンプレートおよびテーマでフォームコンポーネントをサポートしており、開発者は AEM 内でフォームを簡単に作成およびカスタマイズできます。

* **[スタイル設定が容易](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-themes-in-core-components)**：コアコンポーネントは、基盤コンポーネントとは異なり、スタイル設定が容易です。テーマの作成プロセスは Sites に似ていますが、同じテーマと CSS を親 Sites ページから継承できます。 さらに、スタイル設定に BEM モデルが採用されているため、容易にスタイルを理解して変更できます。

* **アクセシビリティ**：アダプティブフォームのコアコンポーネントは、障害のあるユーザー（スクリーンリーダーなどの支援テクノロジーを使用しているユーザーを含む）がフォームを確実に使用できるように、アクセシビリティに関する標準規格およびガイドラインをサポートしています。

* **[バージョン管理](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/add-comments-annotations-versioning-adaptive-form-core-components)**：コアコンポーネントベースのアダプティブフォームの複数のバージョンを作成および管理し、コメントを通じて共同作業でディスカッションを行い、特定のフォームコンポーネントに注釈を添付することで、フォーム作成全体のエクスペリエンスを向上させることができます。

## 使用可能なコンポーネント：コンポーネントタイプ別の分類

AEM Forms の現在のバージョンには、次のコアコンポーネント、[基盤コンポーネント](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/create-an-adaptive-form-on-forms-cs/introduction-forms-authoring#component-toolbar)および[フォームブロックコンポーネント（Edge Delivery Services）](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/edge-delivery/build-forms/forms-references/form-components)があります。

| コンポーネント | 基盤コンポーネント | コアコンポーネント | フォームブロックコンポーネント | 追加情報 |
|------------|:---------------------:|:---------------:|:---------------------:|-----------------------|
| Adobe Sign ブロック | ✔️ | | | [Adobe Sign 統合](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/forms/integrate/services/adobe-sign-integration-adaptive-forms#adobe-acrobat-sign-for-government)は、基盤コンポーネントでのみ使用できます。 |
| アコーディオン | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/accordion.md)</span> | | 基盤コンポーネントの場合は、[パネルコンポーネントのプロパティ](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-layout-of-an-adaptive-form/layout-capabilities-adaptive-forms#panel-layout)でアコーディオンレイアウトを設定できます。 |
| アダプティブフォームフラグメント | ✔️ | ✔️ | | 基盤コンポーネントの場合は、アセットブラウザーから[フラグメントを追加](https://experienceleague.adobe.com/ja/docs/experience-manager-65/content/forms/adaptive-forms-basic-authoring/adaptive-form-fragments#insert-a-fragment-in-an-adaptive-form)できます。 |
| アダプティブフォーム reCAPTCHA | ✔️ | ✔️ | ✔️ | 基盤コンポーネントの場合は、Captcha コンポーネントを使用して、[Google reCaptcha をフォームに追加](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/captcha-adaptive-forms#google-reCAPTCHA)します。 |
| ボタン | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/button.md)</span> | ✔️ | |
| CAPTCHA | ✔️ |  |  | 基盤コンポーネントの場合は、Captcha コンポーネントを使用して、[Google reCaptcha をフォームに追加](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/captcha-adaptive-forms#google-reCAPTCHA)します。 |
| グラフ | ✔️ | | | |
| チェックボックス | ✔️ | ✔️ | | |
| チェックボックスグループ | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/checkbox-group.md)</span> | ✔️ | 基盤コンポーネントの場合は、チェックボックスコンポーネントを使用して、複数のチェックボックスを追加します。 |
| データ入力フィールド | ✔️ | | | コアコンポーネントの場合は、[日付選択](/help/adaptive-forms/components/date-picker.md)コンポーネントを使用します。また、個別の[テキストボックス](/help/adaptive-forms/components/text-box.md)または[数値ボックス](/help/adaptive-forms/components/numeric-box.md)コンポーネントを追加して、日、月、年を取得することもできます。 |
| 日付選択 | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/date-picker.md)</span> | ✔️ | |
| ドロップダウンリスト | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/drop-down-list.md)</span> | ✔️ | |
| メール | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/email.md)</span> | ✔️ | |
| ファイル添付 | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/file-attachment.md)</span> | ✔️ | |
| ファイル添付リスト | ✔️ | | | |
| フッター | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/footer.md)</span> | ✔️ | |
| 脚注プレースホルダー | ✔️ | | | |
| フォームコンテナ | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/form-container.md)</span> | ✔️ | 基盤コンポーネントの場合は、[ルートパネルコンポーネント](https://experienceleague.adobe.com/ja/docs/experience-manager-learn/cloud-service/forms/create-first-af/configure-root-panel)を使用します。 |
| フォームタイトル | ✔️ | ✔️ | | 基盤コンポーネントの場合は、タイトルコンポーネントを使用します。 |
| hCaptcha | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/hcaptcha.md)</span> |  | |
| ヘッダー | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/header.md)</span> | ✔️ | |
| 水平タブ | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/horizontal-tabs.md)</span> | | 基盤コンポーネントの場合は、パネルコンポーネントのプロパティで[上部のタブ（水平タブ）レイアウト](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-layout-of-an-adaptive-form/layout-capabilities-adaptive-forms#panel-layout)を設定できます。 |
| 画像 | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/image.md)</span> | ✔️ | |
| 画像選択 | ✔️ | | | |
| 次へボタン | ✔️ | ✔️ | | 複数のパネル間を移動するには、「次へ」ボタンと「前へ」ボタンに[ウィザードコンポーネント](/help/adaptive-forms/components/wizard.md)を使用します。 |
| 数値ボックス | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/numeric-box.md)</span> | ✔️ | |
| 数値ステッパー | ✔️ | | | |
| パネル | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/panel.md)</span> | ✔️ | |
| パスワードボックス | ✔️ | | ✔️ | |
| 電話 | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/phone.md)</span> | ✔️ | |
| 前へボタン | ✔️ | | | 複数のパネル間を移動するには、「次へ」ボタンと「前へ」ボタンに[ウィザードコンポーネント](/help/adaptive-forms/components/wizard.md)を使用します。 |
| ラジオボタン | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/radio-button.md)</span> | | |
| ラジオボタングループ | | | ✔️ | |
| リセットボタン | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/reset-button.md)</span> | ✔️ | |
| 手書き署名 | ✔️ | | | |
| 区切り文字 | ✔️ | | | |
| 送信ボタン | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/submit-button.md)</span> | ✔️ | |
| 概要ステップ | ✔️ | | | |
| スイッチ | ✔️ | <span style="color:blue"> [✔️](/help/adaptive-forms/components/adaptive-form-switch.md) | | |
| テーブル | ✔️ | | | |
| 利用条件 | ✔️ | ✔️ | | |
| テキスト | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/text.md)</span> | ✔️ | |
| テキストボックス | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/text-box.md)</span> | ✔️ | |
| タイトル | ✔️ | | | コアコンポーネントの場合は、[フォームタイトル](/help/adaptive-forms/components/form-title.md)コンポーネントを使用します。 |
| Turnstile Captcha | ✔️ | | | [Turnstile Captcha](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/integrate-adaptive-forms-turnstile) は、基盤コンポーネントでのみ使用できます。 |
| 垂直タブ | ✔️ | ✔️ | | 基盤コンポーネントの場合は、パネルコンポーネントのプロパティにある[左側のタブ（垂直タブ）レイアウト](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-layout-of-an-adaptive-form/layout-capabilities-adaptive-forms#panel-layout)を設定できます。 |
| ウィザード | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/wizard.md)</span> | ✔️ | 基盤コンポーネントの場合は、パネルコンポーネントのプロパティで[ウィザードレイアウト](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-layout-of-an-adaptive-form/layout-capabilities-adaptive-forms#panel-layout)を設定できます。 |




>[!NOTE]
>
>
> * 上記のコンポーネントに加えて、フォームブロックはすべての有効な [HTML5 入力タイプ](https://developer.mozilla.org/ja-JP/docs/Web/HTML/Element/input#input_types)と[テキスト領域](https://developer.mozilla.org/ja-JP/docs/Web/HTML/Element/textarea)をコンポーネントとしてサポートします。
> * 上記以外のコンポーネントが必要ですか？公式アドレスから aem-forms-ea@adobe.com にメールを送信してリクエストしてください。


<!-- >
* [Accordion](/help/adaptive-forms/components/accordion.md)
* [Adaptive Form Fragment](/help/adaptive-forms/components/adaptive-form-fragment.md)
* [Adaptive Form Switch](/help/adaptive-forms/components/adaptive-form-switch.md)
* [Button](/help/adaptive-forms/components/button.md)
* [Check Box Group](/help/adaptive-forms/components/checkbox-group.md)
* [Date Picker](/help/adaptive-forms/components/date-picker.md)
* [Drop-down list](/help/adaptive-forms/components/drop-down-list.md)
* [Email](/help/adaptive-forms/components/email.md)
* [Form Container](/help/adaptive-forms/components/form-container.md)
* [File Attachment](/help/adaptive-forms/components/file-attachment.md)
* [Footer](/help/adaptive-forms/components/footer.md)
* [Header](/help/adaptive-forms/components/header.md)
* [Horizontal Tabs](/help/adaptive-forms/components/horizontal-tabs.md)
* [Image](/help/adaptive-forms/components/image.md)
* [Numeric Box](/help/adaptive-forms/components/numeric-box.md)
* [Panel](/help/adaptive-forms/components/panel.md)
* [Phone](/help/adaptive-forms/components/phone.md)
* [Radio Button](/help/adaptive-forms/components/radio-button.md)
* [Adaptive Form reCAPTCHA](/help/adaptive-forms/components/adaptive-form-recaptcha.md)
* [Reset Button](/help/adaptive-forms/components/reset-button.md)
* [Submit Button](/help/adaptive-forms/components/submit-button.md)
* [Text Box](/help/adaptive-forms/components/text-box.md)
* [Text](/help/adaptive-forms/components/text.md)
* [Form Title](/help/adaptive-forms/components/form-title.md)
* [Wizard](/help/adaptive-forms/components/wizard.md)

-->

## 使いやすいフォームエディター

コアコンポーネントベースのアダプティブフォームのエディターは、AEM Sites ページの作成に既に使用しているエディターに類似しています。次の機能を利用できます。


* **使い慣れた UI 要素と設定**：フォームコンポーネントのプロパティを設定する際、WCM コアコンポーネントで使用しているプロパティと同様のプロパティダイアログが表示されます。これにより、必要なオプションをより早く見つけることができます。WCM コアコンポーネントと同様に、フォームコンポーネントのプロパティダイアログはエディターの中央に表示されます。ダイアログには、基本オプションと詳細オプション、ヘルプテキスト、アクセシビリティ情報がわかりやすいタブ形式で表示され、容易にナビゲートできます。

* **[ルールエディター](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/rule-editor-core-components)**：コードを記述せずに、フォームにロジックと動的機能を追加できます。組み込みのルールエディターを使用して、次を実行できます。
   * ユーザーの選択に基づいてフィールドを表示または非表示にする
   * オブジェクトの有効／無効を切り替える
   * オブジェクトの値を設定する
   * 計算を実行する
   * オブジェクトのプロパティを設定する
   * データ入力を検証する
   * サービスを呼び出す（外部機能を呼び出す）
   * 組み込み関数（一般的なタスク用の定義済み関数）を使用する
   * カスタム関数（特定のニーズに合わせた独自のコード）を使用する
   * フィールドとパネルを検証する（データが要件を満たしていることを確認する）
   * オブジェクトの値を検証する
   * 関数を実行することにより、オブジェクトの値を計算する
   * フォームデータモデル（FDM）サービスを呼び出して操作を実行する
   * スタイルを動的に追加する（条件に基づいて外観を変更する）
   * その他のルール（チェーンアクションとロジック）を作成する
   * その他

  ルールエディターには、コードエディターがありません。[カスタム関数](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-and-use-custom-functions)を使用して、特定のニーズに合わせた独自のコードをルールエディターに追加できます。



* **フォームへの事前入力**：ユーザーがフォームを開いた際に、フォーム内の特定のフィールドに既存のデータを自動的に入力できます。これにより、既に利用可能な情報を手動で入力する必要がなくなり、ユーザーの時間と労力が節約されます。コアコンポーネントエディターでは、フォームデータモデルを使用してフォームフィールドにデータを入力する OOTB 事前入力サービスを利用できます。また、より複雑なシナリオ向けにカスタム事前入力サービスを作成することもできます。

* **[レコードのドキュメント（DoR）](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/generate-document-of-record-core-components)**：レコードのドキュメント（DoR）とは、フォームを通じて送信されたデータの正式かつ印刷可能な表現を指します。ユーザーが入力した情報の永続的なレコードとして機能し、送信されたデータのスナップショットをユーザーが使いやすい形式（通常は PDF ドキュメント）で利用できます。エディターを使用してカスタムテンプレートを簡単に設定したり、OOTB テンプレートを使用して DoR を生成したりできます。

* **[フォームデータモデル](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/forms/integrate/use-form-data-model/using-form-data-model)**：アダプティブフォームデータモデル（FDM）は、アダプティブフォームとデータソースの間のブリッジとして機能します。基本的に、フォームが収集して操作するデータの構造と編成を定義します。エディターを使用すると、フォームをフォームデータモデル（FDM）に簡単に接続できます。

* **[フォーム送信](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Adaptive%20Form%20Submit%20Action&amp;text=Adobe%20recommends%20using%20Core%20Components,to%20create%20standalone%20Adaptive%20Forms.&amp;text=A%20Submit%20Action%20lets%20you,button%20on%20an%20Adaptive%20Form)**：フォーム送信とは、ユーザーがフォームに必要事項を入力して送信するプロセスを指します。フォームの設定内で定義された一連のアクションがトリガーされ、最終的に送信されたデータが保存または処理されます。アダプティブフォームエディターには、フォーム送信を設定するための様々なオプションが用意されています。一般的な送信アクションの一部は次のとおりです。

   * [メールを送信](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Adaptive%20Form%20Submit%20Action&amp;text=Adobe%20recommends%20using%20Core%20Components,to%20create%20standalone%20Adaptive%20Forms.&amp;text=A%20Submit%20Action%20lets%20you,button%20on%20an%20Adaptive%20Form.)
   * [Power Automate フローを呼び出す](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/forms/integrate/services/forms-microsoft-power-automate-integration)
   * [SharePoint に送信](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-action-sharepoint)
   * [Workfront Fusion を起動](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Invoke%20a%20Workfront%20Fusion)
   * [フォームデータモデル（FDM）を使用して送信](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/forms/integrate/use-form-data-model/using-form-data-model)
   * [Azure Blob Storage に送信](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Submit%20to%20Azure%20Blob%20Storage)
   * [REST エンドポイントへの送信](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-action-restpoint)
   * [OneDrive に送信](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=to%20REST%20endpoint-,Submit%20to%20OneDrive,-Invoke%20an%20AEM)
   * [AEM ワークフローを起動](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Invoke%20an%20AEM%20Workflow)


* [Sites ページエディターでのアダプティブフォームのコアコンポーネント](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page)：AEM ページエディターおよび AEM エクスペリエンスフラグメントでアダプティブフォームのコアコンポーネントを有効にして使用すると、Sites ページの構築と共にデータキャプチャエクスペリエンスを直接作成できます。

  >[!VIDEO](https://video.tv.adobe.com/v/3419284?quality=12&learn=on)


<!-- 
* **Preview Forms**: You can use the editor to  simulates how the form would appear on various devices like desktops, tablets, and smartphones.
-->



## アダプティブフォームのコアコンポーネントの有効化

AEM Forms as a Cloud Service のアダプティブフォームのコアコンポーネントを有効にすると、AEM Forms Cloud Service インスタンスを使用して、複数のチャネルへのコアコンポーネントベースのアダプティブフォームとヘッドレスフォームの作成、公開、配信を開始できます。 アダプティブフォームのコアコンポーネントを有効にする手順について詳しくは、[AEM Forms as a Cloud Service およびローカル開発環境でアダプティブフォームのコアコンポーネントを有効にする](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/setup-configure-migrate/enable-adaptive-forms-core-components.html?lang=ja)を参照してください。

アダプティブフォームのコアコンポーネントには、以下の要件があります。

| AEM のバージョン | AEM Forms のアドオン | アダプティブフォームのコアコンポーネント |
|---|---|---|
| AEM as a Cloud Service | Forms - デジタル登録 | [リリース 2.0.10](version.md)+ |
| AEM 6.5 | Forms のアドオン | [リリース 1.1.12](version.md)+ |

AEM Cloud Service SDK バージョンが 2023.02.0 より前の場合は、2023.02.0 リリースより前にアダプティブフォームのコアコンポーネントがプレリリースの一部であったので、[お使いの環境で `prerelease` フラグが有効になっていることを確認してください](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html?lang=ja#new-features)。


## コアコンポーネントベースのアダプティブフォームの作成

AEM Forms as a Cloud Service 環境と AEM 6.5 Forms 環境の両方で次のアクションを実行できます。

| アクション | AEM Forms バージョン |
|--------|------------------|
| スタンドアロンのアダプティブフォームを作成 | [AEM Forms as Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=ja) |
| AEM Sites ページでのアダプティブフォームの作成 | [AEM 6.5 Forms](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-basic-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=ja#create-an-adaptive-form-in-sites-editor-or-experience-fragment)、[AEM Forms as Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=ja#create-an-adaptive-form-in-sites-editor-or-experience-fragment) |
| AEM エクスペリエンスフラグメントでアダプティブフォームを作成 | [AEM 6.5 Forms](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-basic-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=ja#create-an-adaptive-form-in-experience-fragment)、[AEM Forms as Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=ja#create-an-adaptive-form-in-experience-fragment) |
| アダプティブフォームをエクスペリエンスフラグメントに変換 | [AEM 6.5 Forms](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-basic-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=ja#convert-an-adaptive-form-in-sites-page-to-an-experience-fragment)、[AEM Forms as Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=ja#convert-an-adaptive-form-in-sites-page-to-an-experience-fragment) |





<!-- >, such as  [WCAG 2.1 standard](https://www.w3.org/TR/WCAG21/), to ensure that forms can be used by people with disabilities, including those using assistive technologies such as screen readers.

*   **Alignment with AEM Sites**: The Core Components are designed to be more aligned with AEM Sites, making it easier for Sites users to adopt and use them without having to learn anything new. The components use the same front-end pipeline as Sites, making it easier to style and modify their appearance. 

<!-- Additionally, the following points further illustrate this alignment:

    *   **Authoring experience inline with Page editor**: The Core Components have an authoring experience that is inline with the Sites editor, with dialogs and other experiences similar to the Page editor. This makes it easier for Sites users to create and manage forms within the familiar context of the Sites editor.

    *   **Inline form editing in Sites editor**: The Core Components allow  inline form editing within the Sites editor, avoiding the need to switch back and forth between editors. This streamlines the authoring experience and makes it easier to create and manage forms.

    *   **Inheriting Sites features in Forms**: Forms authored within a Sites page inherit the same features as Sites. This provides a seamless and integrated experience for creating and managing forms within the context of AEM Sites 
    
    <!--including Multi Site Manager, the ability to use Sites components within a form for static content, support for scheduled publish/unpublish, form translation aligned with Sites translation, versioning, and targeting -->

## 関連トピック {#see-also}

{{see-also}}
