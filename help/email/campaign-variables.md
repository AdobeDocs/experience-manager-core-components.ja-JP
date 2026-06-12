---
title: Campaign 変数
description: キャンペーン変数をプレースホルダーとして使用して、パーソナライズされたメールコンテンツを作成します。
role: Developer, Admin, User
exl-id: 124ff5bf-6612-4baf-b0ff-6b1a95b455c1
index: false
TQID: https://experienceleague.adobe.com/MB6K-S4DZbsD3puXls8w4rWi6posFFLxJRewKORMkxA
product_v2: id: c45915cf-e157-4af7-a80d-97b905bcb3a5id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: eb3ad9f8-54a2-45f3-abb1-d3976415a718
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: ce44533e-8ec8-4e11-a9e9-78b0fe561832id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 296
ht-degree: 100%

---

# Campaign 変数 {#campaign-variables}

キャンペーン変数を使用してパーソナライズされたメールコンテンツを作成します。 キャンペーン変数は、Adobe Campaign の値のプレースホルダーとして機能し、メールコンテンツに挿入することができます。 コンテンツが Adobe Campaign 経由で送信されると、Campaign は、これらの変数を受信者のパーソナライズされたコンテンツで置き換えます。

## 使用方法 {#usage}

メールコアコンポーネントを使用すると、共通のテキストフィールドの横にあるパーソナライズ機能ボタンを使用して、キャンペーン変数に簡単にアクセスできます。 ボタンを押すと、パーソナライズ機能フィールドを選択できるダイアログが表示されます。

使用可能なパーソナライズ機能フィールドのリストが Adobe Campaign インスタンスと同期されます。 このフィールドは、スキーマ `nms:seedMember` 内の Adobe Campaign で管理されます。 `nms:seedMember` のすべてのフィールドはまた、受信者テーブルにも存在する必要があります。

## Adobe Campaign の変数ダイアログを選択 {#dialog}

「Adobe Campaign の変数を選択」ダイアログは、メールコアコンポーネントの多くの編集ダイアログで使用できます。 該当するフィールドの横にある「**Adobe Campaign の変数を選択**」アイコンをクリックするだけで、これを使用することができます。 このアイコンは 2 つの形式で表示されます。

![Adobe Campaign ボタン](/help/email/assets/campaign-button.png)
![Adobe Campaign 変数を選択アイコン](/help/email/assets/select-adobe-campaign-variable-icon.png)

両方のアイコンをクリックすると、**Adobe Campaign の変数を選択** ダイアログが開きます。

![Adobe Campaign の変数を選択](assets/select-campaign-variable-dialog.png)

列表示を使用して、挿入する変数を見つけます。 列内のノードをクリックすると、その子が右側の新しい列に表示されます。 これにより、変数コンテンツ構造をナビゲートすることができます。

挿入する変数を選択し、ダイアログの右上にあるチェックマークをクリックします。

![Adobe Campaign の変数を選択](assets/select-campaign-variable-dialog-selected.png)

次に、変数がメールコアコンポーネントの編集ダイアログのフィールドに挿入されます。

![編集ダイアログに挿入されるCampaign の変数](assets/campaign-variable.png)

ダイアログの左上にある X をクリックすると、いつでもキャンセルしてダイアログを閉じることができます。
