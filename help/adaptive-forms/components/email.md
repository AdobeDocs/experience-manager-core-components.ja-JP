---
title: アダプティブフォームのコアコンポーネント - メール入力
description: アダプティブフォームのメール入力コアコンポーネントを使用またはカスタマイズ。
role: Architect, Developer, Admin, User
exl-id: f6a2974b-991e-4cea-9ef8-0b03e8975eeb
source-git-commit: 4c510b8fe59f4be6e1b329ee4257ab1b780fbf22
workflow-type: tm+mt
source-wordcount: '2113'
ht-degree: 100%

---

# メールコンポーネント {#Email-input-adaptive-forms-core-component}

アダプティブフォームの電子メール入力コアコンポーネントは、ユーザーからメールアドレスを収集するために使用します。 メール入力フィールドを使用すると、入力されたデータが有効なメールアドレス形式であるかどうかをブラウザーで検証できます。 通常はテキストボックスとして表示され、有効なメールアドレスのみを受け入れるパターン検証が行われます。 メール入力フィールドは、「必須」、「プレースホルダー」、「パターン」などの追加の属性を使用してさらにカスタマイズし、入力データの検証について設定できます。

**例**
![例](/help/adaptive-forms/assets/emailid-example.png)

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

アダプティブフォームにメール入力コンポーネントを含める方がメリットが大きい理由は、次のようにいくつかあります。

- **ユーザーの利便性**：メール入力では、期待されるデータがフィールドに明確に示されるので、ユーザーはメールアドレスを簡単に入力できます。

- **コミュニケーションのパーソナライズ**：フォームを通じてユーザーからメールアドレスを収集すると、確認メールやニュースレターの送信など、コミュニケーションをパーソナライズできます。

- **リードジェネレーション**：フォームを通じてメールアドレスを収集すると、企業はメールリストを作成してリードジェネレーションに使用できます。

- **ユーザー認証**：メールアドレスは、制限されたコンテンツやサービスにアクセスするための認証の手段として使用できます。

- **フィードバックの収集**：フィードバックフォームへのメールの入力によって、企業はフィードバックのフォローアップや明確化のためにユーザーとコミュニケーションを取れるようになります。

## バージョンと互換性 {#version-and-compatibility}

アダプティブフォームのアコーディオンコアコンポーネントは、Cloud Service のコアコンポーネント 2.0.4 および AEM 6.5.16.0 Forms 以降のコアコンポーネント 1.1.12 の一部として 2023年2月にリリースされました。次の表に、サポートされているすべてのバージョン、AEM の互換性、対応するドキュメントへのリンクを示します。

| コンポーネントのバージョン | AEM as a Cloud Service | AEM 6.5.16.0 Forms 以降 |
|---|---|---|
| v1 | <br>[リリース 2.0.4](/help/adaptive-forms/version.md) 以降と互換性あり | <br>[リリース 1.1.12](/help/adaptive-forms/version.md) 以降、2.0.0 未満と互換性があります。 |

コアコンポーネントのバージョンとリリースについて詳しくは、[コアコンポーネントのバージョン](/help/adaptive-forms/version.md)ドキュメントをご覧ください。

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## 技術的詳細 {#technical-details}

アダプティブフォームのメール入力コアコンポーネントの最新情報については、[GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/emailinput/v1/emailinput) のテクニカルドキュメントをご覧ください。 コアコンポーネントの開発について詳しくは、[コアコンポーネント開発者向けドキュメント](/help/developing/overview.md)をご覧ください。

## 設定ダイアログ {#configure-dialog}

設定ダイアログでは、訪問者によるメール入力の操作を簡単にカスタマイズできます。 また、簡単にメール入力オプションを定義して、シームレスなユーザーエクスペリエンスを実現できます。

### 「基本」タブ {#basic-tab}

![「基本」タブ](/help/adaptive-forms/assets/email_basictab.png)

- **名前** - 名前は、ルールエディター内でコンポーネントを一意に識別します。名前文字列では特殊文字とスペースを使用できません。

