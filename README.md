# EmeraldBank - エメラルド銀行システム

エメラルドを預け入れ・引き出しできる銀行プラグインです。

## 概要

サーバー内の経済システムとして、エメラルドを通貨のように扱えます。GUIで直感的に操作でき、他のプラグインからAPIを通じて残高にアクセスできます。

## ダウンロード

[Releases](https://github.com/henntekosennsi1-rgb/EmeraldBank/releases)

## 主な機能

- エメラルドの預け入れ・引き出し
- プレイヤー間送金
- GUIベースの銀行インターフェース
- 財布アイテム（残高確認）
- 通帳アイテム（取引記録）
- ATM看板システム
- ランキング表示
- 他プラグイン向けAPI

## コマンド

| コマンド | 説明 |
|---------|------|
| `/emerald deposit <額>` | 預け入れ |
| `/emerald withdraw <額>` | 引き出し |
| `/emerald send <プレイヤー> <額>` | 送金 |
| `/emerald money` | 残高確認 |
| `/emerald gui` | GUI を開く |
| `/emerald wallet` | 財布アイテム取得 |
| `/emerald book` | 通帳アイテム取得 |
| `/emerald list` | 残高一覧 |
| `/emerald ranking` | ランキング |
| `/ed <額>` | 預け入れ（ショートカット） |
| `/ew <額>` | 引き出し（ショートカット） |

エイリアス: `/eb`

## API

他のプラグインからAccountRepositoryを通じて残高にアクセスできます。
```java
AccountRepository repo = EmeraldBank.getAccountRepository();
long balance = repo.getBalance(playerUUID);
repo.deposit(playerUUID, amount);
repo.withdraw(playerUUID, amount);
repo.transact(fromUUID, toUUID, amount);
```

## 対応プラグイン

- Tintiro2（チンチロ）
- その他のミニゲームプラグイン

## 動作環境

- Spigot/Paper 1.21.x
- Java 17以上

## コミュニティ

**Discord:** https://discord.gg/zYY55dzhjd

## ライセンス

All Rights Reserved
