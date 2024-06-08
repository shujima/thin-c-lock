![IMG_5870](https://github.com/shujima/thin-c-lock/assets/45596573/ac1d35c8-c507-4596-8f91-b74c8c0164cc)

## Overview / 概要

thin-C-lock is a clock style interior decoration which use thin PCB design technology developped by shujima 
thin-C-lockは shujima の薄型基板開発技術を活用して作られた時計風インテリアです。

お問合せはX(twitter) : @shjma_のDM等にお願いします。

[デザフェスtype-C-lock説明書.pdf](https://github.com/user-attachments/files/15746385/type-C-lock.1.pdf)


## Usage / 使い方
![image](https://github.com/shujima/thin-c-lock/assets/45596573/ccdee241-0d0e-41a8-86d9-bbf4f4813937)

### Normal operation / 通常動作中

|Button|Function|
|-|-|
|Up button / 下ボタン| Color change / 色の変更・秒針表示の変更|
|Down button / 下ボタン| Color change / 色の変更・秒針表示の変更|
|Set button / 設定ボタン| Enter time setting mode / 時刻設定モード |

In v1.0.0 firmware, color of the hands and second display style have 7 x 3 = 21 styles.
v1.0.0のファームウェアにおいては、針の色と秒針のスタイルの設定は 7 x 3 = 21種類あります。

### Time setting mode / 時刻設定モード

時刻設定モードではまず時間（短針）の時間を変えることができます。

|Button|Function|
|-|-|
|Up button / 下ボタン| Change Time / 時刻変更|
|Down button / 下ボタン| Change Time / 時刻変更|
|Set button / 設定ボタン| To long hand setting / 長針設定へ |

長針設定モードも操作は同様です。

|Button|Function|
|-|-|
|Up button / 下ボタン| Change Time / 時刻変更|
|Down button / 下ボタン| Change Time / 時刻変更|
|Set button / 設定ボタン| Back to normal operation / 通常動作へ |

# Open source-data and usage / データの公開および利用
基板データ（BOM含む）とファームウェアを共に公開しています。
公序良俗に反しない範囲で自由にお使いいただけます。

* PCB data / 基板データ
https://github.com/shujima/thin-c-lock/releases
* USB Type-C like connector library for KiCAD / USB Type-C風コネクタ部位のみ(KiCAD用ライブラリ)
https://github.com/shujima/type-c-card/tree/master/hardware/lib_usb-type-c
* Firmware / ファームウェア
https://github.com/shujima/thin-c-lock-firmware

## Firmware update / ファームウェアアップデート

### Firmware Update / ファームウェアアップデート手順

thin-C-lock can update the firmware (will be).
thin-C-lockはファームウェアアップデートが可能となる予定です。

### Caution / 注意
* Firmware Update process is delete all internal data of thin-C-lcok and install new program file.
* If we make any misstake at this Firmware Update process, thin-C-lock may no longer work.
* Need Windows PC.
* ファームウェアアップデートはthin-C-lock内部のデータをすべて削除して、新しいプログラムファイルをインストールする作業です。
* ファームウェアアップデートの手順を間違えたりするとthin-C-lockが動作しなくなる恐れがあります。
* WindowsのPCが必要です。


### 1. ファームウェアのダウンロード

Open below link.
以下のリンクを開いてください。
[https://github.com/shujima/thin-c-lock-firmware]

Open "Releases"
"Releases"を開いてください。
![image](https://github.com/shujima/thin-c-lock/assets/45596573/0766030e-cc5c-4462-abb0-bef42c75d339)

Click and download the ".hex" file on the version which you want (v1.0.0 on this image).
ダウンロードしたいバージョン（この画像はv1.0.0）の欄にある".hex"で終わるファイルをクリックしてダウンロードしてください。
![image](https://github.com/shujima/thin-c-lock/assets/45596573/013e866b-a789-4b44-93ef-881814e04c7a)

### 2. ファームウェア書き込みツールのインストール
Open below link (Chinese chip manufacturer).
以下のリンク（中国のチップメーカーのサイト）を開いてください。
[https://www.wch.cn/download/WCHISPTool_Setup_exe.html]

Click"下載" (means download) then it will start the download.
以下の"下載"（ダウンロードの意）をクリックしてダウンロードしてください。
![image](https://github.com/shujima/thin-c-lock/assets/45596573/1b0d283a-faee-4685-9e9c-6004de72d97e)

インストール作業を行ってください。

### 3.  ファームウェア書き込みツールを開く
インストールしたファームウェア書き込みツール"WCHISPStudio"を開いてください。
![image](https://github.com/shujima/thin-c-lock/assets/45596573/0bce22e5-afed-4464-b9cc-32f1165eda15)

Click ... button
「...」を押してください
![image](https://github.com/shujima/thin-c-lock/assets/45596573/3825a104-083e-470b-852e-d3bcce6189d4)

Select ".hex" file downloaded on the step 1 and select "Open".
Step 1でダウンロードした「.hex」で終わるファイルを選択して「開く」を押してください。
![image](https://github.com/shujima/thin-c-lock/assets/45596573/50c40856-3d7b-4ceb-9682-2f0282a7e8ef)

### 4. 本体を準備する
Please remove thin-C-lock from thin-C-base and insert designated USB Type-C cable to thin-C-lock.
Do not insert to PC yet.
thin-C-lock本体をthin-C-baseから取り外して、thin-C-lockに付属のUSB Type-Cケーブルを差し込んでください。
まだPCには接続しないでください。
![image](https://github.com/shujima/thin-c-lock/assets/45596573/fe0f56e6-2f65-4865-836d-28961e9c49be)

Do step 3 if you didn't yet, open and prepare WCHISPStudio.
まだやっていない場合は、Step 3を行って、WCHISPStudioを開いて準備しておいてください。
![image](https://github.com/shujima/thin-c-lock/assets/45596573/2fc4cb36-d9ba-429b-8766-430be672cf68)

Insert the USB cable to your PC while pushing long the button for the Firmware Update which on near the center on thin-C-lock.
thin-C-lock本体の中央付近にあるファームウェアアップデート用ボタンを長押ししながら、USBケーブルの反対側をPCに挿入してください。
![image](https://github.com/shujima/thin-c-lock/assets/45596573/3a16dbb0-e1d8-471c-ba2c-cab74426867d)

#### if successed / 成功例

All LEDs on thin-C-lock should don't lit. 
And can see green strings on WCHISPStudio.
成功するとthin-C-lockは一切LEDなどが点灯しなくなります。
またWCIHSPStudio上に緑色の文字列が表示されます。
![IMG_6361 (1)](https://github.com/shujima/thin-c-lock/assets/45596573/3e4d2ddf-5605-4720-843e-bdb8293e149b)
![image](https://github.com/shujima/thin-c-lock/assets/45596573/54bf9711-0ec2-4e5b-9192-5c9ba846cc84)


#### if failed / 失敗例

Any LED/s on thin-C-lock lit. 
文字盤を含むthin-C-lockのいずれかのLEDが点灯します。
![IMG_6367 (1)](https://github.com/shujima/thin-c-lock/assets/45596573/d46cc26a-6498-4e7f-a3d9-1ad2bf536507)

### 5. 書き込み操作をする

Re-check the configlation.
設定を再度確認します。
![image](https://github.com/shujima/thin-c-lock/assets/45596573/eab23cda-cc45-4b39-beea-59ede1305490)

Click Download button.
"Download"ボタンを押します。
![image](https://github.com/shujima/thin-c-lock/assets/45596573/7472f4c3-bd04-4576-94c6-eb2b6d96a356)

Re-start thin-C-lock when succeed.
You can remove USB cable and bring back thin-C-lock.
thin-C-lockが動作を再開すれば成功です。
そのままUSBケーブルを抜いてthin-C-lockを元に戻します。

