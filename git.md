# コマンドまとめ

#### 基本的なコマンドとオプションをまとめたもの
<br>

## 基本用語

- ブランチ<br>
履歴の流れを分岐して記録していくもの<br>
⇒merge（合流）することで一つのブランチにまとめなおすことができる<br>
⇒作業単位で履歴を残すことで問題発生時に原因特定や対策を容易にする

- 空ブランチ（独立ブランチ）<br>
master(main)ブランチと何の関連性も持たないブランチ<br>
メリット：既存ブランチとは別に履歴を残せることで、トラブルが発生した際に原因を追求しやすく、対策も練りやすい<br>
docブランチがよく作成される

- ステージする＝インデックスに登録する<br>
次回コミットに含めるようgitに指示する<br>
__**目的：一回のコミットでは、その主題となる変更点と無関係な変更を含めない**__ <br>
__**⇒gitの目的であるバージョン管理する上で重要**__ <br>

- Modified<br>
statusコマンドを実行した際に出てくる<br>
意味：コミットされるべき、修正された<br>
⇒add された状態で止まっているファイル




## 基本コマンド
| コマンド | 意味 |
| ---- | ---- |
| cd | パスを指定し直接フォルダを開く |
| ..\ | ルートディレクトリに移動 |
| mkdir | ディレクトリを作成<br>make directoryの略 |
| type nul > hogehoge.txt | 新規のテキストファイルを作成する<br> （.mdであればmdファイルを作成する） |
| コマンド | mean |
| コマンド | mean |

<br>

## Git

### ローカルリポジトリの作成

| コマンド | 意味 |
| ---- | ---- |
| git colone | リモートのgitリポジトリをコピー<br>（作業ディレクトリとローカルリポジトリを作成する） |
| git init --bare --share | 新しくローカルリポジトリを作成する |


※ clone：既存のリモートリポジトリの内容を落とし込む<br>
※ init：カレントディレクトリにGitの管理ディレクトリを作成する<br>必要によってはaddとcommitをする


### リモートリポジトリの作成

| コマンド | 意味 |
| ---- | ---- |
| git init --bare --share |  |
| git config --global user.email ---@--.-- | 〇〇 |
| git remote add origin https://github.com/---/--- | 〇〇 |


### 登録からプッシュまで

| コマンド | 意味 |
| ---- | ---- |
|  git add | 変更したファイルをインデックスに登録 |
| git add . | ワーキングツリーにあるファイルをまとめて登録 |
| git add *.java | 識別子別に指定<br>（今回の例はJavaファイルを一括登録） |
| git add dir/*.java | ディレクトリ単位で指定 |
| git add -i | 対話形式で指定<br>コマンドを表示さ、表示される選択肢を選んで指定していく |
| git add pathspec | 削除されたファイルも追加される |
| **git add -p**  | 1ファイル内で差分ごとにstageする、しないを対話的に行う |

| git commit -m "---" | メッセージ付きでインデックスをコミット<br>（ローカルリポジトリ内での出来事） |
| git push origin master | ローカルリポジトリ内での作業をリモートリポジトリにプッシュ<br>git push origin(リモートリポジトリ) master(pushしたいブランチ) |
| git commit --amend -m | コミットメッセージの修正 |
| git | mean |
### ブランチの作成
| コマンド | 意味 |
| ---- | ---- |
| git checkout -b branchname | branchnameを作成 |
| git checkout --orphan doc | docという名前の独立ブランチを作成 |
| git clean -f failname | 対象ファイルの削除 |
| git clean -n | 削除対象のファイルの確認 |
| git | mean |
| git | mean |
| git | mean |
| git | mean |

### pull
| コマンド | 意味 |
| ---- | ---- |
| git pull origin doc | pull<br>（リポジトリ、pullしたいブランチ名の順に記載） |
| git | mean |
| git | mean |
| git | mean |
| git | mean |
| git | mean |
| git | mean |
| git | mean |

### 作業ブランチを間違えた場合の対処法<br>
変更内容を引き継いでブランチの切り替え
| コマンド | 意味 |
| ---- | ---- |
| git stash | 変更内容をとりあえず保持してブランチの切り替えを可能にする |
| git chechkout 切り替えたいブランチ名 | ブランチの切り替え |
| git stash pop | 保持していた変更内容を今のブランチに取り入れる |

### git(その他)
| コマンド | 意味 |
| ---- | ---- |
| git status | mean |
| git branch -a | mean |
| git reset --head HEAD@{No} | No番目の履歴まで戻る |
| git ls-files --stage  | indexにあるファイルの確認 |
| git cat-file -p ハッシュ値 | インデックスの中のハッシュ値で指定されたファイルの中身を確認 |
| git diff | 変更の内容を確認 |
| git diff 比較ファイル1 比較ファイル2 | 1、2のファイルの変更点を表示 |
| git diff --cached | 最新のコミットとインデックスの差分を表示 |
| git log | コミットした際のコメント等を表示 |

| git | mean |


### オプション

| オプションコマンド | 意味 |
| ---- | ---- |
| --bare | ベアレポジトリ（管理のみを行う）の作成を行う<br>ベアリポジトリの拡張子は.gitとするのが慣例 |
| --share | パーミッション（グループアクセス可能）を追加する |
| git | mean |
| git | mean |
| git | mean |
| git | mean |
| git | mean |

<br>

## 超簡易イメージ（その他）
| ワード | 意味 |
| ---- | ---- |
| コミット | ゲームでいうセーブ<br>基本どの地点にも戻ることが可能 |
| push | 大元を調整する |
| merge | ローカルで結合する |
| インデックス | リポジトリにコミットする準備をするための場所 |
|  q | (END)から進まないとき |
| ワード | mean |

## メッセージの意味

Your branch is ahead of 'origin/doc' by 1 commit.<be>
ローカルブランチdocがリモートリポジトリより１コミット進んでいる<be>

Changes to be committed:<be>
コミットされるべき変更があります。<be>
⇒ステージされただけの（未コミット）のファイルがあります<be>

Changes not staged for commit:<be>
変更されている、かつ、未ステージのファイルがあります







