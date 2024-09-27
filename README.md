# minimum-chat-app

## 手順メモ
1. laravelインストール
```
composer create-project laravel/laravel app-base
```

2. プロジェクト構成の整理
```
shopt -s dotglob && mv app-base/* .
```
```
rm -rf .github
```

3. プロジェクトの起動確認
```
php artisan serve
```
`http://127.0.0.1:8000` でアクセスできたらOK

4. Lravel Reverbのセットアップ
Lravel Reverbは今年リリースされた Laravel 11 と一緒に登場した、 Laravel 公式の WebSocket サーバ機能

```
php artisan install:broadcasting
```

選択肢は以下
```
 ┌ Would you like to install Laravel Reverb? ───────────────────┐
 │ Yes                                                          │
 └──────────────────────────────────────────────────────────────┘
```
```
 ┌ Would you like to install and build the Node dependencies required for broadcasting? ┐
 │ Yes                                                                                  │
 └──────────────────────────────────────────────────────────────────────────────────────┘
```
※ `laravel-echo` と `pusher-js` がインストールされる

5. コード書き換え
laravel側とjs少し追記

6. Laravel Reverve起動
```
php artisan reverb:start --debug
```

7. vite ローカルサーバ起動
```
npm run dev
```
