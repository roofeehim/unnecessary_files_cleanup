## 使用方法

1. targetディレクトリ配下に対象ディレクトリを一つ配置（対象ディレクトリの中のディレクトリ数は複数でも可）
2. file_list.txtにファイル名を記載（パス付きで記載してもいいが、パスは無視されファイル名だけで比較する）
3. 記載のファイルのみ残して、それ以外のファイルを削除する
4. 残ったファイルリスト（kept_files.txt）,削除したファイルリスト（removed_files.txt）,削除した空ディレクトリリスト（removed_dirs.txt）が生成される

## 用途

基本的には必要なファイルを目視で精査してフォルダから取り出していく代わりに使用する想定となる。

- 開発者がビルド後のdistディレクトリから、リリースファイルのみ抽出したいときに、実行すれば不要ファイルを削除できる
- 大量ファイルが入ったフォルダに対して、必要なファイルだけ取り出したい場合、実行すれば不要ファイルを削除できる

## 注意点

- 実行するときにエクスプローラーが開いていたり、対象ディレクトリ、ファイルがどこかで開かれてると、プロセスが占有されていると判断され最後まで処理が走らない場合がある。そのため、実行時は対象ディレクトリ、ファイルは閉じた状態で行うことを推奨
- 最終的な生成リストを見て、必要なファイルを抽出できてるか確認することを推奨