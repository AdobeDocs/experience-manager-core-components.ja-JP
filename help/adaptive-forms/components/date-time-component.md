---
title: アダプティブ Forms コアコンポーネント – 日時
description: アダプティブFormsの日時コアコンポーネントの使用またはカスタマイズ。
role: Architect, Developer, Admin, User
source-git-commit: daeabccaff39e255c111c6af2540ca4d5be0c709
workflow-type: tm+mt
source-wordcount: '1898'
ht-degree: 74%

---


# 日時コンポーネント

アダプティブフォームの日付と時間コンポーネントは、ユーザーがカレンダーおよび時計インターフェイスを使用して **日付と時間** の両方を選択したり、特定の形式で手動で値を入力したりできるユーザーインターフェイス要素です。 日付と時刻の両方が重要なユースケースに対して、正確で標準化された入力を保証します。

**例**

![例](/help/adaptive-forms/assets/date-time-picker.png)

## 使用方法 {#reasons-to-use-date-time-picker}

日付と時刻の選択をフォームに含める方がメリットが大きい理由は、次のようにいくつかあります。

- **利便性**：ユーザーが値を手動で入力しなくても、日時を簡単に選択できます。
- **一貫性**：フォーム全体で日付と時刻の入力に標準形式を適用します。
- **ユーザーエクスペリエンスの向上**：カレンダーおよび時間セレクターを含む直感的な UI を提供します。
- **イベントのスケジュール設定**：予約、面接、または会議のスケジュール設定フォームで役立ちます。
- **旅行および予約**：ユーザーがチェックイン/チェックアウトの日時を選択できるようにします。
- **データの正確性**：フリーテキスト入力と比較して入力エラーを減らします。

## バージョンと互換性 {#version-and-compatibility}

アダプティブForms日時コアコンポーネントは、Cloud Service以降の **コアコンポーネント 2.24.6** の一部として **2025 年 8 月** にリリースされました。

| コンポーネントのバージョン | AEM as a Cloud Service | AEM 6.5.16.0 Forms 以降 |
|---|---|---|
| v1 | <br>[リリース 2.24.6](/help/adaptive-forms/version.md) 以降と互換性あり | |

バージョンについて詳しくは、[ コアコンポーネントのバージョン ](/help/adaptive-forms/version.md) を参照してください。

## 技術的詳細 {#technical-details}

