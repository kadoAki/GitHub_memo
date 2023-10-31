# pythonとかでよく使うモノ

## python
### 書き方
* ライブラリを使う
    ```python
    # 標準、サードパーティ製ライブラリを使えるようにする
    import 'ライブラリ' as '略名'

    # ディレクトリ内に複数ライブラリがあるパッケージの時に使う
    # あえて下の書き方にしているのはオブジェクト.py内の関数名でも
    #フォルダ名内のファイル名でも対応できるため
    from '親オブジェクト名' import '子オブジェクト名' as '略名'
    ```
* ライブラリを使う際の書き方標準
    ```python
    # 暗黙のルールとして下記のような順番でimportする
    # 同種毎にまとめ、別種との間隔は1行空ける
    # 同種複数ライブラリはA~順で並べる
    import '標準ライブラリ'

    import 'サードパーティ製ライブラリ'

    import 'チーム内作成ライブラリ'

    import '自作ライブラリ'
    ```

* 基本的な書き方
    ```python
    # 処理
    a_num = 12345              # 数値型
    a_str = '12345'            # 文字列型
    a_float = 1.2345           # 浮動小数点型
    a_boolean = TRUE           # ブール値
    a_list = [1, 2, 3, 4, 5]   # リスト
    a_tuple = (1, 2, 3, 4, 5)  # タプル(リストに比べ、設定後変更できない)
    a_dict = {'a':1, 'b':2}    # 辞書(左がキー, 右が値)
    a_set = {1, 2}             # 集合(論理で使う)

    print(a_name)             # 出力

    # 演算
    a = 1
    b = 2
    a = a + 1           # 加算
    a = a - 1           # 減算
    a = a * 1           # 乗算
    a = a / 1           # 除算
    a = a ** 2          # べき乗
    a = a // 2          # 除算(整数)
    a = a % 2           # 余り
    
    # 比較
    a == b              # 等しい
    a < b               # a大なりb
    a > b               # a小なりb
    a <= b              # aはb以下
    a >= b              # aはb以上
    a != b              # aはbでない
    a in b              # aはbに含まれている

    ```


### よく使うライブラリ

* 標準ライブラリ
    ```python
    # python 3.12
    # pythonにあるライブラリ
    import csv                          # csvファイルを操作できる
    import datetime                     # 日時を扱う
    import glob                         # ディレクトリ内のファイルを列挙できる
    import os                           # ファイルの有無や作成～削除等、ファイル操作ができる
    import pathlib                      # 空のファイルを作成する時
    import shutil                       # ファイルのコピー, ディレクトリを中身ごと削除等高度なファイル操作ができる
    import string                       # Templateを使える
    import subprocess                   # ターミナルのコマンドを実行できる
    import sys                          # pythonの基本設定をいじれる(再帰回数の変更で使ったことある)
    import tarfile                      # Linux,macで使う. tarファイルの圧縮・展開ができる
    import tempfile                     # tempファイルを扱う
    import time                         # sleep等相対?的な時間操作ができる
    import zipfile                      # windowsで使う. zipファイルの圧縮・展開ができる
    ```

* サードパーティーライブラリ
    ```python
    # pypl等で配布されている有名なパッケージ
    import cv2 as cv
    import matplotlib.pyplot as plt     # グラフ描画の定番
    import numpy as np                  # 行列式等計算が得意
    import pandas as pd                 # 表計算等データベースみたいに操作できる
    import pyautogui                    # RPA作成時に使う
    import PySimpleGUI as sg            # アプリUIの定番
    from scipy import                   # 科学計算が得意
    ```

### PowerShell(ターミナル)
* PowerShell基本
    * ディレクトリ操作
        ```powershell
        chdir 'Path'                   # カレントディレクトリ
        tree
        ```
* Python系
    * 仮想環境の構築
        ```powershell
        chdir 'path'               # カレントディレクトリを選択する
        py -m venv 'ディレクトリ'   # 仮想環境用のディレクトリとファイル一式作成される
        # 仮想環境呼び出し
        'venvで作成したディレクトリ'/Script/Activate.ps
        (venv)カレントディレクトリ名 と表示されていれば成功
        ```
    * コードスタイルチェック
        ```powershell
        # インストール
        pip install pycodestyle
        pip install flake8
        pip install pylint
        # 使用
        pycodestyle 'ファイル名.py' # 書き方がPEP8に準じているかチェック
        flake8 'ファイル名.py'      # pycodestyle + importで使用されているかチェック
        pylint 'ファイル名.py'      # flake8 + さらに細かくチェック
        ```

## よく使う環境
* vscode
* jupyternotebook

## よく読むべきドキュメント
[pipコマンド一覧 https://pip.pypa.io/en/stable/cli/](https://pip.pypa.io/en/stable/cli/)