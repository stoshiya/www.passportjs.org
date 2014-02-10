---
layout: 'guide'
title: 'はじめに'
---

### はじめに

Passport は [Node](http://nodejs.org/) のための認証ミドルウェアです。
認証リクエストをおこなうための必要最低限の機能をもつように設計されています。
この Passport の素晴らしいところは、認証リクエスト以外の全ての機能をアプリケーション側で自由に実現できるということに尽きます。
このように Passport とアプリケーションを疎結合に保つことによって、コードは簡潔になり保守性が高まることでしょう。
さらに、Passport はとても簡単にアプリケーションに組み込むことができるのです。

モダンな Web アプリケーションは多くの認証形態を採用しています。
これまで、ユーザーはユーザーIDとパスワードでログインしてきました。
しかし、いまどきは[Facebook](https://www.facebook.com/) や [Twitter](https://twitter.com/) などのソーシャルネットワーキングと連携し、 [OAuth](http://oauth.net/) を使ったシングルサインオンをおこなう手法が一般的に普及してきています。
これらの API を公開しているサービスでは、アクセスを保護するためにトークンベースの認証情報を必要としています。

Passport はアプリケーション毎に、それぞれ適した認証があることを踏まえてつくられています。
_アプリケーションへの認証機能の組み込みは、ストラテジー_と呼ばれる独立した認証メカニズムのモジュールを選ぶだけで実現できます。

認証作業は複雑かもしれませんが、何もコードまでも複雑なものになる必要はもうないのです。

```javascript
app.post('/login', passport.authenticate('local', { successRedirect: '/',
                                                    failureRedirect: '/login' }));
```

#### インストール

```bash
$ npm install passport
```