# DB定義書
## ER図
[ER図はこちら](https://github.com/Aso2001174/2021sys-design/blob/main/db/ER%E5%9B%B3_%E3%82%AA%E3%83%AA%E3%82%B8%E3%83%8A%E3%83%AB%E3%82%B5%E3%82%A4%E3%83%88.md "ER図はこちら")

# DBテーブルカラム詳細一覧

# データベース詳細

*****
### 購入テーブル (d_purchase)
|和名|属性名|型|PK|NN|FK|
|---|---|---|:---:|:---:|:---:|
|オーダーID|order_id|bigint(20)|〇|〇||
|顧客コード|customer_code|varchar(50)||〇||
|購入日|purchase_date|date||〇||
|総額|total_price|int(11)||〇||

### 購入詳細テーブル (d_purchase_detail)
|和名|属性名|型|PK|NN|FK|
|---|---|---|:---:|:---:|:---:|
|オーダー詳細ID|detail_id|bigint(20)|〇|〇||
|オーダーID|order_id|bigint(20)|〇|〇|〇|
|商品コード|item_code|int(11)||〇||
|価格|price|int(11)||〇||
|数量|num|int(11)||〇||

### 顧客テーブル (m_customers)
|和名|属性名|型|PK|NN|FK|
|---|---|---|:---:|:---:|:---:|
|顧客コード|customer_code|varchar(50)|〇|〇||
|パスワード|pass|varchar(50)|〇|〇|〇|
|氏名|name|varchar(20)||〇||
|住所|address|varchar(100)||〇||
|電話番号|tel|varchar(20)||〇||
|メールアドレス|mail|varchar(100)||〇||
|削除フラグ|del_flag|int(11)||||
|登録日|reg_date|date||〇||

### お気に入りマスタ (m_favorite)
|和名|属性名|型|PK|NN|FK|
|---|---|---|:---:|:---:|:---:|
|お気に入りID|favorite_id|int(11)|〇|〇||
|氏名|name|varchar(20)||〇||
|登録日|reg_date|date||〇||

### 商品マスタ (m_items)
|和名|属性名|型|PK|NN|FK|
|---|---|---|:---:|:---:|:---:|
|商品コード|item_code|int(11)|〇|〇||
|商品名|item_name|varchar(50)||〇||
|価格|price|int(11)||〇||
|お気に入りID|favorite_id|int(11)||〇|〇|
|画像ファイル名|image|varchar(200)||〇||
|商品詳細説明|detail|varchar(500)||||
|削除フラグ|del_flag|int(11)||||
|登録日|reg_date|date||〇||
