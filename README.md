# 組み込みRust: Raspberry Pi Pico でLチカ (タイマーを利用)

## 概要

タイマー割り込みを発生させて、割り込みハンドラでRaspberry Pi PicoのLEDを点滅させます。

## ポイント

* 例外ハンドラからHALを操作する
  * `static` 変数で共有
  * 排他制御 `Mutex<RefCell<Option<共有変数>>>`
* タイマー割り込み
  * タイマー割り込みの発生方法
  * NVICでの割り込みマスク解除
  * 割り込みハンドラの書き方

## ライセンス

MIT / Apache 2.0 のデュアルライセンスとします。

## 連絡先

KIKUCHI Yusuke
ac100v.net@gmail.com
