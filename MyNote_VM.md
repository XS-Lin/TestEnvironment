# VM #

## VMwareのスナップショットにおけるバックアップ ##

[情報源](https://docs.vmware.com/jp/VMware-vSphere/6.5/com.vmware.vsphere.vm_admin.doc/GUID-CA948C69-7F58-4519-AEB1-739545EA94E5.html)

1. メモリ状態を含めるスナップショット作成の注意点

   メモリのスナップショットを作成する場合、仮想マシンのメモリの状態と、仮想マシンの電源設定がスナップショットで取得されます。仮想マシンのメモリの状態をスナップショットで取得する場合、完了まで時間がかかります。ネットワークによっては、瞬間的に中断が生じる場合もあります。

   仮想マシンがほかのコンピュータと通信しているとき、特に本番環境にある場合、問題が起こる可能性が高くなります。たとえば、仮想マシンがネットワーク上のサーバからファイルをダウンロードしているときにスナップショットを作成する場合、仮想マシンはファイルのダウンロードを継続し、サーバに進捗状況を通知します。そのスナップショットに戻すと、仮想マシンとサーバ間の通信は混乱し、ファイルの転送は失敗します。

   **唯一の、または長期的なバックアップ ソリューションとしてスナップショットを使用しないでください。**

   引用元:[仮想マシンのスナップショットの作成](https://docs.vmware.com/jp/VMware-vSphere/6.5/com.vmware.vsphere.vm_admin.doc/GUID-64B866EF-7636-401C-A8FF-2B4584D9CA72.html)

1. 静止スナップショットの注意点

   静止スナップショットは、自動バックアップや定期バックアップに適しています。静止操作により、スナップショット ディスクはゲスト ファイル システムの一貫した状態を表します。仮想マシン ファイルの静止は、仮想マシンがパワーオン状態であり、仮想マシン メモリのスナップショットを取得する必要がない場合にのみ実行してください。静止操作によって、仮想マシンで実行中のプロセスの状態が一時停止するか、変更されます。特に、リストア中に、ディスク上の情報を変更する可能性があるプロセスに影響があります。大容量ディスクがある仮想マシンを静止させることはできません。
