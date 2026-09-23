# Unit 1: 初めてのAndroidアプリ

## MainActivity.kt

Androidアプリ起動時に最初に呼び出されるファイル。

### onCreate()

- Androidアプリのエントリポイント
- Activityの作成時に呼び出される
- 初期設定や画面表示の準備を行う

### setContent()

- Jetpack Composeで画面を描画するために使用する
- コンポーズ可能な関数を指定してUIを構築する

### コンポーズ可能な関数（Composable Function）

- `@Composable` アノテーションが付いた関数
- UIを宣言的に記述するための関数
- 基本的にUIを描画することを目的とする

例

```kotlin
@Composable
fun Greeting(name: String) {
    Text(text = "Hello $name")
}
```

### アノテーション

プログラムのコードに対して付与するメタデータ。

#### @Composable

`@Composable` を付与すると Compose コンパイラが特別な処理を追加する。

- UIツリーへの登録
- パラメータ変更の監視
- 再コンポジションの最適化
- 不要な再描画のスキップ

---

## ユーザーインターフェース（UI）

画面上に表示される要素と、それらの配置のこと。

### UIコンポーネント

アプリ上に表示される要素。

例

- Text
- Image
- Button
- Card
- TextField

---

## Jetpack Compose

AndroidのUIを構築するための最新のツールキット。

### 特徴

- 宣言的UI
- Kotlinで記述できる
- コード量を削減できる
- UIの状態管理がしやすい

## UI階層

1つのコンポーネントの中に別のコンポーネントを配置できる。

例

```text
Column
├── Text
├── Image
└── Button
```

このように親子関係を持った構造をUI階層と呼ぶ。

---

## 画像の追加

### 手順

1. `View > Tool Windows > Resource Manager` をクリック
2. `+ > Import Drawable` をクリック
3. 画像ファイルを選択して `Open`
4. `Import Drawables` ダイアログでインポート
