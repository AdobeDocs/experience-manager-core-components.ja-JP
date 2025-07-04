---
title: アダプティブフォームのコアコンポーネント - スイッチコンポーネント
description: アダプティブフォームのスイッチコアコンポーネントの使用またはカスタマイズ。
role: Architect, Developer, Admin, User
exl-id: 6ff2ca76-1514-42eb-bde3-60259af2d187
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: ht
source-wordcount: '1922'
ht-degree: 100%

---


# アダプティブフォームのスイッチコンポーネント{#switch-adaptive-forms-core-component}

スイッチコンポーネントは、フォームで使用されるグラフィカルユーザーインターフェイスです。このコンポーネントを使用すると、2 つのオプションから選択できるようになります。通常、2 つの状態を切り替えます。例えば、機能や設定を有効または無効にできます。スイッチコンポーネントは、現在の状態を視覚的に表し、特定の機能のオン／オフを表示するように設計されています。

スイッチコンポーネントは、値を true または false に設定するブーリアン型のコントロール要素です。例えば、サウンドのミュート／ミュート解除、Bluetooth や WiFi の有効化／無効化など、機能のオンとオフを切り替えるために使用されます。

![スイッチコンポーネントの例](/help/adaptive-forms/assets/switch-example.png)

{{traditional-aem}}

## 使用方法 {#reasons-to-use-switch}

アダプティブフォームでスイッチを使用する一般的な理由は次のとおりです。

- **ユーザーインタラクション**：ユーザーは、スイッチコンポーネントをクリックまたはタップして操作できます。

- **状態**：スイッチコンポーネントには、オンとオフの 2 つの状態があります。 スイッチコンポーネントの初期状態は、デフォルト設定や、制御する機能の現在の状態によって異なります。

- **視覚的な表示**：スイッチコンポーネントは、色や位置を変更することで、現在の状態を視覚的に表示します。

- **コントロール機能**：スイッチコンポーネントは、AEM Form の特定の機能を有効または無効にするために使用されます。例えば、ユーザーは機能のオン／オフを切り替えることができます。

## バージョンと互換性 {#version-and-compatibility}

アダプティブフォームのスイッチコアコンポーネントは、コアコンポーネント 2.0.64 の一部としてリリースされました。次の表に、サポートされているすべてのバージョン、AEM の互換性、対応するドキュメントへのリンクを示します。

|  |  |
|---|---|
| コンポーネントのバージョン | AEM as a Cloud Service |
| --- | --- |
| v1 | <br>[リリース 2.0.64](/help/adaptive-forms/version.md) 以降と互換性あり | 互換性あり | 互換性あり |

コアコンポーネントのバージョンとリリースについて詳しくは、[コアコンポーネントのバージョン](/help/adaptive-forms/version.md)ドキュメントをご覧ください。

## 技術的詳細 {#technical-details}

アダプティブフォームのスイッチコアコンポーネントの最新情報については、[GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/switch/v1/switch) のテクニカルドキュメントをご覧ください。コアコンポーネントの開発について詳しくは、[コアコンポーネント開発者向けドキュメント](/help/developing/overview.md)をご覧ください。

## 設定ダイアログ {#configure-dialog}

設定ダイアログを使用すると、スイッチコンポーネントのエクスペリエンスを訪問者に合わせて簡単にカスタマイズできます。また、スイッチコンポーネントのオプションを簡単に定義して、シームレスなユーザーエクスペリエンスを実現できます。

### 「基本」タブ

![「基本」タブ](/help/adaptive-forms/assets/switch-basic.png)

- **名前** - フォームコンポーネントは、フォーム内とルールエディター内の両方で一意の名前で簡単に識別できますが、名前にスペースや特殊文字を含めることはできません。

- **タイトル** - タイトルを使用すると、フォーム内のコンポーネントを簡単に識別できます。デフォルトでは、コンポーネントの横にタイトルが表示されます。 タイトルを追加しない場合、コンポーネントは表示されません。
- **タイトルのリッチテキストを許可** - この機能により、ユーザーは、太字、斜体、下線付きのテキスト、様々なフォント、フォントサイズ、カラー、追加オプションなどの機能を組み込んで、プレーンテキストのタイトルを書式設定でき、視覚的なプレゼンテーションとカスタマイズが強化されます。 これにより、ドキュメント、web サイト、アプリケーション内でタイトルを目立たせる際の柔軟性とクリエイティブなコントロールが向上します。\
  「**タイトルのリッチテキストを許可**」 チェックボックスをオンにすると、コンポーネントのタイトルをスタイル設定するための書式設定オプションが表示されます。 使用可能なすべての書式設定オプションにアクセスするには、![全画面表示アイコン](/help/adaptive-forms/assets/fullscreen-icon.png) タブをクリックします。

  ![リッチテキストのサポート](/help/adaptive-forms/assets/richtext-support-title.png)

