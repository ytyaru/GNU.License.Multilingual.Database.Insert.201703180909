# このソフトウェアについて

GNUのライセンスDB(複数言語版)にデータを挿入する。

# 開発環境

* Linux Mint 17.3 MATE 32bit
* [SQLite3](https://www.sqlite.org/index.html) 3.8.2

# 元データ

* https://www.gnu.org/licenses/license-list.en.html
* https://www.gnu.org/licenses/license-list.ca.html
* https://www.gnu.org/licenses/license-list.cs.html
* https://www.gnu.org/licenses/license-list.de.html
* https://www.gnu.org/licenses/license-list.es.html
* https://www.gnu.org/licenses/license-list.fr.html
* https://www.gnu.org/licenses/license-list.it.html
* https://www.gnu.org/licenses/license-list.ja.html
* https://www.gnu.org/licenses/license-list.pl.html
* https://www.gnu.org/licenses/license-list.pt-br.html
* https://www.gnu.org/licenses/license-list.ru.html

上記文書からデータを抽出し、DBファイルを作成する。
# 準備

## DBを作成する

* [GNU.License.Multilingual.Database.Insert.201703180909](https://github.com/ytyaru/GNU.License.Multilingual.Database.Insert.201703180909)
* DBファイル名を変更する
    * `GNU.Licenses.{lang}.sqlite3`

## 設定

`main.py`で言語コードとDBパスを指定する。

```python
if __name__ == '__main__':
    lang = 'ja'
    gnuJa = GnuSite(
        path_gnu_licenses_sqlite3 = './GNU.Licenses.{0}.sqlite3'.format(lang)
    )
    gnuJa.GetAll(lang)
```

# 実行

```sh
python3 main.py
```

# 結果

* `GNU.Licenses.{lang}.sqlite3`ファイルにデータが挿入される
* 処理出力がターミナルに表示される

# ライセンス #

このソフトウェアはCC0ライセンスである。

[![CC0](http://i.creativecommons.org/p/zero/1.0/88x31.png "CC0")](http://creativecommons.org/publicdomain/zero/1.0/deed.ja)

なお、使用させていただいたソフトウェアは以下のライセンスである。感謝。

Library|License|Copyright
-------|-------|---------
https://www.gnu.org/licenses/license-list.ja.html|[CC-BY-ND-4.0](https://creativecommons.org/licenses/by-nd/4.0/deed.ja)|Copyright © 2014, 2015, 2016 Free Software Foundation, Inc.

改変禁止のため、作成したDBファイルは配布できない。

