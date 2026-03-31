# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

卒業旅行（2026年4月6〜7日、富士急・河口湖）の旅行しおりサイト。単一の静的 HTML ファイルで構成されており、ビルドツール・依存関係・テストフレームワークは一切使用していない。

## Structure

- `index.html` — HTML + CSS + JavaScript をすべて含む単一ファイル。GitHub Pages でホスティングされることを前提に `index.html` という名前になっている。

## Design Constraints

- **iPhone 最適化**: `safe-area-inset-*` / `env()` を使用したノッチ・Dynamic Island 対応済み。変更時はこれらの CSS 変数を維持すること。
- **フォントサイズ**: タップ領域は 44px 以上（Apple HIG 準拠）を維持すること。
- **コントラスト**: `--muted` は `#4a5568`（`#6b7280` からコントラスト改善済み）。薄くしない。
- **スタイル変数**: カラーパレットは `:root` の CSS 変数（`--fuji-blue`, `--sakura` など）で管理されている。直書きせず変数を使うこと。

## Deployment

GitHub Pages 経由で公開。`main` ブランチへの push で自動反映される（ルートの `index.html` がそのまま配信される）。
