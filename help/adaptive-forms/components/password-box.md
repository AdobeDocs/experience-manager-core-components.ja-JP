---
title: アダプティブフォームのコアコンポーネント - パスワードボックス
description: アダプティブフォームのパスワードボックスコアコンポーネントの使用またはカスタマイズ。
role: Architect, Developer, Admin, User
hide: true
hidefromtoc: true
exl-id: 7e70d9e9-b066-4ba3-b7ed-e4aad026c5e0
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: ht
source-wordcount: '1914'
ht-degree: 100%

---


# パスワードボックスコンポーネント

<span class="preview">これはプレリリース機能で、[プレリリースチャネル](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html?lang=ja#new-features)を通してアクセスできます。</span>

パスワードボックスコンポーネントを使用すると、ユーザーは、通常はプライバシーのためにマスクされた機密情報を入力および編集できます。パスワードコンポーネントは、様々な検証ルールを使用して設定し、データの正確性を確保できます。フォームで一般的に使用されるパスワードフィールドはわかりやすく、データのセキュリティを強化します。

{{traditional-aem}}

**例**

![パスワードボックスの例](/help/adaptive-forms/assets/password.png)

ユーザーは目のアイコンをクリックして、入力したパスワードテキストの表示／非表示を切り替えることができます。これにより、セキュリティが強化され、ユーザーは機密情報を正確に入力できます。

## 使用方法

アダプティブフォーム内でパスワードボックスコンポーネントを使用する理由はいくつかあります。

- **安全なデータ収集**：パスワードボックスフィールドは、パスワード、PIN、その他の機密エントリなどの機密情報を収集するために使用され、プライバシーのためにマスクされた文字が表示されます。

- **わかりやすい**：パスワードボックスフィールドを使用すると、ユーザーは情報を画面に表示することなく、安全に入力および編集できます。

- **柔軟性**：パスワードボックスコンポーネントは、最小文字長、特殊文字、その他のカスタム検証などのセキュリティ要件を満たすように設定して、強力なデータ保護と正確性を確保できます。

<!--
## Version and Compatibility {#version-and-compatibility}

The Adaptive Forms Password box Core Component was released in Feb 2023 as part of the Core Components 2.0.4 for Cloud Service and Core Components 1.1.12 for AEM 6.5.16.0 Forms or later. Here's a table showing all supported versions, AEM compatibility, and links to corresponding documentation:

|Component Version|AEM as a Cloud Service|AEM 6.5.16.0 Forms or later|
|---|---|---|
|v1|Compatible with<br>[release 2.0.4](/help/adaptive-forms/version.md) and later| Compatible with<br>[release 1.1.12](/help/adaptive-forms/version.md) and later but less than 2.0.0.|

For information on Core Component versions and releases, refer to the [Core Components Versions](/help/adaptive-forms/version.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion_jp). -->

## 技術的詳細 {#technical-details}

アダプティブフォームパスワードのコアコンポーネントの最新情報については、[GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput) のテクニカルドキュメントをご覧ください。コアコンポーネントの開発について詳しくは、[コアコンポーネント開発者向けドキュメント](/help/developing/overview.md)をご覧ください。

## 設定ダイアログ {#configure-dialog}

設定ダイアログを使用すると、訪問者のテキスト入力エクスペリエンスを簡単にカスタマイズできます。 また、シームレスなユーザーエクスペリエンスを実現するために、簡単にテキスト入力オプションを定義できます。

### 「基本」タブ

![「基本」タブ](/help/adaptive-forms/assets/password-basic.png)

- **名前** - フォームコンポーネントは、フォーム内とルールエディター内の両方で一意の名前で簡単に識別できますが、名前にスペースや特殊文字を含めることはできません。

- **タイトル** - タイトルを使用すると、フォーム内のコンポーネントを簡単に識別できます。デフォルトでは、コンポーネントの上にタイトルが表示されます。 タイトルを追加しない場合、コンポーネントの名前がタイトルテキストの代わりに表示されます。
- **タイトルのリッチテキストを許可** - この機能により、ユーザーは、太字、斜体、下線付きのテキスト、様々なフォント、フォントサイズ、カラー、追加オプションなどの機能を組み込んで、プレーンテキストのタイトルを書式設定でき、視覚的なプレゼンテーションとカスタマイズが強化されます。 これにより、ドキュメント、web サイト、アプリケーション内でタイトルを目立たせる際の柔軟性とクリエイティブなコントロールが向上します。\
  「**タイトルのリッチテキストを許可**」 チェックボックスをオンにすると、コンポーネントのタイトルをスタイル設定するための書式設定オプションが表示されます。 使用可能なすべての書式設定オプションにアクセスするには、![全画面表示アイコン](/help/adaptive-forms/assets/fullscreen-icon.png) タブをクリックします。

  ![リッチテキストのサポート](/help/adaptive-forms/assets/richtext-support-title.png)

- **タイトルを非表示** - コンポーネントのタイトルを非表示にするには、このオプションを選択します。

- **プレースホルダーテキスト** - フォームコンポーネント内のプレースホルダーテキストとは、入力フィールド内に表示される短いラベルまたはプロンプトのことで、そのフィールドに入力する必要のある情報の種類に関するヒントとしてユーザーに表示されます。 ユーザーがフィールドへの入力を開始するとプレースホルダーテキストが消え、フィールドが空のままの場合は再び表示されます。 ユーザーに視覚的なキューを提供しますが、フィールドの永続的なラベルや値としては機能しません。
- **バインド参照** - バインド参照は、外部データソースに保存され、フォーム内で使用されるデータ要素への参照です。 バインド参照を使用すると、データをフォームフィールドに動的にバインドして、フォームにデータソースの最新のデータを表示できます。 例えば、フォームに入力された顧客 ID に基づいて、顧客の名前と住所をフォームに表示できます。 さらに、フォームに入力されたデータでデータソースを更新することもできます。 このようにして、AEM Forms で外部データソースとやり取りするフォームを作成し、データの収集と管理においてシームレスなユーザーエクスペリエンスを提供できます。
- **非連結フォーム要素としてマーク**：どのスキーマにもリンクされていないフォームフィールドを設定する場合は、このオプションを選択します。 このオプションを使用すると、データソースを更新せずにデータを保存できます。 また、標準のデータベース統合とは別に、カスタム方法でデータを処理できます。

- **コンポーネントを非表示** - フォームでコンポーネントを非表示にするには、このオプションを選択します。 このコンポーネントは、他の目的（ルールエディターでの計算に使用するなど）にも利用できます。 これは、ユーザーが表示する必要のない情報や直接変更した情報を保存する必要がある場合に役立ちます。

- **コンポーネントの無効化** - コンポーネントを無効にする場合は、このオプションを選択します。 エンドユーザーは、無効になっているコンポーネントをアクティブにしたり、編集したりすることはできません。 ユーザーはフィールドの値を表示できますが、変更することはできません。 このコンポーネントは、他の目的（ルールエディターでの計算に使用するなど）にも利用できます。

- **読み取り専用** - コンポーネントを編集不可にするには、このオプションを選択します。 ユーザーはフィールドの値を表示できますが、変更することはできません。 このコンポーネントは、他の目的（ルールエディターでの計算に使用するなど）にも利用できます。

### 「検証」タブ {#validation-tab}

![「検証」タブ](/help/adaptive-forms/assets/password-validation.png)

- **必須** - コンポーネントをアダプティブフォームに表示する場合は、このオプションを選択します。 オプションを選択した後、フォームの送信を続行する前に値を入力する必要があります。 このオプションが選択されていると、「**基本**」タブの「**コンポーネントを非表示**」または「**コンポーネントの無効化**」は選択できません。

- **エラーメッセージ** - このオプションを使用すると、「**必須**」チェックボックスがオンになっており、フィールドが空白の場合に表示されるメッセージを入力できます。

- **スクリプト検証メッセージ** - スクリプトの検証が失敗した場合に表示するメッセージを入力できます。

- **最大文字数** - このオプションを使用すると、コンポーネントで許可する最大文字数を指定できます。 「**最大文字数**」に指定した値を超えて文字を入力すると、エラーメッセージが画面に表示されます。 **最大文字数のエラーメッセージ**&#x200B;ダイアログボックスでは、カスタムエラーメッセージを追加できます。

- **最大文字数のエラーメッセージ** - **最大文字数のエラーメッセージ**&#x200B;ダイアログボックスでは、「**最大文字数**」オプションで指定した値を超える文字数を入力したときに表示されるカスタムのエラーメッセージを追加できます。

- **最小文字数** - このオプションを使用すると、フィールドで許可する最小文字数を指定できます。 「**最小文字数**」に指定した値を下回る文字を入力すると、エラーメッセージが画面に表示されます。 **最小文字数エラーメッセージ**&#x200B;ダイアログボックスでは、カスタムエラーメッセージを追加できます。

- **最小文字数エラーメッセージ** - **最小文字数エラーメッセージ**&#x200B;ダイアログボックスでは、「**最小文字数**」オプションで指定した値を下回る文字数を入力した場合に表示されるカスタムのエラーメッセージを追加できます。

「**検証パターン**」オプションを使用すると、入力したテキストを検証するパターンを入力できます。 テキストが「**パターン**」オプションに入力された値の検証に失敗すると、エラーメッセージが画面に表示されます。

- **パターン** - このオプションを使用すると、テキストで許可される検証パターンを指定できます。 ここでは正規表現も使用できます。

- **エラーメッセージ** - このオプションを使用すると、入力したテキストが「**パターン**」オプションで指定した値での検証に失敗した場合に、画面に表示されるメッセージを指定できます

### 「ヘルプコンテンツ」タブ {#help-content-tab}

![「ヘルプコンテンツ」タブ](/help/adaptive-forms/assets/password-help.png)

- **短い説明** - 短い説明は、特定のフォームフィールドの目的に関する追加の情報や説明を提供する簡単な説明文です。 これにより、ユーザーは、フィールドに入力するデータの種類を理解しやすくなります。また、入力された情報が有効で目的の条件を満たしていることを確認できるように、ガイドラインや例を提供できます。 デフォルトでは、短い説明は非表示になっています。 「**短い説明を常に表示**」オプションを有効にすると、コンポーネントの下に説明が表示されます。

- **短い説明を常に表示** - このオプションを有効にすると、コンポーネントの下に短い説明が表示されます。

- **ヘルプテキスト** - ヘルプテキストとは、フォームフィールドの正しい入力を支援するためにユーザーに提供される追加の情報やガイダンスを指します。 コンポーネントの横に配置されているヘルプアイコン（i）をクリックすると表示されます。 ユーザーがフィールドの要件や制約を理解できるように設計されているヘルプテキストは、フォームフィールドのラベルやプレースホルダーテキストよりも詳細な情報を提供できます。 また、フォームへの入力をより簡単かつ正確にするための提案や例を提供することも可能です。

### 「アクセシビリティ」タブ {#accessibility-tab}

![「アクセシビリティ」タブ](/help/adaptive-forms/assets/password-accessibilty.png)

- **スクリーンリーダー用テキスト** - スクリーンリーダー用テキストとは、視覚に障害のあるユーザーが使用する、支援テクノロジー（スクリーンリーダーなど）によって読み上げられる追加のテキストを指します。 このテキストでは、フォームフィールドの目的に関するオーディオの説明が提供され、フィールドのタイトル、説明、名前および関連するメッセージ（カスタムテキスト）に関する情報を含めることができます。 スクリーンリーダー用のテキストを使用すると、視覚に障害のあるユーザーを含むすべてのユーザーがフォームに確実にアクセスして、フォームフィールドとその要件を完全に理解できるようになります。
   - **カスタムテキスト**：ARIA アクセシビリティラベルにカスタムテキストを使用する場合は、このオプションを選択します。 このオプションを選択すると、「カスタムテキスト」ダイアログボックスが表示されます。 関連情報は、「カスタムテキスト」ダイアログボックスで追加できます。
   - **説明**：ARIA アクセシビリティラベルの説明を使用する場合は、このオプションを選択します。
   - **タイトル**：ARIA アクセシビリティラベルのタイトルを使用する場合は、このオプションを選択します。
   - **名前**：ARIA アクセシビリティラベルの名前を使用する場合は、このオプションを選択します。
   - **なし**：ARIA アクセシビリティラベルに追加しない場合は、このオプションを選択します。

## デザインダイアログ {#design-dialog}

デザインダイアログは、テキストボックスコンポーネントの CSS スタイルを定義および管理するために使用します。

### 「スタイル」タブ {#styles-tab}

タブを使用して、コンポーネントの CSS スタイルの定義と管理を行います。 アダプティブフォームのテキストボックスコアコンポーネントは、AEM の[スタイルシステム](/help/get-started/authoring.md#component-styling)をサポートしています。

![「スタイル」タブ](/help/adaptive-forms/assets/datepicker_styletab.png)

- **デフォルトの CSS クラス**：アダプティブフォームのテキストボックスコアコンポーネントのデフォルト CSS クラスを指定できます。

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

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=ja)

-->

## 関連記事 {#related-articles}

{{more-like-this}}

## 関連トピック {#see-also}

{{see-also}}
