# dxf4segmentation

## 概要

- `.sim` ファイルをドラッグ＆ドロップでアップロードし、オフセット計算後 `.dxf` ファイルとしてダウンロードできるWebツール
- GitHub Pagesで公開可能なシンプル構成

## ディレクトリ構成

```
├── index.html         # メインページ（UI・JS含む）
├── plan.md            # 仕様・設計メモ
├── README.md          # プロジェクト説明
├── input_data/        # サンプル .sim ファイル（任意）
│   └── plygon.sim
├── output_data/       # サンプル .dxf ファイル（任意）
│   └── polygon.dxf
```

## 使い方

1. GitHub Pagesで本リポジトリを公開
2. ブラウザで `index.html` を開く
3. `.sim` ファイルをドラッグ＆ドロップ
4. オフセット計算後、`.dxf` ファイルが自動でダウンロードされます

---

開発・テスト用に `input_data/` と `output_data/` ディレクトリを用意していますが、公開時は不要です。