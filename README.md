## Overview

プルリクエストのサイズが一定を超えた場合に警告を出すGithub Actionsです。

## Usage

1. 自身のリポジトリ設定にてGithub Actionsを有効化してください。
1. 本スクリプトを.github/workflows/配下に設置してください。
1. リポジトリの環境変数に以下を定義してください。
  1. PULL_REQUEST_LIMIT_FILES: 警告を出す差分ファイル数の閾値
  1. PULL_REQUEST_LIMIT_LINES: 警告を出す差分行数の閾値
  1. EXCLUDE_PATH: 除外するパス
1. プルリクエストを作成すると発火し差分を計算してコメントをつけてくれます。