- **タイトル** - タイトルを使用すると、フォーム内のコンポーネントを簡単に識別できます。デフォルトでは、コンポーネントの上にタイトルが表示されます。 タイトルを追加しない場合、コンポーネントの名前がタイトルテキストの代わりに表示されます。
- **タイトルのリッチテキストを許可** - この機能により、ユーザーは、太字、斜体、下線付きのテキスト、様々なフォント、フォントサイズ、カラー、追加オプションなどの機能を組み込んで、プレーンテキストのタイトルを書式設定でき、視覚的なプレゼンテーションとカスタマイズが強化されます。 これにより、ドキュメント、web サイト、アプリケーション内でタイトルを目立たせる際の柔軟性とクリエイティブなコントロールが向上します。\
  「**タイトルのリッチテキストを許可**」 チェックボックスをオンにすると、コンポーネントのタイトルをスタイル設定するための書式設定オプションが表示されます。 使用可能なすべての書式設定オプションにアクセスするには、![全画面表示アイコン](/help/adaptive-forms/assets/fullscreen-icon.png) タブをクリックします。

  ![リッチテキストのサポート](/help/adaptive-forms/assets/richtext-support-title.png)

- **タイトルを非表示** - コンポーネントのタイトルを非表示にするには、このオプションを選択します。

- **プレースホルダーテキスト** - フォームコンポーネント内のプレースホルダーテキストとは、入力フィールド内に表示される短いラベルまたはプロンプトのことで、そのフィールドに入力する必要のある情報の種類に関するヒントとしてユーザーに表示します。 ユーザーがフィールドへの入力を開始するとプレースホルダーテキストが消え、フィールドが空のままの場合は再び表示されます。 ユーザーに視覚的なキューを提供しますが、フィールドの永続的なラベルや値としては機能しません。
- **バインド参照** - バインド参照は、外部データソースに保存され、フォーム内で使用されるデータ要素への参照です。 バインド参照を使用すると、データをフォームフィールドに動的にバインドして、フォームにデータソースの最新のデータを表示できます。 例えば、フォームに入力された顧客 ID に基づいて、顧客の名前と住所をフォームに表示できます。 さらに、フォームに入力されたデータでデータソースを更新することもできます。 このようにして、AEM Forms で外部データソースとやり取りするフォームを作成し、データの収集と管理においてシームレスなユーザーエクスペリエンスを提供できます。
- **非連結フォーム要素としてマーク**：どのスキーマにもリンクされていないフォームフィールドを設定する場合は、このオプションを選択します。 このオプションを使用すると、データソースを更新せずにデータを保存できます。 また、標準のデータベース統合とは別に、カスタム方法でデータを処理できます。
- **コンポーネントを非表示** - フォームでコンポーネントを非表示にするには、このオプションを選択します。 このコンポーネントは、他の目的（ルールエディターでの計算に使用するなど）にも利用できます。 これは、ユーザーが表示する必要のない情報や直接変更した情報を保存する必要がある場合に役立ちます。
- **コンポーネントの無効化** - コンポーネントを無効にする場合は、このオプションを選択します。 エンドユーザーは、無効になっているコンポーネントをアクティブにしたり、編集したりすることはできません。 ユーザーはフィールドの値を表示できますが、変更することはできません。 このコンポーネントは、他の目的（ルールエディターでの計算に使用するなど）にも利用できます。
- **読み取り専用** - コンポーネントを編集不可にするには、このオプションを選択します。 ユーザーはフィールドの値を表示できますが、変更することはできません。 このコンポーネントは、他の目的（ルールエディターでの計算に使用するなど）にも利用できます。

- **デフォルト値** - このオプションを使用すると、フォームフィールドにデフォルト値を追加できます。 「**無効なコンポーネント**」または「**読み取り専用コンポーネント**」が選択されている場合は、デフォルト値が画面に表示されます。 ユーザーがフォームフィールドに値を入力しない場合、この値はフォーム送信時に送信されます
- **自動入力属性**：このオプションを使用すると、ユーザーは、保存された情報に基づいてフォームフィールド内に自動的に入力される値を入力できます。

### 「検証」タブ {#validation-tab}

![「検証」タブ](/help/adaptive-forms/assets/email_validationtab.png)

