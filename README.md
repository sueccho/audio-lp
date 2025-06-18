# 音声ガイド付き採用ランディングページテンプレート

音声ナレーションとビジュアルを連動させた、採用向けランディングページのテンプレートです。HTML、CSS、JavaScriptのみで実装されており、様々な業種・企業で再利用可能な構成となっています。

## 特徴

- 音声ガイドとビジュアルの連動による没入感のある体験
- レスポンシブデザインによるモバイル対応
- シンプルでカスタマイズしやすい設計
- 外部ライブラリに依存しない実装
- GitHubリポジトリからの音声・画像ファイルの読み込みに対応
- Google Apps Script (GAS) での実装を考慮した設計

## ページ構成

1. **イントロセクション**
   - 企業名とコンセプトの紹介
   - イヤホン推奨メッセージ
   - 音声ガイド開始ボタン

2. **仕事内容セクション**
   - 3つの主要事業の紹介
   - 音声に連動したカードのハイライト表示
   - 対応する画像のフェードイン表示

3. **社員の声セクション**
   - 3名の社員インタビュー
   - 音声に連動したカードのハイライト表示
   - 社員写真のフェードイン表示

4. **福利厚生セクション**
   - 4つの主要な福利厚生の紹介
   - アイコンと音声による説明
   - ハイライト表示による強調

5. **1日の流れセクション**
   - タイムライン形式での業務スケジュール紹介
   - 音声に連動した項目のハイライト表示

6. **応募案内セクション**
   - 応募ボタンとメッセージ
   - 音声ガイド終了時のアニメーション効果

## 技術仕様

### 使用技術
- HTML5
- CSS3
- JavaScript (ES6+)
- Google Apps Script (GAS) 対応

### 主要機能
- 音声再生制御（`<audio>`タグ使用）
- スクロール位置の自動調整
- セクション間のナビゲーション
- プログレスバー表示
- 要素のハイライト表示
- 画像のフェードイン/アウト

## 使用方法

1. リポジトリをクローン
```bash
git clone [リポジトリURL]
```

2. 音声ファイルの準備
- GitHubリポジトリに以下の音声ファイルをアップロード
  - `section-intro.mp3`
  - `section-work.mp3`
  - `section-employees.mp3`
  - `section-benefits.mp3`
  - `section-schedule.mp3`
  - `section-cta.mp3`
- 音声ファイルのURLを`index.html`内の`audioConfig`に設定
```javascript
audioFile: 'https://raw.githubusercontent.com/[ユーザー名]/[リポジトリ名]/main/[ファイル名].mp3'
```

3. 画像ファイルの準備
- GitHubリポジトリに以下の画像ファイルをアップロード
  - 仕事内容画像：`work01.jpg`、`work02.jpg`、`work03.jpg`
  - 社員写真：`staff-tanaka.jpg`、`staff-sato.jpg`、`staff-yamada.jpg`
- 画像ファイルのURLを`index.html`内の`audioConfig`に設定
```javascript
image: 'https://raw.githubusercontent.com/[ユーザー名]/[リポジトリ名]/main/images/[ファイル名].jpg'
```

4. Google Apps Script (GAS) での実装
- GASプロジェクトを作成
- `index.html`の内容をGASのHTMLファイルとして実装
- 音声・画像ファイルはGitHubのraw URLを使用
- 必要に応じてGASの機能（フォーム送信など）を追加

5. カスタマイズ
- `index.html`の内容を企業情報に合わせて編集
- `audioConfig`オブジェクトの設定を音声ファイルの長さに合わせて調整
- CSSでデザインをカスタマイズ

## カスタマイズポイント

### 音声設定
```javascript
const audioConfig = {
    sections: [
        {
            id: 'section-id',
            audioFile: 'https://raw.githubusercontent.com/[ユーザー名]/[リポジトリ名]/main/[ファイル名].mp3',
            duration: 秒数,
            elements: [
                {
                    id: 'element-id',
                    startTime: 開始秒数,
                    duration: 表示秒数,
                    image: 'https://raw.githubusercontent.com/[ユーザー名]/[リポジトリ名]/main/images/[ファイル名].jpg'
                }
            ]
        }
    ]
};
```

### スタイルカスタマイズ
- カラースキーム
- フォント
- アニメーション効果
- レイアウト

## 注意事項

- 音声ファイルは適切なライセンスのものを使用してください
- 画像ファイルは最適化してから使用してください
- モバイル対応のため、画像サイズに注意してください
- GitHubのraw URLを使用する際は、リポジトリが公開されていることを確認してください
- GASでの実装時は、CORSポリシーに注意してください

## ライセンス

MITライセンス

## 作者

[あなたの名前/組織名]
