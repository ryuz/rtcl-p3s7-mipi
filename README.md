English version: [README_en.md](README_en.md)

# グローバルシャッターMIPI高速度カメラ(PYTHON300 + Spartan7)

## 概要

[こちら](https://rtc-lab.com/products/rtcl-cam-p3s7-mipi/)で紹介しておりますグローバルシャッターMIPI高速度カメラの KiCAD による設計データです。

オンセミコンダクター社 [PYTHON300イメージセンサー](https://www.onsemi.jp/products/sensors/image-sensors/python300) と AMD(Xilinx) の [Spartan7](https://www.amd.com/ja/products/adaptive-socs-and-fpgas/fpga/spartan-7.html) FPGA を用いた研究開発向けの小型のカメラモジュールです。

データシート上は VGA サイズながら 815fps の高速度撮影が可能と記載されているセンサーを利用しており、当方では [KV260](https://www.amd.com/ja/products/system-on-modules/kria/k26/kv260-vision-starter-kit.html) と [Zybo Z7](https://digilent.com/shop/zybo-z7-zynq-7000-arm-fpga-soc-development-board/) に接続して 320x320 サイズで 1000fps 撮像が出来ております。

![カメラ外観写真](docs/images/camera_photo.png)

撮影動画なども[こちら](https://rtc-lab.com/products/rtcl-cam-p3s7-mipi/)で紹介しております。

## 回路図

回路図は以下です。

- [イメージセンサー子基板](sensor_python300/sensor_python300.pdf)
- [FPGA親基板](mipi_spartan7/mipi_spartan7.pdf)


## 基板販売

当方で製造したものを[BOOTH](https://rtc-lab.booth.pm/) 及び [BASE](https://rtcl.base.shop/) にて販売中です。

詳細は下記をご覧ください。

https://rtc-lab.com/products/rtcl-cam-p3s7-mipi/


## 関連ソフトウェア

現時点では、KV260 に独自仕様でデータを送るプロジェクトがあります。

- [Spartan-7 のデザイン](https://github.com/ryuz/rtcl-designs/tree/main/projects/rtcl_p3s7_mipi/rtcl_p3s7_mipi)
- [KV260 の デザイン](https://github.com/ryuz/rtcl-designs/tree/main/projects/kv260/kv260_rtcl_p3s7_hs)


他に速度を落として ZYBO と接続できる事や、MIPI-CSI に準拠することも可能なことを確認していますが、まだプロジェクトとして準備できておりませんので今後にご期待ください。


## リポジトリ構成

| ディレクトリ |  説明                                            |
|:------------|:------------------------------------------------|
| mipi_spartan7    | Spartan7 FPGA の載った親基板のプロジェクト |
| sensor_python300 | PYTHON300 イメージセンサーの載った子基板のプロジェクト |
| sensor_mipi      | 親子基板を共取り製造用に結合したプロジェクト |


## 免責事項

本設計データは、研究開発用の試作実験に用するものであり、利用に際して発生した如何なる損害も作者は補償いたしませんので予めご了承ください。

## ライセンス(License)

本設計データは、[クリエイティブ・コモンズ 表示-非営利 4.0 国際 ライセンス](https://creativecommons.org/licenses/by-nc/4.0/deed.ja)の下で提供されています。

製造した本基板の無断での販売や配布を行わない限りは、趣味や研究開発用途でご自由にお使いいただく事が出来ます。

また、商用に製造販売を希望される場合は、別途ライセンス契約を作者までご相談ください。[お問い合わせフォーム](https://rtc-lab.com/contact/)などからお問い合わせ頂けます。


## 作者情報

渕上 竜司(Ryuji Fuchikami)
[リアルタイムコンピューティング研究所](https://rtc-lab.com/)
