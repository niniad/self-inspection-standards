# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## プロジェクト

AWグループ（約200社）の財務「自主点検」実施基準を内製化するプロジェクト。
2026年3月期はデロイト主導の単発施策として実施。来期（2026年7月〜）から各社が自走できる内製運用へ移行する。

**期限**: 6月中に実施基準完成 → **7月 Q1（第1四半期）点検から内製運用開始**。

## 設計上の非自明なルール（壊してはいけない）

1. **「対象外」は廃止**。残高がない場合も「該当なし宣言」を正式提出物として格納する（適用パスBモデル）。詳細: `@自主点検実施基準_設計書.md` セクション3-1。
2. **要否は計算で導出**。200社×28項目×CPのマトリクスを手動で維持しない。
3. **提出フォルダは論理パスで設計**。SharePoint廃止可能性があるため物理運用に依存しない。

## どこに何があるか

| ファイル | 役割 |
|---|---|
| `@.claude/status.md` | **進捗・次アクション・期限** ← 作業前に読む |
| `@自主点検実施基準_設計書.md` | 設計仕様書（テーブル定義・判定フロー・未決事項） |
| `@input/input_index.md` | input/ 配下の全データファイルの説明 |
| `output/自主点検_提出成果物一覧.xlsx` | 提出物マスタの土台（82件×17列） |
| `output/自主点検概要説明書.md` | 成果物①（ほぼ完成） |
| `archive/自主点検_実施基準マスタ.xlsx` | CPマスタの土台（19/28項目のみ・参照専用） |

Python実行: `C:/Users/ninni/scoop/apps/python/current/python.exe`。日本語出力時は `sys.stdout.reconfigure(encoding='utf-8')`。Excel処理は `openpyxl` / `pandas`。
