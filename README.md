3gpi-network-manager
====================

3GPIでネットワーク接続を行うための設定ファイルを提供します。

## 提供ファイル
以下のファイルがパッケージに含まれています。

* /usr/share/doc/3gpi-network-manager/changelog.Debian.gz  
  パッケージの変更履歴を記録したファイルです。  

* /usr/share/doc/3gpi-network-manager/copyright  
  ソースの著作権とライセンスを記載したファイルです。  

* /lib/udev/rules.d/81-3gpi-mm-blacklist.rules  
  3GPIのモデムとして認識させないデバイスを定義した設定ファイルです。  

* /lib/udev/rules.d/81-3gpi-mm-candidate.rules  
  3GPIのモデムとして認識させるデバイスを定義した設定ファイルです。  

## 作成ファイル  
以下のファイルが存在しない場合、インストール時に作成されます。  

* /etc/NetworkManager/system-connections/gsm-3gpi-soracom
  次のコマンドによって作成されます。  
  ```
  nmcli con add type gsm ifname "*" con-name gsm-3gpi-soracom apn soracom.io user sora password sora
  ```

* /etc/NetworkManager/system-connections/gsm-3gpi-iij  
  次のコマンドによって作成されます。  
  ```
  nmcli con add type gsm ifname "*" con-name gsm-3gpi-iij apn iijmio.jp user mio@iij password iij
  ```