[GitHub](https://github.com/adobe/aem-core-forms-components) のアダプティブForms日時コアコンポーネントに関する最新の技術的な詳細について説明します。 コアコンポーネントの開発について詳しくは、[ コアコンポーネント開発者向けドキュメント ](/help/developing/overview.md) を参照してください。

## 設定ダイアログ {#configure-dialog}

設定ダイアログでは、日付と時刻をカスタマイズできます。

### 「基本」タブ {#basic-tab}

![「基本」タブ](/help/adaptive-forms/assets/datetime_basictab.png)

- **名前** - 名前によって、ルールエディターでコンポーネントを一意に識別できます。 名前文字列には特殊文字とスペースを使用できません。

- **タイトル** - タイトルは、アダプティブフォームのコンポーネントの上部に表示される文字列です。タイトルによって、アダプティブフォームのツリー構造内のコンポーネントを一意に識別できます。タイトルを追加しない場合、コンポーネントの名前がタイトルテキストの代わりに表示されます。
- **タイトルのリッチテキストを許可** - この機能により、ユーザーは、太字、斜体、下線付きのテキスト、様々なフォント、フォントサイズ、カラー、追加オプションなどの機能を組み込んで、プレーンテキストのタイトルを書式設定でき、視覚的なプレゼンテーションとカスタマイズが強化されます。 これにより、ドキュメント、web サイト、アプリケーション内でタイトルを目立たせる際の柔軟性とクリエイティブなコントロールが向上します。\
  「**タイトルのリッチテキストを許可**」 チェックボックスをオンにすると、コンポーネントのタイトルをスタイル設定するための書式設定オプションが表示されます。 使用可能なすべての書式設定オプションにアクセスするには、![全画面表示アイコン](/help/adaptive-forms/assets/fullscreen-icon.png) タブをクリックします。

  ![リッチテキストのサポート](/help/adaptive-forms/assets/richtext-support-title.png)

- **タイトルを非表示** - アダプティブフォーム内のコンポーネントタイプのタイトルを非表示にするには、このオプションを選択します。

- **プレースホルダーテキスト** - フォームコンポーネント内のプレースホルダーテキストとは、入力フィールド内に表示される短いラベルまたはプロンプトのことで、そのフィールドに入力する必要のある情報の種類に関するヒントとしてユーザーに表示します。ユーザーがフィールドへの入力を開始するとプレースホルダーテキストが消え、フィールドが空のままの場合は再び表示されます。 ユーザーに視覚的なキューを提供しますが、フィールドの永続的なラベルや値としては機能しません。
- **バインド参照** - バインド参照は、外部データソースに保存され、フォーム内で使用されるデータ要素への参照です。 バインド参照を使用すると、データをフォームフィールドに動的にバインドして、フォームにデータソースの最新のデータを表示できます。 例えば、フォームに入力された顧客 ID に基づいて、顧客の名前と住所をフォームに表示できます。 さらに、フォームに入力されたデータでデータソースを更新することもできます。 このように AEM Formsで外部データソースとやり取りするフォームを作成して、データの収集と管理のためのシームレスなユーザーエクスペリエンスを提供できます。

- **非連結フォーム要素としてマーク**：どのスキーマにもリンクされていないフォームフィールドを設定する場合は、このオプションを選択します。 このオプションを使用すると、データソースを更新せずにデータを保存できます。 また、標準のデータベース統合とは別に、カスタム方法でデータを処理できます。

- **コンポーネントを非表示** - フォームでコンポーネントを非表示にするには、このオプションを選択します。 このコンポーネントは、他の目的（ルールエディターでの計算に使用するなど）にも利用できます。 これは、ユーザーが表示する必要のない情報や直接変更した情報を保存する必要がある場合に役立ちます。
- **コンポーネントの無効化** - コンポーネントを無効にする場合は、このオプションを選択します。 エンドユーザーは、無効になっているコンポーネントをアクティブにしたり、編集したりすることはできません。 ユーザーはフィールドの値を表示できますが、変更することはできません。 このコンポーネントは、他の目的（ルールエディターでの計算に使用するなど）にも利用できます。
- **読み取り専用** - コンポーネントを編集不可にするには、このオプションを選択します。 ユーザーはフィールドの値を表示できますが、変更することはできません。 このコンポーネントは、他の目的（ルールエディターでの計算に使用するなど）にも利用できます。
- **デフォルトの日時** – このオプションを使用すると、フォームフィールドに日時を追加できます。 入力した日付は、デフォルトでコンポーネントの場所に表示されます。ユーザーが日時を入力しない場合、この値はフォームの送信時に送信されます。 **無効なコンポーネント** または **読み取り専用コンポーネント** が選択されている場合、デフォルトの日時が画面に表示され、フォームの送信時に送信されます。

### 「検証」タブ {#validation-tab}

![「検証」タブ](/help/adaptive-forms/assets/datetime_validation.png)

- **必須** - コンポーネントをアダプティブフォームに表示する場合は、このオプションを選択します。 オプションを選択した後、フォームの送信を続行する前に選択を行う必要があります。このオプションが選択されていると、「**基本**」タブの「**コンポーネントを非表示**」または「**コンポーネントの無効化**」選択できません。

- **エラーメッセージ** - このオプションを使用すると、「**必須**」チェックボックスがオンで、かつフォームフィールドが空白の場合に表示されるメッセージを入力できます。

- **スクリプト検証メッセージ** - スクリプトの検証が失敗した場合に表示するメッセージを入力できます。

- **最短の日付** - 必要となる最短の日付を指定できます。「最短の日付と時刻」で指定した日付より前の日付を入力すると、エラーメッセージが画面に表示されます。 **最短エラーメッセージ**&#x200B;ダイアログボックスでは、カスタムのエラーメッセージを追加できます。

- **最短エラーメッセージ** - **最短エラーメッセージ** ダイアログボックスでは、「**最短の日付**」オプションで指定した日付または時刻以前の日付または時刻を入力した場合に表示されるカスタムのエラーメッセージを追加できます。

- **最長の日付** – 必要となる最長の日時を指定できます。 「最長の日付」で指定した日付または時刻より後の日付または時刻を入力すると、エラーメッセージが画面に表示されます。 **最長エラーメッセージ**&#x200B;ダイアログボックスでは、カスタムのエラーメッセージを追加できます。

- **最長エラーメッセージ** - **最長エラーメッセージ** ダイアログボックスでは、「**最長の日付**」オプションで指定した日付または時刻より後の日付または時刻を入力した場合に表示されるカスタムのエラーメッセージを追加できます。

### 「ヘルプコンテンツ」タブ {#help-content-tab}

![「ヘルプコンテンツ」タブ](/help/adaptive-forms/assets/datetime_helptab.png)

- **短い説明** - 短い説明は、特定のフォームフィールドの目的に関する追加の情報や説明を提供する簡単な説明文です。 これにより、ユーザーは、フィールドに入力するデータの種類を理解しやすくなります。また、入力された情報が有効で目的の条件を満たしていることを確認できるように、ガイドラインや例を提供できます。 デフォルトでは、短い説明は非表示になっています。 「**短い説明を常に表示**」オプションを有効にすると、コンポーネントの下に短い説明が表示されます。

- **短い説明を常に表示** - このオプションを有効にすると、コンポーネントの下に短い説明が表示されます。

- **ヘルプテキスト** - ヘルプテキストとは、フォームフィールドの正しい入力を支援するためにユーザーに提供される追加の情報やガイダンスのことです。コンポーネントの横に配置されているヘルプアイコン（i）をクリックすると表示されます。 ユーザーがフィールドの要件や制約を理解できるように設計されているヘルプテキストは、フォームフィールドのラベルやプレースホルダーテキストよりも詳細な情報を提供できます。 また、フォームへの入力をより簡単かつ正確にするための提案や例を提供することも可能です。


### 「アクセシビリティ」タブ {#accessibility-tab}

![「アクセシビリティ」タブ](/help/adaptive-forms/assets/datetime_accessibilitytab.png)

- **スクリーンリーダー用テキスト** - スクリーンリーダー用テキストとは、視覚に障害のあるユーザーが使用する、支援テクノロジー（スクリーンリーダーなど）によって読み上げられる追加のテキストを指します。 このテキストでは、フォームフィールドの目的に関するオーディオの説明が提供され、フィールドのタイトル、説明、名前および関連するメッセージ（カスタムテキスト）に関する情報を含めることができます。 スクリーンリーダー用のテキストを使用すると、視覚に障害のあるユーザーを含むすべてのユーザーがフォームに確実にアクセスして、フォームフィールドとその要件を完全に理解できるようになります。
   - **カスタムテキスト**：ARIA アクセシビリティラベルにカスタムテキストを使用する場合は、このオプションを選択します。 このオプションを選択すると、「カスタムテキスト」ダイアログボックスが表示されます。 関連情報は、「カスタムテキスト」ダイアログボックスで追加できます。
   - **説明**：ARIA アクセシビリティラベルの説明を使用する場合は、このオプションを選択します。
   - **タイトル**：ARIA アクセシビリティラベルのタイトルを使用する場合は、このオプションを選択します。
   - **名前**：ARIA アクセシビリティラベルの名前を使用する場合は、このオプションを選択します。
   - **なし**：ARIA アクセシビリティラベルに追加しない場合は、このオプションを選択します。

<!--
### Formats Tab {#format-tab}

![Formats tab](/help/adaptive-forms/assets/datepicker_formattab.png)

-   **Display Format** - It represents the date format that is displayed to the user. The **Type** option allows the user to select the date format. You can also customize the date format using the **Custom** option in the **Type** dropdown menu.

-   **Edit Format** - It represents a date format in which the user can edit the date. The **Type** option allows the user to select the date format. You can also customize the date format using the **Custom** option in the **Type** dropdown menu.
-  **Format error message** - This option allows you to enter the message displayed on the screen when the entered date is not in the correct format.
- **Language** - This feature is used for formatting the specific field. When a user selects any language option from the **Type** drop-down menu, the **IETF BCP 47 language tag** option appears in the panel. You can choose the language for field formatting when translating an Adaptive Form into a specific language.
  
The set of languages is not visible by default, but users can input a custom **IETF BCP 47 language tag** by updating the template policy:

  1. Open the corresponding template associated with an Adaptive Form in the template editor.
  2. Select the existing policy as `datepicker-default-policy` from the drop-down menu.
   
        ![Date Picker template Policy](/help/adaptive-forms/assets/date-picker-template-policy.png)

  3. Click **Done**.

        >[!NOTE]
        >
        > For further information on how to translate an Adaptive Form to a specific locale, [click here](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/supporting-new-language-localization-core-components).
-->

## デザインダイアログ {#design-dialog}

デザインダイアログでは、日時コンポーネントの CSS スタイルを定義および管理できます。

### 「スタイル」タブ {#styles-tab}

タブを使用して、コンポーネントの CSS スタイルの定義と管理を行います。 アダプティブForms日時コアコンポーネントは、AEM[ スタイルシステム ](/help/get-started/authoring.md#component-styling) をサポートしています。

![「スタイル」タブ](/help/adaptive-forms/assets/datepicker_styletab.png)

- **デフォルトの CSS クラス**：アダプティブForms日時コアコンポーネントのデフォルト CSS クラスを指定できます。

- **許可されたスタイル**：スタイルを表す名前と CSS クラスを指定してスタイルを定義します。 例えば、「bold text」という名前のスタイルを作成し、CSS クラス「font-weight: bold」を指定できます。 アダプティブフォームエディターでアダプティブフォームにこれらのスタイルを使用または適用できます。 スタイルを適用するには、アダプティブフォームエディターでスタイルを適用するコンポーネントを選択し、「プロパティ」ダイアログに移動して「**スタイル**」ドロップダウンリストから希望のスタイルを選択します。 スタイルを更新または変更する必要がある場合は、デザインダイアログに戻り、「スタイル」タブでスタイルを更新して変更を保存します。

### カスタムプロパティ

![カスタムプロパティダイアログ](/help/adaptive-forms/assets/datepicker_customproperties.png)

カスタムプロパティを使用すると、フォームテンプレートを使用してカスタム属性（キーと値のペア）をアダプティブフォームのコアコンポーネントに関連付けることができます。 カスタムプロパティは、コンポーネントのヘッドレスレンディションのプロパティセクションに反映されます。 これにより、カスタム属性値に基づいて適応する動的なフォーム動作を作成できます。 例えば、開発者は、モバイル、デスクトップ、web プラットフォーム上にヘッドレスフォームコンポーネントの様々なレンディションをデザインできるので、幅広いデバイスでのユーザーエクスペリエンスが大幅に向上します。

- **グループ名**：カスタムプロパティグループを識別する名前を指定できます。 複数のカスタムプロパティグループを追加、削除または並べ替えることができます。 カスタムプロパティグループを追加すると、次のオプションが表示されます。

   - **キーと値のペア**：各カスタムプロパティグループの「**追加**」ボタンをクリックすると、複数のカスタムプロパティ名とカスタムプロパティ値を追加できます。

   - **削除**：タップまたはクリックすると、カスタムプロパティ名とカスタムプロパティ値を削除できます。

   - **並べ替え**：タップまたはクリックしてドラッグすると、カスタムプロパティ名とカスタムプロパティ値の順序を並べ替えることができます。

<!--
### Formats Tab {#formats-tab}

The formats tab allows you to specify default and custom date formats.

![Formattab](/help/adaptive-forms/assets/datepicker_formatpolicy.png)



## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=ja)

-->

## 関連記事 {#related-articles}

{{more-like-this}}

## 関連トピック {#see-also}

{{see-also}}


