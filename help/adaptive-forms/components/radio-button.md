---
title: アダプティブフォームのコアコンポーネント - ラジオボタン
description: アダプティブフォームのラジオボタンコアコンポーネントの使用またはカスタマイズ。
role: Architect, Developer, Admin, User
exl-id: 86b5e9ec-58ac-4cd5-9c7c-4269247ec34f
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: ht
source-wordcount: '2135'
ht-degree: 100%

---


# ラジオボタンコンポーネント {#radio-button-adaptive-forms-core-component}

アダプティブフォームのラジオボタンは、ユーザーが関連オプションのグループから 1 つのオプションを選択できる入力要素のひとつです。これは、このオプションが選択されているかどうかを示す、塗りつぶされた、または空の小さな円形のボタンで表示されます。ユーザーがいずれかのラジオボタンを選択すると、グループ内の他のラジオボタンの選択が解除されます。通常、ラジオボタンは相互に排他的な複数のオプションがあり、一度に 1 つのみ選択できる場合に使用されます。

{{traditional-aem}}

**例**

![例](/help/adaptive-forms/assets/radio-button.png)

**プロパティダイアログ**

![例](/help/adaptive-forms/assets/radio-button-properties.png)

この例では、オプション要素を使用して、ラジオボタンがグループ化されています。 「 **テキストを表示**」要素は、項目のラベルを提供するために使用され、 **データ値** は、フォームの送信時にサーバーに送信される値を指定するために使用されます。

各「ラジオボタン」オプションには、一意のデータ値と表示テキスト属性があります。 ユーザーが「1-10」を選択すると、フォームの送信時に、対応するデータ値がサーバーに送信されます。 その後、このデータをサーバーサイドスクリプトで処理して、ユーザーが選択したオプションを判断し、フォーム内の他のフィールドを更新したり、フォームデータをサーバーサイドスクリプトに送信してさらに処理するなど、様々な操作を実行できます。

さらに、アダプティブフォームルールエディターを使用して、各ラジオボタンの処理値をオプションごとに異なるように設定することもできます

## 使用方法 {#reasons-to-use-radio-button}

フォームでラジオボタンを使用する理由は、次のようにいくつかあります。

- **選択肢の制限**：ラジオボタンは、ユーザーが選択できる事前定義済みオプションのリストを提供するために使用され、一度に 1 つのオプションのみを選択できます。 これは、オプションの数が制限され、相互に排他的な場合に役立ちます。

- **クリアな表示域**：ラジオボタンは明確でわかりやすく、選択内容を簡単に把握できます。

- **一貫性**：一貫した標準化された方法でオプションを表示できるため、ユーザーはフォームを理解して操作しやすくなります。

- **使いやすさ**：ラジオボタンは、特にテクノロジーに詳しくないユーザーやモビリティに制限があるユーザーにとって、使いやすい要素です。

## バージョンと互換性 {#version-and-compatibility}

アダプティブフォームのラジオボタンコアコンポーネントは、Cloud Service 向けコアコンポーネント 2.0.4 および AEM 6.5.16.0 Forms 向けコアコンポーネント 1.1.12 以降の一部として、2023年2月にリリースされました。 次の表に、サポートされているすべてのバージョン、AEM の互換性、対応するドキュメントへのリンクを示します。

| コンポーネントのバージョン | AEM as a Cloud Service | AEM 6.5.16.0 Forms 以降 |
|---|---|---|
| v1 | <br>[リリース 2.0.4](/help/adaptive-forms/version.md) 以降と互換性あり | <br>[リリース 1.1.12](/help/adaptive-forms/version.md) 以降、2.0.0 未満と互換性があります。 |

コアコンポーネントのバージョンとリリースについて詳しくは、[コアコンポーネントのバージョン](/help/adaptive-forms/version.md)ドキュメントをご覧ください。

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion_jp). -->

## 技術的詳細 {#technical-details}

アダプティブフォームのラジオボタンコアコンポーネントに関する最新情報については、[GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/radiobutton/v1/radiobutton) のテクニカルドキュメントをご覧ください。コアコンポーネントの開発について詳しくは、[コアコンポーネント開発者向けドキュメント](/help/developing/overview.md)をご覧ください。

