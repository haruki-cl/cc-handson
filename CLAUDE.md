# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## リポジトリ概要

Claude Code ハンズオン Section 1「Claude Code の基本」（85分）の教材リポジトリ。インターンシップ向けのスピンオフで、業務での活用を前提にした書き方はしない。ビルド・テスト・依存パッケージは無く、静的 HTML 1枚と画像のみで構成される。閲覧確認は `open index.html`。

## ファイル構成と編集ルール

- `index.html`：講義資料本体。**内容の変更はここに直接行う**（Markdown のソースは無い）
- `Image/`：スクリーンショット・図版置き場。ファイル名は ASCII セーフ（例: `status.png`, `context-diagram.svg`）を維持する。index.html から参照しなくなった画像は削除する

## スタイル・表記

- index.html は外部依存なしの単一ファイル。CSS はファイル内に埋め込んであり、デザイントークン（テラコッタ基調 `--accent: #d97757`、`.callout` / `.prompt-box` / `.lesson` 等のコンポーネント）を使う
- 日本語テキストは Unicode **NFC** で統一する（過去に NFD（濁点分離）混入で Edit の文字列一致が失敗した経緯あり）
- 時間配分の合計は 60〜90分の範囲に収める（現在は 85分）。章の分数を変えたら、時間配分の表・各章の見出し・冒頭のバッジの分数をそろえる
- 演習の題材は `hello-world`（シェルスクリプトの Hello world と CLAUDE.md の演習）と `mini-game`（テトリス風の落ち物パズル。index.html・style.css・game.js の3ファイル）。コマンド例・プロンプト例はこの題材に合わせる
- 説明は前から順に積み上げる。「後述」や後ろの章番号への参照は書かない（後ろの章から前の章を振り返る参照はよい）。図版（SVG）の文字も同じ
- Section 2 以降の内容には触れない。「Section 2 で扱う」のような後続 Section への参照・予告は書かない
- 単独の講座として見せるため、ページ上では「Section 1」の表記も使わない（タイトルは「Claude Code の基本」）

## Git / GitHub 運用

- このリポジトリは `cl-y-arai/cc-handson` のフォークで、origin は `haruki-cl/cc-handson`
- **フォーク元 `cl-y-arai/cc-handson` へは Pull Request を絶対に送らない**。push も PR も宛先は常に `haruki-cl/cc-handson` に限る
- フォークでは `gh pr create` がフォーク元を PR の宛先に選ぶことがある。PR を作るときは必ず `--repo haruki-cl/cc-handson --base main` を明示し、作成前に宛先が `haruki-cl/cc-handson` であることを確認する
