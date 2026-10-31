# task-crud-practice

## 概要

COACHTECH 教材 Tutorial 11-2「タスク管理APIのCRUD実装」で作成した成果物です。
タスク管理APIのCRUD操作を実装しました。

## 使用技術

- PHP 8.x
- Laravel 10.x
- REST API（CRUD）
- API Resources
- Laravel Sail
- Postman

## 実装するAPI:

HTTPメソッド URL 操作 ステータスコード

- GET /api/tasks 一覧取得 200
- POST /api/tasks 作成 201 / 422
- GET /api/tasks/{id} 詳細取得 200 / 404
- PUT /api/tasks/{id} 更新 200 / 404 / 422
- DELETE /api/tasks/{id} 削除 204 / 404

## 実装内容

- APIリソースコントローラーによるCRUD処理
- `Route::apiResource()` によるルーティング設定
- Eloquent ORMを使用したデータベース操作
- `$request->validate()` によるバリデーション
- JSON形式でのレスポンス返却
- HTTPステータスコードによる処理結果の通知
- 存在しないタスクに対する404エラー処理

## 動作確認

Postmanを使用して、各APIエンドポイントにリクエストを送信し、正常系・異常系の動作を確認しました。

- GET：タスク一覧・詳細の取得（200）
- POST：タスクの新規作成（201）
- PUT：タスクの更新（200）
- DELETE：タスクの削除（204）
- バリデーションエラー時の422レスポンス
- 存在しないタスクを指定した場合の404レスポンス

各リクエストに対するJSONレスポンスとHTTPステータスコードを確認しました。

## 学習したこと

- RESTful APIの基本的な設計
- CRUDとHTTPメソッドの関係
- LaravelでのAPIルーティング
- コントローラーでのリクエスト処理
- バリデーションによる入力値の検証
- 正常系・異常系を考慮したAPIの実装
- Postmanを使用したAPIの動作確認
