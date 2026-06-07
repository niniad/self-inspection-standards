# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## プロジェクト

AWグループ（約200社）の財務「自主点検」実施基準を内製化するプロジェクト。
2026年3月期はデロイト主導の単発施策として実施。来期（2026年7月〜）から各社が自走できる内製運用へ移行する。

**期限**: 6月中に実施基準完成 → **7月 Q1（第1四半期）点検から内製運用開始**。

## どこに何があるか

| ファイル | 役割 |
|---|---|
| `@.claude/status.md` | **進捗・次アクション・期限** ← 作業前に必ず読む |
| `@input/input_index.md` | input/ 配下の全データファイルの説明（一次ソース一覧） |
| `@output/output_index.md` | output/ 配下の全成果物の説明（一次ソース明記） |
| `output/自主点検チェックリスト_v2.xlsx` | **最新編集ファイル**（3シート・82提出物・163CP） |
| `output/20260605時点QA管理表_統合ver.xlsx` | QA過去事例 2,514件（CP ブラッシュアップの素材） |
| `output/自主点検_統合マスタ.xlsx` | 旧バージョンの内部マスタ（v2 の生成元・今後は参照専用） |
| `output/自主点検概要説明書.md` | 成果物①（ほぼ完成） |

## インデックスの維持ルール

- `input/input_index.md` と `output/output_index.md` は常に最新の状態に保つ
- ファイルを追加・削除・名称変更した場合は必ず両ファイルを更新する
- output の各項目には**一次ソース**（input/ 配下の元データ）を明記する。中間加工ファイルやarchive/は一次ソースとして記載しない

## Python 実行環境

`C:/Users/ninni/scoop/apps/python/current/python.exe`。日本語出力時は `sys.stdout.reconfigure(encoding='utf-8')`。Excel処理は `openpyxl` / `pandas`。
