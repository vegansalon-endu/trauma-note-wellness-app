# Trauma Note Wellness App

ユーザーの心と体の健康をサポートするための統合ウェブアプリケーション

## 📋 プロジェクト概要

このプロジェクトは、Firebase をバックエンドとして使用し、以下の機能を統合したウェルネスプラットフォームです：

### 🌟 主要機能

1. **TraumaNote（AI対話型トラウマノート）**
   - トラウマの記録と管理
   - AIとの対話によるトラウマ解消サポート
   - 安全なクラウドストレージ

2. **AI心と体の根本原因診断**
   - 多角的な健康状態分析
   - パーソナライズされた改善プラン提案
   - 診断結果の永続保存

3. **進捗管理システム**
   - 日々の食生活・体調・気分の記録
   - カレンダー形式での視覚的な進捗確認
   - データ連携による総合的な健康管理

## 🛠 技術スタック

- **フロントエンド**: HTML5, CSS3 (Tailwind CSS), JavaScript, React
- **バックエンド**: Firebase
  - Authentication: メール/パスワード認証
  - Firestore: NoSQLデータベース
  - Cloud Functions: サーバーレス処理
  - Hosting: 静的サイトホスティング
- **AI**: Google Gemini API
- **デプロイ**: Firebase Hosting

## 📊 データ構造

```
/users/{uid}/
├─ profile: { ... }
├─ trauma_notes/
│   └─ {noteId}: { content, timestamp, chatHistory }
├─ ai_diagnoses/
│   └─ {diagId}: { report, scores, createdAt }
└─ progress_records/
    └─ {dateKey}: { diet, mood, health, memo }
```

## 🚀 デプロイ

- **本番URL**: https://trauma-note-app.web.app/
- **開発環境**: ローカル開発サーバー

## 🔒 セキュリティとプライバシー

- **データの機密性**: TraumaNoteの内容は厳格に保護
- **アクセス制御**: Firebase Authenticationによる認証
- **データ暗号化**: Firebase標準の暗号化

## 📝 開発ガイドライン

### 重要な制約事項

1. **TraumaNoteデータの取り扱い**
   - ノートの内容（contentフィールド）は他のアプリやAIに渡さない
   - メタデータ（記録日、記録の有無）のみ連携可能

2. **AIとの連携**
   - Cloud Function `generateAiReport` を使用
   - 直接的なAPI呼び出しは禁止

## 🎯 今後の展望

- データ連携機能の強化
- より高度な分析とレコメンデーション
- ユーザー体験の向上

---

🤖 Generated with [Claude Code](https://claude.ai/code)

Co-Authored-By: Claude <noreply@anthropic.com>