# tssubscript

元データの MPEG-TS に頂上されている PSI/SI/Supermiose/DSM-CC を エンコード済みの MPEG-TS に張り付けるツールです。

## 使用方法

```bash
tssubscript -i <入力TSファイル> -m <貼り付け元メタデータTSファイル> -o <出力TSファイル>
```

また、パイプを使ってエンコードしながら張り付ける事もできます。

```bash
エンコードコマンド | tssubscript -m <貼り付け元メタデータTSファイル> -o <出力TSファイル>
```

## オプション

### -i, --input <path>

入力TSファイルのファイルパス。省略した場合には標準入力から受け取ります。

### -o, --output <path>

出力TSファイルのファイルパス。省略した場合には標準出力に出力します。

### -m, --metadata <path>

メタデータTSファイルのファイルパス。省略した場合にはメタデータを張り付けません。

## 制限事項

* 入力TSファイル/メタデータTSファイルの制限
  * 188 bytes のみの対応となります

## ソースコードについて

* MIT ライセンスです
* [`getopts`](https://github.com/rust-lang/getopts) クレートに依存しています
