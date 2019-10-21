
## LAN Messenger 日本語化

このソフトウェアを起動した同士で、LAN内でメッセンジャーがつながります。ログインとかパスワードとか不要です。ファイルも送れますし、通信は暗号化されています。それくらいの簡単な感じです。Win/Mac/Linux対応。ブロードキャスト機能では、IPが変わったとか見つからなくてもメッセージできます。スマホもやり取りしたければ、別の日本産の似たようなソフトウェア IP Messenger があります。これとの違いは、LAN Messenger ではインストール不要、一方で日本産は高機能なログ検索機能とかがあります。LAN Messenger の日本語化ファイルがなかったので用意しました。

- [GitHub](https://lanmessenger.github.io/), 1.2.39 (2018-12-25)
- [sourceforge](http://lanmsngr.sourceforge.net/), 1.2.35 (2013-02-01)
- [LAN Messenger Portable](https://portableapps.com/apps/internet/lan-messenger-portable), 1.2.35 (2013-02-01)

### 日本語化の仕方
`ja_JP.qm` を入れれば、設定から表示言語に日本語 (Japanese) が選べます。配置先は `lang` フォルダです。ポータブルでは `LANMessengerPortable\App\LANMessenger\lang`。

心配な方はテキストデータの元の `ja_JP.ts` ファイルを自分でコンパイルすればこのファイルができます（[ここのプロジェクトのソースコード](https://github.com/lanmessenger/lanmessenger/tree/master/lmc/src)にコミットしました）。[Qt-Linguist](https://github.com/thurask/Qt-Linguist/releases)で読み込んで Release を実行すれば `.qm` ファイルへとコンパイルされます。

### ポータブル化
1. 1.2.35 のポータブルの`App\LANMessenger` の中身を削除し、1.2.39のファイルを上書きすればポータブル化できる（1.2.39にはテーマファイルが抜けているが1.2.35のは利用できない？）。
2. それから日本語言語ファイルの `ja_JP.qm` を入れる。
3. ポータブルでは、「ファイル転送の受信フォルダ」が、LAN Messenger Portable のフォルダになっているのでこれを変更する。