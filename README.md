# dxf4segmentation

## 概要

- `.sim` ファイルをドラッグ＆ドロップでアップロードし、オフセット計算後 `.dxf` ファイルとしてダウンロードできるWebツール
- GitHub Pagesで公開可能なシンプル構成
- 元ポリゴン（center.dxf）、内側5mmオフセット（inter.dxf）、外側5mmオフセット（outer.dxf）の3種類のDXFを自動出力
- SIMA→DXF変換時はXY座標を反転（SIMAのX→DXFのY、SIMAのY→DXFのX）

## 処理フロー（図解）

```mermaid
flowchart TD
    A[.simファイルをドラッグ＆ドロップ] --> B[.simをパースしてポリゴン座標配列に変換]
    B --> C[元ポリゴン(center)をDXF出力]
    B --> D[Clipper.jsで内外5mmオフセット計算]
    D --> E[内側(inter)ポリゴンをDXF出力]
    D --> F[外側(outer)ポリゴンをDXF出力]
    C & E & F --> G[3種類のDXFを自動ダウンロード]
```

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
4. オフセット計算後、`center.dxf`・`inter.dxf`・`outer.dxf` の3ファイルが自動でダウンロードされます

---

開発・テスト用に `input_data/` と `output_data/` ディレクトリを用意していますが、公開時は不要です。