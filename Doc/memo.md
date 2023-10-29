## よく使うライブラリ

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
    import pandas as pd                 # 表計算等データベースみたいに操作できる
    import numpy as np                  # 行列式等計算が得意
    from scipy import                   # 科学計算が得意
    import matplotlib.pyplot as plt     # グラフ描画の定番
    import cv2 as cv
    ```

## ターミナルコマンド
* windows powershellで実行する


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