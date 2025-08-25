# 🎨 三角形メッシュ画像変換ツール

Delaunay三角分割を使用して、画像をアーティスティックなローポリゴン三角形メッシュエフェクトに変換するWebベースのツールです。

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)

基本的にCLAUDEに書かせました。

## ✨ 機能
画像ファイルから画素を読み取り、Delaunay三角分割をしてポリゴンメッシュ的なエフェクトに変化する。

## 🚀 クイックスタート

### オンラインデモ
任意のモダンWebブラウザで`index.html`を開くだけです。アプリケーションは自動的にデモ画像を読み込みます。

### ローカル開発
```bash
# リポジトリをクローン
git clone https://github.com/a-yasui/triangle-mesh-html.git

# プロジェクトに移動
cd triangle-mesh-html

# ブラウザで開く（macOS）
open index.html

# またはローカルサーバーを使用
php -S localhost:8000
# その後 http://localhost:8000 にアクセス
```

### 色の近似
各三角形はその境界内のピクセルの平均色で塗りつぶされ、特徴的なローポリゴンを作り出します。
## 🛠️ 技術詳細

- **言語**: Pure JavaScript (ES6+)
- **レンダリング**: HTML5 Canvas API
- **エクスポート形式**: SVG (Scalable Vector Graphics)
- **ブラウザサポート**: Chrome、Firefox、Safari、Edge（最新バージョン）

## 📝 ライセンス

このプロジェクトはオープンソースで、MITライセンスの下で利用可能です。
