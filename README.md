## Overview

プルリクエストのサイズが一定を超えた場合に警告を出すGithub Actionsです。

## Usage

1. 自身のリポジトリ設定にてGithub Actionsを有効化してください。
    1. その際、書き込み権限も許可してください。
3. 本スクリプトを.github/workflows/配下に設置してください。
4. リポジトリの環境変数に以下を定義してください。
    1. PULL_REQUEST_LIMIT_FILES: 警告を出す差分ファイル数の閾値
    1. PULL_REQUEST_LIMIT_LINES: 警告を出す差分行数の閾値
    1. EXCLUDE_PATH: 除外するパス
5. プルリクエストを作成すると発火し差分を計算してコメントをつけてくれます。

## DEMO

<img width="443" alt="スクリーンショット 2023-05-30 15 54 52" src="https://github.com/yamamoto-hiroya/pull_request_size_checker/assets/16412726/e341b5ca-550d-4a3b-9b49-0eb7bedd12ef">

## SAMPLE

https://github.com/yamamoto-hiroya/pull_request_size_checker/pull/1

本リポジトリでは以下のように設定してあります。

<img width="295" alt="スクリーンショット 2023-05-30 15 58 33" src="https://github.com/yamamoto-hiroya/pull_request_size_checker/assets/16412726/38a58494-e5eb-4b15-a8a2-0cfde4f04e40">

tests/配下は除外して集計されます。
もし閾値を超えた場合は以下のような表示となります。

![image](https://github.com/yamamoto-hiroya/pull_request_size_checker/assets/16412726/a1549db3-468c-4da5-bdb9-4831ae587d98)
