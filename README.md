# Metta Ragga Club Recorder(配布用)

[![ダウンロード macOS](https://img.shields.io/badge/%E3%83%80%E3%82%A6%E3%83%B3%E3%83%AD%E3%83%BC%E3%83%89-macOS%20(Apple%20silicon)-009b3a?style=for-the-badge&logo=apple&logoColor=white)](https://github.com/Yutahhhhh/metta-ragga-club-recorder-releases/releases/latest/download/MettaRaggaClubRecorder.dmg)
[![ダウンロード Windows](https://img.shields.io/badge/%E3%83%80%E3%82%A6%E3%83%B3%E3%83%AD%E3%83%BC%E3%83%89-Windows%2011%20(x64)-009b3a?style=for-the-badge&logo=windows&logoColor=white)](https://github.com/Yutahhhhh/metta-ragga-club-recorder-releases/releases/latest/download/MettaRaggaClubRecorder-setup.exe)

最新版をダウンロードします。macOS は `.dmg`、Windows は `-setup.exe` です。ほかのバージョンは [Releases](https://github.com/Yutahhhhh/metta-ragga-club-recorder-releases/releases) にあります。

SNS 向けの動画と音声を収録する、macOS と Windows のアプリの配布用リポジトリです。ソースコードは含まず、リリースした成果物だけを置いています。

画面、BGM、MC のマイク音声を 1 回の収録でまとめて録り、YouTube、TikTok・Reels・Shorts、Instagram に合わせた縦横比の MP4 を同時に書き出します。音声だけの収録では、WAV と MP3 を書き出します。

## 動作環境

- macOS: Apple silicon の Mac、macOS 14 以上
- Windows: Windows 11(x64)

## インストール(macOS)

1. 上のボタンから `.dmg` をダウンロードして開き、`Metta Ragga Club Recorder.app` を「アプリケーション」フォルダへ移します。
2. アプリを開きます。初回は「“Metta Ragga Club Recorder”は開いていません」と表示され、開けません。アプリが Apple の公証を受けていないためです。「完了」を押し、次のどちらかの方法で許可してください。
   - 「システム設定」→「プライバシーとセキュリティ」を開きます。下の方にある「“Metta Ragga Club Recorder”はブロックされました」の「このまま開く」を押します。もう一度アプリを開き、確認の画面で「開く」を押します(Mac のパスワードか Touch ID を求められます)。
   - ターミナルで次のコマンドを実行してから、アプリを開きます。

     ```sh
     xattr -dr com.apple.quarantine "/Applications/Metta Ragga Club Recorder.app"
     ```

   macOS 15 以降では、Finder で右クリックして「開く」を選んでも、許可できません。
3. 初回の起動時に、画面収録とマイクの許可を求められます。システム設定の「プライバシーとセキュリティ」で許可してください。

## インストール(Windows)

1. 上のボタンから `MettaRaggaClubRecorder-setup.exe` をダウンロードして実行します。
2. インストーラは署名していないため、「Windows によって PC が保護されました」と表示されます。「詳細情報」を押し、表示された「実行」を押してください。
3. インストール先は、ユーザーごとの場所(`%LOCALAPPDATA%\Metta Ragga Club Recorder`)です。管理者の権限は要りません。
4. マイクを使うには、「設定」→「プライバシーとセキュリティ」→「マイク」で、デスクトップ アプリのマイクへのアクセスを許可してください。

Windows 版と macOS 版の違い:

- 動画の音声は AAC 192 kbps です(Windows 標準のエンコーダの上限)。WAV と MP3 は同じです。
- このアプリのウィンドウは、録画だけでなく、スクリーンショットや他の録画ソフトにも映りません。
- 開始・停止のショートカットの既定は Ctrl+Alt+Shift+R です。
- 性能の低い GPU(内蔵 GPU など)では、複数のサイズを同時に書き出すと、コマが抜けることがあります。60 fps で 3 サイズ以上を選ぶと、録画前のチェックで注意が出ます。

## アップデート

アプリは起動時に、このリポジトリの最新のリリースを確認します(設定画面でオフにできます)。手動で確認するには、設定画面の「アップデートを確認」を押してください。更新があるときは、「更新して再起動」でダウンロード、署名の検証、インストール、再起動を行います。ボタンを押すまで、更新は適用されません。macOS では、アプリのアップデートで入れた版を開くときに、上の初回の許可(「このまま開く」)は要りません。

外部への通信は、更新の確認と更新ファイルのダウンロードだけです。録画した内容や設定を送信する処理はありません。

## 署名について

macOS のアプリは、Apple Developer ID での署名と公証をしていません(アドホック署名)。そのため、アップデートのあとに macOS が画面収録とマイクの許可を確認し直すことがあります。Windows のインストーラも、コード署名をしていません。

更新ファイルは、どちらの OS も別の鍵で署名してあり、アプリが検証してからインストールします。
