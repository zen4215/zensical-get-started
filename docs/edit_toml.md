# zensical.tomlを編集する

Zensicalでドキュメントを書く際、設定ファイルは通常`zensical.toml`です。

## ドキュメントの追加

`docs/`フォルダ内に任意のmarkdownドキュメントを追加します。

`zensical.toml`で、navigation(左に出されるドキュメントの構造)を割り振ってください。[参考](https://zensical.org/docs/setup/navigation/#navigation-sections)

```toml
[project]
nav = [
    "index.md",
    { "わーい" = "fuga.md" },
    { "dir" = [
        "dir/dex.md",
        { "にゃーん" = "nya.md" },
    ]}
]
```

markdownを指定するとドキュメント内のタイトルが、`{ "title" = "file" }`で別途指定したタイトルが表示されます。

まとめるときは`[]`で囲んで下さい。

## 機能の選別

`zensical.toml/project.theme/features`を編集します。

```toml
[project.theme]
features = [
    "navigation.tabs",
    ...
]
```

