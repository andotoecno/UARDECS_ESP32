## Uardecs_ESP32
- [UARDECS](https://uecs.org/arduino/uardecs.html)をESP32のWiFiで使えるように移植したライブラリです。使い方はUARDECSと同じです。
  - mainブランチにはArduino Uno版を移植し、試験的にMega版を[future/mega_imigration](https://github.com/andotoecno/UARDECS_ESP32/tree/feature/mega-imigration)ブランチに移植しています。
- 以下の動作確認済みです。
    - ブラウザからノードの設定を見に行き、IPアドレス等を更新。
    - UECSパケット送受信支援ツールでUDPが来ているのを確認。
    - UECS-GEARでテストデータの受信を確認。
    - UECS-Pi, Arsprout Piでの受信確認。
- 実装の詳細や移植時のメモは[README_dev.md](README_dev.md)を参照してください。

## 使用上の注意
- UECSの外でEEPROM.begin()を呼ぶ必要があります。
  - UECSsetup内で実行すると、UECS以外でEEPROMを使う際に多重にEEPROM.begin()し意図しないアドレスを使う可能性があるので、あえてUECSの外で明示的に呼ぶ仕様にしています。
  - UECSのデフォルトでは0x32~1024までを使っています。UECS以外でEEPROMを利用する場合はアドレスをかぶせないように注意してください。

## ライセンス
- [MITライセンス](https://opensource.org/licenses/MIT)に基づいています。
- 詳細は[LICENSE](LICENSE)を参照してください。