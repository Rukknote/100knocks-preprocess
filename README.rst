取り組んだこと
====
データサイエンス100本ノック（構造化データ加工編）

概要
====
- データサイエンティスト協会スキル定義委員の[データサイエンス100本ノック（構造化データ加工編）](https://github.com/The-Japan-DataScientist-Society/100knocks-preprocess)を利用
- Dockerは使わず、pyenv+pipenvで仮想環境を作って演習に取り組んだ

ディレクトリの詳細
====
- answerフォルダ：Pythonで演習を解く場合の解答例が格納されている
- dataフォルダ：演習で扱うデータが格納されている
- notebook：演習問題と演習問題に直接記述したものが入っている

インストール（Mac OS）
====
## 1. pyenvのインストール
Homebrewでpyenvをインストールする

```sh
brew install pyenv
```

## 2. pyenvのパスを通すためにzshrcを編集する
使用しているshellを確認する

```sh
echo $SHELL
/bin/zsh
```

zshを使用していることを確認できたので、`~/.zshrc`に以下の内容を追記する

```sh
export PYENV_ROOT="$HOME/.pyenv"
export PATH="$PYENV_ROOT/bin:$PATH"
eval "$(pyenv init --path)"
eval "$(pyenv init -)"
```

shellの設定を読み込む

```sh
source ~/.zshrc 
```

## 3. pythonをインストール
仮想環境（pyenv）に好きなpythonのバージョンを指定してインストール

```sh
pyenv install 3.10.9 
```

## 4. 使用するpythonのバージョンを指定
インストール済みのpythonのバージョンを確認する

```sh
pyenv versions
  system
  3.9.18
* 3.10.9 (set by /Users/username/.pyenv/version)

```

python 3.10.9を設定
```sh
# globalで設定する場合
pyenv global 3.10.9

# localで設定する場合
pyenv local 3.10.9
```

pythonのバージョンを確認

```sh
python --version
# 設定されたバージョンが出力される
Python 3.10.9
```

## 5. pipenvのインストール
pipでpipenvをインストールする

```sh
pip install pipenv
```

## 6. モジュールのインストール
既存のPipfileからインストール（Pipfileがあるディレクトリで実行）

```sh
pipenv install
```

## 仮想環境の有効化
シェルを起動する

```sh
pipenv shell
```

シェルを終了する

```sh
exit
```

## 7. jupyter notebookで演習に取り組む
pipでjupyter notebookをインストール

```sh
pip install notebook 
```

jupyter notebookを起動する

```sh
jupyter notebook
```


元の作成者
====
The Data Scientist Society