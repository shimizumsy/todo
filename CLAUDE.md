# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## コマンド

- `npm run dev` — Vite開発サーバーを起動（HMR対応）
- `npm run build` — `tsc -b`で型チェック後、Viteでバンドル
- `npm run lint` — ESLintを実行
- `npm run preview` — 本番ビルドをローカルでプレビュー

## アーキテクチャ

React 19 + TypeScript + ViteのSPA。エントリーポイントは`src/main.tsx`で、`<App />`を`index.html`にレンダリングする。

TypeScriptはstrictモードで、`noUnusedLocals`と`noUnusedParameters`が有効。`verbatimModuleSyntax`を使用しているため、型のみのインポートには`import type`を使うこと。
