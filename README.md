# Thermo-M5stack
概要

マイコンM5stackとConta™ サーモグラフィー AMG8833を使用して非接触温度計測と監視カメラのようなものを作りました。

↓2021年2月時点では、SWITCHSIENCEさんで購入可能です。  
[M5stack](https://www.switch-science.com/catalog/3647/)  
[AMG8833](https://www.switch-science.com/catalog/3395/)

[作成に当たり参考にしたサイト](https://ambidata.io/samples/m5stack/thermalcamera/)


## Description
M5stackには3つのボタンがあり、一番左のボタンを押すとモード0、真ん中のボタンを押すとモード1、一番右のボタンを押すとモード2としています。  
各モードの機能・使い方は以下のとおりです。

### モード0
サーモグラフィーの動作確認用に実装しました。
[画面](https://user-images.githubusercontent.com/78978860/107856827-464f6b80-6e6e-11eb-9fbb-7d27006dd593.JPG)

### モード1
監視カメラのようなものです。
温度変化が一定以上になった場合、人が入ったと検知します。

### モード2
非接触体温計のようなものです。
最初に温度計測しておいて、それ以上であれば体温上昇していると判断します。
サーモグラフィー AMG8833の温度精度がTyp.±2.5℃なので、あまり信頼できません。
あくまで参考程度にでも。


## Usage
用途



## Install
インストール方法
