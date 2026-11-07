# Metta Ragga Club Recorder(配布用)

[![ダウンロード](https://img.shields.io/badge/%E3%83%80%E3%82%A6%E3%83%B3%E3%83%AD%E3%83%BC%E3%83%89-macOS%20(Apple%20silicon)-009b3a?style=for-the-badge&logo=apple&logoColor=white)](https://github.com/Yutahhhhh/metta-ragga-club-recorder-releases/releases/latest/download/MettaRaggaClubRecorder.dmg)

最新版の `.dmg` をダウンロードします。ほかのバージョンは [Releases](https://github.com/Yutahhhhh/metta-ragga-club-recorder-releases/releases) にあります。

SNS 向けの動画と音声を収録する、macOS 専用アプリ(Apple silicon)の配布用リポジトリです。ソースコードは含まず、リリースした成果物だけを置いています。

画面、BGM、MC のマイク音声を 1 回の収録でまとめて録り、YouTube、TikTok・Reels・Shorts、Instagram に合わせた縦横比の MP4 を同時に書き出します。音声だけの収録では、WAV と MP3 を書き出します。

## 動作環境

- Apple silicon の Mac
- macOS 14 以上

## インストール

1. 上のボタンから `.dmg` をダウンロードして開き、`Metta Ragga Club Recorder.app` を「アプリケーション」フォルダへ移します。
2. 初回は、macOS にブロックされることがあります。「システム設定 → プライバシーとセキュリティ」の「このまま開く」で許可するか、ターミナルで次のコマンドを実行してください。

   ```sh
   xattr -dr com.apple.quarantine "/Applications/Metta Ragga Club Recorder.app"
   ```

3. 初回の起動時に、画面収録とマイクの許可を求められます。システム設定の「プライバシーとセキュリティ」で許可してください。

## アップデート

アプリは起動時に、このリポジトリの最新のリリースを確認します(設定画面でオフにできます)。手動で確認するには、設定画面の「アップデートを確認」を押してください。更新があるときは、「更新して再起動」でダウンロード、署名の検証、インストール、再起動を行います。ボタンを押すまで、更新は適用されません。

外部への通信は、更新の確認と更新ファイルのダウンロードだけです。録画した内容や設定を送信する処理はありません。

## 署名について

アプリは Apple Developer ID での署名と公証をしていません(アドホック署名)。そのため、アップデートのあとに macOS が画面収録とマイクの許可を確認し直すことがあります。更新ファイルは別の鍵で署名してあり、アプリが検証してからインストールします。