- **必須** - コンポーネントをアダプティブフォームに表示する場合は、このオプションを選択します。 オプションを選択した後、フォームの送信を続行する前に値を入力する必要があります。このオプションを選択すると、「**基本**」タブで「**コンポーネントを非表示**」または「**コンポーネントを無効にする**」を選択できません。

- **エラーメッセージ** - このオプションを使用すると、「**必須**」チェックボックスがオンで、かつフォームフィールドが空白の場合に表示されるメッセージを入力できます。

- **スクリプト検証メッセージ** - スクリプトの検証が失敗した場合に表示するメッセージを入力できます。

- **最大文字数** - フィールドで許可される最大文字数を指定できます。 「**最大文字数**」で指定した値を超える文字数を入力すると、エラーメッセージが画面に表示されます。 **最大文字数のエラーメッセージ**&#x200B;ダイアログボックスでは、カスタムエラーメッセージを追加できます。

- **最大文字数のエラーメッセージ** - **最大文字数のエラーメッセージ**&#x200B;ダイアログボックスでは、「**最大文字数**」オプションで指定した値を超える文字数を入力したときに表示されるカスタムのエラーメッセージを追加できます。

- **最小文字数** - このオプションを使用すると、フィールドで許可する最小文字数を指定できます。 「**最小文字数**」に指定した値を下回る文字を入力すると、エラーメッセージが画面に表示されます。 **最小文字数エラーメッセージ**&#x200B;ダイアログボックスでは、カスタムエラーメッセージを追加できます。

- **最小文字数エラーメッセージ** - **最小文字数エラーメッセージ**&#x200B;ダイアログボックスでは、「**最小文字数**」オプションで指定した値を下回る文字数を入力した場合に表示されるカスタムのエラーメッセージを追加できます。
<br>

「**検証パターン**」オプションでは、入力したメール ID を検証するパターンを指定できます。 「**パターン**」オプションに入力された値でメール ID を検証できない場合は、エラーメッセージが画面に表示されます。

- **パターン** - このオプションを使用すると、メールで許可する検証パターンを入力できます。 ここでは正規表現も使用できます。
- **エラーメッセージ**- このオプションを使用すると、「**パターン**」オプションに入力した値でメール ID の検証に失敗した際、画面に表示するメッセージを指定できます

### 「ヘルプコンテンツ」タブ {#help-content-tab}

![「ヘルプコンテンツ」タブ](/help/adaptive-forms/assets/email_helptab.png)

- **短い説明** - 短い説明は、特定のフォームフィールドの目的に関する追加の情報や説明を提供する簡単な説明文です。 これにより、ユーザーは、フィールドに入力するデータの種類を理解しやすくなります。また、入力された情報が有効で目的の条件を満たしていることを確認できるように、ガイドラインや例を提供できます。 デフォルトでは、短い説明は非表示になっています。 「**短い説明を常に表示**」オプションを有効にすると、コンポーネントの下に説明が表示されます。

- **短い説明を常に表示** - このオプションを有効にすると、コンポーネントの下に短い説明が表示されます。

- **ヘルプテキスト** - ヘルプテキストとは、フォームフィールドの正しい入力を支援するためにユーザーに提供される追加の情報やガイダンスを指します。 コンポーネントの横に配置されているヘルプアイコン（i）をクリックすると表示されます。 ユーザーがフィールドの要件や制約を理解できるように設計されているヘルプテキストは、フォームフィールドのラベルやプレースホルダーテキストよりも詳細な情報を提供できます。 また、フォームへの入力をより簡単かつ正確にするための提案や例を提供することも可能です。

### 「アクセシビリティ」タブ {#accessibility-tab}

![「アクセシビリティ」タブ](/help/adaptive-forms/assets/email_accessibilitytab.png)

