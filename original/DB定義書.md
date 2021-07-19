# DB定義書
## ER図
[ER図はこちら](https://github.com/Aso2001413/2021sys-design/blob/main/original/%E3%82%AA%E3%83%AA%E3%82%B8%E3%83%8A%E3%83%AB%E3%82%B5%E3%82%A4%E3%83%88ER%E5%9B%B3.md "ER図はこちら")

## DBテーブルカラム詳細一覧

### 購入テーブル（d_purchase）

|和名|属性名(カラム名)|型         |PK  |NN |FK |
|---|---          |---        |--- |---|---|
|オーダーID|order_id     |bigint(20) |o   |o  |   |
|顧客コード|custimer_code|verchar(50)|    |o  |   |
|購入日|purchase_date|date       |    |o  |   |
|総額|total_price  |int(11)    |    |o  |   |

### 購入詳細（d_purchase_detail）

|和名|属性名(カラム名)|型         |PK  |NN |FK |
|---|---          |---        |--- |---|---|
|オーダー詳細ID|detail_id    |bigint(20) |o   |o  |o  |
|オーダーID|order_id     |bigint(20) |o   |o  |   |
|商品コード|item_code    |int(11)    |    |o  |   |
|価格|price        |int(11)    |    |o  |   |
|数量|num          |int(11)    |    |o  |   |

### 顧客マスタ(m_customers)

|和名|属性名(カラム名)|型         |PK  |NN |FK |
|---|---          |---         |--- |---|---|
|顧客コード|custimer_id  |verchar(50) |o   |o  |   |
|パスワード|pass         |verchar(50) |o   |o  |o  |
|氏名|name         |verchar(20) |    |o  |   |
|住所|adress       |verchar(100)|    |o  |   |
|電話番号|tel          |verchar(20) |    |o  |   |
|メールアドレス|mail         |verchar(100)|    |o  |   |
|削除フラグ|del_flag     |int(11)     |    |   |   |
|登録日|reg_date     |date        |    |o  |   |


### カテゴリマスタ(m_category)

|和名|属性名(カラム名)|型         |PK  |NN |FK |
|---|---          |---        |--- |---|---|
|カテゴリID|category_id  |int(11)    |o   |o  |   |
|氏名|name         |verchar(50)|    |o  |   |
|登録日|reg_flag     |date       |    |o  |   |

### 商品マスタ(m_customers)

|和名|属性名(カラム名)|型         |PK  |NN |FK |
|---|---          |---         |--- |---|---|
|商品コード|item_code    |int(11)     |o   |o  |   |
|商品名|item_name    |verchar(50) |o   |o  |   |
|価格|price        |int(11)     |    |o  |   |
|カテゴリID|category_id  |int(11)     |    |o  |o  |
|画像ファイル名|image        |verchar(200)|    |o  |   |
|商品詳細説明|detail       |verchar(500)|    |   |   |
|削除フラグ|del_flag     |int(11)     |    |   |   |
|登録日|reg_date     |date        |    |o  |   |