## 設定ダイアログ {#configure-dialog}

設定ダイアログでは、ラジオボタンのエクスペリエンスを訪問者に合わせて簡単にカスタマイズできます。 また、簡単にラジオボタンのオプションを定義して、シームレスなユーザーエクスペリエンスを実現することもできます。

### 「基本」タブ

![「基本」タブ](/help/adaptive-forms/assets/radiobutton_basictab.png)

- **名前** - フォームコンポーネントは、フォーム内とルールエディター内の両方で一意の名前で簡単に識別できますが、名前にスペースや特殊文字を含めることはできません。

- **タイトル** - タイトルを使用すると、フォーム内のコンポーネントを簡単に識別できます。デフォルトでは、コンポーネントの上にタイトルが表示されます。 タイトルを追加しない場合、コンポーネントの名前がタイトルテキストの代わりに表示されます。
- **タイトルのリッチテキストを許可** - この機能により、ユーザーは、太字、斜体、下線付きのテキスト、様々なフォント、フォントサイズ、カラー、追加オプションなどの機能を組み込んで、プレーンテキストのタイトルを書式設定でき、視覚的なプレゼンテーションとカスタマイズが強化されます。 これにより、ドキュメント、web サイト、アプリケーション内でタイトルを目立たせる際の柔軟性とクリエイティブなコントロールが向上します。\
  「**タイトルのリッチテキストを許可**」 チェックボックスをオンにすると、コンポーネントのタイトルをスタイル設定するための書式設定オプションが表示されます。 使用可能なすべての書式設定オプションにアクセスするには、![全画面表示アイコン](/help/adaptive-forms/assets/fullscreen-icon.png) タブをクリックします。

  ![リッチテキストのサポート](/help/adaptive-forms/assets/richtext-support-title.png)

- **タイトルを非表示** - コンポーネントのタイトルを非表示にするには、このオプションを選択します。

- **オプション** -「**追加**」ボタンからデータ値と表示テキストのペアを追加できます。\
  新しいオプションを追加したら、次の操作を実行できます。
   - **データ値** — このオプションでは、オプションが選択された際に送信するコンテンツを指定できます。
   - **テキストを表示** - このオプションでは、アダプティブフォームに表示する内容を入力できます。
   - **削除** - タップまたはクリックすると、ラジオボタンのオプションが削除されます。
   - **並べ替え** - タップまたはクリックしてドラッグすると、オプションの順序を並べ替えることができます。
また、**オプションのリッチテキストを許可**&#x200B;を使用して、ラジオボタングループのオプションを書式設定することもできます。

  ![オプションのリッチテキストのサポート](/help/adaptive-forms/assets/richtext-for-options.png)

  「**オプションのリッチテキストを許可**」 チェックボックスをオンにすると、コンポーネントのオプションをスタイル設定するための書式設定オプションが表示されます。使用可能なすべての書式設定オプションにアクセスするには、`Fullscreen` ![全画面表示アイコン](/help/adaptive-forms/assets/fullscreen-icon.png) タブをクリックします。

  ![オプションのリッチテキストのサポート](/help/adaptive-forms/assets/richtextoptions-support.png)

- **バインド参照** - バインド参照は、外部データソースに保存され、フォーム内で使用されるデータ要素への参照です。 バインド参照を使用すると、データをフォームフィールドに動的にバインドして、フォームにデータソースの最新のデータを表示できます。 例えば、フォームに入力された顧客 ID に基づいて、顧客の名前と住所をフォームに表示できます。 さらに、フォームに入力されたデータでデータソースを更新することもできます。 このようにして、AEM Forms で外部データソースとやり取りするフォームを作成し、データの収集と管理においてシームレスなユーザーエクスペリエンスを提供できます。

- **非連結フォーム要素としてマーク**：どのスキーマにもリンクされていないフォームフィールドを設定する場合は、このオプションを選択します。 このオプションを使用すると、データソースを更新せずにデータを保存できます。 また、標準のデータベース統合とは別に、カスタム方法でデータを処理できます。

