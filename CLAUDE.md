# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

zenn.devに投稿する記事（articles）と本（books）を管理するリポジトリ。Zenn CLIを使ってコンテンツの作成・プレビューを行う。

## Setup

```bash
npm init --yes
npx zenn init
npm install zenn-cli
```

## Common Commands

```bash
# 記事の新規作成
npx zenn new:article --slug <slug>

# 本の新規作成
npx zenn new:book --slug <slug>

# ローカルプレビュー（http://localhost:8000）
npx zenn preview
```

## Content Structure

- `articles/` — 記事ファイル（Markdown、`<slug>.md`）
- `books/` — 本（各本がサブディレクトリ）
- `images/` — 画像ファイル

## Article Frontmatter

記事のMarkdownファイル先頭にはfrontmatterが必要:

```yaml
---
title: "記事タイトル"
emoji: "😸"
type: "tech" # tech or idea
topics: ["topic1", "topic2"]  # 最大5つ
published: true  # falseで下書き
---
```

## Conventions

- slugは半角英数字（a-z0-9）・ハイフン・アンダースコアのみ、12〜50文字
- 画像は `/images/` ディレクトリに配置し、記事から `![](/images/xxx.png)` で参照
- GitHub連携により、mainブランチへのpushで自動的にzenn.devに反映される
- 記事の言語は日本語
