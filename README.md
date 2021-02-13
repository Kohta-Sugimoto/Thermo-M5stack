# Thermo-M5stack
概要

マイコンM5stackとConta™ サーモグラフィー AMG8833を使用して非接触温度計測と監視カメラのようなものを作りました。
[作成に当たり参考にしたサイト](https://ambidata.io/samples/m5stack/thermalcamera/)

## Description
詳細の説明
### モード0
サーモグラフィーの動作確認用に実装しました。

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
