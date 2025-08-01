# リモートIO基板
# Remote IO Board
Remote IO Board with Shift Register 


## 概要 
  * 本基板はIO信号をシリアル化してメイン基板とサブ基板間で同期する基板です  
  * メイン基板、サブ基板ともにそれぞれ8本の入力と出力を備えており、メイン基板とサブ基盤間で各信号のON/OFF状態が同期されます
  * 本基板はマイコンやFPGA等を使用せず、シフトレジスタ、タイマ、カウンタ等のICのみで構成されています  
  * ボタンやLED等のユーザ入出力の配線を省配線化する際に便利です  
  * 本基板を使用せずに8入力/8出力の信号をそのまま伝送すると一般的には計16本の信号線が必要となります  
  * 本基板を使用すると信号線3本のみで伝送することが可能です（同期クロック＋シリアルデータx2、電源線除く）
  * 本基板を使用すると電源線を含めても計5本の配線で双方向に8入力/8出力の信号を伝送できます  
  * 片方向のみの場合は信号線2本のみで伝送することが可能です（同期クロック＋シリアルデータx1※D0 or D1を未接続、電源線除く）  
  * 各入出力の動作確認用にそれぞれボタン及びLEDを備えています
  * 例えば、操作盤と制御盤が離れている場合に操作盤と制御盤間の省配線化が可能になります

## 仕様
  * 電源電圧DC2V~5.5V  
  * メイン基板とサブ基板でそれぞれ8入力/8出力  
  * メイン基板とサブ基板の電源は同一の電源電圧を供給してください  
  * 約1kHzの周期で双方向に同期します(内部クロック約8kHz、8bit+同期1bit)
  * 入力に74HC165、出力に74HC595を使用しているため、シリアル転送中に変換途中の信号出力を防止しています    
  * 入力ポートは基板内部でプルダウンされています  
  * メイン基板とサブ基板の伝送距離は最大数m程度を想定しています
  * メイン基板外形47.5mm x 38mm, M3x2(穴幅41mm)
  * サブ基板外形41.5mm x38mm, M3x2(穴幅35mm)

## 使用方法
  * 出荷時はメイン基板とサブ基板が一体になっています　　
  * 基板にはミシン目（スリット）が入っていますので必要に応じてカットして使用してください　　
  * メイン基板とサブ基板のSCK同士、D0同士、D1同士をケーブルで接続します  
  * 片方向のみで使用する場合はD0もしくはD1のどちらかを未接続で使用します  
  * メイン基板とサブ基板のVCCとGNDに電源を接続します 
  * 必要に応じてIN0-15にスイッチ、OUT0-15にLED等を配線してください  
  * 基板内部でプルダウンされているため、未使用の入力は未接続で使用します  
    
<img src="img/img3.jpeg" width="360">

## 注意 
  * ON/OFFのデジタル信号が同期されます。アナログ信号の同期はできません  
  * 電源投入直後は同期状態や出力が不安定な場合があります  
  * 伝送距離が長い場合やノイズ環境下等では信号同期が安定しない場合があります  
  * ノイズ環境下や長い伝送距離の場合は必要に応じて、シールドケーブルやフォトカプラ等でノイズ対策を追加してください  
  * 高い信頼性が求められる用途には使用しないでください    
  * メイン基板とサブ基板は必要に応じて分離して使用してください  
  * 分離の際や分離後のエッジ部分は鋭利なため、怪我をしないように注意してください    
  * 基板をカットする際はそれぞれの基板に過大な力が掛からない様にして下さい　　

<img src="img/img1.jpeg" width="360">
<img src="img/img2.jpeg" width="360">
<img src="img/img5.jpg" width="360">
<img src="img/img4.gif" width="360">
※LEDが高速に点滅しているように見えますが、実際はスイッチ状態に応じて点灯しています  




MIT Lisense
