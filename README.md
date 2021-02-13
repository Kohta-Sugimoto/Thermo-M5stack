# Thermo-M5stack
概要

マイコンM5stackとConta™ サーモグラフィー AMG8833を使用して非接触温度計測と監視カメラのようなものを作りました。

↓2021年2月時点では、SWITCHSIENCEさんで購入可能です。  
[M5stack](https://www.switch-science.com/catalog/3647/)  
[AMG8833](https://www.switch-science.com/catalog/3395/)

[参考にしたサイト](https://ambidata.io/samples/m5stack/thermalcamera/)


## Description
M5stackには3つのボタンがあり、一番左のボタンを押すとモード0、真ん中のボタンを押すとモード1、一番右のボタンを押すとモード2としています。  
各モードの機能・使い方は以下のとおりです。

### モード0
サーモグラフィーの動作確認用に実装しました。  
下画像のように、温度が表示されれば正常です。  
[モード0の画面](https://user-images.githubusercontent.com/78978860/107856827-464f6b80-6e6e-11eb-9fbb-7d27006dd593.JPG)

### モード1
監視カメラのようなものです。  
温度変化が一定以上になった場合、人が入ったと検知します。  
[モード1の画面](https://user-images.githubusercontent.com/78978860/107857239-96c7c880-6e70-11eb-9e97-64d282f1b169.JPG)

指をサーモグラフィーの視野内で動かすと「detect」と表示されることが確認できます。  
[人を検知したときの画面](https://user-images.githubusercontent.com/78978860/107857562-43567a00-6e72-11eb-9a26-394ba4e90693.JPG)  
本来は「detect」の表示だけでなく、音を鳴らしたり、スマホに通知が来るようにしたほうがいいですが、そこまでは作りこんでいません。

モード1になっている状態で、もう一度真ん中のボタンを押すと、感度が変化しますので調節可能です。

### モード2
非接触体温計のようなものです。
最初に温度計測しておいて、それ以上であれば体温上昇していると判断します。  
[モード2の画面](https://user-images.githubusercontent.com/78978860/107857608-aba55b80-6e72-11eb-8953-dd99aee11b8d.JPG)

モード2になっている状態で、もう一度一番右のボタンを押すと、体温計測ができます。  
平熱や計測部位はヒトによって異なると思うので、最初の体温計測を基準とします。  
2回目以降は1回目の体温より低ければ何も表示せず、高ければした画像のように「Be Careful」と表示します。  
[上昇検知時の画面](https://user-images.githubusercontent.com/78978860/107857707-633a6d80-6e73-11eb-8642-f113414ded07.JPG)

サーモグラフィー AMG8833の温度精度がTyp.±2.5℃なので、あまり信頼できません。
あくまで参考程度にでも。


## Setting
以下のように接続しています。
[ピン構成](https://user-images.githubusercontent.com/78978860/107857884-8ca7c900-6e74-11eb-95c9-3d9127dcc5f1.PNG)  
データのやり取りはI2Cで、電源は3.3Vです。
