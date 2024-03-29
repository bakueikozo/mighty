# Mighty for ATOM
公開準備中  

## これは？
市販されているATOM Camのハードウェアを利用し、販売元の提供するサーバと接続せず、  
閉じたネットワーク上でIPカメラを利用するためのツールキットです  

## できること
・H264のストリーミング(v4lrtspserverを利用)→ VLC等、PCやスマートフォンから映像を受信できます  
※ルータ外に出るためには、別途VPNなどの利用が必要です。  
無設定ではルータの外に配信することはできないため、外出先からスマートフォンのアプリで簡単に見る機能は失われます。  
・mjpg-streamerを利用し、WebBroserやwget,curlなどから随時リアルタイムスナップショットが取得可能です(理論値25FPS)  
・SDカード内にmp4ファイルを録画できます  
・FTPサーバとして動作するため、外部から動画を取得できます  
・FTPクライアントとして動作させ、外部FTPサーバに動画をアップロードできます  
・SSHサーバが動作するため、自作のスクリプトなどを動作させることができます。  

## できないこと
・動体検知やAI人体検出などは、アトムテックの実装と異なりますので、現時点では非対応です。  
（※動体検知ぐらいはなんとなく動くかもしれません）  


## もしかしたらできること
・OSD(On Screen Display)の設定  
※アトムテックの実装では、ATOMのロゴと時間表示しかできませんが、例えばカメラ・監視場所の名前などをオーバーレイできるかもしれません。  
・USB有線LANアダプタの使用  
　どうしても無線LAN環境が安定して使用できない場合、市販のUSB-LANアダプタが使用できるかもしれません  
 
 ## より上級者には
 ・ツールキットでは、v4l2loopbackモジュールを使用し、H264ストリーム、H265ストリーム、JPEGストリームを仮想/dev/videoxから出力します  
 　必要であれば、その出力をv4l2でキャプチャし、任意の処理を行うことができます。
  
 ## ちょっと困ったこと
 ・なんかUSBガジェットドライバが壊れてるのか、RNDISドライバとかがうまく動きません。
これがうまく動くならUSBケーブルでPCと直結してストリーミングしたり、メモリカードリーダとして使えると思ったんだけど…  
