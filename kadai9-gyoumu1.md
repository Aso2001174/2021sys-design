```
@startuml
ユーザー -> Webサーバー: 商品検索
Webサーバー -> DBサーバー: 検索処理
DBサーバー -> DBサーバー: 検索処理
DBサーバー -> Webサーバー: 検索結果
Webサーバー -> ユーザー: 検索結果
@enduml
```
