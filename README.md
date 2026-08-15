# Kinga!!

お正月のミニゲームアプリ。ポチ袋を連打してスコアを競い、その日のランキングに載ります。

https://kinga-n43year.vercel.app/

## 機能

- ポチ袋連打のゲーム（`/game`）とリザルト表示（`/game/result`）
- 当日分に絞ったランキング（`/ranking`, `/choice`）と TOP5 表示
- スコアのシェア（`/game/share`）
- 遊び方ページ（`/howto`）

## 設計で考えたこと

- 「多くの人に気軽に触ってもらう」ことを狙い、ユーザー登録やログインを挟まず、開いたらすぐ遊べる構成にしました
- ランキングを当日分に絞ることで、実際に遊んでいる人が見える／競える状態を作っています
- スコアとクリック数は Zustand で保持し、リトライ時の状態管理を軽量に済ませています

## 技術スタック

T3 Stack（create-t3-app）ベース。

| 領域 | 技術 |
| --- | --- |
| フレームワーク | Next.js (App Router) |
| 型安全なAPI | tRPC + Zod |
| DB / ORM | Supabase (PostgreSQL) + Drizzle ORM |
| 状態管理 | Zustand |
| スタイリング | Tailwind CSS |
| デプロイ | Vercel |

## 開発

```sh
npm install
npm run db:push
npm run dev
```
