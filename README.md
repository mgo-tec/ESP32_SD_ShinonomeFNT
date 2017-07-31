# ESP32_SD_ShinonomeFNT
This is the Arduino core for the ESP32 library for reading Shinonome 16x16 Japanese font.  
  
Beta ver1.2  
  
これはShift_JISコードからフリーの東雲フォント(16x16)を ESP-WROOM-32( ESP32 )で読み込むためのライブラリです。  
SPI ( VSPI )接続の micro SD カードからの読み込み専用です。  
UTF8toSjisライブラリをインクルードしているので、１行の関数のみでUTF-8文字列から16x16ドットの日本語漢字に変換できます。  
  
予め以下のファイルをSDカードにコピーしておく必要があります。  
（fontというフォルダを作成しておくと良いです。）  
※ファイル名は半角英数字8文字、拡張子3文字  
  
Utf8Sjis.tbl (UTF-8 Shift_JIS変換テーブル)  
shnmk16.bdf (全角東雲フォント)  
shnm8x16.bdf (半角東雲フォント, ファイル名の'r'をカットしたもの)  
  
【更新履歴】  
(1.2)  
軽微な修正をしました。  
  
(1.1)  
２ファイルのみ開く、以下の関数を追加しました。  
StrDirect_ShinoFNT_readALL2F  
その他、Utf8toSjis ライブラリのファイルハンドル _UtoS を参照できるようにして、同時に開くファイル数を節約できるようにしました。  
  
(1.0)  
ESP32 用リリース  
  
Licence:  
  
  MITライセンス　　
  Copyright (c) 2017 Mgo-tec  
  
  東雲フォントは/efont/さんが保守開発を行い、ライセンスはPublic Domainです。  
  
詳しくはブログ参照：  
  
https://www.mgo-tec.com  