# [cytanb-vrm-works](https://github.com/oocytanb/cytanb-vrm-works)

このプロジェクトは、[VRM](https://vrm.dev/) を、制作するための Unity プロジェクトです。

[VCI](https://github.com/virtual-cast/VCI) を制作するためのプロジェクトは、[cytanb-tso-collab](https://github.com/oocytanb/cytanb-tso-collab) になります。

## Softwares / Assets

- [Unity](https://unity3d.com/) 2018.2
- [UniVRM](https://github.com/vrm-c/UniVRM)
- [oO-hands](https://github.com/oocytanb/oO-hands)

## Git

- [Git Large File Storage (LFS)](https://git-lfs.github.com/) を導入しています。

- 独立したリポジトリとして公開されているアセットを、まとめて扱うために、
 [depot_tools/gclient](https://dev.chromium.org/developers/how-tos/depottools) を採用しています。

- [depot_tools のインストール方法](https://commondatastorage.googleapis.com/chrome-infra-docs/flat/depot_tools/docs/html/depot_tools_tutorial.html) に従って、導入します。
    1. Windows 環境では、[depot_tools.zip](https://storage.googleapis.com/chrome-infra/depot_tools.zip) をダウンロード・展開し、`PATH` 環境変数に追加します。

    1. コマンドプロンプト (cmd) から、初回の `gclient` コマンドを実行し、アップデートを行います。

    1. 作業ディレクトリで `gclient config` コマンドを実行し `.gclient` ファイルを作成します。
        ```
        gclient config --name=cytanb-vrm-works "https://github.com/oocytanb/cytanb-vrm-works.git@2018.2"
        ```
    
    1. リポジトリからソースコードを取得します。
        ```
        gclient sync
        ```

- Git に関する詳しい情報は、Web の資料に当たってください。

## License

- このプロジェクト固有のものについては、[MIT License](./LICENSE) です。

- 外部のアセット/ライブラリーについては、それぞれのライセンスをご確認ください。

- アセット等に適用するライセンスは、制作者の著作権表示とその成果物をオープンで自由に利用できることを明示する目的で、主に以下のものから選択しています。
    - [MIT License](https://opensource.org/licenses/MIT)
    - [ISC License](https://opensource.org/licenses/ISC)
    - [BSD 2-Clause License](https://opensource.org/licenses/BSD-2-Clause)
    - [Apache License, Version 2.0](https://opensource.org/licenses/Apache-2.0)
    - [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)

## Community

[Discord](https://discord.gg/FwFjw5n)
