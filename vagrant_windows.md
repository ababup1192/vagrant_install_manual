# Vagrantインストールマニュアル Windows7用

Windows8も同じ感じでいけるといいな。

1 スタートメニューからコマンドプロンプト(*cmd*)を検索し、右クリックメニューから「管理者として実行」を選択。

![](/Users/watanabemirai/Desktop/vagrant_windows/img/01-cmd.png "cmdの起動" "width:180px;height:200px")

2 [https://chocolatey.org](https://chocolatey.org)にアクセスし、以下の様なコマンドを*cmd*へコピペする。

		@powershell -NoProfile -ExecutionPolicy unrestricted -Command "iex ((new-object net.webclient).DownloadString('https://chocolatey.org/install.ps1'))" && SET PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin

3 *PowerShell*も*cmd*と同じ要領で、管理者として実行する。(今後良く使うのでタスクバーに、登録しておくと良い。)

![](/Users/watanabemirai/Desktop/vagrant_windows/img/02-power.png "powershellの起動" "width:180px;height:220px")

![](/Users/watanabemirai/Desktop/vagrant_windows/img/03-power_task.png "タスクバーからの起動" "width:350px;height:180px")

4 *PowerShell*に以下のコマンドを打ち、実行していく。実行が終わったら、一度*PowerShell*を終了する。


	choco install -y git
	choco install -y vagrant
	choco install -y virtualbox

![](/Users/watanabemirai/Desktop/vagrant_windows/img/04-choco.png "タスクバーからの起動" "width:550px;height:200px")

5 ユーザの環境変数を、コントロール パネル/システムとセキュリティ/システム/システムの詳細設定/環境変数 の順で開いていく。

![](/Users/watanabemirai/Desktop/vagrant_windows/img/05-ctrl_pane1.png "コントロールパネル" "width:360px;height:200px")

![](/Users/watanabemirai/Desktop/vagrant_windows/img/06-ctrl_pane2.png "コントロールパネルシステム・セキュリティ" "width:550px;height:240px")

![](/Users/watanabemirai/Desktop/vagrant_windows/img/07-system.png "コントロールパネルシステムの詳細設定" "width:450px;height:150px")

![](/Users/watanabemirai/Desktop/vagrant_windows/img/08-path1.png "環境変数" "width:300px;height:280px")

![](/Users/watanabemirai/Desktop/vagrant_windows/img/09-path2.png "ユーザ変数" "width:300px;height:280px")

6 変数名**PATH**で、C:\Program Files (x86)\Git\bin; を追加する。(実際にこのフォルダまで行きコピーしたほうが良いかも。)

![](/Users/watanabemirai/Desktop/vagrant_windows/img/10-path3.png "PATHの設定" "width:300px;height:280px")

Cygwinのほうが色などが綺麗なのでチャレンジ(罠いくつかアリ)
