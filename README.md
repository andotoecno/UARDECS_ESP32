## Uardecs_ESP32
- [UARDECS](https://uecs.org/arduino/uardecs.html)をESP32のWiFiで使えるように移植したライブラリです。使い方はUARDECSと同じです。
- 本ブランチでは、試験的にArduino Mega版を移植しました
  - Uno版と違い、CCMのAttributeとtypeをブラウザ上で設定できます。
- PlatformIO内でライブラリとして使うことを想定したリポジトリになっています。実装の詳細は[README_dev.md](README_dev.md)を参照してください。
- 以下の動作確認済みです。
    - ブラウザからノードの設定を見に行き、IPアドレス等を更新。
    - UECSパケット送受信支援ツールでUDPが来ているのを確認。
    - UECS-GEARでテストデータの受信を確認。(サンプルのデータ受信は、RoomEst1.iniを使って確認できます。)
    - UECS-pi, Arsprout Piでの受信確認。
- ESP32のWiFi機能を使うため、WiFiのSSIDとパスワードを設定する必要があります。

## EPROM使用上の注意
- EEPROMは4k byte確保しています(元々のMega版のライブラリに合わせています)。
- 最近のESP32はメモリが多いので、4k byteくらいは余裕だと思います。古いESP32を使う場合はヘッダファイルのEEPROMのアドレス定義を変更して使ってください。

## ライセンス
- [MITライセンス](https://opensource.org/licenses/MIT)に基づいています。
- 詳細は[LICENSE](LICENSE)を参照してください。