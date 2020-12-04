# Robotsystem-kadai1
授業の課題提出のために製作

LEDを1個から3個に増やした。


使用した部品

・Raspberry Pi4

・抵抗の200~300[Ω]を3個

・LEDを3個


GPIOは25, 16, 6を使用


LEDの光らせ方<以下の順に操作>

・make
 
・sudo insmod myled.ko  //失敗したら sudo rmmod myled を実行後、再試行
 
・sudo chmod 666 /dev/myled0
 
・echo 1 > /dev/myled0  //LEDが3個光る
 
・echo 0 > /dev/myled0  //LEDが3個消える
