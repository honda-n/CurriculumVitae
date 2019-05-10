# 職務経歴書

## 基本情報

|key|value|
|---|-----|
|Name|nao honda |
|Twitter|[@1wa46](https://twitter.com/1wa46)|
|Qiita|[1wa46](https://qiita.com/settings/account)
|MENTA|[Honda](https://menta.work/user/354)

## スキル
### 言語
- Swift
- Objective-c
- PHP
- Javascript ( + TypeScript)

### フレームワーク
- ReSwift
- ReactNative
- ionic4
- cordove
- stancilJS
- React.js
- Angular 6

## 強み
0-1フェーズに設計実装速度

## やったことはないが興味があるもの

だれかの課題解決になるサービスを作りたい！携わりたい!

## 職務経歴

### 2014/03 - 2015/09: KDDIエボルバ

職務: iOS アプリケーションエンジニア

#### シフトカレンダーアプリ
##### 担当
iOSネイティブアプリケーション

##### 概要
既存のAndroid版の移植プロジェクトでした。サーバー通信がないオフラインで動作可能なアプリケーションの為、アプリ内にDBにSQLiteを選定して構築を行いました。リリース後、機能追加等でデータ構造が複雑化していまい、スケジュール読み込みパフォーマンスの指摘があった為、RealmへDBを移行を行いました。
ローカルのDBの置き換えとなるので、DBの構造変更、Realmへのリプレイスを分けてリリースし、無事移行させることができました。
又、1系でObjective-cで作られていたアプリを、Swift1.2 -> Swift2系までバージョンを上げて管理を行い、メンテナンス性を保持する為に修正を行いました。

### 2015/10 - 現在 : 株式会社カタリストシステム

職務: アプリケーションエンジニア

#### タスク管理サービス開発

##### 担当
PWAアプリケーション(iOS側は、ハイブリッドアプリケーション)
バックエンド(API(PHP), websocket(Node.js))
フロントエンド(Angular6)

##### 概要
自社開発のタスク管理アプリケーションをモバイル向けへ対応する為、PWA版を新規構築するプロジェクトへ途中からジョイン。
iOS側のservice workerの対応がすすんでいない為(PUSH未対応、常に初期画面からリロードされる等)、ハイブリッドアプリを構築する流れとなり、当初は設計構築を担当しました。ionic4推奨のcapacitorがbata版だったため、cordovaを選択し、capacitorと同様の挙動を再現する為、cordova pluginを選定し構築しました。
ionic4バージョンアップに合わせ、更新が行えるように、CIサーバーを整備し、b版配布には、CIサーバー上に設定したFastlaneで行い、自動化しました。
wab側のAnguler6側にも参加し、wabアプリ、スマホアプリ、バックエンド、全てワントップで開発に携わっています。


#### B to B to C 開発(モビリティ系)

##### 担当
ユーザーアプリケーション(iOS)
業務アプリケーション(iOS, Android)
API
管理画面

##### 概要
インフラ構築以外のところの設計とコーディングを担当しました。
ベースとなるが業務の管理画面は、フロントエンドはPHPとReact.jsで構築し、リアルタイムな同期が必要な要件だった為、工数の兼ね合いからFirebaseを採用し構築しました。モバイル、管理画面のリアルタイムな反映には、タイムゾーン問題やタイミング等の問題があり苦労しましたが、DBトランジションとJSを有効に活用して、不具合なく動作しています。

ユーザーアプリケーションほぼ一人実装を担当したため、以前の開発で、AppleMVCへ限界を感じていたため、Redux を導入し、アーキテクチャの大幅な変更を行いました。Firebaseとは相性がよく、頻繁に変更される内容の同期もよいとなり、2ヶ月ほどで、b版を社内へ配布することができました。
b版配布には、CIサーバー上に設定したFastlaneで行い、自動化しました。

業務アプリは要件定義から設計、実装まで任され、リーダー職任されました。
要件上、iOSとAndroidの構築が必要な関係上、人員、管理の観点から、1ソースで構築することを検討しました。検討の結果、Reactの経験者が社内に多く、バフォーマンスの問題も検証の結果問題ないと判断し、
React Nativeで構築しました。結果97%同一のコードで動作し、3ヶ月程度運用していますが、問題なく要望に対応し、改善をおこなうことが出来ています。
す。


#### 不動産管理システム

##### 担当
PHPアプリケーション
PHPを使った管理画面開発で、物件管理画面を担当。

##### 概要
旧システムからの移行案件で、旧システムの機能を踏襲しつつ、新システムでは、肥大化してDBカラムを整理しテーブル分割を行いました。物件テーブルは100カラム以上から、本体テーブルは20カラム程度になり、メモリに乗るようになった為、検索速度を改善することができました。
フロント側は、jQueryで構築されていましたが、React.jsを使ってリプレイスすることで、ES5で記述可能となり、メンテナンス性が向上することができました。
大量に画像がサーバー上で管理されており、肥大化してしまっていました。
一括でS3へアップロードする旧システム作業は、仕様書のない状態から、Codeベースで解読し、９割程度一括で移行し管理機能を導入したことで、管理コストをへらすことに貢献できました


#### 販促アプリケーション開発

##### 担当
iOSアプリネイティブアプリアプリケーション
PHP API

#### 概要
iOSはSwift2系を使用して構築していましたが、自社内にObjective-cの資産が多くあった為、cocoapods経由で導入できるようにLibraries化を行いました。
コア機能として画像加工(フィルター、透過処理)機能があり、調査の結果OpenCVを使用することで再現が可能とわかりました。C++でOpenCVを扱い、Objective-cでLibraries化し、Swiftで使用する流れで構築することができました。しかし、画像解像度によってピクセル単位で処理を行う、OpenCV上でクラッシュするデバック中に多発してしまいました。検証の結果、一定サイズでリサイズすることで負荷を軽減することが出来たため、トリミングUIの追加、圧縮処理を追加し、解決しました。