- **送信された値のデータタイプ** - このオプションでは、いずれかのオプションが選択された際に送信される値のデータタイプを指定します。 「**送信された値のデータタイプ**」が「`Number`」に指定されている場合に、「**オプション** 」タブの「**データ値**」に文字列データを追加すると、画面に `Value type mismatch` エラーメッセージが表示されます。

- **デフォルトのオプション** - このオプションを使用すると、フォームの読み込み時に事前に選択されたデフォルト値を追加できます。**送信された値のデータタイプ**&#x200B;が `Number` に設定されていて、「**デフォルトのオプション**」に文字列データを追加した場合、画面には `Value type mismatch` エラーメッセージが表示されます。

- **表示オプション** - このオプションは、アダプティブフォームでラジオボタンの視覚的なアラインメントを設定するために使用されます。 次の 2 つのオプションがサポートされています。
   - **水平方向** - このオプションを選択すると、アダプティブフォームでラジオボタンが左から右に表示されます。
   - **垂直方向** - このオプションを選択すると、アダプティブフォームでラジオボタンが上から下に表示されます。
- **コンポーネントを非表示** - フォームでコンポーネントを非表示にするには、このオプションを選択します。 このコンポーネントは、他の目的（ルールエディターでの計算に使用するなど）にも利用できます。 これは、ユーザーが表示する必要のない情報や直接変更した情報を保存する必要がある場合に役立ちます。
- **コンポーネントの無効化** - コンポーネントを無効にする場合は、このオプションを選択します。 エンドユーザーは、無効になっているコンポーネントをアクティブにしたり、編集したりすることはできません。 ユーザーはフィールドの値を表示できますが、変更することはできません。 このコンポーネントは、他の目的（ルールエディターでの計算に使用するなど）にも利用できます。
- **読み取り専用** - コンポーネントを編集不可にするには、このオプションを選択します。 ユーザーはフィールドの値を表示できますが、変更することはできません。 このコンポーネントは、他の目的（ルールエディターでの計算に使用するなど）にも利用できます。

### 「検証」タブ {#validation-tab}

![「検証」タブ](/help/adaptive-forms/assets/radiobutton_validationtab.png)

- **必須** - コンポーネントをアダプティブフォームに表示する場合は、このオプションを選択します。 オプションを選択した後、フォームの送信を続行する前に選択を行う必要があります。 このオプションを選択すると、「**基本**」タブの「**コンポーネントを非表示**」または「**コンポーネントの無効化**」は選択できなくなります。
- **エラーメッセージ** - このオプションを使用すると、「**必須**」チェックボックスがオンで、かつフォームフィールドが空白の場合に表示されるメッセージを入力できます。

- **スクリプト検証メッセージ** - スクリプトの検証が失敗した場合に表示するメッセージを入力できます。

### 「ヘルプコンテンツ」タブ {#helpcontent-tab}

![「ヘルプコンテンツ」タブ](/help/adaptive-forms/assets/radiobutton_helptab.png)

- **短い説明** - 短い説明は、特定のフォームフィールドの目的に関する追加の情報や説明を提供する簡単な説明文です。 これにより、ユーザーは、フィールドに入力するデータの種類を理解しやすくなります。また、入力された情報が有効で目的の条件を満たしていることを確認できるように、ガイドラインや例を提供できます。 デフォルトでは、短い説明は非表示になっています。 「**短い説明を常に表示**」オプションを有効にすると、コンポーネントの下に説明が表示されます。

- **短い説明を常に表示** - このオプションを有効にすると、コンポーネントの下に短い説明が表示されます。

- **ヘルプテキスト** - ヘルプテキストとは、フォームフィールドの正しい入力を支援するためにユーザーに提供される追加の情報やガイダンスを指します。 コンポーネントの横に配置されているヘルプアイコン（i）をクリックすると表示されます。 ユーザーがフィールドの要件や制約を理解できるように設計されているヘルプテキストは、フォームフィールドのラベルやプレースホルダーテキストよりも詳細な情報を提供できます。 また、フォームへの入力をより簡単かつ正確にするための提案や例を提供することも可能です。

### 「アクセシビリティ」タブ {#accessibility-tab}

![「アクセシビリティ」タブ](/help/adaptive-forms/assets/radiobutton_accessibilitytab.png)

