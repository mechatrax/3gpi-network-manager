3gpi-network-manager
====================

3GPIでネットワーク接続を行うための設定ファイルを提供します。

## 提供ファイル
以下のファイルがパッケージに含まれています。

* /usr/share/doc/3gpi-network-manager/changelog.Debian.gz  
  パッケージの変更履歴が記録されているファイルです。  

* /lib/udev/rules.d/81-3gpi-mm-blacklist.rules  
  3GPIのモデムとして認識させないデバイスを定義した設定ファイルです。  

* /lib/udev/rules.d/81-3gpi-mm-candidate.rules  
  3GPIのモデムとして認識させるデバイスを定義した設定ファイルです。  

## 作成ファイル  
以下のファイルが存在しない場合、インストール時に作成されます。  

* /etc/NetworkManager/system-connections/gsm-3gpi-asahinet  
  次のコマンドによって作成されます。  
  ```
  nmcli con add type gsm ifname “*” con-name gsm-3gpi-asahinet apn 3g.mobac.net user f@y.asahinet.jp password 0000  
  ```

* /etc/NetworkManager/system-connections/gsm-3gpi-dti  
  次のコマンドによって作成されます。  
  ```
  nmcli con add type gsm ifname “*” con-name gsm-3gpi-dti apn dream.jp user user@dream.jp password dti  
  ```

