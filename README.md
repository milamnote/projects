# projects

## Read Me                                                                                   
サイトを作成する際に、ここにあるフォルダを丸ごと、デスクトップに移動して作成して下さい。  



##【まず最初にすること】
１．node.jsインストール

２．npmインストール


ここまでできていれば、このディレクトリを保存しておいて
サイト制作プロジェクトごとに、丸ごとディレクトリーをコピーをし、

１．npm i 

２．bower i


とコマンドすることで、必要な物をすべてインストールします。
(-dはいらなかった・・・はずっ（確認して下さい＜ぇ




##【制作開始】

cd 新しく始めるプロジェクトファイルパス\projects
gulp　

もしくは

gulp ejs 　など　使いたいタスク設定を専用に使う。
※gulpは監視モードとなり、保存されるごとに、コンパイル（サイト作成）を行います。



##メインコマンド一覧。
gulp
gulp build
gulp copy
gulp zip
gulp clean

deployで開発(gulp)⇒完成！<各種スナップショットからヘッダー入れなど行います>

(build)⇒Releaseへコピー(copy)⇒ワードプレス用圧縮化（zip)⇒開発環境リリースを削除！（clean)

詳しくはマニュアルディレクトリにある、gulpを確認して下さい。

※いろいろ不完成なので、それぞれでタスク修正するように(； ･`д･´)＜ぉぃ



###################################################
#             サイト 完  成！                     #
###################################################
サイトにアップするものは、deploy/Releaseディレクトリーにまとまっています。(作られます)

※wordpress用設定は完成していません。適当に直して下さい＜ぇ

※個別タスクは動きます




Sass/Compass用設定済み

タスクランナー仕込み済み（gulp)

##[構成]
  ・package.jsonは、開発環境設定ファイルです。

  ・node_modulesディレクトリは、開発ツールフォルダです。 ※package.jsonに、使えるように記載あり。

  ・config.rbは、compassの設定ファイル。 SublimeText3でcompassにより、Sass（JSが早く掛ける！）の自動化を行っています。

  ・gulpfile.jsは、タスクランナー設定ファイルです。（タスクを自由に書き込めます：自動化）

  ・bower.jsonにはインストールしたツール一覧が記載されています（プロジェクト開始時、一括インストール）

  ・bowerrcはBowerのツール保存先などを設定しています。

  ・styledown_config.mdは、スタイルガイドジェネレーター（styledown)の設定ファイルです。

  ・libsディレクトリは、サイト作成で楽にできるフレームワーク類（Scss/ejs/js）(今は主にBower関係)などが入っています。

  ・deploy/site.jsonに、サイトのデーターを入れると、EJSで選んだHTMLテンプレートに、データーが自動的に流し込まれ、HTMLができます。

  ・deploy/projects.mdにまず、サイト仕様を記載しましょう。

  ・htaccessは、サイト高速化へ向けてのパスです。自動的に完成したサイトデーターにコピーされるので削除しないで下さい。

  ・header_banner.txtは、WordPress用にCSSへテーマなど付ける場合に利用されます。必要に応じ内容を書き換えて下さい。


CSSなどの各モジュールなどは基本ファイルを参照、もしくはクロームリンクを確認して下さい。


フレームワークに対応。J:\framework内に各種そろっています。

SCSSはリンクして呼び出J:\frameworkへ可能に設定。

EJS類はコピーしてdeployフォルダ内に保存して下さい。


##新たにタスクなどをツールを入れる際は、以下の手順で実施。

コマンドプロント：管理者権限で実行

cd パス/projects

npm install ツールプラグイン名 --save-dev

gulpfile.jsにタスクを記載する。



【npm コマンド】

nodist update

nodist selfupdate

nodist stable


#指定したバージョンを追加
nodist add v4.2.1  or nodist + v4.2.1

#指定したバージョンをアンイストール
nodist rm v4.2.1 or nodist - v4.2.1

インストールされているnode.jsの一覧を表示
nodist ls

インストール可能なバージョンが表示
nodist dist

指定バージョンの切り替え
nodist v0.10.32
 or
nodist use v0.10.32

node.jsの最新バージョンを表示
nodist latest

nodist依存ファイルのアップデート
nodist update

node.jsの最新の安定板をインストール
nodist stable

npmのアップデート
npm update -g npm

足りないモジュールをたったの一行でインストールするコマンド
npm install -g npm-install-missing

「npm-install-missing」コマンドでモジュールをインストールする
 npm-install-missing


Forkして、もっと簡潔なバージョン作ってみたっ！(； ･`д･´)
ってのもまってますｗ
