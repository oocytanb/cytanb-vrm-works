# [cytanb-vrm-works](https://github.com/oocytanb/cytanb-vrm-works)

このプロジェクトは、[VRM](https://vrm.dev/) を制作するための Unity プロジェクトです。

オープンソースで公開することで、どなたでもアイディアの追加を行えるようになっています。

## Softwares / Assets

- [Unity](https://unity3d.com/) 2019.4
- [UniVRM](https://github.com/vrm-c/UniVRM)

## プロジェクトの構成

独立したリポジトリとして公開されているアセットを扱いやすくするため、プロジェクトを以下のように構成しています。

- 本リポジトリでは、Unity のプロジェクトファイルと、アセットの依存関係を記述した [DEPS](./DEPS) ファイルを扱います。
    プロジェクトにアセットのリポジトリを追加する場合には、このファイルを変更します。

- [oO-vrm-pack](https://github.com/oocytanb/oO-vrm-pack) : VRM のサンプル

- [cytanb-tso-collab](https://github.com/oocytanb/cytanb-tso-collab) : [VCI](https://github.com/virtual-cast/VCI) を制作するためのプロジェクト

## Git

- 独立したリポジトリとして公開されているアセットを、まとめて扱うために、
 [depot_tools/gclient](https://dev.chromium.org/developers/how-tos/depottools) を採用しています。

- [depot_tools のインストール方法](https://commondatastorage.googleapis.com/chrome-infra-docs/flat/depot_tools/docs/html/depot_tools_tutorial.html) に従って、導入します。
    1. Windows 環境では、[depot_tools.zip](https://storage.googleapis.com/chrome-infra/depot_tools.zip) をダウンロード・展開し、`PATH` 環境変数の優先順位が高い位置に追加します。

    1. コマンドプロンプト (cmd) から、初回の `gclient` コマンドを実行し、アップデートを行います。

    1. 作業ディレクトリで `gclient config` コマンドを実行し `.gclient` ファイルを作成します。
        ```
        gclient config --name=cytanb-vrm-works "https://github.com/oocytanb/cytanb-vrm-works.git@2019.4"
        ```
    
    1. リポジトリからソースコードを取得します。
        ```
        gclient sync
        ```

    1. UniVRM のリポジトリで、サブモジュールが使われているため、初期化を行います。
        ```
        cd cytanb-vrm-works/Assets/VRM
        git submodule init
        git submodule update
        ```

- Git に関する詳しい情報は、Web の資料に当たってください。

## License

- 本プロジェクト固有のものについては、[MIT License](./LICENSE) です。

- 個々のアセット/ライブラリーについては、それぞれのライセンスをご確認ください。

- アセット等に適用するライセンスは、制作者の著作権表示とその成果物をオープンで自由に利用できることを明示する目的で、主に以下のものから選択しています。
    - [MIT License](https://opensource.org/licenses/MIT)
    - [BSD 2-Clause License](https://opensource.org/licenses/BSD-2-Clause)
    - [Apache License, Version 2.0](https://opensource.org/licenses/Apache-2.0)
    - [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)
