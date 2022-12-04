# 概要
Laravelを用いてRestAPIを実現するためのサンプル。
## 参考にしたサイトページ
https://www.twilio.com/blog/building-and-consuming-a-restful-api-in-laravel-php-jp

# 動作確認環境
- Laradock
- nginx (Ver 1.23.x)
- MySQL (Ver 8.0.x)
- Laravel (Ver 8.83.x)

# 起動
```bash
#laradock環境に入る
cd /laradock

# コンテナ起動
docker-compose up -d nginx mysql

# workspaceのコンテナに入って操作
docker-compose exec --user=laradock workspace bash

# MySQLのコンテナに入って操作
docker-compose exec mysql bash 
# MySQLにログイン
 mysql -h 127.0.0.1 -P 3306 -u root -p
```

# 確認
- get http://localhost/api/students
  - 全ての学生レコードを取得 
- get http://localhost/api/students/{id}
  - 対象の学生レコードを取得
- post http://localhost/api/students'
  - 学生レコード作成
- put('http://localhost/api/students/{id}'
  - 対象の学生レコード更新
- delete http://localhost/api/students/{id}
  - 対象の学生レコード削除