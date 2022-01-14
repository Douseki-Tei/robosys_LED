# robosys_LED
2021年度ロボットシステム学の課題1です。デバイスドライバです。
<br>
数値入力(0、1)によって、LEDが点灯、消灯することができる。

---
# 動作環境
・OS : ubuntu 20.04 server
<br>
・Raspberry Pi 4 Model B

---
# 使用したもの
・Raspberry Pi4 model B x1
<br>
・ブレッドボード x1
<br>
・ジャンプワイヤ ×6
<br>
・LED ×1
<br>
・抵抗 ×1

---
# 回路（配線図）
![配線図](https://user-images.githubusercontent.com/71487790/146228757-09daa59f-f723-446a-87a8-e2db42eb9340.jpg)
#回路図
![回路図](https://user-images.githubusercontent.com/71487790/149570220-8c9747a0-48f9-447b-9a29-e51f6f02c1b4.jpg)

---
# 使用方法
以下のコマンドを実行.

```sh
$ git clone https://github.com/Douseki-Tei/robosys_LED.git
$ cd robosys_LED
$ make

$ sudo insmod myled.ko
$ sudo chmod 666 /dev/myled0
```
以下のコマンドで点灯。

```sh
$ echo 1 > /dev/myled0
```
以下のコマンドで消灯。

```sh
$ echo 0 > /dev/myled0
```
実行後の後処理は以下のコマンドを実行。
```sh
$ sudo rmmod myled
$ make clean
```

---
# ライセンス
[GNU General Public License v3.0](https://github.com/TonoLeo/robosys_LED/blob/main/COPYING)