- **タイトルを非表示** - コンポーネントのタイトルを非表示にするには、このオプションを選択します。

- **状態値をオフにして保持** - このオプションを選択すると、スイッチコンポーネントが選択されていない場合に返される値を指定できます。
- **オプション** - 各オプションのデータ値と表示テキストを指定します。
   - **有効時のデータ値** - アダプティブフォームでスイッチが有効な場合に送信される値を指定します。
   - **有効時の表示テキスト** - アダプティブフォームでスイッチが有効な場合にラベルとして表示するテキストを指定します。
   - **無効時のデータ値** - アダプティブフォームでスイッチが有効になっていない場合に送信される値を指定します。このオプションは、「**状態値をオフにして保持**」スイッチが有効になっている場合にのみ表示されます。
   - **無効時の表示テキスト** - アダプティブフォームでスイッチが有効になっていない場合にラベルとして表示するテキストを指定します。このオプションは、「**状態値をオフにして保持**」スイッチが有効になっている場合にのみ表示されます。

  また、**オプションのリッチテキストを許可**&#x200B;を使用して、スイッチコンポーネントのオプションを書式設定することもできます。

  ![オプションのリッチテキストのサポート](/help/adaptive-forms/assets/switch-optipn-rich-text.png)

  「**オプションのリッチテキストを許可**」 チェックボックスをオンにすると、コンポーネントのオプションをスタイル設定するための書式設定オプションが表示されます。使用可能なすべての書式設定オプションにアクセスするには、`Fullscreen` ![全画面表示アイコン](/help/adaptive-forms/assets/fullscreen-icon.png) タブをクリックします。

  ![オプションのリッチテキストのサポート](/help/adaptive-forms/assets/switch-richtext-for-display.png)

- **バインド参照** - バインド参照は、外部データソースに保存され、フォーム内で使用されるデータ要素への参照です。 バインド参照を使用すると、データをフォームフィールドに動的にバインドして、フォームにデータソースの最新のデータを表示できます。 例えば、フォームに入力された顧客 ID に基づいて、顧客の名前と住所をフォームに表示できます。 さらに、フォームに入力されたデータでデータソースを更新することもできます。 このように AEM Formsで外部データソースとやり取りするフォームを作成して、データの収集と管理のためのシームレスなユーザーエクスペリエンスを提供できます。
- **非連結フォーム要素としてマーク**：どのスキーマにもリンクされていないフォームフィールドを設定する場合は、このオプションを選択します。 このオプションを使用すると、データソースを更新せずにデータを保存できます。 また、標準のデータベース統合とは別に、カスタム方法でデータを処理できます。
- **送信された値のデータタイプ**：このオプションでは、いずれかのオプションが選択された場合に送信される値のデータタイプを指定します。「**送信された値のデータタイプ**」が「`Number`」に設定されている場合に、「**オプション**」タブの「**データ値**」に文字列データを追加すると、画面に `Value type mismatch` エラーメッセージが表示されます。
- **コンポーネントを非表示** - フォームでコンポーネントを非表示にするには、このオプションを選択します。 このコンポーネントは、他の目的（ルールエディターでの計算に使用するなど）にも利用できます。 これは、ユーザーが表示する必要のない情報や直接変更した情報を保存する必要がある場合に役立ちます。

- **コンポーネントの無効化** - コンポーネントを無効にするかロックする場合は、このオプションを選択します。 エンドユーザーは、無効になっているコンポーネントをアクティブにしたり、編集したりすることはできません。 ユーザーはフィールドの値を表示できますが、変更することはできません。 このコンポーネントは、他の目的（ルールエディターでの計算に使用するなど）にも利用できます。

- **デフォルト値** - このオプションを使用すると、フォームフィールドにデフォルト値を追加できます。**無効なコンポーネント**&#x200B;または&#x200B;**読み取り専用コンポーネント**&#x200B;が選択されている場合、デフォルト値が画面に表示されます。 ユーザーがフォームフィールドに値を入力しない場合、この値はフォームの送信時に送信されます。

### 「検証」タブ {#validation-tab}

