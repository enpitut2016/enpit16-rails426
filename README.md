# enPiT 2016 スターターキット (Rails4.2.6入り)

本ツールは、enPiT 2016 PBLの開発環境を用意するためのツールです。
[Railsチュートリアルスターターキット](https://github.com/yasslab/railstutorial.jp_starter_kit)をもとに, ruby/railsのバージョンアップ, Herokuコマンド, Hubコマンドのインストールを追加しています。

HerokuやGitHubのセットアップは各自でやる必要があります。

## ファイル構成

### `Vagrantfile` ファイル

ゲストOSをダウンロードするための必要な設定が書かれています。
`ls` コマンドで Vagrant ファイルが見える位置 (ディレクトリ) まで移動して `vagrant up` と実行するだけで
Railsチュートリアルが始められる環境が整います (Windows 10 / Mac OS X 10.11 にて確認済み)。

### `workspace` ディレクトリ

`workspace`ディレクトリは、Vagrant というツールを使って立ち上げた
ゲストOSの `/home/vagrant/workspace` ディレクトリと同期しています。

ホストOS (お手持ちのパソコン) に Sublime Text などのエディタをインストールし、
`workspace` 以下にあるファイルを操作することで、ゲストOS上のファイルを操作することができます。

これにより、ゲストOSの中でRailsアプリを立ち上げ、コーディングや編集、
ブラウザでの確認(※)をホストOSで行う、といった開発が可能になります。

```
※ ゲストOS上で`rails server` を立ち上げると、
　Vagrant のポートフォワーディングという機能が働き、
　ホストOSの localhost:3000 というURLからRailsのアプリケーションを確認することができます。
```

## 本ツールを使った環境構築の手順(railstutorial.jpスターターキットから引用)

1. [VirtualBox](http://www.oracle.com/technetwork/server-storage/virtualbox/downloads/index.html?ssSourceSiteId=otnjp)をインストールする
2. [Vagrant](https://www.vagrantup.com/downloads.html)をインストールする
3. Windowsの場合: 英字のローカルアカウントを作る (`ror`など)
4. Windowsの場合: sshクライアント([TeraTerm](http://ttssh2.sourceforge.jp/)など)をインストールする
5. `Vagrantfile` があるディレクトリに移動して、`vagrant up`を実行する
6. `vagrant ssh` でゲストOSにログインする
7. `ruby --version` や `rails --version` でちゃんと動くか確かめる

## 関連リポジトリ/リンク
- [yasslab/railstutorial.jp_starter_kit](https://github.com/yasslab/railstutorial.jp_starter_kit)
- [yasslab/sample_apps](https://github.com/yasslab/sample_apps)
- [yasslab/railstutorial.jp](https://github.com/yasslab/railstutorial.jp)
- [Rails チュートリアル](http://railstutorial.jp)
- [Rails 解説セミナー](http://railstutorial.jp/seminars)
- [Rails スクリーンキャスト](http://railstutorial.jp/screencasts)
- [Rails ガイド](http://railsguides.jp)


## ライセンス
The MIT License (MIT)

Copyright &copy; 2015 [YassLab](http://yasslab.jp)

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
