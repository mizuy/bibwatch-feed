# bibwatch-feed

[bibwatch](https://github.com/mizuy/bibwatch) の **公開 RSS** 置き場。watch 定義と論文 state は private の [bibwatch-data](https://github.com/mizuy/bibwatch-data) に残す。

GitHub の無料プランは private repo に Pages を置けないため、feed XML だけこの public repo から配信する。

## 購読 URL（コピー用）

RSS リーダーにそのまま貼る。同じ一覧は https://mizuy.github.io/bibwatch-feed/ にもある。一括取込は [OPML](https://mizuy.github.io/bibwatch-feed/bibwatch.opml)。

```
https://mizuy.github.io/bibwatch-feed/feeds/1727b064-fca2-4a61-ac39-d04984c1dcd5/all.xml
https://mizuy.github.io/bibwatch-feed/feeds/1727b064-fca2-4a61-ac39-d04984c1dcd5/priority.xml
https://mizuy.github.io/bibwatch-feed/feeds/1727b064-fca2-4a61-ac39-d04984c1dcd5/major-gi.xml
https://mizuy.github.io/bibwatch-feed/feeds/1727b064-fca2-4a61-ac39-d04984c1dcd5/susa.xml
https://mizuy.github.io/bibwatch-feed/feeds/1727b064-fca2-4a61-ac39-d04984c1dcd5/rspo.xml
https://mizuy.github.io/bibwatch-feed/feeds/1727b064-fca2-4a61-ac39-d04984c1dcd5/pccrc.xml
https://mizuy.github.io/bibwatch-feed/feeds/1727b064-fca2-4a61-ac39-d04984c1dcd5/authors.xml
https://mizuy.github.io/bibwatch-feed/feeds/1727b064-fca2-4a61-ac39-d04984c1dcd5/endo-cea.xml
https://mizuy.github.io/bibwatch-feed/feeds/1727b064-fca2-4a61-ac39-d04984c1dcd5/braf-crc.xml
https://mizuy.github.io/bibwatch-feed/feeds/1727b064-fca2-4a61-ac39-d04984c1dcd5/sps.xml
https://mizuy.github.io/bibwatch-feed/feeds/1727b064-fca2-4a61-ac39-d04984c1dcd5/tsa.xml
```

| feed | 内容 |
|------|------|
| all | テーマ論文（指定誌を先に） |
| priority | 指定誌だけ |
| major-gi | 上記誌の消化管腔 GI（肝胆膵は除く） |
| susa | Superficially serrated adenoma |
| rspo | RSPO / R-spondin |
| pccrc | Post-colonoscopy colorectal cancer |
| authors | 指定著者 |
| endo-cea | 消化管内視鏡の費用対効果（雑誌不問） |
| braf-crc | BRAF陽性大腸癌（雑誌不問） |
| sps | serrated polyposis syndrome（雑誌不問） |
| tsa | traditional serrated adenoma（雑誌不問） |

Pages がまだなら raw:

```
https://raw.githubusercontent.com/mizuy/bibwatch-feed/main/docs/feeds/1727b064-fca2-4a61-ac39-d04984c1dcd5/all.xml
```

## 更新

`bibwatch run --site-base https://mizuy.github.io/bibwatch-feed` が `BIBWATCH_FEED` 経由で `docs/feeds/<token>/*.xml` を書き、この repo の **`main`** へ push する（Pages は `main` / `/docs`）。

定期実行は Cursor Automation（手順は [bibwatch/AUTOMATION.md](https://github.com/mizuy/bibwatch/blob/main/AUTOMATION.md)）。作成画面の Repository でこの repo と `bibwatch` / `bibwatch-data` を一緒に選ぶ。