![「検証」タブ](/help/adaptive-forms/assets/switch-validation.png)

- **必須** - コンポーネントをアダプティブフォームに表示する場合は、このオプションを選択します。 オプションを選択した後、フォームの送信を続行する前に選択を行う必要があります。 このオプションを選択すると、「**基本**」タブの「**コンポーネントを非表示**」または「**コンポーネントの無効化**」は選択できなくなります。

- **エラーメッセージ** - このオプションを使用すると、「**必須**」チェックボックスがオンで、かつフォームフィールドが空白の場合に表示されるメッセージを入力できます。

- **スクリプト検証メッセージ** - スクリプトの検証が失敗した場合に表示するメッセージを入力できます。

### 「ヘルプコンテンツ」タブ {#helpcontent-tab}

![「ヘルプコンテンツ」タブ](/help/adaptive-forms/assets/switch-help.png)

- **短い説明** - 短い説明は、特定のフォームフィールドの目的に関する追加の情報や説明を提供する簡単な説明文です。 これにより、ユーザーは、フィールドに入力するデータの種類を理解しやすくなります。また、入力された情報が有効で目的の条件を満たしていることを確認できるように、ガイドラインや例を提供できます。 デフォルトでは、短い説明は非表示になっています。 「**短い説明を常に表示**」オプションを有効にすると、コンポーネントの下に説明が表示されます。

- **短い説明を常に表示** - このオプションを有効にすると、コンポーネントの下に短い説明が表示されます。

- **ヘルプテキスト** - ヘルプテキストとは、フォームフィールドの正しい入力を支援するためにユーザーに提供される追加の情報やガイダンスを指します。 コンポーネントの横に配置されているヘルプアイコン（i）をクリックすると表示されます。 ユーザーがフィールドの要件や制約を理解できるように設計されているヘルプテキストは、フォームフィールドのラベルやプレースホルダーテキストよりも詳細な情報を提供できます。 また、フォームへの入力をより簡単かつ正確にするための提案や例を提供することも可能です。

### 「アクセシビリティ」タブ {#accessibility-tab}

![「アクセシビリティ」タブ](/help/adaptive-forms/assets/switch-accessibility.png)

- **スクリーンリーダー用テキスト** - スクリーンリーダー用テキストとは、視覚に障がいのあるユーザーが使用する支援テクノロジー（スクリーンリーダー）によって読み上げられる追加のテキストを指します。 このテキストでは、フォームフィールドの目的に関するオーディオの説明が提供され、フィールドのタイトル、説明、名前および関連するメッセージ（カスタムテキスト）に関する情報を含めることができます。 スクリーンリーダー用のテキストを使用すると、視覚に障害のあるユーザーを含むすべてのユーザーがフォームに確実にアクセスして、フォームフィールドとその要件を完全に理解できるようになります。
   - **カスタムテキスト**：ARIA アクセシビリティラベルにカスタムテキストを使用する場合は、このオプションを選択します。 このオプションを選択すると、「カスタムテキスト」ダイアログボックスが表示されます。 関連情報は、「カスタムテキスト」ダイアログボックスで追加できます。
   - **説明**：ARIA アクセシビリティラベルの説明を使用する場合は、このオプションを選択します。
   - **タイトル**：ARIA アクセシビリティラベルのタイトルを使用する場合は、このオプションを選択します。
   - **名前**：ARIA アクセシビリティラベルの名前を使用する場合は、このオプションを選択します。
   - **なし**：ARIA アクセシビリティラベルに追加しない場合は、このオプションを選択します。

### 「スタイル」タブ {#styles-tab}

![「スタイル」タブ](/help/adaptive-forms/assets/switch-styles.png)

- **ラベルを非表示** - スイッチコンポーネントのラベルを非表示にするには、このオプションを選択します。

- **ラベルを表示** - スイッチコンポーネントのラベルを表示するには、このオプションを選択します。

## デザインダイアログ {#design-dialog}

デザインダイアログでは、スイッチコンポーネントの CSS スタイルを定義および管理できます。

### 「スタイル」タブ {#styles-design-tab}

アダプティブフォームのスイッチコアコンポーネントは、AEM の[スタイルシステム](/help/get-started/authoring.md#component-styling)をサポートしています。

![デザインダイアログ](/help/adaptive-forms/assets/checkbox-style.png)

- **デフォルトの CSS クラス**：アダプティブフォームのスイッチコアコンポーネントに、デフォルトの CSS クラスを指定できます。

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