- **スクリーンリーダー用テキスト** - スクリーンリーダー用テキストとは、視覚に障害のあるユーザーが使用する、支援テクノロジー（スクリーンリーダーなど）によって読み上げられる追加のテキストを指します。 このテキストでは、フォームフィールドの目的に関するオーディオの説明が提供され、フィールドのタイトル、説明、名前および関連するメッセージ（カスタムテキスト）に関する情報を含めることができます。 スクリーンリーダー用のテキストを使用すると、視覚に障害のあるユーザーを含むすべてのユーザーがフォームに確実にアクセスして、フォームフィールドとその要件を完全に理解できるようになります。
   - **カスタムテキスト**：ARIA アクセシビリティラベルにカスタムテキストを使用する場合は、このオプションを選択します。 このオプションを選択すると、「カスタムテキスト」ダイアログボックスが表示されます。 関連情報は、「カスタムテキスト」ダイアログボックスで追加できます。
   - **説明**：ARIA アクセシビリティラベルの説明を使用する場合は、このオプションを選択します。
   - **タイトル**：ARIA アクセシビリティラベルのタイトルを使用する場合は、このオプションを選択します。
   - **名前**：ARIA アクセシビリティラベルの名前を使用する場合は、このオプションを選択します。
   - **なし**：ARIA アクセシビリティラベルに追加しない場合は、このオプションを選択します。

## デザインダイアログ {#design-dialog}

デザインダイアログでは、ラジオボタンコンポーネントの CSS スタイルを定義および管理します。


### 「スタイル」タブ {#styles-tab}

タブを使用して、コンポーネントの CSS スタイルの定義と管理を行います。アダプティブフォームのラジオボタンコアコンポーネントは、AEM の[スタイルシステム](/help/get-started/authoring.md#component-styling)をサポートしています。

![デザインダイアログ](/help/adaptive-forms/assets/checkbox-style.png)

- **デフォルトの CSS クラス**：アダプティブフォームのラジオボタンコアコンポーネントにデフォルトの CSS クラスを指定できます。

- **許可されたスタイル**：スタイルを表す名前と CSS クラスを指定してスタイルを定義します。 例えば、「bold text」という名前のスタイルを作成し、CSS クラス「font-weight: bold」を指定できます。 アダプティブフォームエディターでアダプティブフォームにこれらのスタイルを使用または適用できます。 スタイルを適用するには、アダプティブフォームエディターでスタイルを適用するコンポーネントを選択し、「プロパティ」ダイアログに移動して「**スタイル**」ドロップダウンリストから希望のスタイルを選択します。 スタイルを更新または変更する必要がある場合は、デザインダイアログに戻り、「スタイル」タブでスタイルを更新して変更を保存します。

### カスタムプロパティ

![カスタムプロパティダイアログ](/help/adaptive-forms/assets/checkbox-customproperties.png)

カスタムプロパティを使用すると、フォームテンプレートを使用してカスタム属性（キーと値のペア）をアダプティブフォームのコアコンポーネントに関連付けることができます。 カスタムプロパティは、コンポーネントのヘッドレスレンディションのプロパティセクションに反映されます。 これにより、カスタム属性値に基づいて適応する動的なフォーム動作を作成できます。 例えば、開発者は、モバイル、デスクトップ、web プラットフォーム上にヘッドレスフォームコンポーネントの様々なレンディションをデザインできるので、幅広いデバイスでのユーザーエクスペリエンスが大幅に向上します。

- **グループ名**：カスタムプロパティグループを識別する名前を指定できます。 複数のカスタムプロパティグループを追加、削除または並べ替えることができます。 カスタムプロパティグループを追加すると、次のオプションが表示されます。

   - **キーと値のペア**：各カスタムプロパティグループの「**追加**」ボタンをクリックすると、複数のカスタムプロパティ名とカスタムプロパティ値を追加できます。

   - **削除**：タップまたはクリックすると、カスタムプロパティ名とカスタムプロパティ値を削除できます。

   - **並べ替え**：タップまたはクリックしてドラッグすると、カスタムプロパティ名とカスタムプロパティ値の順序を並べ替えることができます。

## 関連記事 {#related-articles}

{{more-like-this}}

## 関連トピック {#see-also}

{{see-also}}