- **スクリーンリーダー用テキスト** - スクリーンリーダー用テキストとは、視覚に障害のあるユーザーが使用する、支援テクノロジー（スクリーンリーダーなど）によって読み上げられる追加のテキストを指します。 このテキストでは、フォームフィールドの目的に関するオーディオの説明が提供され、フィールドのタイトル、説明、名前および関連するメッセージ（カスタムテキスト）に関する情報を含めることができます。 スクリーンリーダー用のテキストを使用すると、視覚に障害のあるユーザーを含むすべてのユーザーがフォームに確実にアクセスして、フォームフィールドとその要件を完全に理解できるようになります。

   - **カスタムテキスト**：ARIA アクセシビリティラベルにカスタムテキストを使用する場合は、このオプションを選択します。 このオプションを選択すると、「カスタムテキスト」ダイアログボックスが表示されます。 関連情報は、「カスタムテキスト」ダイアログボックスで追加できます。
   - **説明**：ARIA アクセシビリティラベルの説明を使用する場合は、このオプションを選択します。
   - **タイトル**：ARIA アクセシビリティラベルのタイトルを使用する場合は、このオプションを選択します。
   - **名前**：ARIA アクセシビリティラベルの名前を使用する場合は、このオプションを選択します。
   - **なし**：ARIA アクセシビリティラベルに追加しない場合は、このオプションを選択します。

## デザインダイアログ {#design-dialog}

デザインダイアログでは、メール入力コンポーネントの CSS スタイルを定義および管理するために使用されます。

### 「スタイル」タブ {#styles-tab}

タブを使用して、コンポーネントの CSS スタイルの定義と管理を行います。 アダプティブフォームのメール入力コアコンポーネントは、AEM の[スタイルシステム](/help/get-started/authoring.md#component-styling)をサポートしています。

![「スタイル」タブ](/help/adaptive-forms/assets/datepicker_styletab.png)

- **デフォルトの CSS クラス**：アダプティブフォームのメール入力コアコンポーネントにデフォルトの CSS クラスを指定できます。

- **許可されたスタイル**：スタイルを表す名前と CSS クラスを指定してスタイルを定義します。 例えば、「bold text」という名前のスタイルを作成し、CSS クラス「font-weight: bold」を指定できます。 アダプティブフォームエディターでアダプティブフォームにこれらのスタイルを使用または適用できます。 スタイルを適用するには、アダプティブフォームエディターでスタイルを適用するコンポーネントを選択し、「プロパティ」ダイアログに移動して「**スタイル**」ドロップダウンリストから希望のスタイルを選択します。 スタイルを更新または変更する必要がある場合は、デザインダイアログに戻り、「スタイル」タブでスタイルを更新して変更を保存します。

### カスタムプロパティ

![カスタムプロパティダイアログ](/help/adaptive-forms/assets/datepicker_customproperties.png)

カスタムプロパティを使用すると、フォームテンプレートを使用してカスタム属性（キーと値のペア）をアダプティブフォームのコアコンポーネントに関連付けることができます。 カスタムプロパティは、コンポーネントのヘッドレスレンディションのプロパティセクションに反映されます。 これにより、カスタム属性値に基づいて適応する動的なフォーム動作を作成できます。 例えば、開発者は、モバイル、デスクトップ、web プラットフォーム上にヘッドレスフォームコンポーネントの様々なレンディションをデザインできるので、幅広いデバイスでのユーザーエクスペリエンスが大幅に向上します。

- **グループ名**：カスタムプロパティグループを識別する名前を指定できます。 複数のカスタムプロパティグループを追加、削除または並べ替えることができます。 カスタムプロパティグループを追加すると、次のオプションが表示されます。

   - **キーと値のペア**：各カスタムプロパティグループの「**追加**」ボタンをクリックすると、複数のカスタムプロパティ名とカスタムプロパティ値を追加できます。

   - **削除**：タップまたはクリックすると、カスタムプロパティ名とカスタムプロパティ値を削除できます。

   - **並べ替え**：タップまたはクリックしてドラッグすると、カスタムプロパティ名とカスタムプロパティ値の順序を並べ替えることができます。

### 「形式」タブ {#formats-tab}

「形式」タブでは、デフォルトおよびカスタムの日付形式を指定できます。

![「形式」タブ](/help/adaptive-forms/assets/emailinput_formattab.png)

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->

## 関連記事 {#related-articles}

{{more-like-this}}

## 関連トピック {#see-also}

{{see-also}}