# Robotsystem-kadai1
2020年度のロボットシステム学の授業の課題1提出のために製作


#授業のプログラムからの変更点

・LEDを1個から3個に増やした。  
・抵抗の数を1個から3個に増やした。


#使用した部品

・Raspberry Pi4(OS:ubuntu 20.04)  
・抵抗の200~300[Ω]を3個  
・LEDを3個  
・ブレッドボード  
・ジャンパー線


#配線

・GPIOは25, 16, 6を使用してそれぞれLEDのアノードとつながるように配線する。  
・その時にLED1個に対して抵抗が1個挟まるようにする。  
・カソードはRaspberry Pi4のGroundとつなぐ。


#LEDの光らせ方<以下の順に操作>

・githubからデータをクローン  
・make  
・sudo insmod myled.ko  //失敗したら sudo rmmod myled を実行後、再試行  
・sudo chmod 666 /dev/myled0  
・echo 1 > /dev/myled0  //LEDが3個光る  
・echo 0 > /dev/myled0  //LEDが3個消える


#プログラムを変更したいときの操作<テキストエディター：vim>


##myled.cを変更したい

・vi myled.c


##Makefileを変更したい

・vi Makefile
