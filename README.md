# bibwatch-feed

[bibwatch](https://github.com/mizuy/bibwatch) の **公開 RSS** 置き場。watch 定義と論文 state は private の [bibwatch-data](https://github.com/mizuy/bibwatch-data) に残す。

GitHub の無料プランは private repo に Pages を置けないため、feed XML だけこの public repo から配信する。

## GitHub Pages

Settings → Pages → **`main` / `/docs`** を有効にする。

購読 URL（Inoreader 等）:

```
https://mizuy.github.io/bibwatch-feed/feeds/<token>/all.xml
```

`<token>` は `bibwatch-data` の `state/feed-token`（この README には書かない）。

Pages 反映前は raw でも取れる:

```
https://raw.githubusercontent.com/mizuy/bibwatch-feed/main/docs/feeds/<token>/all.xml
```

## 更新

`bibwatch run --site-base https://mizuy.github.io/bibwatch-feed` が `BIBWATCH_FEED` 経由で `docs/feeds/<token>/all.xml` を書き、この repo へ push する。
