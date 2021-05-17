```uml
@startuml
ユーザー -> Webサーバー: お気に入りに追加
Webサーバー -> DBサーバー: 追加処理
DBサーバー -> DBサーバー: 追加処理
DBサーバー -> Webサーバー: 追加結果
@enduml
```
